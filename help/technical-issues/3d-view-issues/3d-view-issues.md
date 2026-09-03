---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: Beheben Sie Probleme mit der 3D-Ansicht in Substance 3D Designer, einschließlich Rendering-, Anzeige- und Leistungsproblemen.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Probleme mit 3D-Ansicht
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---


# Probleme mit 3D-Ansicht

Auf dieser Seite werden technische Probleme im Zusammenhang mit der [3D-Ansicht](../../interface/3d-view/3d-view.md) in Substance 3D Designer aufgeführt. Für jede dieser Probleme werden Schritte zur Fehlerbehebung angeboten.

## Geringe Performance: Keine separate GPU verwendet.

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Substance 3D Designer verwendet nicht die *separate* GPU (<b>dGPU</b>) des Systems und verwendet stattdessen die *integrierte* GPU (<b>iGPU</b>). Dies führt zu geringer Leistung beim Rendern von Graphen und/oder der [3D-Ansicht](../../interface/3d-view/3d-view.md).

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Systeme mit umschaltbaren Grafiken können *die dGPU* erzwingen, die für eine *spezifische Anwendung* in dedizierter Software verwendet werden soll, abhängig vom GPU-Hersteller.

Benutzer mit einer <b>Nvidia dGPU</b> können beispielsweise Folgendes tun:

1. Substance 3D Designer schließen
2. Öffnen Sie die <b>NVIDIA-Systemsteuerung</b>.
3. Gehen Sie zum Bildschirm <b>3D-Einstellungen verwalten</b> im Abschnitt <b>3D-Einstellungen</b>
4. Suchen Sie auf der Registerkarte <b>Programmeinstellungen</b> nach dem Eintrag &quot;Substance 3D Designer&quot;.
5. Wählen Sie <b>NVIDIA-Hochleistungsprozessor</b> im Kombinationsfeld <b>Bevorzugte GPU</b> aus.
6. Substance 3D Designer starten

>[!WARNING]
>
> Beachten Sie, dass integrierte GPUs (iGPU) *nicht unterstützt werden*. Weitere Informationen finden Sie auf der Seite [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md).

## 3D-Objekt ist flach

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Ein 3D-Objekt, das detaillierte Volumes in einer Session enthält, wird in der nächsten Session flach. Das Diagramm hat sich jedoch nicht geändert, und die Height-Map enthält dieselben Daten.

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Der Deformationseffekt eines 3D-Objekts gemäß einer Height-Map wird mit der Methode **Tesselierungsmethode** Versatz ausgeführt. Diese Technik umfasst zwei Schritte:

1. **Tesselation**: Die Objektgeometrie ist *in Scheitelpunkte unterteilt*, was zu einer *dichteren Geometrie* führt, um feinere Volumendetails zu unterstützen.
2. **Versatz**: Die Scheitelpunkte werden *verschoben* - d. h. verschoben - entlang ihres *normalen Vektors*. Der Normalenvektor folgt der Richtung, der ein Polygon zugewandt ist, und hat eine Größe (d. h. Länge) von 1

Der Versatz &quot;*direction*&quot; ist bekannt: die Richtung des Normalenvektors.\
Der Versatz *Abstand*, um den die Scheitelpunkte verschoben werden, wird wie folgt berechnet: `Distance = Height scale * Height map` Da die Height-Map im Diagramm *nicht geändert* hat, bleibt die **Height-Skala** erhalten.

Der Standardwert für die Skalierung von Heights ist **1.0**. Dies kann zu einem Versatz führen, der *nicht auffällt*, je nachdem, welches Gitter in der 3D-Ansicht angezeigt wird und welche Height-Map darauf angewendet wird.

Dieser Wert kann wie folgt geändert werden:

| In der 3D-Ansicht | In der Diagrammansicht |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verwenden Sie das Popup **Versatz** in der linken Symbolleiste.<br>Weitere Informationen auf der [dedizierten Seite](../../interface/3d-view/displacement/displacement.md). | Erstellen Sie einen [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)-Knoten, und legen Sie die `heightScale`-Verwendung in den Eigenschaften fest.<br>Geben Sie für diese Ausgabe einen Wert an, z. B. mithilfe eines [konstanten Float-Knotens](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats). Wenden Sie dann *das Diagramm* in der 3D-Ansicht erneut an. |

>[!TIP]
>
> Mit dieser Methode können Sie einen benutzerdefinierten Materialskalierungswert *pro Height* festlegen, mit dem Sie ihn an das spezifische Material dieses Diagramms anpassen können.

## 3D-Ansicht ist komplett schwarz

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

In den Versionen 15.0.0 und höher ist der Viewport der 3D-Ansicht flach schwarz. Ich sehe einige Textüberlagerungen (z. B. Samples und Renderzeit), aber die 3D-Szene ist nicht sichtbar.

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Version 15.1 und höher

Die neuen 3D-Renderer wurden in Version 15.1 aktualisiert und erfordern aktuelle GPU-Treiber. Aktualisieren Sie die GPU-Treiber Ihres Systems auf die neueste Version.

Hier finden Sie Treiber:   [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Version 15.0 und höher

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) hat unsere neuen internen [3D-Renderer](../../interface/3d-view/3d-renderers/3d-renderers.md) eingeführt, die moderne Technologien verwenden und daher von älteren GPUs nicht unterstützt werden.

Zu den unterstützten GPUs gehören die NVIDIA RTX 20-Serie (Turing) oder höher gemäß den [Systemanforderungen von Designer](../../getting-started/system-requirements/system-requirements.md).

Sie können den OpenGL-Renderer standardmäßig weiterhin verwenden, indem Sie die Option [neu in den Projekteinstellungen &#x200B;](../../interface/preferences-window/project-settings/project-settings.md) verwenden:

1. Gehen Sie zu Bearbeiten > Voreinstellungen > Projekte .
2. Die letzte Projektdatei in der Liste auswählen
3. Wählen Sie in der Liste der Projektdateien die Registerkarte 3D-Ansicht aus.
4. Legen Sie die Option &quot;Standard-Renderer&quot; auf &quot;OpenGL (veraltet)&quot; fest.
5. Klicken Sie auf &quot;OK&quot;, um die Änderungen zu bestätigen.

In der neuen 3D-Ansicht wird jetzt standardmäßig der OpenGL-Renderer verwendet, mit dem Sie wie gewohnt weiterarbeiten können.

>[!NOTE]
>
> Die gleichen Probleme und Schritte zur Fehlerbehebung gelten für die meisten AMD- und Intel-GPUs, die derzeit von unseren neuen 3D-Renderern *nicht unterstützt* werden.

>[!IMPORTANT]
>
> Der OpenGL-Renderer ist *veraltet* und wird möglicherweise in Zukunft aus Designer entfernt. Wir empfehlen, ein Upgrade der GPU des Systems durchzuführen, um Unterbrechungen Ihres Workflows zu vermeiden und eine kontinuierliche Unterstützung zu gewährleisten.

## Meldung &quot;Renderer nicht unterstützt&quot; wird angezeigt

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

In den Versionen 15.0.0 und höher wird die Meldung &quot;Renderer not supported&quot; (Renderer nicht unterstützt) in der rechten unteren Ecke des Viewports angezeigt, wenn die neuen 3D-Renderer (Rasterizer, GPU-Pfadverfolgung) verwendet werden. Die 3D-Szene ist nicht sichtbar.

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) hat unsere neuen internen [3D-Renderer](../../interface/3d-view/3d-renderers/3d-renderers.md) eingeführt, die moderne Technologien verwenden und daher von älteren GPUs nicht unterstützt werden.

Zu den unterstützten GPUs gehören die NVIDIA RTX 20-Serie (Turing) oder höher gemäß den [Systemanforderungen von Designer](../../getting-started/system-requirements/system-requirements.md).

Bei den Standardeinstellungen wird die 3D-Ansicht automatisch auf den OpenGL-Renderer zurückgesetzt, wenn die Option &quot;Standard-Renderer&quot; in den [Projekteinstellungen](../../interface/preferences-window/project-settings/project-settings.md) auf &quot;Standard (vordefinierter Renderer)&quot; festgelegt ist.

Sie können diese Option finden und anpassen, indem Sie folgende Schritte ausführen:

1. Gehen Sie zu Bearbeiten > Voreinstellungen > Projekte .
2. Die letzte Projektdatei in der Liste auswählen
3. Wählen Sie in der Liste der Projektdateien die Registerkarte 3D-Ansicht aus.
4. Die Option &quot;Standard-Renderer&quot; ist in den Einstellungen auf der Registerkarte aufgeführt

>[!NOTE]
>
> Nur GPUs in der <b>NVIDIA GTX-Serie</b> können derzeit als nicht unterstützt erkannt werden.
> 
> Die meisten AMD- und Intel-GPUs werden jedoch ebenfalls nicht unterstützt und erzeugen einen schwarzen Render ohne Meldung. Lesen Sie den obigen Eintrag &quot;3D-Ansicht ist vollständig schwarz&quot;, um Anleitungen für diese GPUs zu erhalten.

>[!IMPORTANT]
>
> Der OpenGL-Renderer ist *veraltet* und wird möglicherweise in Zukunft aus Designer entfernt. Wir empfehlen, ein Upgrade der GPU des Systems durchzuführen, um Unterbrechungen Ihres Workflows zu vermeiden und eine kontinuierliche Unterstützung zu gewährleisten.

## 3D-Objekt sieht völlig glatt aus

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Nach der Bearbeitung der an das **Height** [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) gesendeten Daten scheint das Objekt ein gewisses Volume zu haben, aber *sieht völlig glatt aus*, als ob die Height-Informationen in der Schattierung ignoriert wurden.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Stellen Sie sicher, dass die Height-Daten *in Normale* konvertiert sind, die mit der **Normal** [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) verbunden sind.

Bei Verwendung der **Tesselation Versatz**-Technik - siehe oben &quot;3D-Objekt ist flach&quot; - können die Objekte *deformieren*, um den Lichtdaten zu folgen, aber ihre Oberfläche reagiert *nicht anders auf Height*, bis ihre *Normalen* ebenfalls geändert werden, um die Lichtdaten zu berücksichtigen.

Die Lösung ist recht einfach: verbinden den letzten Knoten des Streams, der zur Height-Ausgabe führt, mit einem [Normal](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)-Knoten. Passen Sie den Parameter **Intensität** dieses Knotens entsprechend dem Material an, an dem Sie arbeiten, und verbinden Sie den Knoten Normal mit der Ausgabe **Normal**.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/3d-view-issues-01.gif){width="256px"}

</td>
</tr>
</table>

## Rendern ist verschwommen/verpixelt

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Das gerenderte Bild sieht verschwommen oder verpixelt aus, wenn das System *Anzeigeskalierung* verwendet.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Standardmäßig verwendet Designer die *skalierte* Anzeigeauflösung, um die Renderauflösung der [3D-Ansicht](../../interface/3d-view/3d-view.md) zu definieren. Sie können dies so ändern, dass die *native* Anzeigeauflösung stattdessen für ein scharfes Rendering verwendet wird.

Öffnen Sie das Menü **Bearbeiten** und wählen Sie die Option **Voreinstellungen...**-Option. Öffnen Sie im Fenster [Voreinstellungen](../../interface/preferences-window/preferences-window.md) den Abschnitt **3D-Ansicht**, und legen Sie den Parameter **Viewport-Skalierung** auf *Keine* fest.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](3d-view-issues.resources/3d-view-issues-02.png){width="256px"}

</td>
</tr>
</table>

## Ich kann die Eigenschaft &quot;Tessellation&quot; nicht finden.

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Nach dem Upgrade von Designer auf Version 15.0.0 kann ich den Parameter &quot;Tessellation&quot; in den Material-Eigenschaften, in denen er sich zuvor befunden hat, nicht mehr finden.

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Bei Verwendung der neuen Renderer (Rasterprogramm und GPU-Pathtracer) finden Sie den &quot;Tessellationsfaktor&quot; in den Eigenschaften dieser Renderer. Wechseln Sie in der 3D-Ansicht zu <b>Renderer > Einstellungen bearbeiten</b>. Die Eigenschaft wird im Eigenschaften-Dock aufgelistet.

>[!NOTE]
>
> Der Umfang der Tesselierung variiert je nach Renderer:
> 
> * Rastergerät/GPU-Pathtracer: einem eindeutigen Wert, der global auf die gesamte Szene angewendet wird.
> * OpenGL: ein Wert pro Material.
> * Iray: ein Wert pro Mesh.

## 3D-Objekte sehen falsch aus: ihre Schattierung passt nicht zur Beleuchtung

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Die Schattierung von Objekten beruht auf ihren Normal-, Tangente- und binormal-Vektoren. Ihre Koordinaten verwenden den Bereich &quot;`[-1, 1]`&quot;, während Normalen-Map den Bereich &quot;`[0, 1]`&quot; in den meisten Fällen verwenden. Um die Werte von einem zum anderen anzupassen, müssen ein <b>bias und eine </b>-Skalierung angewendet werden: `value * scale + bias`

Beispiel: Eine Skala von 2 und ein Bias von -1 passen den x-Wert von `[0, 1]` an `[-1, 1]` an: `x * 2 - 1`

Designer wendet keine Standardskala und -abweichung an, es sei denn, sie werden durch ein 3D-Gitter angegeben. Wenn diese Informationen fehlen, wird in der Konsole eine Warnung ausgelöst, wenn [eines der Material überschrieben wird](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md):

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Für Szenen, die vor einiger Zeit in USD-Formate exportiert wurden: Exportieren Sie die Szene erneut mit einer aktuellen Version von USD, die die erforderlichen Daten enthält. Achten Sie auf Eigenschaften im Zusammenhang mit der normalen Skalierung und der Voreinstellung, sofern vorhanden, die von der Software abhängen, die zum Exportieren der Szene verwendet wird.

Wenn [&#x200B; ein Material &#x200B;](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) überschreibt, verarbeitet Designer den Mesh und berechnet alle fehlenden Daten, die sich auf seine Normalen, Tangenten und Binormalitäten beziehen. Wenn die Standardeinstellungen für Skalierung und Bias von Designer mit denen für das Gitter übereinstimmen, wird das Gitter korrekt angezeigt, wenn es überschrieben wird.

## Absturz beim Starten der 3D-Ansicht

**![(Fehler)](3d-view-issues.resources/error.svg) Problem**

Designer stürzt beim Starten der 3D-Ansicht ab, wenn ein Projekt erstellt wird, ein Projekt geladen wird oder wenn eine 3D-Ansicht manuell gestartet wird.

**![(tick)](3d-view-issues.resources/check.svg) Empfohlene Schritte**

Stellen Sie zunächst sicher, dass Ihr System die [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md) von Designer erfüllt.

Aktualisieren Sie dann Ihre Grafiktreiber. Sie können die neuesten Treiber für Ihre GPU finden, indem Sie auf diese Links klicken:   [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Wenn Ihr System sowohl eine integrierte GPU (iGPU) als auch eine separate GPU (dGPU) enthält, stellen Sie sicher, dass *die Treiber für beide aktualisieren*!

Deaktiviere dann alle Programme, die Daten in einen 3D-Grafikprozess einschleusen oder überlagern. Beispiele:

* Nachbearbeitungs-Injektoren wie ReShade
* Überlagerungen wie benutzerdefinierte Fadenkreuze oder GPU-Leistungsmetriken
* Software zur Erfassung und gemeinsamen Nutzung von 3D-Bildern in Echtzeit

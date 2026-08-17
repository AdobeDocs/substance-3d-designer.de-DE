---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/working-with-3d-scenes/overriding-scene-materials.html"
breadcrumb-title: ''
description: Überschreiben Sie vorhandene Materialien in 3D-Szenen, um sie zum Testen und in der Vorschau durch Ihre eigenen Substance-Materialien zu ersetzen.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Overriding scene materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Außerkraftsetzte Szenenmaterialien
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---


# Außerkraftsetzte Szenenmaterialien

Wenn Sie mit 3D-Szenen mit vorhandenen Materialien arbeiten, müssen Sie diese Materialien überschreiben, um sie durch Ihre eigenen zu ersetzen.

Ihr Material kann von Grund auf neu erstellt werden oder eine angepasste Version des Materials einer Szene, die [in ein Substance-Diagramm extrahiert wurde](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md).

![Überschreiben von Szenenmaterial, Anpassen und Zurücksetzen auf den Szenenstatus](../../assets/tweakOverriddenMaterial.gif "Überschreiben von Szenenmaterial, Anpassen und Zurücksetzen auf den Szenenstatus"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Szenenmaterial überschreiben

</td>
<td style="border: 0;" valign="top">

### Auf Szenenzustand zurücksetzen

</td>
<td style="border: 0;" valign="top">

### Verbundenes Material

</td>
</tr>
</table>

## Szenenmaterial überschreiben

Jedes Material, das in einer Szene verwendet wird, kann mit Ihrer eigenen Version überschrieben werden, d. h. mit einem neuen Material oder einer bearbeiteten Version des vorhandenen Materials.

Die Aktion &quot;Material überschreiben&quot; kann an zwei Stellen gefunden werden:

* Öffnen Sie das Menü &quot;Materialien&quot; und gehen Sie zum Untermenü des gewünschten Materials
* Drücken Sie Umschalt+LMB auf einem Szenenobjekt, um es auszuwählen, und klicken Sie dann auf RMB, um das Kontextmenü zu öffnen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Material überschreiben - Aktion im Viewport &quot;3D-Ansicht&quot;](../../assets/overrideMaterialActionViewport.png "Material überschreiben - Aktion im Viewport &quot;3D-Ansicht&quot;"){zoomable="yes"}

*Aktion im Ansichtsport der 3D-Ansicht*

</td>
<td style="border: 0;" valign="top">

![Material überschreiben - Aktion im Menü &quot;Materialien&quot;](../../assets/overrideMaterialActionMaterials.png "Material überschreiben - Aktion im Menü &quot;Materialien&quot;"){zoomable="yes"}

*Aktion im Materialmenü*

</td>
</tr>
</table>

Im Kontext von Designer, das USD für die interne Szenenbeschreibung verwendet, bedeutet &quot;Überschreiben&quot;, dass *eine Kopie* des Materials erstellt wird, die dem Original so genau wie möglich entspricht, und dass die *Materialbindung* der Gitter der Szene von dem Original in die Kopie geändert wird.

>[!NOTE]
>
> Die Kopien werden in der Szene in einem Ordner &quot;<b>Material</b>&quot; (&quot;Umfang&quot; in USD) unter dem Stamm erstellt und verwenden denselben Bezeichner wie das Original sowie ein numerisches Suffix (z. B.: &quot;rostedMetal\_0&quot;)

Das bedeutet zwei wichtige Dinge:

1. Das Originalmaterial wird nie verändert.
1. Alle in Designer vorgenommenen Änderungen werden auf die Kopie angewendet.

Sie können jede Modifikation jederzeit über dieselbe Aktion &quot;Material überschreiben&quot; aktivieren bzw. deaktivieren, wenn Sie das Material der ursprünglichen Szene wiederherstellen oder eine schnelle Vorher-/Nachher-Prüfung durchführen möchten

Da die Kopie so erstellt wird, dass sie mit dem Original übereinstimmt, sollte das Überschreiben eines Materials sein Aussehen in den meisten Fällen nicht ändern (siehe Hinweis unten), bis Sie ein Substance-Diagramm damit verbinden oder seine Eigenschaften bearbeiten.

>[!NOTE]
>
> Wenn ein irreguläres Format angewendet wird, berechnet Designer die Tangenten und Binormalen der betroffenen Meshes. Dies kann einige Zeit dauern und das Aussehen dieser Meshes ändern, insbesondere wenn diese Meshes keine definierte Normalskala und -neigung aufweisen oder andere verwenden.

>[!IMPORTANT]
>
> Die <b>AdobeStandardMaterial</b>-Schattierung wird im gesamten Substance 3D-Ökosystem unterstützt, ist jedoch kein Industriestandard und *kann daher möglicherweise nicht von Drittanbieteranwendungen wie Blender* unterstützt werden.
> 
> Für die optimale Interoperabilität außerhalb von Substance 3D-Anwendungen wird derzeit empfohlen, das <b>UsdPreviewSurface</b>-Schattierung-Modell zu verwenden, selbst wenn dieses Modell wesentlich weniger Materialeigenschaften und -effekte unterstützt.

## Auf Szenenzustand zurücksetzen

Wenn Sie den Ausgangszustand eines Materials wiederherstellen müssen, es aber überschrieben bleiben und trotzdem bearbeiten können, kann jede Materialkopie auf ihre ursprünglichen Werte zurückgesetzt werden.

Wenn ein Materialeigenschaftswert geändert oder eine Textur aus einem Diagramm darauf angewendet wurde, wird die Eigenschaft auf ihren ursprünglichen Wert oder ihre Textur zurückgesetzt.

Ein Material kann vollständig oder pro Eigenschaft zurückgesetzt werden.

Mit der Aktion &quot;Material auf Szenenzustand zurücksetzen&quot; im Untermenü des Materials oder im Kontextmenü eines Gitters können Sie das Material vollständig zurücksetzen.

Die Aktion kann an drei Stellen durchgeführt werden:

* Öffnen Sie das Menü &quot;Materialien&quot; und gehen Sie zum Untermenü des gewünschten Materials
* Drücken Sie Umschalt+LMB auf einem Szenenobjekt, um es auszuwählen, und klicken Sie dann auf RMB, um das Kontextmenü zu öffnen
* Das Hamburger-Menü oben in den Eigenschaften des Materials

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Material auf Szenenstatus zurücksetzen - Aktion im Viewport &quot;3D-Ansicht&quot;](../../assets/resetMaterialToSceneStateActionViewport.png "Material auf Szenenstatus zurücksetzen - Aktion im Viewport &quot;3D-Ansicht&quot;"){zoomable="yes"}

*Aktion im Ansichtsport der 3D-Ansicht*

</td>
<td style="border: 0;" valign="top">

![Material auf Szenenstatus zurücksetzen - Aktion im Menü &quot;Materialien&quot;](../../assets/resetMaterialToSceneStateActionMaterials.png "Material auf Szenenstatus zurücksetzen - Aktion im Menü &quot;Materialien&quot;"){zoomable="yes"}

*Aktion im Materialmenü*

</td>
<td style="border: 0;" valign="top">

![Material auf Szenenstatus zurücksetzen - Aktion im Dock &quot;Eigenschaften&quot;](../../assets/resetMaterialToSceneStateActionProps.png "Material auf Szenenstatus zurücksetzen - Aktion im Dock &quot;Eigenschaften&quot;"){zoomable="yes"}

*Aktion in den Materialeigenschaften*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Die Aktion ist auch *pro Eigenschaft* in den Materialeigenschaften verfügbar, falls Sie nur einige Aspekte eines Materials zurücksetzen möchten.

Öffnen Sie das Hamburger-Menü der Materialeigenschaft, um die Aktion &quot;Auf Standardszenenstatus zurücksetzen&quot; zu finden.

</td>
<td style="border: 0;" valign="top">

![Auf Szenenstatus zurücksetzen - Aktion in Materialeigenschaften](../../assets/resetPropertyToSceneStateAction.png "Auf Szenenstatus zurücksetzen - Aktion in Materialeigenschaften"){zoomable="yes"}

</td>
</tr>
</table>

## Verbundenes Material

Erneut: Designer ändert das Szenenmaterial nicht direkt. Es wird eine Kopie der Szene erstellt und die Gitter werden an diese Kopie anstatt an das Original gebunden.

Auf der anderen Seite verfügt Designer über eine *eigene* separate Materialliste im Menü &quot;Materialien&quot;, die standardmäßig mit der Materialliste der Szene übereinstimmt. Du kannst jederzeit neue Materialien in diese Liste einfügen.

Dies ist ein *anderer* Datensatz, der nur in Designer erstellt und verwaltet wird. Diese Materialien sind dann *mit den Kopien* verbunden, die die ursprünglichen Materialien der Szene überschreiben.

![Überschreiben von Materialien - Datenschema](../../assets/overridingMaterialsSchematic.png "Überschreiben von Materialien - Datenschema"){zoomable="yes"}

Sie können jedes der im Menü &quot;Materialien&quot; aufgeführten Materialien mit den von Designer in der Szene erstellten Kopien verbinden: Klicken Sie auf RMB in einer Kopie im Szenenbrowser und wechseln Sie zum Untermenü &quot;Material verbinden&quot;.

Das Untermenü listet alle Materialien in der Szene sowie alle Materialien auf, die Sie möglicherweise manuell über das Menü &quot;Materialien&quot; erstellt haben.

![Materialien verbinden](../../assets/connectMaterials.gif "Materialien verbinden"){zoomable="yes"}

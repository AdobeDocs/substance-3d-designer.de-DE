---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Mit der Funktion "An Interoperabilität senden" in Substance 3D Designer können Sie Materialien in andere Anwendungen exportieren.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Senden an...  Interoperabilität
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Senden an...  Interoperabilität

![Von Designer an Substance 3D-Apps senden](../../../assets/explorer-interop.png "Von Designer an Substance 3D-Apps senden"){width="512px"}

Adobe Substance 3D Designer ist mit [Substance 3D Sampler](https://www.adobe.com/de/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) und [Substance 3D Stager](https://www.adobe.com/de/products/substance3d-stager.html) kompatibel. Dadurch können Sie *senden* und *senden* schnell bearbeiten und die Iteration im gesamten Substance 3D-Ökosystem erleichtern.

Der Arbeitsablauf ist in der Regel wie folgt:

1. Legen Sie das Attribut <b>Type</b> in den Eigenschaften eines [Substance-Grafen fest.](../../../compositing-graphs/graph-parameters/graph-parameters.md)
1. Wählen Sie im Bereich [Explorer](../the-explorer-window.md) das Paket aus, das Sie senden möchten.
1. Wählen Sie in der Dropdown-Liste <b>Publish/Send</b> des Explorers die Zielanwendung aus
1. Nehmen Sie Änderungen an Grafen vor
1. Wiederholen Sie Schritt 3, um das Paket erneut zu senden und das vorhandene gesendete Element mit Ihren Änderungen zu aktualisieren.

>[!WARNING]
>
> Interoperabilitätsfeatures sind *nicht* in der <b>Steam</b>-Version verfügbar.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Festlegen des Grafen

Substance-Graf können viele Funktionen haben. Sie müssen im Voraus festlegen, wie ein Graf genau funktioniert, um sicherzustellen, dass er ordnungsgemäß übertragen werden kann.

Im Abschnitt <b>Attribute </b> der Eigenschaften eines [Substance-Grafen &#x200B;](../../../compositing-graphs/graph-parameters/graph-parameters.md) gibt es eine <b>Type</b>-Option mit einem Dropdown-Menü, das die folgenden Optionen enthält:

</td>
<td style="border: 0;" valign="top">

![Typattribut des Substance-Grafen](../../../assets/type-attribute.jpg "Typattribut des Substance-Grafen")

</td>
</tr>
</table>

* **Nicht angegeben** ist der Standardtyp, wenn Sie ihn nicht festgelegt haben. Je nachdem, an welche Anwendung Sie senden, kann dies unterschiedlich interpretiert werden. [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) verwendet standardmäßig zum Beispiel Material.
* **Das Standard-Material** ist für Mehrkanal-PBR-Material mit ordnungsgemäß beschrifteten [Ausgaben](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) vorgesehen.
* **Decal Material** ist für ein Mehrkanal-PBR-Material mit Alphakanal, das als Decal in [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) oder [Substance 3D Sampler](https://www.adobe.com/de/products/substance3d-sampler.html) angewendet wird;
* **Atlas Material** ist für ein Mehrkanal-PBR-Material, das aus mehreren Atlasbildern besteht, zur Verwendung mit dem [Atlas Scatter-Knoten](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md) in Designer oder [Substance 3D Sampler](https://www.adobe.com/de/products/substance3d-sampler.html);
* **Filter** ist für universelle Filter vorgesehen, die beide in [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) oder [Substance 3D Sampler](https://www.adobe.com/de/products/substance3d-sampler.html) verwendet werden.
* Der **Mesh-basierte Generator** ist für Maskengenerator mit mehreren Eingaben vorgesehen. Dieser wird nur von [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) verwendet;
* **Textur Generator** ist für Einkanalzuordnungen wie 2D-Prozeduren und Rauschen;
* **Umgebungslicht** ist für eine Einzelkanal-Beleuchtungsumgebung vorgesehen, die zum Beleuchten von Szenen und Objekten verwendet wird.
* **Light Textur** ist für eine Ein Kanal-Textur, die auf eine physische Light angewendet wird.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menü &quot;Senden an&quot;

Der Sendevorgang umfasste das [Veröffentlichen](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) eines oder mehrerer Pakete in Substance 3D Asset Files (SBSAR) hinter den Szenen.

Das Senden von Inhalten kann auf folgende Weise erfolgen:

* Klicken Sie mit der rechten Maustaste auf ein Paket, und öffnen Sie die Datei <b>Senden an...Untermenü &quot;</b>&quot; im Kontextmenü und anschließend die Option &quot;<b>Senden an&quot; auswählen...</b>-Option für die Zielanwendung
* Klicken Sie oben im Bedienfeld &quot;Explorer&quot; auf die Schaltfläche ![](../../../assets/sendto-icon.jpg) <b>Publish/Send</b>, und wählen Sie dann <b>Senden an...</b>-Option für die Zielanwendung.

</td>
<td style="border: 0;" valign="top">

![Menü &quot;Publish/Senden an&quot; im Explorer](../../../assets/explorer-sendto-displayed.jpg "Menü &quot;Publish/Senden an&quot; im Explorer")

</td>
</tr>
</table>

### zurückhaltend

Wenn Sie ein Paket, das *war, erneut senden, das bereits einmal* an die *gleiche Ziel*-Anwendung gesendet wurde, wird das Asset in der Zielanwendung mit der neuen Version *aktualisiert*.

## An Player senden

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) unterstützt *sowohl* <b>Substance 3D-Dateien</b> (SBS) als auch <b>Substance 3D-Assets</b> (SBSAR).

Für das Senden an den Player muss die ausführbare Datei des Substance Players vom Benutzer manuell *gefunden* werden. Dies kann wie folgt erfolgen:

* Wenn Sie dazu aufgefordert werden, ob der Player *seit der Installation von Designer nie gefunden wurde*;
* Sie können jederzeit im Menü <b>Extras</b> die Option <b>Substance Player > Suchen... verwenden.</b>-Option.

Für den Empfang von Designer im Player muss das Substance 3D Designer *Installationsverzeichnis* manuell vom Benutzer gespeichert werden. Dies kann wie folgt erfolgen:

* Wenn Sie dazu aufgefordert werden, ob Designer seit der Installation von Player *nie gefunden* wurde;
* Sie können jederzeit im Menü &quot;<b>Optionen</b>&quot; die Option &quot;<b>Adobe Substance 3D Designer suchen</b>&quot; verwenden.

>[!NOTE]
>
> Beim Senden von Substance 3D-Dateien (SBS) an Player wird ein Substance 3D-Asset (SBSAR) als *temporäre Datei* veröffentlicht.

## Probleme

Möglicherweise treten beim Senden von Paketen Fehler auf, z. B.:

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


Dies liegt in der Regel an Standardfehlern und -warnungen. Beheben Sie diese, um das Problem zu beheben:

* Keine [Ausgabeknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)in Ihrem Diagramm definiert. Ausgabeknoten hinzufügen und etwas mit ihnen verbinden;
* Fehlende oder fehlerhafte Variablen in [Knoten abrufen](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) in [Funktionsdiagrammen](../../../function-graphs/function-graphs.md). Verfolgen Sie sie mit dem *gelben Warnschild* auf den betroffenen Knoten.

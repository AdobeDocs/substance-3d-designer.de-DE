---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Automatisches Freistellen , um Texturen automatisch zuzuschneiden, um leere Rahmen zu entfernen und die Texturabmessungen zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Automatisches Freistellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Automatisches Freistellen

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**In:** Filter*/Transformationen*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Automatisches Freistellen** passt die **Eingabe** so an, dass der Inhalt entweder in der *Mitte* des Bildes platziert wird, ohne dass die Größe geändert wird, oder *die Größe auf den Bereich* des Bildes angepasst wird.

Der Inhalt des Bildes wird durch ein Feld definiert, das an die *ersten und letzten Pixel* auf **X** und **Y** angepasst ist, deren Werte *höher als 0* sind (d. h. nicht schwarz). Mit der **Color**-Version können Sie aus den RGB- und Alpha-Kanälen auswählen, um dieses Feld zu definieren.

</td>
</tr>
</table>

## Parameter

* **Modus** *Integer* Legen Sie die Zuschneidemethode fest, die angewendet werden soll:
  * *Quadrat zuschneiden*: Das Bild wird so zugeschnitten, dass sich die Form in der Mitte des kleinsten *quadratischen* Bildes befindet, das es vollständig enthalten kann.
  * *Automatisches Freistellen*: Das Bild wird so beschnitten, dass sich die Form in der Mitte des kleinsten *quadratischen oder nicht quadratischen* Bildes befindet, das es vollständig enthalten kann
  * *Einpassen (Verhältnis beibehalten)*: Die Größe des Bildes wird auf die *volle Bildbreite* angepasst, wobei die *Proportionen* (d. h. das Verhältnis von Breite zu Länge) beibehalten werden.
  * *Füllen (Dehnen)*: Die Größe des Bildes wird auf den *vollen Bereich* des Bildes geändert.
* **Alpha verwenden** *Boolesch* Verwenden Sie den Alphakanal der **Eingabe**, um die *Grenzen* des Bildinhalts für das Zuschneiden zu bestimmen. Bei der Einstellung &quot;*False*&quot; werden stattdessen schwarze Pixel verwendet.\
  *Hinweis*: Dieser Parameter ist nur in der **Color**-Version des Knotens verfügbar.
* **Filtermodus** *Integer* Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn *zwischen Pixeln interpoliert wird*:
  * *Nächste*: nimmt genau den *gleichen* Wert auf (schneller)
  * *Bilinear*: wendet einen bilinearen Filter auf das Ergebnis für einen *glatteren*-Look an.
  * *Auto*: Verwendet je nach dem ausgewählten **Modus** zum Zuschneiden den am besten geeigneten der beiden oben genannten Modi

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>

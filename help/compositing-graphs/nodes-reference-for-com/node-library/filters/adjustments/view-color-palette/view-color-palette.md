---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Farbpalette anzeigen , um aus Texturen extrahierte Farbpalettendaten für die Analyse anzuzeigen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbpalette anzeigen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# Farbpalette anzeigen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Farbe quantisieren&quot;](view-color-palette.resources/view-color-palette-01.png "Symbol &quot;Farbe quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verpackt eine Farbpalette in ein Quadrat oder Rechteck, um sie leichter in der Diagramm- oder 2D-Ansicht darzustellen.\
Das Packing zielt darauf ab, so wenig freie Zeitnischen wie möglich zu lassen.

</td>
</tr>
</table>

Die Reihenfolge der Farben in der Palette bleibt erhalten, wobei die Farben ähnlich wie beim Textumbruch von links nach rechts und von oben nach unten fließen.

Dieser Knoten kann verwendet werden, um die Paletten zu visualisieren, die von den folgenden Knoten erzeugt werden: [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Farbpalette erstellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Palette</b> <i>Farbe</i> PRIMÄR | Eine geordnete Liste von RGB-Farben, die als Pixelzeile codiert sind. Die Palette kann maximal 256 Farben enthalten.   Dies ist die Palette, die der Knoten verpackt und rendert. |
| <b>Farbmenge der Palette</b> <i>Integer</i> | Die Menge der in der Palette gespeicherten Farben.   Wenn diese Zahl nicht mit der tatsächlichen Farbmenge in der Bildeingabe der Palette übereinstimmt, ist die Visualisierung möglicherweise unvollständig oder weist mehr leere Steckplätze auf als unbedingt erforderlich. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Farbe</i> | Die Visualisierung der verpackten Palette. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Farbpalette anzeigen: Beispiel 1](view-color-palette.resources/view-color-palette-02.png "Farbpalette anzeigen: Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Farbpalette anzeigen: Beispiel 2](view-color-palette.resources/view-color-palette-03.png "Farbpalette anzeigen: Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Farbpalette anzeigen: Beispiel 3](view-color-palette.resources/view-color-palette-04.png "Farbpalette anzeigen: Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Farbpalette anzeigen: Beispiel 4](view-color-palette.resources/view-color-palette-05.png "Farbpalette anzeigen: Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

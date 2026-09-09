---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Farbpalette erstellen , um eine 16-Farben-Palette aus Texturen für stilisierte Effekte zu extrahieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbpalette erstellen (16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Farbpalette erstellen (16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Farbe quantisieren&quot;](create-color-palette-16.resources/CreateColorPalette16.png "Symbol &quot;Farbe quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erstellt eine geordnete Liste der Farben und gibt diese als Palette aus, mit maximal 16 Farben.

Der Knoten kann neue Farben an eine vorhandene Palette anhängen, indem er den Satz von Paletteneingaben verwendet.

Dieser Knoten kann in Kombination mit den folgenden Knoten verwendet werden: [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Farbpalette anwenden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Palette</b> <i>Farbe</i> PRIMÄR | Eine geordnete Liste von RGB-Farben, die als Pixelzeile codiert sind. Die Palette kann maximal 256 Farben enthalten.   Diese Eingabe ist optional. Wenn sie verwendet wird, werden die vom Knoten eingerichteten Farben an diese Palette angehängt.   Die Palette kann mit dem Knoten [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) angezeigt werden. |
| <b>Farbmenge der Palette</b> <i>Integer</i> | Die Menge der in der Palette gespeicherten Farben.   Wenn diese Zahl nicht mit der tatsächlichen Farbmenge in der Bildeingabe der Palette übereinstimmt, ist die Visualisierung möglicherweise unvollständig oder weist mehr leere Steckplätze auf als unbedingt erforderlich. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Palette</b> <i>Farbe</i> | Die aktualisierte Palette, an die die angegebenen Farben angehängt wurden. |
| <b>Farbmenge der Palette</b> <i>Integer</i> | Die aktualisierte Anzahl von Farben, die in der Palette gespeichert sind, wobei die angegebene Anzahl von Farben hinzugefügt wird. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Farbmenge</b> *Integer* | Die Anzahl der Farben, die der Palette hinzugefügt werden sollen. |
| <b>Farbe #</b> *Fließkommazahl3* *Es sind so viele Parameter wie der Wert &quot;Farbmenge&quot; verfügbar* | Eine Farbe, die der Palette hinzugefügt werden soll.   Die Farben werden der Palette in derselben Reihenfolge angehängt wie diese nummerierte Liste. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Farbpalette erstellen: Beispiel 1](create-color-palette-16.resources/create_color_palette_example_1.png "Farbpalette erstellen: Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Farbpalette erstellen: Beispiel 2](create-color-palette-16.resources/create_color_palette_example_2.png "Farbpalette erstellen: Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

![Farbpalette erstellen: Beispiel 3](create-color-palette-16.resources/create_color_palette_example_3.png "Farbpalette erstellen: Beispiel 3"){zoomable="yes"}

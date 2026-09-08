---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Farbpalette anwenden , um Texturen mithilfe einer Farbpalette für stilisierte Farbeffekte neu zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbpalette anwenden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Farbpalette anwenden

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Farbe quantisieren&quot;](../../../../../../assets/ApplyColorPalette.png "Symbol &quot;Farbe quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet die Farben in einer geordneten Palette mithilfe einer ID-Map auf ein Bild an.

Die Farben werden verteilt, indem die Farbindizes auf der ID-Map mit den Farbindizes in der Palette übereinstimmen.

Beispielsweise wird die #2 in der Palette auf alle Pixel in der ID-Map mit einem ID-Wert von 2 angewendet.

Dieser Knoten kann in Kombination mit den folgenden Knoten verwendet werden: [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Farbpalette erstellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>ID</b> <i>Graustufen</i> PRIMÄR | Die Eingabe-ID-Map, die zum Verteilen der Farben in der Eingabepalette verwendet wird.   Eine ID-Map ist ein Bild, bei dem Pixel, die Teil eines Ganzen sind (z. B. eine Form), alle denselben eindeutigen Identifikationswert aufweisen. In diesem Fall ist der Wert eine Ganzzahl.   Eine ID-Zuordnung kann mithilfe eines Knotens [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) erstellt werden. |
| <b>Palette</b> <i>Farbe</i> | Eine geordnete Liste von RGB-Farben, die als Pixelzeile codiert sind. Die Palette kann maximal 256 Farben enthalten. Dies ist die Palette, die der Knoten den Indizes der ID-Map zuordnet.   Paletten können mit einem Knoten [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) erzeugt und mit einem Knoten [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md) geändert werden. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Farbe</i> | Das Ergebnis der Zuordnung der Farben in der Palette zu den Indizes der ID-Map. |

## Beispiele

![Farbpalette anwenden: Beispiel 1](../../../../../../assets/apply_color_palette_example_2.png "Farbpalette anwenden: Beispiel 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Farbpalette anwenden: Beispiel 3](../../../../../../assets/apply_color_palette_example_4.png "Farbpalette anwenden: Beispiel 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

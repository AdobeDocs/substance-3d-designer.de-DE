---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Krümmung glätten , um glatte Krümmungs-Map aus Höhen-Map für die Extraktion von Oberflächendetails zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kurvenglättung
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# Kurvenglättung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Krümmung Glattes Knotensymbol](../../../../../../assets/CurvatureSmooth.png "Krümmung Glattes Knotensymbol"){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet die Krümmung einer Fläche, die durch einen Normalen-Map beschrieben wird.

Eine Krümmungs-Map stellt die konkaven und konvexen Flächen einer Fläche dar.\
Flache Bereiche sind zu 50 % grau. Konvexe Bereiche sind heller, konkave Bereiche sind dunkler.

</td>
</tr>
</table>

Die konkaven und konvexen Bereiche werden ebenfalls in ihre eigenen Ausgänge aufgeteilt, um die Auswahl bzw. Maskierung von Bereichen basierend auf diesen Eigenschaften zu vereinfachen.

>[!TIP]
>
> Sehen Sie sich [Krümmung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) nach, um eine schärfere Version zu erhalten, oder [Krümmung Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md), wenn Sie weitere Optionen benötigen.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normal</b> <i>Farbe</i> <b>PRIMÄR</b> | Die Normalen-Map, die die Fläche beschreibt, für die die Krümmung berechnet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen</i> | Die Krümmungs-Map wurde von der Eingabe-Normalen-Map berechnet.   Flache Bereiche sind zu 50 % grau. Konvexe Bereiche sind heller, konkave Bereiche sind dunkler. |
| <b>Konvexität</b> <i>Graustufen</i> | Die Konvexitätskarte wurde aus der Eingabe-Normalen-Map berechnet.   Je konvexer ein Bereich ist, desto heller ist er auf der Karte.  Flache oder konkave Bereiche sind schwarz. |
| <b>Konkavität</b> <i>Graustufen</i> | Die Konkavitäts-Map wurde aus der Eingabe-Normalmap berechnet.   Je konkaver ein Gebiet ist, desto heller ist es auf der Karte.  Flache oder konvexe Bereiche sind schwarz. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normales Format</b> *Integer* | Das Format der Eingabe-Normalmap. Kehrt den grünen Kanal effektiv um.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Die Y-Achse zeigt nach oben</li> <li data-preserve-html="true"><b style="">OpenGL:</b> Die Y-Achse zeigt nach unten</li> </ul> |

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Glatte Krümmung: Beispiel 2](../../../../../../assets/curvature_smooth_example_2.jpg "Kurvenglättung: Beispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Glatte Krümmung: Beispiel 3](../../../../../../assets/curvature_smooth_example_3.jpg "Kurvenglättung: Beispiel 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Glatte Krümmung: Beispiel 4](../../../../../../assets/curvature_smooth_example_5.jpg "Kurvenglättung: Beispiel 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Glatte Krümmung: Beispiel 5](../../../../../../assets/curvature_smooth_example_6.jpg "Kurvenglättung: Beispiel 5"){zoomable="yes"}

</td>
</tr>
</table>

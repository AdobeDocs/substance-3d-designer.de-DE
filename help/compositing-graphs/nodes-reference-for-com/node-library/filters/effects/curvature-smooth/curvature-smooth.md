---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Kurvenglättung , um aus Height-Maps glatte Krümmungszuordnungen für die Oberflächendetailextraktion zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kurvenglättung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Kurvenglättung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Krümmungsglätten-Knotensymbol](../../../../../../assets/CurvatureSmooth.png "Krümmungsglätten-Knotensymbol"){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet die Krümmung einer Fläche, die durch eine Normalmap beschrieben wird.

Eine Krümmungskarte stellt die konkaven und konvexen Bereiche einer Oberfläche dar.\
Flache Bereiche sind zu 50 % grau. Konvexe Bereiche sind heller, konkave Bereiche sind dunkler.

</td>
</tr>
</table>

Die konkaven und konvexen Bereiche werden ebenfalls in ihre eigenen Ausgänge aufgeteilt, um die Auswahl bzw. Maskierung von Bereichen basierend auf diesen Eigenschaften zu vereinfachen.

>[!TIP]
>
> Sehen Sie sich [Kurvenzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) nach, um eine schärfere Version zu erhalten, oder [Kurvenzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md), wenn Sie weitere Optionen benötigen.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Normal</b> *Farbe* <b>PRIMÄR</b> | Die Normalmap, die die Oberfläche beschreibt, deren Krümmung berechnet werden soll. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Krümmung</b> *Graustufen* | Die aus der Eingabe-Normalmap berechnete Krümmungskarte.   Flache Bereiche sind zu 50 % grau. Konvexe Bereiche sind heller, konkave Bereiche sind dunkler. |
| <b>Konvexität</b> *Graustufen* | Die Konvexitätskarte, die aus der Eingabe-Normalmap berechnet wurde.   Je konvexer ein Bereich ist, desto heller ist er auf der Karte.  Flache oder konkave Bereiche sind schwarz. |
| <b>Konkavität</b> *Graustufen* | Die Konkavitäts-Map wurde aus der Eingabe-Normalmap berechnet.   Je konkaver ein Gebiet ist, desto heller ist es auf der Karte.  Flache oder konvexe Bereiche sind schwarz. |

## Parameter

|  |  |
| --- | --- |
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

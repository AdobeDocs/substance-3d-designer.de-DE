---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Quad-Transformation auf Pfad", um Elemente entlang von Pfadkurven quadratisch zu transformieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quad-Transformation auf Pfad
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Quad-Transformation auf Pfad

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](quad-transform-on-path.resources/quad-transform-on-path-01.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Deformieren Sie einen Pfad mit 4 Griffen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen *Pfad*-Verarbeitungsknoten. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>p00</b> <i>Float2</i> | Die Position des oberen linken Handles. |
| <b>p01</b> <i>Float2</i> | Die Position des oberen rechten Handles. |
| <b>p02</b> <i>Float2</i> | Die Position des linken unteren Griffs. |
| <b>p03</b> <i>Float2</i> | Die Position des rechten unteren Griffs. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-02.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-03.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-02.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-04.jpg" alt="QuadTransformOnPaths-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](quad-transform-on-path.resources/quad-transform-on-path-05.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](quad-transform-on-path.resources/quad-transform-on-path-06.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

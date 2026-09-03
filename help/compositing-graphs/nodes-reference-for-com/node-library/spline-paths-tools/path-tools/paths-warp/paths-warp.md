---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Pfadverkrümmung", um Texturen entlang Pfadkurven zu verkrümmen, um gekrümmte und organische Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfadverkrümmung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Pfadverkrümmung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](paths-warp.resources/paths-warp-01.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verformen Sie die Eingabepfade entsprechend der <b>Verlaufseingabe</b>. (Derselbe Effekt wie der Knoten [Verkrümmen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).)

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |
| <b>Verlaufseingabe</b> <i>Graustufen</i> | Der Height-ähnliche Eingang steuert sowohl den Grad als auch die Richtung der Verformung. (Derselbe Effekt wie der Knoten [Verkrümmen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).) |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Die transformierten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>Gleitend</i> | Der Parameter <b>Intensität</b> legt die Intensität der Verformung fest. |
| <b>Anzahl der Schritte</b> <i>Integer</i> | Verwenden Sie einen höheren Wert, um die Eingabepfade in mehreren kleinen Schritten zu verkrümmen.<br>Dies kann verhindern, dass sich der Pfad selbst kreuzt, insbesondere wenn hohe <b>Intensitätswerte</b> verwendet werden. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/paths-warp-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-warp.resources/paths-warp-03.jpg" alt="PathsWarp-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/paths-warp-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-warp.resources/paths-warp-04.jpg" alt="PathsWarp-Variant2-After">
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

![Knotenbeispiel 1](paths-warp.resources/paths-warp-05.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

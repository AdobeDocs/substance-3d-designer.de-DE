---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Pfade verformen", um Texturen entlang von Pfadkurven zu verformen und so gekrümmte und organische Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfadverkrümmung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Pfadverkrümmung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/paths-warp-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verformen Sie die Eingabepfade entsprechend der <b>Verlaufseingabe</b>. (Derselbe Effekt wie der Knoten [Verkrümmen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).)

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Pfade</b> *Farbe*\
Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten.

<b>Verlaufseingabe</b> *Graustufen*\
Der Height-ähnliche Eingang steuert sowohl den Grad als auch die Richtung der Verformung. (Derselbe Effekt wie der Knoten [Verkrümmen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).)

## Ausgangsanschlüsse

<b>Pfade</b> *Farbe*\
Die transformierten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten.

## Parameter

<b>Intensität</b> *Gleitend*\
Der Parameter <b>Intensität</b> legt die Intensität der Verformung fest.

<b>Anzahl der Schritte</b> *Integer*\
Verwenden Sie einen höheren Wert, um die Eingabepfade in mehreren kleinen Schritten zu verkrümmen.\
Dies kann verhindern, dass sich der Pfad selbst kreuzt, insbesondere wenn hohe <b>Intensitätswerte</b> verwendet werden.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
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

![Knotenbeispiel 1](../../../../../../assets/PathsWarp-Demo1.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

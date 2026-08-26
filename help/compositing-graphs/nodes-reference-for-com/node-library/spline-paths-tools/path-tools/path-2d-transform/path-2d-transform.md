---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "2D-Pfad transformieren", um Pfade mit Translations-, Dreh- und Skalierungsvorgängen zu transformieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfad-2D-Transformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Pfad-2D-Transformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/path-2d-transform-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Transformiert Pfade mithilfe eines Gizmos.

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Pfade</b> *Farbe*\
Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten.

## Ausgangsanschlüsse

<b>Pfade</b> *Farbe*\
Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten.

## Parameter

<b>Transformationsmatrix</b> *Float4*\
Die Transformationsmatrix, die auf die Splines angewendet wird. Es stehen drei Bearbeitungsmodi für die Matrixparameter zur Verfügung:\
*- Transformations-Gizmo:* optimieren die Handles des Gizmos, das in der [2D-Ansicht](../../../../../../interface/2d-view/2d-view.md) angezeigt wird, wenn der Knoten 2D-Transformation (Spline) ausgewählt ist;\
*- Drehung/Dehnung:* Steuern Sie die Drehung und Dehnung der Splines einzeln. Beachten Sie, dass Werte immer relativ zur aktuellen Transformation angewendet werden. Wenn Sie z. B. 50 % Breite zweimal anwenden, erhalten Sie eine Breite von 25 %.\
*- Matrixwerte:* Klicken Sie auf die Schaltfläche <b>Matrixwerte bearbeiten</b>, um die numerischen Rohwerte der Matrix direkt einzugeben.

<b>Offset</b> *Float2*\
Wendet einen Positionsversatz auf die Splines in X (horizontal) und Y (vertikal) an.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Pfade2DTransform-Variant1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Pfade2DTransform-Variant2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

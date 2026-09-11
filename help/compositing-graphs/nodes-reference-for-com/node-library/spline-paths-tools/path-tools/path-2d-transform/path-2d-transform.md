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
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# Pfad-2D-Transformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](path-2d-transform.resources/path-2d-transform-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Transformiert Pfade mithilfe eines Gizmos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Transformationsmatrix</b> <i>Float4</i> | Die Transformationsmatrix, die auf die Splines angewendet wird. Es stehen drei Bearbeitungsmodi für die Matrixparameter zur Verfügung:<br>*- Transformations-Gizmo:* zum Anpassen der Handles des Gizmos, das in der [2D-Ansicht](../../../../../../interface/2d-view/2d-view.md) angezeigt wird, wenn der Transformieren 2D-Spline-Knoten ausgewählt ist;<br>*- Drehung/Dehn:* Sie können die Drehung und den dehn der Splines einzeln steuern. Beachten Sie, dass Werte immer relativ zur aktuellen Transformation angewendet werden. Wenn Sie z. B. 50 % Breite zweimal anwenden, erhalten Sie eine Breite von 25 %;<br>*- Matrixwerte:* Klicken Sie auf die Schaltfläche <b>Matrixwerte bearbeiten</b>, um die numerischen Rohwerte der Matrix direkt einzugeben. |
| <b>Offset</b> <i>Float2</i> | Wendet einen Positionsversatz auf die Splines in X (horizontal) und Y (vertikal) an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant1.jpg" alt="Pfade2DTransform-Variant1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PfadePolygon_Variant1">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant2.jpg" alt="Pfade2DTransform-Variant2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

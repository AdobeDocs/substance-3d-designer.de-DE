---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Pfade zu Spline", um Pfaddaten in Splines zu konvertieren, um sie mit Spline-basierten Knoten zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfade zum Spline-Effekt
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Pfade zum Spline-Effekt

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](paths-to-spline.resources/paths-to-splines-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert Pfade in Splines, die mit einem [Spline Render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md)-Knoten dargestellt und mit [Spline Nodes](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) verarbeitet werden können.

</td>
</tr>
</table>

>[!NOTE]
>
> Splines sind Kurven und können daher die Schärfe von Pfaden nicht beibehalten. Erwarten Sie eine Glättung von Formen, wenn Sie Pfade in Splines konvertieren.

>[!TIP]
>
> Dieser Knoten kann nach dem Knoten [Maske in Pfade](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) verwendet werden, um eine Kette zu bilden, die eine Maske in Splines konvertiert.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> * Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> * Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines <b>Farbbilds</b> codiert sind:<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Ganzzahl</i> | Die Anzahl der Eingabe-Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Splines Precision</b> <i>Ganzzahl</i> | Der Logarithmus zur Basis 2 (log2) der Anzahl der Scheitelpunkt, die in jedem Pfad der Pfadeingabe abgetastet werden, um den entsprechenden Spline zu erstellen. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant1-Before.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant1-After.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/PathsToSpline-Variant2-After.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

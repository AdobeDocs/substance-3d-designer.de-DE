---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: Mit dem Knoten "Pfadevorschau" können Sie Pfaddaten in den 2D-Ansichten für das Debuggen und die Überprüfung anzeigen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vorschau von Pfaden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Vorschau von Pfaden

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/preview-paths-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Tracken Sie Segmente und Scheitelpunkt des Pfades auf dem angegebenen Hintergrund. Eine zufällige Farbe pro Pfad.

Sie erhalten ein ähnliches Ergebnis wie die <b>Vorschau</b>-Ausgabe der [Maske zu Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), jedoch mit weiteren Optionen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrund</b> <i>Farbe</i> | Ein Hintergrundbild über dem Bild mit dem Pfad wird angezeigt. Dadurch wird auch die Rendergröße gesteuert. |
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ecken anzeigen</b> <i>Boolescher Wert</i> | Zeigt auf jedem Scheitelpunkt ein Quadrat an, das als Ecke markiert ist (additive Überblendung). |
| <b>Scheitelpunkt anzeigen</b> <i>Boolescher Wert</i> | Zeigt auf jedem Scheitelpunkt eine Kreisform an (additive Füllmethode). Ecken werden weiterhin als Quadrate angezeigt. |
| <b>Segments-Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness gerenderter Segmente in Pixel an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

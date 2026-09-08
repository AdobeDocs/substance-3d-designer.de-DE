---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Polygon 1, um grundlegende Polygonmuster mit anpassbaren Seiten und Eigenschaften für geometrische Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polygon 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# Polygon 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Polygonform mit vielen Anpassungsoptionen. Eine einfachere Version finden Sie unter [Polygon 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Seiten</b> <i>3 - 32</i> | Legt die Anzahl der Seiten fest, die das Polygon haben soll. |
| <b>Explodieren</b> <i>0.0 - 1.0</i> | Verschiebt Polygon-&quot;Slices&quot; auseinander. |
| <b>Dreiecksgröße</b> <i>0.0 - 1.0</i> | Passt die Größe von Slices/Dreiecken an. Durch jede Anpassung könnte die Form auseinandergebrochen werden - nur bei 1,1. ist perfekt vernetzt! |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Skaliert die gesamte Form als Einheit. |
| <b>Automatische Skalierung</b> <i>False/True</i> | Passt die Skalierung so an, dass das gesamte Polygon mit Standardparametern in die Ansicht passt. |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Dreht die gesamte Form. |
| <b>Verlauf</b> <i>False/True</i> | Generiert Verlaufsscheiben/Dreiecke anstelle von Volltonrastern. Hinweis: ähnelt Polygon 2, wenn diese Einstellung aktiviert ist. |
| <b>Verlaufsumkehr</b> <i>False/True</i> | Spiegelt die Verlaufsrichtung, wenn &quot;Verlauf&quot; aktiviert ist. |
| <b>Kachelung</b> <i>1 - 16</i> | Legt fest, wie oft das Ergebnis gekachelt werden soll. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Squash und dehn mit nicht quadratischen Verhältnissen. |
| <b>Nicht quadratische Kachelung</b> <i>False/True</i> | Wenn die Quadratische Ausbreitung aktiviert ist, wird die Form ohne Quetschen gekachelt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/polygon-1-ex.gif" />
        </td>
    </tr>
</table>

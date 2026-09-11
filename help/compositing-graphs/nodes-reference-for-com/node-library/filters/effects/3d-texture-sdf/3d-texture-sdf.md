---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D Textur SDF-Knoten, um aus 3D-Daten Texturen für vorzeichenbehaftete Abstandsfelder zu generieren, um glatte Formen und Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Textur SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3D Textur SDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>In:</b> Filter > Effekt

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der SDF **-Knoten der** 3D-Textur generiert das *vorzeichenbehaftete Abstandsfeld* einer Form aus der *3D-Textur* der **Eingabe**, die die Slices des *Volumes* der Form darstellt.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maskeneingabe</b> <i>Graustufen</i> | Die <i>3D-Textur</i>, die die Slices des <i>Volumes</i> einer Form darstellt. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Schwellenwert</b> <i>Gleitend</i> | Wenn das Formvolumen durch einen <i>verblassenden Verlauf</i> beschrieben wird, wird der Verlaufswert festgelegt, bei dem die <i>Oberfläche</i> der Form <i>erkannt</i> wird. |
| <b>Ausgabe</b> <i>Integer</i> | Der Typ des Distanzfelds, das ausgegeben werden soll: <br>- <i>Distanzfeld</i>: gibt ein Abstandsfeld aus, das die Abstände <i>außerhalb</i> der Form beschreibt.<br>- <i>Vorzeichenbehaftetes Abstandsfeld</i>: gibt ein Abstandsfeld aus, das die Abstände <i>außerhalb</i> (positiv) und <i>innerhalb</i> (negativ) der Form beschreibt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>

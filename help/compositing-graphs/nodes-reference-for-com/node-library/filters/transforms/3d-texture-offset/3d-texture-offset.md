---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D-Texturversatz , um Texturen im 3D-Raum zu versetzen und Parallaxeffekte und Oberflächenvariationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Texturversatz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 3D-Texturversatz

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3d-texture-offset-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3d-texture-offset-02.png){width="200px"}

</td>
</tr>
</table>

<b>In:</b> Filter > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Texture Offset** wendet eine *Offset-Transformation* in den Achsen **X**, **Y** und **Z** auf ein Objekt an, das durch die *3D Textur* beschrieben wird, die mit dem **Eingang** verbunden ist.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen/Farbe</i> | Die <i>3D-Textur</i>, die ein 3D-Objekt beschreibt.<br>Das Objekt wird häufig in einem <i>Einheitscube </i> beschrieben. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Offset</b> <i>Float3</i> | Die Menge des Offsets im <i>Welt-Raum</i>, der auf das Objekt angewendet wird, das durch die <i>3D-Textur</i> beschrieben wird, die mit dem <b>Eingang</b> verbunden ist. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3d-texture-offset-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3d-texture-offset-04.png" />
        </td>
    </tr>
</table>

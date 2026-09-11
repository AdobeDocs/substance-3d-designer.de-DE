---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Mosaik , um Mosaikkacheleffekte zu erstellen, indem Sie Texturen in verpixelte Blöcke und Muster unterteilen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaik
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# Mosaik

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

&quot;Facetisiert&quot; eine vorhandene, glatte Verlaufsumsetzung mit abfallendem Verlauf, indem ein Multidurchgangseffekt [Verkrümmen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) ausgeführt wird. Wenn dieselbe Karte für beide Eingänge verwendet wird, wächst sie im Wesentlichen und betont die hellsten Bereiche.

Dies ist nützlich, um Graustufenzuordnungen wie Höhenkarte mehr Definition hinzuzufügen, da Formen mehr Definition erhalten können.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Farbe</b> <i>Farb-/Graustufeneingabe</i> |  |
| <b>Mosaikkarte</b> <i>Graustufen-Eingabe</i> | Verkrümmungstreiberzuordnung. Kann mit der ersten Eingabe identisch sein. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Beispiele</b> <i>0 - 16</i> | Bestimmt die Qualität mehrerer Samples. |
| <b>Intensität</b> <i>0.0 - 1.0</i> | Stärke des Effekts. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>

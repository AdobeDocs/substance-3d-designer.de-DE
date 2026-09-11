---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Steigung-Weichzeichner , um zum Erstellen von Bewegungsunschärfen Richtungs-Unschärfe-Effekt anzuwenden, die auf Höhen-Map-Steigungen basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Steigung weichzeichnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Steigung weichzeichnen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](slope-blur.resources/slope-blur.png){width="128px"}

![](slope-blur.resources/slope-blur-grayscale.png){width="128px"}

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen erweiterten, qualitativ hochwertigen Weichzeichner durch, bei dem die Anisotropie/Richtung durch eine Graustufen-&quot;Steigung Map&quot; gesteuert wird. Stellen Sie sich den Unschärfe-Effekt als Steigung vor, der den Steigungen Ihrer Steigung Map folgt, als wäre es eine Höhenkarte, ähnlich wie [Richtungsverzerrung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (auf der er intern basiert).

Das ist einer der interessantesten und mächtigsten Weichzeichner in Designer. Es kann verwendet werden, um einige sehr interessante und unerwartete Effekte zu erzielen, wie z. B. Splittern und Kanten der Verwitterung oder Verschmieren und Lecken von Dirt oder Rost.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Steigung-Weichzeichner&quot; für Farbeingaben bzw. &quot;Steigung-Weichzeichner-Graustufen&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Steigung</b> <i>Graustufen-Eingabe</i> | Steigung-Map zum Antriebswinkel der Anisotropie. sollte idealerweise geneigte Farbverläufe enthalten; harte, scharfe Übergänge werden nicht gut funktionieren! |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Beispiele</b> <i>0 - 32</i> | Die Anzahl der Samples beeinflusst die Qualität auf Kosten der Geschwindigkeit. |
| <b>Intensität</b> <i>0.0 - 16.0</i> | Weichzeichnungsgrad oder Stärke. |
| <b>Modus</b> <i>Weichzeichnen, Min, Max</i> | Füllmethode für nachfolgende Weichzeichnungspässe. &quot;Weichzeichnen&quot; verhält sich eher wie ein standardmäßiger [Anisotroper Weichzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), während Min vorhandene Bereiche &quot;wegfrisst&quot; und Max weiße Bereiche &quot;wegschmiert&quot;. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur02.gif" />
        </td>
    </tr>
</table>

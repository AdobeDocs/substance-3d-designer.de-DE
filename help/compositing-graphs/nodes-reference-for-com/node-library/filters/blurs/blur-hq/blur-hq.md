---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Weichzeichnen HQ , um hochwertige Unschärfe-Effekte auf Texturen anzuwenden und so sanfte, professionelle Weichzeichnungsergebnisse zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HQ-Weichzeichnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# HQ-Weichzeichnen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-1.png){width="128px"}

![](blur-hq.resources/blur-hq-grayscale.png){width="128px"}

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Gaußschen Weichzeichner hoher Qualität auf das Ergebnis durch. Viel bessere Qualität als [die Standardunschärfe des atomaren Rahmens](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Weichzeichner-HQ&quot; für Farbeingaben bzw. &quot;Weichzeichner-HQ-Graustufen&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 16.0</i> | Stärke (Radius) der Weichzeichnung. Je höher dieser Wert ist, desto weiter reicht die Weichzeichnung. |
| <b>Qualität</b> <i>0 - 1</i> | Erhöht den internen Sampling-Betrag für noch höhere Qualität bei reduzierter Berechnung. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/hqblur-example.gif" />
        </td>
    </tr>
</table>

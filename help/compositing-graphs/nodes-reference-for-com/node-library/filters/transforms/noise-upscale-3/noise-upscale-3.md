---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Rauschen Upscale 3, um Texturen mithilfe erweiterter Rauschen-basierter Algorithmen hochzuskalieren, um Details bei höheren Auflösungen beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rauschen Hochskalieren 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# Rauschen Hochskalieren 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-3.resources/noise-upscale.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verwendet eine Eingabe-Rauschen prozedural und skaliert sie auf die doppelte Auflösung, wobei die Details erhalten bleiben, ohne jedoch zu viel Kachelung einzuführen. Verwendet eine benutzerdefinierte Maske, um Rauschen über der Originalskala zu mischen.

Dieser Node ist hauptsächlich für die Optimierung von langsamen Grafen gedacht, die große, große Rauschen verwenden. Sie ermöglicht es Ihnen, höhere Auflösungen zu verwenden, ohne zu viel zusätzliche Rechenzeit zu verursachen.

Siehe auch [Rauschen Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) und [Rauschen Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), die in den meisten Fällen etwas besser darin sind, Kachelung auszublenden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Graustufen</b> <i>Graustufen-Eingabe</i> | Rauschen-Zielabbild. |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-3.resources/noise3ex.png" />
        </td>
    </tr>
</table>

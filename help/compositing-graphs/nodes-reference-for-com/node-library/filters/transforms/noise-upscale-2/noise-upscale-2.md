---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Rauschen Upscale 2, um Texturen mithilfe der Rauschen-basierten Interpolation hochzuskalieren, um die Qualität der Textur bei größeren Abmessungen beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rauschen Hochskalieren 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---


# Rauschen Hochskalieren 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-2.resources/noise-upscale-2-01.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verwendet eine Eingabe-Rauschen prozedural und skaliert sie auf die doppelte Auflösung, wobei die Details erhalten bleiben, ohne jedoch zu viel Kachelung einzuführen. Verwendet einen &quot;X&quot;-Maskentyp und überblendet den Text mit weniger Kontrast als die ursprüngliche Eingabe (die internen Mischmodi sind &quot;Max&quot; und &quot;Min&quot;).

Dieser Node ist hauptsächlich für die Optimierung von langsamen Grafen gedacht, die große, große Rauschen verwenden. Sie ermöglicht es Ihnen, höhere Auflösungen zu verwenden, ohne zu viel zusätzliche Rechenzeit zu verursachen.

Siehe auch [Rauschen Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) und [Rauschen Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) für verschiedene Varianten dieses Prozesses.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Offset1X</b> <i>0.0 - 1.0</i> | Schiebt den oberen und unteren Teil über die X-Achse. |
| <b>Offset1Y</b> <i>0.0 - 1.0</i> | Schiebt den oberen und unteren Teil über die Y-Achse. |
| <b>Offset2X</b> <i>0.0 - 1.0</i> | Schiebt den linken und rechten Teil über die X-Achse. |
| <b>Offset2Y</b> <i>0.0 - 1.0</i> | Führt den Schieberegler nach links und rechts über die Y-Achse. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-2.resources/noise-upscale-2-02.png" />
        </td>
    </tr>
</table>

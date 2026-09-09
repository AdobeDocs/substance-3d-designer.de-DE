---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Rauschen Upscale 1, um Texturen mithilfe von Rauschen-basierten Algorithmen hochzuskalieren, um beim Erhöhen der Auflösung der Textur Details beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rauschen Upscale 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# Rauschen Upscale 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-1.resources/noise-upscale.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verwendet eine Eingabe-Rauschen prozedural und skaliert sie auf die doppelte Auflösung, wobei die Details erhalten bleiben, ohne jedoch zu viel Kachelung einzuführen. Verwendet einen Masken-Typ &quot;X&quot; und überblendet den Text mit einem ähnlichen Kontrast wie die ursprüngliche Eingabe (der interne Mischmodus ist &quot;Kopieren&quot;).

Dieser Node ist hauptsächlich für die Optimierung von langsamen Grafen gedacht, die große, große Rauschen verwenden. Sie ermöglicht es Ihnen, höhere Auflösungen zu verwenden, ohne zu viel zusätzliche Rechenzeit zu verursachen.

Siehe auch [Rauschen Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) und [Rauschen Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) für verschiedene Varianten dieses Prozesses.

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
            <img src="noise-upscale-1.resources/noise1ex.png" />
        </td>
    </tr>
</table>

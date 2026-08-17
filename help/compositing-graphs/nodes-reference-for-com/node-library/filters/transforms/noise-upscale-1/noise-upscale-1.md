---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Noise Upscale 1 -Knoten, um Texturen mithilfe von rauschbasierten Algorithmen hochzuskalieren, um beim Erhöhen der Texturauflösung Details zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rauschen Hochskalieren 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Rauschen Hochskalieren 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Rauschen Hochskalieren 1

**In:** *Filter/Transformationen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Verwendet ein prozedurales Eingangsrauschen und skaliert es auf eine doppelte Auflösung, wobei die Details erhalten bleiben, ohne dass jedoch zu viel Unterteilung erforderlich ist. Verwendet einen Masken-Typ &quot;X&quot; und überblendet den Text mit einem ähnlichen Kontrast wie die ursprüngliche Eingabe (der interne Mischmodus ist &quot;Kopieren&quot;).

Dieser Knoten ist hauptsächlich für die Optimierung von langsamen Graphen gedacht, die starke, große Geräusche verwenden. Sie ermöglicht es Ihnen, höhere Auflösungen zu verwenden, ohne zu viel zusätzliche Rechenzeit zu verursachen.

Weitere Varianten dieses Prozesses finden Sie unter [Rauschen-Hochskalierung 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) und [Rauschen-Hochskalierung 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md).

## Parameter

* **Offset1X**: *0.0 - 1.0* Verschiebt den oberen und unteren Teil über die X-Achse.
* **Offset1Y**: *0.0 - 1.0*\
  Verschiebt den oberen und unteren Teil über die Y-Achse.
* **Offset2X**: *0.0 - 1.0* Verschiebt den linken und rechten Teil über die X-Achse.
* **Offset2Y**: *0.0 - 1.0* Verschiebt den linken und rechten Teil über die Y-Achse.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise1ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Verwenden Sie den Noise Upscale 3-Knoten, um Texturen mithilfe erweiterter, rauschbasierter Algorithmen hochzuskalieren, um Details bei höheren Auflösungen zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rauschen Hochskalieren 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Rauschen Hochskalieren 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Rauschen Hochskalieren 3

**In:** *Filter/Transformationen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Verwendet ein prozedurales Eingangsrauschen und skaliert es auf eine doppelte Auflösung, wobei die Details erhalten bleiben, ohne dass jedoch zu viel Unterteilung erforderlich ist. Verwendet eine benutzerdefinierte Maske, um das Rauschen über der ursprünglichen Skalierung zu überblenden.

Dieser Knoten ist hauptsächlich für die Optimierung von langsamen Graphen gedacht, die starke, große Geräusche verwenden. Sie ermöglicht es Ihnen, höhere Auflösungen zu verwenden, ohne zu viel zusätzliche Rechenzeit zu verursachen.

Siehe auch [Rauschen-Hochskalierung 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) und [Rauschen-Hochskalierung 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), die in den meisten Fällen etwas besser darin sind, Untertitel auszublenden.

## Parameter

### Eingaben

* **Graustufen**: *Graustufen-Eingabe*\
  Zielrauschen-Bild.
* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

*Keine Parameter.*

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

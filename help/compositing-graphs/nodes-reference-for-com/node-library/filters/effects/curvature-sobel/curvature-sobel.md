---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Sobel-Krümmung", um Krümmungskanten mithilfe von Sobel-Operatoren zum Erstellen von kantenbasierten Masken zu erkennen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Krümmungssobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# Krümmungssobel

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## Krümmungssobel

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt eine einfache, harte Konversion der Einmalpasskrümmung zur Eingabe von [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) durch. Die resultierende Karte enthält weiße Farbtöne für konvexe Bereiche und schwarze Farbtöne für konkave Bereiche. Der Kurvenzeichner erzeugt immer dickere Linien und scharfe Übergänge.

Dieser Knoten ist nützlich, um bestimmte Kanten schnell hervorzuheben oder abzudunkeln. Sie unterscheidet sich leicht von [Krümmung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), da sie qualitativ bessere Ergebnisse liefert, aber immer noch scharf und hart ist.

## Parameter

* **Intensität**: *0.0 - 1.0* Intensität des Effekts, passt den Kontrast an.
* **Normaler Typ**: *DirectX, OpenGL*

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

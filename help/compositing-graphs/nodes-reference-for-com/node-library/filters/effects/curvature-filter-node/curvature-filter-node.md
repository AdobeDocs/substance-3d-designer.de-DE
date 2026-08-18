---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Filterknoten "Krümmung", um aus Height-Maps Krümmungszuordnungen zum Erkennen konvexer und konkaver Flächen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Krümmung (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# Krümmung (Filterknoten)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## Krümmung

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt eine einfache, harte Konversion der Einmalpasskrümmung zur Eingabe von [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) durch. Die resultierende Karte enthält weiße Farbtöne für konvexe Bereiche und schwarze Farbtöne für konkave Bereiche. Die Krümmung erzeugt immer pixeldünne Linien und scharfe Übergänge.

Dieser Knoten ist nützlich, um bestimmte Kanten schnell hervorzuheben oder abzudunkeln. Sie ist im Vergleich zu [Kurvenglättung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (mit höherwertigen Ergebnissen) und [Kurvenglättung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (mit mehr Optionen) beschränkt.

## Parameter

* **Intensität**: *0.0 - 10.0* Intensität des Effekts. Erhöht den Kontrast des Ergebnisses.
* **Normales Format**: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

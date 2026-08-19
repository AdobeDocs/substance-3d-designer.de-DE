---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill zu Box-Größe", um Bereiche mit Werten für die Größe des Begrenzungsrahmens für prozedurale Skalierungseffekte zu füllen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill in Box-Größe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Flood Fill in Box-Größe

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

## Flood Fill in Box-Größe

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Graustufenzuordnung aus einer [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)-Basis, wobei die Werte mit der individuellen Größe jeder Kachel verknüpft sind.

Die Werte sind relativ zur Gesamtgröße der Arbeitsfläche (eine vollständig weiße Kachel würde bedeuten, dass sie die gesamte Arbeitsfläche dehnt), daher ist der Kontrast oft gering.

## Parameter

* **Ausgabe**: *max(X, Y), X, Y* Legt fest, auf welcher Metrik der Wert basiert: Breite, Länge oder beides.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodbbox-ex1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

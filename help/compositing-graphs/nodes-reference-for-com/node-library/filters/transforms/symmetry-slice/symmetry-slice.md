---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Symmetrie-Slice", um Strukturen entlang von Symmetrieachsen zu segmentieren und so gespiegelte Muster und Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Symmetrie-Slice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Symmetrie-Slice

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## Symmetrie-Slice

**In:** *Filter/Transformationen*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Komplexer Symmetrie-/Spiegelungs-Betriebsknoten. Ermöglicht eine Vielzahl von geometrischen Operationen mit voller Kontrolle, erfordert jedoch einige Experimente.

Im Vergleich zu [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) und [Symmetry](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md) verfügt dieser Knoten über viele weitere Optionen.

## Parameter

* **Symmetriemodus**: *0 - 6* Wählen Sie Symmetriegeometrie/Spiegellinie aus. Folgende Optionen stehen zur Auswahl: Horizontal, Vertikal, Diagonal von links nach rechts, Diagonal von rechts nach links, Vertikal umkehren, Ecke und Diagonale Ecke.
* **Übertragungsmodus**: *0 - 6\
  Füllmethode. Folgende Optionen stehen zur Verfügung:*
* **Überblendung**: *0.0 - 1.0* Fügt das Originalbild wieder in das Ergebnis ein.
* **Seite spiegeln**: *Falsch/Wahr* Dreht den Ursprung um, was bedeutet, dass die ursprüngliche Seite des Vorgangs umgekehrt wird. Die Symmetrie von links nach rechts wird beispielsweise von rechts nach links.
* **Seite spiegeln2**: *Falsch/Wahr* Wird nur verwendet, wenn der Symmetriemodus 5 oder 6 ist. Ursprung der gedrehten Ecke.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

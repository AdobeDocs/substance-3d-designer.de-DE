---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D Worley Rauschen-Knoten, um Worley Rauschen auf der Grundlage der 3D-Position zu generieren, um volumetrische Textur-Effekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Worley Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 3D Worley Rauschen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## 3D Worley Rauschen

**In:** *Texturgeneratoren**/Noises*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Es ist eine der vielseitigsten und fortschrittlichsten Rauschen in der Library und generiert eine Worley Rauschen im 3D-Raum, basierend auf einer Eingangspositionskarte. Verfügt über eine Vielzahl von Optionen, die es viel leistungsfähiger machen als die standardmäßigen [Zellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) oder [Entfernungen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)-basierten Rauschen.

## Parameter

* **Skalierung**: *1 - 64*\
  Legen Sie die globale Skalierung für den Effekt fest.
* **Größe**: *0.0 - 1.0* Führen Sie eine ungleichmäßige Skalierung auf X-, Y- und Z-Achsen separat durch.
* **Modus**: *Euklidean, Manhattan, Chebyshev, Minkowski\
  Ändern Sie die Abstandsmetrik. Lässt einige sehr unterschiedliche Rauschen-Typen zu.*
* **Minkowski-Zahl**: *0.0 - 20.0* Nur mit Minkowski-Entfernungsmetrik. Überblendungen zwischen verschiedenen Kennzahlen.
* **Stil**: *F1, F2, F2-F1, Border, Random Color* Legen Sie die metrische Kombinationsmathematik fest. Ermöglicht viele weitere Kombinationen.
* **Rahmenbreite**: *0.0 - 1.0* Wenn die Rahmenkombinationsmathematik aktiv ist, steuert sie die Breite des Rahmens.
* **Rundheit**: *0.0 - 1.0* Nur verfügbar mit den Modi F1, F2 und F2-F1. Legt die mittlere Position des Levels fest.
* **Umkehren**: *False/True*\
  Kehrt das Ergebnis um.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>

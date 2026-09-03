---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Verwenden Sie Vektor- und SWZZLE-Graf in Substance 3D Designer-Funktionsknoten zum Bearbeiten von Vektordaten und -komponenten.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vektor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Vektor- und Swizzle-Knoten

Mit Vektor- und Schwenkknoten können Sie Vektor-Knoten aus bzw. in separate Komponenten konstruieren bzw. dekonstruieren.Sie ähneln der [RGBA-Zusammenführung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) und der [RGBA-Teilung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), werden dann jedoch für Funktions-Graf verwendet. Sie sind auch eine primäre Methode für die Konvertierung zwischen Vektordatentypen, da [Wirf](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) in vielen Fällen keine Option ist.

## Vektorknoten

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Mit Vektorknoten können Sie Vektoren oder Elemente mit weniger Komponenten zu Vektoren mit mehr Komponenten kombinieren. Für Vektorknoten gibt es einige spezifische Regeln oder Einschränkungen:

* Vektorknoten haben **nur zwei Eingänge**, selbst wenn der resultierende Vektor mehr als 2 Komponenten enthält.
* Vektoreingaben sind **nicht auf einen Typ beschränkt**: können sie eine beliebige geringere Komponente als Eingabe verwenden.
* Die Reihenfolge der Ergebnisausgabe wird durch die **Reihenfolge der Eingaben** bestimmt.

Das bedeutet, dass die folgenden Methoden am besten angewendet werden:

* Konstruiert einen Vektor 4 auf zwei Arten: entweder zwei 2-Komponenten-Vektoren verbinden oder einen 1-Komponenten- und einen 3-Komponenten-Vektor verbinden.
* Wenn Sie einen 3- oder 4-Komponenten-Vektor aus einer einzigen Ganzzahl oder Fließkommazahl konstruieren möchten, müssen Sie zunächst mindestens eine Vektor 2-Kombination ausführen, bevor Sie sie zu einem 3-Komponenten-Vektor kombinieren können.

Denke gut über die Reihenfolge der Verbindungen nach. Die Anschlussreihenfolge der Eingänge ist unten dargestellt.

![](vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-01.png){width="200px"}

Beispiel auf links: Verbindet zuerst eine Ganzzahl(1) und dann eine Ganzzahl(3). Ergebnis ist wie folgt

| Ausgabe | X | Y | Z | B |
| --- | --- | --- | --- | --- |
| Eingabe 1 | 0 |  |  |  |
| Eingabe 2 |  | 1 | 2 | 4 |

![](vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-02.png){width="200px"}

Beispiel für Left Swap Eingaben um das erste Beispiel, erste Ganzzahl 3, dann eine Ganzzahl(1).

| Ausgabe | X | Y | Z | B |
| --- | --- | --- | --- | --- |
| Eingabe 1 | 1 | 2 | 4 |  |
| Eingabe 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-03.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-04.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-05.png"/></div> |
| --- | --- | --- |
| **Vector Ganzzahl2** | **Vector Ganzzahl3** | **Vector Ganzzahl4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-06.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-07.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-08.png"/></div> |
| **Vektor-Gleitkommazahl2** | **Vektor-Gleitkommazahl3** | **Vektor-Gleitkommazahl4** |

</td>
</tr>
</table>

## Wechselknoten

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Swizzle Nodes dekonstruieren oder teilen Komponenten von Mehrkomponenten-Vektoren ab, sodass Sie X-, Y-, Z- und W-Komponenten einzeln verwenden und austauschen können. Es gelten die folgenden Regeln und Einschränkungen:

* Wechselknoten haben **nur eine Ausgabe**.
* Wechselknoten **nehmen jede Eingabe** des richtigen Typs (Int oder Fließkommazahl).

### Komponenten teilen

Der häufigste Anwendungsfall für Swizzle ist die Teilung von Komponenten, wie das Abbremsen einer Ganzzahl4 in 4 Ganzzahlen. Die Einschränkungen bedeuten, dass Sie hierfür vier separate Swizzle-Ganzzahl-Nodes benötigen.

Jede andere Art der Aufteilung ist auch für eine Ganzzahl4 möglich, wie z.B. zwei Ganzzahl2, oder eine Ganzzahl und eine Ganzzahl3, wobei jedes Ergebnis einen eigenen Node benötigt.

### Swap-/Swizzle-Komponenten

Wie der Name schon andeutet, kann Swizzle verwendet werden, um die Reihenfolge der Werte zu ändern oder sogar Werte zu überschreiben. Sie können die Reihenfolge von X,Y,Z,W in W,Y,X,Z ändern und die Werte von X,Y,Z,W in X,X,X,W ändern.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-09.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-10.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-11.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-12.png"/></div> |
| --- | --- | --- | --- |
| **Swizzle-Ganzzahl** | **Swizzle** **Ganzzahl2** | **Swizzle** **Ganzzahl3** | **Swizzle** **Ganzzahl4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-13.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-14.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-15.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-16.png"/></div> |
| **Swizzle** **Fließkommazahl** | **Swizzle** **Fließkommazahl2** | **Swizzle** **Fließkommazahl3** | **Swizzle** **Fließkommazahl4** |

</td>
</tr>
</table>

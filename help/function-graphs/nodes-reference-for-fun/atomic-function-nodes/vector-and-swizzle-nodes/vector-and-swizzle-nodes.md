---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Verwenden Sie Vektor- und SWZZLE-Knoten in Substance 3D Designer-Funktionsdiagrammen, um Vektordaten und -komponenten zu bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vektor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Vektor- und Swizzle-Knoten

Mit Vektor- und Schwenkknoten können Sie Vektor-Knoten aus bzw. in separate Komponenten konstruieren bzw. dekonstruieren.Sie ähneln der [RGBA-Zusammenführung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) und der [RGBA-Teilung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), gelten dann jedoch für Funktionsdiagramme. Sie sind auch eine erstklassige Methode für die Konvertierung zwischen Vektordatentypen, da [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) in vielen Fällen keine Option ist.

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
* Wenn Sie einen 3- oder 4-Komponenten-Vektor aus einzelnen Ganzzahlen oder einem Gleitkomma erstellen möchten, müssen Sie zunächst mindestens eine Vektor 2-Kombination ausführen, bevor Sie diese zu einem 3-Komponenten-Vektor kombinieren können.

Denke gut über die Reihenfolge der Verbindungen nach. Die Anschlussreihenfolge der Eingänge ist unten dargestellt.

![](../../../../assets/vector-int1.png){width="200px"}

Beispiel auf Left Verbindet zuerst eine Integer(1) und dann eine Integer(3). Ergebnis ist wie folgt

| Ausgabe | X | Y | Z | B |
| --- | --- | --- | --- | --- |
| Eingabe 1 | 0 |  |  |  |
| Eingabe 2 |  | 1 | 2 | 4 |

![](../../../../assets/vector-int2.png){width="200px"}

Beispiel für Left Swap-Eingaben vom ersten Beispiel, zuerst Integer 3, dann Integer(1).

| Ausgabe | X | Y | Z | B |
| --- | --- | --- | --- | --- |
| Eingabe 1 | 1 | 2 | 4 |  |
| Eingabe 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **Vector Integer2** | **Vector Integer3** | **Vector Integer4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-vectofloat4.png"/></div> |
| **Vector Float2** | **Vektor-Float3** | **Vektor-Float4** |

</td>
</tr>
</table>

## Wechselknoten

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Swizzle Nodes dekonstruieren oder teilen Komponenten von Mehrkomponenten-Vektoren ab, sodass Sie X-, Y-, Z- und W-Komponenten einzeln verwenden und austauschen können. Es gelten die folgenden Regeln und Einschränkungen:

* Wechselknoten haben **nur eine Ausgabe**.
* Wechselknoten **nehmen jede Eingabe** des richtigen Typs (Int oder Float).

### Komponenten teilen

Der gängigste Anwendungsfall für Swizzle ist die Aufteilung von Komponenten, z. B. das Abbremsen eines Integer4 in 4 einzelne Integer. Die Einschränkungen bedeuten, dass Sie dafür vier separate Swizzle Integer-Knoten benötigen.

Jede andere Art der Teilung ist auch für eine Integer4 möglich, z. B. zwei Integer2, oder eine Integer und eine Integer3, wobei jedes Ergebnis einen eigenen Knoten benötigt.

### Swap-/Swizzle-Komponenten

Wie der Name schon andeutet, kann Swizzle verwendet werden, um die Reihenfolge der Werte zu ändern oder sogar Werte zu überschreiben. Sie können die Reihenfolge von X,Y,Z,W in W,Y,X,Z ändern und die Werte von X,Y,Z,W in X,X,X,W ändern.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../assets/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **Swizzle Integer** | **Swizzle** **Integer2** | **Swizzle** **Integer3** | **Swizzle** **Integer4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="../../../../assets/fn-vector-swizzlefloat4.png"/></div> |
| **Swizzle** **Float** | **Swizzle** **Float2** | **Swizzle** **Float3** | **Swizzle** **Float4** |

</td>
</tr>
</table>

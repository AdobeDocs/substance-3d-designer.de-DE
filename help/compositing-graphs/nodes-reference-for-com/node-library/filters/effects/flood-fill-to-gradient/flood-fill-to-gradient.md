---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill zu Verlauf", um Bereiche mit Verlaufswerten zu füllen, um glatte Farbübergänge zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill zu Verlauf
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Flood Fill zu Verlauf

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## Flood Fill zu Verlauf

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Transformiert eine [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)-Base in (zufällig orientierte) Farbverläufe. Sehr nützlich zum Erstellen einer Höhenkarte, bei der Kacheln zufällig geneigt und geneigt sind.

## Parameter

### Eingaben

* **Flood Fill**: *Farbeingabe* Daten des Basis-Flood Fills.
* **Winkeleingabe**: *Graustufen-Eingabe*\
  Optionale Karte zur Bestimmung des Winkels pro Zelle mit einer externen Karte.
* **Steigung-Eingabe**: *Graustufeneingabe* Optionale Zuordnung zum Bestimmen der Steigung des Verlaufs pro Zelle.

### *Parameter*

* **Winkel**: *0.0 - 1.0* Legt für alle Kacheln einen einheitlichen globalen Winkel/eine einheitliche globale Richtung fest.
* **Winkelabweichung**: *0.0 - 1.0* Verteilt den Winkel für jede Kachel einzeln mit Zufallswerten. Dies ist der nützlichste und mächtigste Parameter!
* **Multiplizieren mit der Größe des Begrenzungsrahmens**: *0.0 - 1.0* Skaliert den gesamten linearen Effekt anhand der Größe des individuellen Begrenzungsrahmens der Kachel. Das bedeutet, dass kleinere Kacheln am Ende dunkler sind als größere.
* **Winkel-Bildeingabemultiplikator**: *0.0 - 1.0* Festlegen des Einflusses der optionalen Winkeleingabe-Map auf die generierten Verlaufsrichtungen
* **Steigung-Bildeingabemultiplikator**: *0.0 - 1.0*\
  Legen Sie den Einfluss der optionalen Steigung-Eingabemap auf die generierte Steigung des Verlaufs fest.
* **Multiplizieren mit der Intensität der Steigung**: *0.0 - 1.0*
* **Einfache Steigung**: *(Graustufenwert)*Ermöglicht die Einstellung des Farbflächenwerts für flache Steigungen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>

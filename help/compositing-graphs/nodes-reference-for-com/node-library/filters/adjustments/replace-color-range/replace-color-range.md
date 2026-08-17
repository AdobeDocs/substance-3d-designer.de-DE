---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Farbbereich ersetzen", um Farben innerhalb eines bestimmten Bereichs zur Farbkorrektur durch neue Farben zu ersetzen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbbereich ersetzen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# Farbbereich ersetzen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## Farbbereich ersetzen

**In:** *Filter/Korrekturen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ersetzt die Quellfarbe durch die Zielfarbe mit zusätzlichen Steuerelementen. Kann beispielsweise verwendet werden, um Teile einer Material ID-Karte neu zu färben (backen).

Eine erweiterte Version finden Sie unter [Farbabgleich.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## Parameter

* **Quellfarbe**: *(Farbwert)*Farbe, die ersetzt werden soll.
* **Zielfarbe**: *(Farbwert)*Farbe, durch die ersetzt werden soll.
* **Quellbereich**: *0.0 -* 1.0\
  Bereich oder Toleranz der ausgewählten Quelle. Kann erhöht werden, damit auch weitere benachbarte Farben farblich verschoben werden.
* **Schwellenwert**: *0.0 - 1.0* Abfall/Kontrast für den Bereich. Wählen Sie &quot;Niedrig&quot;, um nur die Quellfarbe zu ersetzen, und &quot;Hoch&quot;, um auch die Farben zu ersetzen, die in die Quelle übergehen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

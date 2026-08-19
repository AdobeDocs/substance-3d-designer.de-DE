---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialauswahl , um Materialien basierend auf Gitterdaten auszuwählen, um Textureffekte aus mehreren Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialauswahl
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Materialauswahl

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## Materialauswahl

**In:** *Mesh-basierte Generatoren**/Dienstprogramme*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Konvertiert eine Vollfarben-ID-Map in eine binäre Schwarzweiß-Maske. Ermöglicht das Mischen und Kombinieren verschiedener Farben zu einer Maske.

Dies ist praktisch, wenn Sie [Multi-Material Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) nicht verwenden möchten und die Maske lieber manuell verwenden möchten, oder alternativ, wenn Sie dieselben Masken manuell an anderen Speicherorten verwenden möchten.

## Parameter

* **Materialien**: 1-16\
  Legt die Anzahl der Materialien fest, für die das Kombinieren aktiviert ist.
* **#1-16 aktivieren**: False/True\
  Schaltet das Mischen und Kombinieren von Farben in die endgültige Ausgabemaske um. Kann für so viele Farben aktiviert werden, wie Sie kombinieren möchten.
* **#1-16**: (Farbwert)\
  Farbwähler für die Materialfarbe, die in Schwarz-Weiß konvertiert wird.
* **Farbwählerparameter**\
  Ändert die Füllmethode und die Konvertierung der Farbe in Schwarzweiß.
  * **Unschärfe**: 0,01 - 1,0\
    Wie viel Farben Sie mit den Nachbarfarben mischen können.
  * **Auffüllen**: 0,0 - 1,0\
    Die Schärfe des Übergangs ist wie &quot;Kontrast&quot;.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

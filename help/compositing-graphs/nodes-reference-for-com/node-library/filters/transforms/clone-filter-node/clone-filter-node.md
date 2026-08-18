---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Filterknoten "Klonen", um Texturbereiche zu duplizieren und zu versetzen, um nahtlose Muster und Kacheleffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Klonen (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Klonen (Filterknoten)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## Klonen

**In:** *Filter/Transformationen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Klont das Eingabebild einmal an eine bestimmte Position. Kann als primitives Werkzeug zum &quot;Klonstempel&quot; fungieren.

Sorgfältig, um die gewünschten Ergebnisse zu erzielen:

* Idealerweise hat das Eingabebild einen Alphakanal (wie ein Aufkleber), da das Mischen nur eine gerade Kopie ist.
* Die Maske ist standardmäßig schwarz, sodass für alle Ergebnisse ein einheitlicher Graustufenwert für Weiß mindestens angeschlossen werden muss.
* Der Offset wird außerhalb des Bildes abgeschnitten, verwende also kleine Werte.

## Parameter

### Eingaben

* **Quelle**: *Farbeingabe*\
  Zu klonendes Bild. Wichtig: Idealerweise hat das Bild einen Alphakanal!
* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Standardmäßig ist es schwarz.

### Parameter

* **Offset**: *-*\
  Verschiebt oder verschiebt das Ergebnis. &quot;Positiv&quot; steht für &quot;Links und oben&quot;, &quot;Negativ&quot; für &quot;Rechts und unten&quot;. Verwenden Sie kleine Werte, 1,0 und höher, um sie aus dem Bild zu verschieben!
* **Weichzeichnungsmaske**: *0.0 - 10.0\
  Wenden Sie einen Weichzeichnungsfilter auf eine Maske an, um Kanten weichzuzeichnen.*

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

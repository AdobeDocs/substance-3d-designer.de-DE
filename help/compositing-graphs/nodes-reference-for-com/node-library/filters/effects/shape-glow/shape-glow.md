---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Formenglühen", um Formen und Texturen Leuchteffekte hinzuzufügen, um helle und atmosphärische visuelle Effekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glühen in Formen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Glühen in Formen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## Formglühen (Graustufen)

**In:** *Filter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erstellt einen weichen Leuchteffekt um eine Eingabemaske (für die Graustufenversion) oder eine Form mit einem Alphakanal (für die Farbversion). Im Vergleich zu [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md) funktioniert dies in einer Weise, die der anderer 2D-Bildbearbeitungssoftware ähnlicher ist, da es ein umfassenderer Effekt mit mehr Steuerelementen ist.

## Parameter

* **Modus**: *Weich, präzise* Wechselt zwischen zwei Genauigkeitsmodi.
* **Breite**: *-1.0 - 1.0* Steuert, wie weit der Schein reicht.
* **Druckbogen**: *0.0 - 1.0* Schwellenwertabgrenzung für den Weichzeichnungseffekt lässt das Leuchten dicht an der Form fest erscheinen.
* **Deckkraft**: *0.0 - 1.0*\
  Fülldeckkraft für den Effekt &quot;Glühen&quot;.
* **(Shadow) Color**: *(Farbwert)*Farbton, der auf den Schein angewendet werden soll.
* **Maskenfarbe**: *(Farbwert) *(Nur Graustufenversion)**Volltonfarbe, die für die Ausgabe mit Transparenzzuordnung verwendet wird.
* **Eingabe ist vormultipliziert**: *Falsch/Wahr *(Nur Farbversion)**Gibt an, ob die Eingabe als vormultipliziert angenommen werden soll.
* **Ausgabe vormultiplizieren**: *Falsch/Wahr* Ob die Ausgabe vormultipliziert werden soll.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

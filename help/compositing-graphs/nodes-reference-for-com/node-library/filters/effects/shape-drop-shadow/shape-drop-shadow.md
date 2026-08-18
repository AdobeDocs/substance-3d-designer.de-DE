---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Shape-Schlagschatten", um den Formen Schlagschatteneffekte hinzuzufügen, um die Tiefe und Dimension von Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape-Schlagschatten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Shape-Schlagschatten

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## Form-Schlagschatten (Graustufen)

**In:** *Filter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt den bekannten Effekt &quot;Schlagschatten&quot; anderer 2D-Bildverarbeitungssoftware auf einer Schwarzweißmaske (für die Graustufenversion) oder einem Bild mit Transparenz (für die Farbversion) durch.

Er unterscheidet sich vom [Shadows](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md)-Effekt dadurch, dass er Bilder mit voller Transparenz zurückgibt, sodass ein vollständigerer Effekt erzielt wird, der dem ähnelt, was Sie in anderer Software erwarten würden.

## Parameter

* **Winkel**: *0.0 - 1.0* Einfallswinkel des (gefälschten) Lichts.
* **Entfernung**: *-0.5 - 0.5* Entfernt den Schatten-Dropdown von der Form nach unten bzw. entfernt ihn von der Form.
* **Größe**: *0.0 - 1.0* Steuert die Weichzeichnung/Unschärfen des Schattens.
* **Druckbogen**: *0.0 - 1.0* Schwellenwertabgrenzung für den Weichzeichnungseffekt sorgt dafür, dass sich der Schatten weiter entfernt.
* **Deckkraft**: *0.0 - 1.0*\
  Fülldeckkraft für den Schatteneffekt.
* **(Shadow) Color**: *(Farbwert)*Der auf den Schatten anzuwendende Farbton.
* **Maskenfarbe**: *(Farbwert) *(Nur Graustufenversion)**Volltonfarbe, die für die Ausgabe mit Transparenzzuordnung verwendet wird.
* **Eingabe ist vormultipliziert**: *Falsch/Wahr *(Nur Farbversion)**Gibt an, ob die Eingabe als vormultipliziert angenommen werden soll.
* **Ausgabe vormultiplizieren**: *Falsch/Wahr* Ob die Ausgabe vormultipliziert werden soll.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

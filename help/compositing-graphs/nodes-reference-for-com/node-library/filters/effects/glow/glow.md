---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Glühen", um Texturen Leuchteffekte hinzuzufügen, um helle und emittierende Materialerscheinungen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glühen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Glühen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## Glühen

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt einen Effekt vom Typ &quot;Schein nach außen&quot; aus, wie man ihn in anderen gängigen Bildbearbeitungsprogrammen sieht. Fügt im Wesentlichen eine verblassende Verlaufskontur um die Eingabe hinzu.

Beachten Sie, dass dies nicht für Bilder mit Alpha-Kanälen geeignet ist, wie Sie vielleicht erwarten. Selbst die Farbversion erwartet nur binäre, schwarz-weiße Masken als Eingabe. es erlaubt nur einen farbigen Schein zu verwenden. Wenn Sie nach einer Version suchen, die für Bilder mit Transparenz funktioniert, finden Sie weitere Informationen unter [Formenglühen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Glühen&quot; für Farbeingaben bzw. &quot;Graustufen glühen&quot; für Graustufeneingaben.

## Parameter

* **Glühstärke**: *0.0 - 1.0* Globale Deckkraft für den Leuchteffekt.
* **Betrag löschen**: *0.0 - 1.0* Schwellenwert, um festzulegen, wann der Glüheffekt abgeschnitten werden soll. Nützlich für halbtransparente Bereiche.
* **Leuchtgröße**: *0.0 - 20.0* Steuert, wie weit der Leuchteffekt reicht.
* **Leuchtfarbe**: *(Farbwert) (Nur Farbversion)*Legt die Farbe des Effekts &quot;Leuchten&quot; fest.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

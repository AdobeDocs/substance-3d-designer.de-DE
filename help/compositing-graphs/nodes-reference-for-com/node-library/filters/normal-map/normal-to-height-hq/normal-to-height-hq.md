---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Normal zu Height HQ", um Normalmaps in hochwertige Height-Maps für die Oberflächendetailextraktion umzuwandeln.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal bis Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Normal bis Height HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## Normal bis Height HQ

**In:** *Filters/Normal Map*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein Umkehrkonvertierungsknoten, der versucht, eine Normalmap des Tangentenraums zurück in eine Höhenkarte zu konvertieren. Dies ist der fortgeschrittenere Knoten. [Normal zu Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) hat weniger Optionen und verwendet unterschiedliche Berechnungen.

Dies ist nützlich, wenn Sie nur eine Normalmap-Quelle haben, diese aber dennoch mit einer Heightmap kombinieren möchten. Beachten Sie, dass dies niemals zu 100 % zu einem korrekten Ergebnis führen kann, da Informationen aufgrund der Natur des Prozesses verloren gehen, wenn das Height in &quot;Normal&quot; konvertiert wird. Es kann niemals eine korrekt generierte Höhenkarte ersetzen!

## Parameter

* **Normales Format**: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
* **Relief-Saldo**: *0.0 - 1.0*&#x200B;Überblendungen zwischen Nieder- und Hochfrequenzvorspannung.
* **Height-Intensität**: *0.0 - 1.0* Die Intensität oder der Multiplikator für die Höhenkarte funktioniert ein bisschen wie die globale Deckkraft.
* **Height normalisieren**: *Falsch/Wahr* Skaliert den Höhenkartenbereich automatisch so, dass er den vollen Kontrast verwendet, wie eine [Auto-Stufe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md).
* **Qualität**: *Normal, Hoch* Wechselt zwischen Geschwindigkeit oder Qualität.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

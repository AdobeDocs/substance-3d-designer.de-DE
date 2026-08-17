---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal in Height, um Normalmaps in Height-Maps zu konvertieren, um Informationen zur Tiefe der Flächen zu extrahieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal zu Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Normal zu Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Normal zu Height

**In:** *Filters/Normal Map*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein Umkehrkonvertierungsknoten, der versucht, eine Normalmap des Tangentenraums zurück in eine Höhenkarte zu konvertieren. Dies ist die etwas einfachere Version. [Das HQ von Normal bis Height ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) verfügt über mehr Optionen.

Dies ist nützlich, wenn Sie nur eine Normalmap-Quelle haben, diese aber dennoch mit einer Heightmap kombinieren möchten. Beachten Sie, dass dies niemals zu 100 % zu einem korrekten Ergebnis führen kann, da Informationen aufgrund der Natur des Prozesses verloren gehen, wenn das Height in &quot;Normal&quot; konvertiert wird. Wenn Sie die Einstellungen entsprechend einstellen, leistet diese Nicht-HQ-Version eine anständige Arbeit bei der Konvertierung einfacher Details.

## Parameter

* **Relief-Saldo**: *0.0 - 1.0* Passen Sie an, in welchem Maße die verschiedenen Frequenzen das Endergebnis beeinflussen. Dies hängt weitgehend von der Eingabemap ab und erfordert ein gutes Stück Feinabstimmung.
* **Normales Format**: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
* **Globale Deckkraft**: *0.0 - 1.0* Passt die globale Deckkraft des Effekts an.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

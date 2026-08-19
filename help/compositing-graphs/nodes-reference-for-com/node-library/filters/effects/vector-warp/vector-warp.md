---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Vektorverkrümmung", um Texturen mithilfe von Vektorfeldern zu verkrümmen und so flüssige und organische Verzerrungen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verkrümmen
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Verkrümmen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-warp.png){width="128px"}

![](../../../../../../assets/vector-warp-grayscale.png){width="128px"}

## Verkrümmen (Graustufen)

**In:** *Filter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Die Vektorverkrümmung ist ein Effekt mit erweiterten Verzerrungen, ähnlich wie [Verkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) und [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), mit dem Hauptunterschied, dass sie von einer (Farb-)Vektorbitmap und nicht von einer Graustufenmap gesteuert wird. Das bedeutet, dass es leistungsfähiger und vielseitiger ist als seine atomaren Knotencousins.

Die Vektorkarte ähnelt einer Normalmap, muss jedoch nicht normalisiert werden und es werden nur die Kanäle R und Grün (X und Y) verwendet. Blau- und Alpha-Kanäle können schwarz bleiben, wenn du willst. Das Erstellen einer guten Vektorkarte kann die größte Herausforderung bei der Verwendung dieses Knotens sein; Sie können entweder [Graustufenzuordnungen in Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) konvertieren oder die Karte durch Kombinieren von Kanälen mit [RGBA-Zusammenfügung erstellen.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) Alternativ ist auch so etwas wie eine [&quot;Flow Map&quot;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting) verwendbar.

Dieser Knoten kann nützlich sein, wenn Sie sehr spezifische Verzerrungen mit unterschiedlichen Richtungen durchführen möchten, bei denen Standardverkrümmungsknoten ihn nicht schneiden.

## Parameter

### Eingaben

* **Eingabe**: *Farbeingabe*\
  Verzerren.
* **Vektorzuordnung**: *Farbeingabe*\
  Verzerrung-Treiberzuordnung. Die Farbkanäle Rot und Blau werden verwendet.

### Parameter

* **Intensität**: *0.0 - 1.0* Intensitätsmultiplikator für die Vektorkarte.
* **Vektorformat**: *DirectX, OpenGL* Tauscht den grünen Kanal zwischen der Nach-oben- und Nach-unten-Interpretation aus.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/vector-warp-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

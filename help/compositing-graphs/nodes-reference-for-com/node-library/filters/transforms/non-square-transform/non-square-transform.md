---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Nicht-quadratische Transformation", um nicht-quadratische Texturen mit unabhängiger X- und Y-Skalierung zu transformieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformieren ohne Quadrat
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Transformieren ohne Quadrat

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformieren ohne Quadrat (Graustufen)

**In:** *Filter/Transformationen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Nicht quadratsichere Version von [2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) transformieren. Erkennt automatisch nicht quadratische Seitenverhältnisse und kann quadratische Eingabebilder auf eine nicht quadratische Arbeitsfläche transformieren.

Vergewissern Sie sich, dass Sie die [Graph-Parameter](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) vollständig verstehen, um diesen Knoten optimal zu nutzen, da Sie einige Einstellungen richtig festlegen müssen:

* Ihre **Graph**-Größe sollte nicht quadratisch sein, andernfalls ist dieser Knoten nicht erforderlich.
* Legen Sie die **-Ausgabegröße des Knotens &quot;**&quot; als &quot;Nicht quadratisch transformieren&quot; auf &quot;*Relativ zu übergeordneten Knoten*&quot; fest.
* Setzen Sie den **Kachelmodus des Knotens** auf &quot;*Keine Kachelung*&quot;, wenn Sie Ihre Eingabe nur in eine einzelne Position umwandeln möchten.

## Parameter

* **Kachelmodus**: *Automatisch, Manuell* Aktivieren Sie automatische nichtquadratische Kompensationen, oder nicht.
* **Kachel**: *1 - 16* Nur verfügbar, wenn der Kachelmodus auf &quot;Manuell&quot; eingestellt ist. Ermöglicht das Ändern der Skalierung kachelsicher.
* **Offset**: *0.0 - 1.0*\
  Verschiebt oder verschiebt das Ergebnis. Doppelklicken Sie auf den Regler, um negative Werte einzugeben.
* **Drehung**: *0.0 - 1.0* Dreht das Eingabebild.
* **Sichere Drehung (nur Quadrat)**: *Falsch/Wahr* Ausrichtung an sicheren Werten, um die Schärfe der Pixel beizubehalten.
* **Hintergrundfarbe**: *(Farbwert)*Hintergrundfarbe zum Füllen des Bildes. Nur sichtbar, wenn der [Kachelmodus in Basisparametern auf &quot;*Keine Kachelung*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) festgelegt ist.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

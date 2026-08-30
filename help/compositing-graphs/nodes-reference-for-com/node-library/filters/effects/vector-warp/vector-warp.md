---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# Verkrümmen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp.png){width="128px"}

![](vector-warp.resources/vector-warp-grayscale.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Die Vektorverkrümmung ist ein Effekt mit erweiterten Verzerrungen, ähnlich wie [Verkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) und [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), mit dem Hauptunterschied, dass sie von einer (Farb-)Vektorbitmap und nicht von einer Graustufenmap gesteuert wird. Das bedeutet, dass es leistungsfähiger und vielseitiger ist als seine atomaren Knotencousins.

Die Vektorkarte ähnelt einer Normalmap, muss jedoch nicht normalisiert werden und es werden nur die Kanäle R und Grün (X und Y) verwendet. Blau- und Alpha-Kanäle können schwarz bleiben, wenn du willst. Das Erstellen einer guten Vektorkarte kann die größte Herausforderung bei der Verwendung dieses Knotens sein; Sie können entweder [Graustufenzuordnungen in Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) konvertieren oder die Karte durch Kombinieren von Kanälen mit [RGBA-Zusammenfügung erstellen.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) Alternativ ist auch so etwas wie eine [&quot;Flow Map&quot;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting) verwendbar.

Dieser Knoten kann nützlich sein, wenn Sie sehr spezifische Verzerrungen mit unterschiedlichen Richtungen durchführen möchten, bei denen Standardverkrümmungsknoten ihn nicht schneiden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbeingabe</i> | Verzerren. |
| <b>Vektorzuordnung</b> <i>Farbeingabe</i> | Verzerrung-Treiberzuordnung. Die Farbkanäle Rot und Blau werden verwendet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 1.0</i> | Intensitätsmultiplikator für die Vektorgrafik. |
| <b>Vektorformat</b> <i>DirectX, OpenGL</i> | Tauscht den grünen Kanal zwischen Nach-oben- und Nach-unten-Interpretation aus. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-ex.png" />
        </td>
    </tr>
</table>

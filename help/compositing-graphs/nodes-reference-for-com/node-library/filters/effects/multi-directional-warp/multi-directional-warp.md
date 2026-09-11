---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multidirektionale Verkrümmung", um Verkrümmungseffekte in mehrere Verzerrungen anzuwenden und so komplexe Richtungsmuster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Multidirektionale Verkrümmung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# Multidirektionale Verkrümmung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-color.png)![](multi-directional-warp.resources/multi-directional-warp-grayscalepng.png)

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Multidirektionale Verkrümmung wendet [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) mehrmals in entgegengesetzte Richtungen an, während die verschobene Textur an Ort und Stelle bleibt. Er unterscheidet sich von der Standard-Richtungsverkrümmung dadurch, dass er in mehrere Richtungen drücken kann, während die Atomversion nur eine zulässt. Auf diese Weise löst es das klassische Problem, bei dem die Richtungsverkrümmung Ihr Bild immer zu sehr in eine Richtung wegdrückt. Stattdessen arbeitet es entlang mehrerer Richtungen oder Achsen statt einer einzelnen Richtung.

Er unterscheidet sich hauptsächlich von [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) dadurch, dass er etwas eingeschränkter ist: Die Richtung für die Verkrümmung wird nur über Parameter gesteuert und kann nicht über eine Eingabemap festgelegt werden. Der Vorteil ist, dass er etwas einfacher zu bedienen ist und je nach Anwendungsfall präziser sein kann.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen-/Farbeingabe</i> | Basiskarte, auf die die Verkrümmung angewendet wird. Kann Farbe oder Graustufen sein. |
| <b>Intensitätseingabe</b> <i>Graustufen-Eingabe</i> | Die obligatorische Maskenzuordnung, die die Intensität des Verkrümmungseffekts steuert, muss in Graustufen erfolgen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 20.0</i> | Legt die Intensität des Verkrümmungseffekts fest, d. h. wie weit Pixel entfernt werden sollen. |
| <b>Verkrümmungswinkel</b> <i>0.0 - 1.0</i> | Legt den Winkel oder die Richtung fest, in der der Effekt &quot;Verformen&quot; angewendet werden soll. |
| <b>Modus</b> <i>Durchschnitt, Max, Min, Kette</i> | Legt den Mischmodus für aufeinander folgende Durchgänge fest. Wirkt sich nur aus, wenn die Richtung 2 oder 4 ist! |
| <b>Richtungen</b> <i>1, 2, 4</i> | Legt fest, wie viele Achsen die Verkrümmung durchführt. 1 bedeutet, dass es sich in Richtung des Winkels bewegt, und das Gegenteil dieser Richtung, 2 bedeutet die Achse des Winkels plus die senkrechte Achse, 4 bedeutet die vorhergehenden Achsen plus 45 Grad Einschnitte. |

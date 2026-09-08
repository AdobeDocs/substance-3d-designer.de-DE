---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Non Uniform Directional Warp-Knoten, um eine ungleichmäßige Richtungsverkrümmung anzuwenden, um unterschiedliche Verzerrungen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 5%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Nicht-gleichförmige Richtungsverkrümmung ist eine erweiterte Version von [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), mit der Intensität und Richtung der Verkrümmung durch eine Bildeingabe gesteuert werden können. Sie bietet viel mehr Kontrolle und kann sehr nützliche und interessante Verzerrungen erstellen, genau wie [Steigung-Weichzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Sie unterscheidet sich von [Multidirektionaler Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) dadurch, dass sie die Steuerung des Winkels über eine benutzerdefinierte Map-Eingabe ermöglicht, während Multidirektionaler Warp nur die Steuerung der Richtung über Parameter zulässt. Dies bedeutet, dass Sie erweiterte abschließende und gekrümmte Effekte erstellen können, die andernfalls nicht möglich sind.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen-Eingabe</i> | Basiskarte, auf die die Verkrümmung angewendet wird. |
| <b>Intensitätseingabe</b> <i>Graustufen-Eingabe</i> | Die obligatorische Maskenzuordnung, die die Intensität des Verkrümmungseffekts steuert, muss in Graustufen erfolgen. |
| <b>Verkrümmungswinkeleingabe</b> <i>Graustufen-Eingabe</i> | Die obligatorische Maskenzuordnung, die den Winkel des Verkrümmungseffekts bestimmt, muss in Graustufen vorliegen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 20.0</i> | Legt die Intensität des Verkrümmungseffekts fest, d. h. wie weit Pixel entfernt werden sollen. |
| <b>Verkrümmungswinkel</b> <i>0.0 - 1.0</i> | Legt den Winkel oder die Richtung fest, in der der Effekt &quot;Verformen&quot; angewendet werden soll. |
| <b>Multiplikator für Verkrümmungswinkel-Eingabe</b> <i>0.0 - 1.0</i> | Legt den Effekt der Zuordnungseingabe fest. Die Karte &quot;Verkrümmungswinkel-Eingabe&quot; wird dann verwendet, um von 0 bis zum Wert dieses Parameters zu interpolieren. |
| <b>Pfadmodus</b> <i>Min., Max., Durchschnitt</i> | Legt fest, wie die Spuren überblendet werden. |
| <b>Länge des Pfades</b> <i>0.0 - 1.0</i> | Legt die Länge der Spuren fest. |
| <b>Trail Verblassen</b> <i>0.0 - 1.0</i> | Legt fest, wie stark jeder Trail ausgeblendet werden soll |
| <b>Gradationskurve</b> <i>-1.0 - 1.0</i> | Wird nur wirksam, wenn Trail Verblassen nicht 0 ist. Legt das Verhalten des Verblassen-Effekts fest. |

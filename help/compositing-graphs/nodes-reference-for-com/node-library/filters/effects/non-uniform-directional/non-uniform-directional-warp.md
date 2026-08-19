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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## Nicht einheitliches Verzeichnis. Verkrümmen (Graustufen)

**In:** *Filter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Nicht-gleichförmige Richtungsverkrümmung ist eine erweiterte Version von [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), mit der Intensität und Richtung der Verkrümmung durch eine Bildeingabe gesteuert werden können. Sie bietet viel mehr Kontrolle und kann sehr nützliche und interessante Verzerrungen erstellen, genau wie [Steigung-Weichzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Sie unterscheidet sich von [Multidirektionaler Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) dadurch, dass sie die Steuerung des Winkels über eine benutzerdefinierte Map-Eingabe ermöglicht, während Multidirektionaler Warp nur die Steuerung der Richtung über Parameter zulässt. Dies bedeutet, dass Sie erweiterte abschließende und gekrümmte Effekte erstellen können, die andernfalls nicht möglich sind.

## Parameter

### Eingaben

* **Eingabe**: *Graustufen-Eingabe*\
  Basiskarte, auf die die Verkrümmung angewendet wird.
* **Intensitätseingabe**: *Graustufen-Eingabe*\
  Die obligatorische Maskenzuordnung, die die Intensität des Verkrümmungseffekts steuert, muss in Graustufen erfolgen.
* **Verkrümmungswinkeleingabe**: *Graustufen-Eingabe*\
  Die obligatorische Maskenzuordnung, die den Winkel des Verkrümmungseffekts bestimmt, muss in Graustufen vorliegen.

### Parameter

* **Intensität**: *0.0 - 20.0*\
  Legt die Intensität des Verkrümmungseffekts fest, d. h. wie weit Pixel entfernt werden sollen.
* **Verkrümmungswinkel**: *0.0 - 1.0*\
  Legt den Winkel oder die Richtung fest, in der der Effekt &quot;Verformen&quot; angewendet werden soll.
* **Verzerrungswinkel-Eingangsmultiplikator**: *0.0 - 1.0*\
  Legt den Effekt der Zuordnungseingabe fest. Die Karte &quot;Verkrümmungswinkel-Eingabe&quot; wird dann verwendet, um von 0 bis zum Wert dieses Parameters zu interpolieren.
* **Pfadmodus**: *Min., Max., Durchschnitt*\
  Legt fest, wie die Spuren überblendet werden.
* **Länge des Pfades**: *0.0 - 1.0*\
  Legt die Länge der Spuren fest.
* **Spurübergang**: *0.0 - 1.0*\
  Legt fest, wie stark jeder Trail ausgeblendet werden soll
* **Kurve verfolgen**: *-1.0 - 1.0* Es ist nur wirksam, wenn die Spurüberblendung nicht 0 ist. Legt das Verhalten des Verblassen-Effekts fest.

## Beispielbilder

</td>
</tr>
</table>

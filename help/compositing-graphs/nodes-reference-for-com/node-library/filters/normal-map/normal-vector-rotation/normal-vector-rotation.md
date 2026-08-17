---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Normale Vektordrehung", um normale Kartenvektoren zu drehen, um die Flächenbeleuchtung und die Detailausrichtung anzupassen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Vektordrehung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Normale Vektordrehung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## Normale Vektordrehung

**In:** *Filters/Normal Map*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Normaler Dienstprogrammknoten, der alle Vektoren einer Eingabe-Normalmap im Tangent-Raum dreht. Transformiert Pixel nicht, sondern ändert die Werte, die sie darstellen. Es kann eine optionale Karte verwenden, um Graustufenfacetten zufällige Drehungen hinzuzufügen.

## Eingaben

* **Normal**: *Farbeingabe*\
  Basisplan, auf dem die Drehung ausgeführt wird. Erforderlich.
* **Rotation Map (optional)**: *Graustufen-Eingabe*\
  Graustufen-Map, die die Rotationsstärke moduliert.

## Parameter

* **Drehwinkel**: *0.0 - 1.0*\
  Legt den Winkel fest, um den die Normalmap gedreht wird.
* **Normales Format**: *DirectX, OpenGL*\
  Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal)

## Beispiele

</td>
</tr>
</table>

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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# Normale Vektordrehung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Normaler Dienstprogrammknoten, der alle Vektoren einer Eingabe-Normalmap im Tangent-Raum dreht. Transformiert Pixel nicht, sondern ändert die Werte, die sie darstellen. Es kann eine optionale Karte verwenden, um Graustufenfacetten zufällige Drehungen hinzuzufügen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normal</b> <i>Farbeingabe</i> | Basisplan, auf dem die Drehung ausgeführt wird. Erforderlich. |
| <b>Rotation Map (optional)</b> <i>Graustufen-Eingabe</i> | Graustufen-Map, die die Rotationsstärke moduliert. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Drehwinkel</b> <i>0.0 - 1.0</i> | Legt den Winkel fest, um den die Normalmap gedreht wird. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal) |

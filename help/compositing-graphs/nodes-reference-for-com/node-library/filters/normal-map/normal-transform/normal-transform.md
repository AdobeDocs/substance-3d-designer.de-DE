---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Normale Transformation", um Transformationen auf normale Maps anzuwenden und dabei die Vektorrichtungen korrekt beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Transformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Normale Transformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ähnlich wie der atomare Knoten 2D transformieren ermöglicht dies die Transformation von Normalmaps, ohne den Tangent-Raum zu unterbrechen. Stattdessen wird er im laufenden Betrieb neu berechnet, was zu immer korrekten Normalmaps führt.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>(Transformationsmatrix):</i> | Drehen oder skalieren Sie die Eingabe. |
| <b>Offset</b> <i>-0.5 - 0.5</i> | Verschiebt oder verschiebt das Ergebnis. Wenn die Transformationssteuerung vorhanden ist, kann das Ergebnis durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal) |

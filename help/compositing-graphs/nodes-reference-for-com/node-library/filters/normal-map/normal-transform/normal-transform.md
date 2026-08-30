---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Normal Transformieren", um Transformationen auf Normalen-Map anzuwenden und gleichzeitig die Vektorrichtungen korrekt beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normaler Transformieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Normaler Transformieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ähnlich wie der atomare Transformieren 2D-Knoten ermöglicht dies die Transformation von Normalmaps, ohne den Tangente-Raum zu unterbrechen. Stattdessen wird er im laufenden Betrieb neu berechnet, was zu immer richtigen Normalmaps führt.

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

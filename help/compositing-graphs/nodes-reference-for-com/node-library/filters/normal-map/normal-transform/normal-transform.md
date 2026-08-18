---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Normale Transformation

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## Normale Transformation

**In:** *Filters/Normal Map*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ähnlich wie der atomare Knoten 2D transformieren ermöglicht dies die Transformation von Normalmaps, ohne den Tangent-Raum zu unterbrechen. Stattdessen wird er im laufenden Betrieb neu berechnet, was zu immer korrekten Normalmaps führt.

## Parameter

* **Matrix2x2**: *(Transformationsmatrix):*\
  Drehen oder skalieren Sie die Eingabe.
* **Offset**: *-0.5 - 0.5*\
  Verschiebt oder verschiebt das Ergebnis. Wenn die Transformationssteuerung vorhanden ist, kann das Ergebnis durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Normales Format**: *DirectX, OpenGL*\
  Zwischen verschiedenen Normalen-Map-Format wechseln (invertiert den grünen Kanal)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal Sobel, um Normalen-Map aus Höhen-Map mithilfe der Sobel-Kantenerkennung für Oberflächendetails zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# Normal Sobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-hq.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert einen Heightmap-Eingang in eine normale Map-Ausgabe. Eine etwas komplexere Version des [normalen atomaren Knotens](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) verwendet dieser Knoten Sobel-Sampling und nicht die Standard-Sampling-Methode.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 3.0</i> | Stärke der konvertierten Normalen. |
| <b>Normales Format</b> <i>OpenGL, DirectX</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |

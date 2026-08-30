---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
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

Konvertiert einen Heightmap-Eingang in eine normale Map-Ausgabe. Eine etwas komplexere Version des [Normal-Elementaren Knotens](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), bei der anstelle der Standardauswahlmethode Sobel-Sampling verwendet wird.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 3.0</i> | Stärke der konvertierten Normalen. |
| <b>Normales Format</b> <i>OpenGL, DirectX</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |

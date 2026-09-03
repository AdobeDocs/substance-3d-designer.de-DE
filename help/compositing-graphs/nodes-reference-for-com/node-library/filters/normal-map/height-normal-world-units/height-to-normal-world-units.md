---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Height in Normal World Units, um Höhen-Map in Normalen-Map zu konvertieren, indem Sie die Skalierung von Welteinheiten verwenden, um präzise Details zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height zu normalen Welteinheiten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Height zu normalen Welteinheiten

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/height-to-normal-world-units-01.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein erweiterter Konvertierungsknoten Height-Normal, der während der Konvertierung reale Einheiten verwendet.

Dies ist nützlich, wenn Sie die Abmessungen Ihrer Quellhöhenkarte kennen und eine möglichst genaue Konvertierung durchführen möchten, z. B. beim Arbeiten mit gescannten Materialien.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Oberflächengröße (cm)</b> <i>0.0 - 1000.0</i> | Dimensionen der Eingabe-Höhenzuordnung. |
| <b>Height Tiefe (cm)</b> <i>0.0 - 100.0</i> | Maximale Tiefe der Höhenzuordnungsdetails. |
| <b>Normales Format</b> <i>OpenGL, DirectX</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Sampling</b> <i>Standard, Sobel</i> | Wechselt zwischen zwei Abtastmodi, die die Genauigkeit bestimmen. |

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "PBR Albedo Safe Color", um sicherzustellen, dass die Farbbereiche der Albedo innerhalb physikalisch plausibler Bereiche für PBR-Material liegen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR Albedo Safe Color
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# PBR Albedo Safe Color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color.png){width="128px"}

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Hilfsknoten, der Korrekturen vornimmt, wenn die Werte für Grundfarbe oder Diffuse außerhalb eines zulässigen, PBR-korrekten Bereichs liegen. Wenn der Knoten auf &quot;Metallic&quot; festgelegt ist, versucht er auch, die Grundfarbwerte auf der Grundlage der Metallic Intensität zu korrigieren.

Sehen Sie sich auch [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) an, um visuelles Feedback dazu zu erhalten, welche Bereiche möglicherweise falsch sind.

Dies ist nützlich für schnelle Korrekturen, insbesondere wenn man noch PBR lernt, aber nicht als absolutes Maß gedacht ist, das immer korrekt sein soll.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>PBR-Workflow</b> <i>Grundfarbe - Metallic, Diffuse - Specular</i> | Wechselt zwischen zwei verschiedenen PBR-Workflows. |
| <b>Toleranz</b> <i>0.0 - 1.0</i> | Toleranzbetrag für Werte außerhalb des zulässigen Bereichs. |

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Stellen Sie mithilfe des Knotens "PBR Albedo Safe Color" sicher, dass die Farbbereiche der Albedo für PBR-Materialien physikalisch plausibel sind.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR Albedo Safe Color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# PBR Albedo Safe Color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color-01.png){width="128px"}

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Hilfsknoten, der Korrekturen vornimmt, wenn die Werte &quot;Grundfarbe&quot; oder &quot;Diffus&quot; außerhalb eines akzeptablen, PBR-korrekten Bereichs liegen. Bei der Einstellung &quot;Metallisch&quot; versucht der Knoten auch, Grundfarbwerte basierend auf der Metallic-Intensität zu korrigieren.

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

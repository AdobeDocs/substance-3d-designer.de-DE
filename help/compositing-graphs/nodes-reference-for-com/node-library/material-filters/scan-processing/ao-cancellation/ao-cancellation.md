---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Verwenden Sie den AO-Stornierungsknoten, um ambient occlusion aus gescannten Materialien zu entfernen, damit Texturen fehlerfrei verarbeitet werden können.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO-Kündigung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# AO-Kündigung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten versucht, alle Ambient occlusion-Beleuchtungsinformationen aus Ihrer Albedo- (Grundfarbe-) Map basierend auf einem separaten AO-Map-Eingang zu entfernen. Es kann verwendet werden, um sicherzustellen, dass Ihre Albedo-Informationen PBR-korrekt sind und meist keine (starken) Beleuchtungsinformationen enthalten.

Ein nützlicher Node, wenn Sie eine Baking geführt AO-Map von einem gescannten Mesh haben, oder alternativ sogar eine AO-Map, die aus Height- oder Normal-Informationen generiert wurde.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>AO-Abbruch</b> <i>0.0 - 1.0</i> | Stärke, mit der Beleuchtungsinformationen entfernt werden. |
| <b>AO-Sättigung</b> <i>0.0 - 1.0</i> | (De)Sättigungskompensation für Bereiche, in denen die Beleuchtung entfernt wird. So können Sie Farbverluste in dunkleren Bereichen ausgleichen. |

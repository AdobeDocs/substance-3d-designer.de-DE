---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "AO-Stornierung", um Umgebungsgeräusche aus gescannten Verdeckungen für eine saubere Texturverarbeitung zu entfernen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO-Kündigung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# AO-Kündigung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## AO-Kündigung

**In:** *Materialfilter/Scanverarbeitung*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten versucht, alle Umgebungsfarben-Beleuchtungsinformationen aus Ihrer Albedo-Map (Grundfarbe) zu entfernen, die auf einem separaten AO-Map-Eingang basieren. Es kann verwendet werden, um sicherzustellen, dass Ihre Albedo-Informationen PBR-korrekt sind und meist keine (starken) Beleuchtungsinformationen enthalten.

Ein nützlicher Knoten, wenn Sie eine AO-Map aus einem gescannten Gitter oder auch eine AO-Map aus Height- oder Normalinformationen erstellt haben.

## Parameter

* **AO-Abbruch**: *0.0 - 1.0* Stärke, mit der Beleuchtungsinformationen entfernt werden.
* **AO-Sättigung**: *0.0 - 1.0*(De)Sättigungskompensation für Bereiche, in denen die Beleuchtung entfernt wird. So können Sie Farbverluste in dunkleren Bereichen ausgleichen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

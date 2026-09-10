---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Material-Überblendung , um ganze Material mithilfe von Masken zu verblenden, um Composite-Material-Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Material Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>In:</b> Materialfilter > Mischen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Die Material-Überblendung ist das Multi-Channel-Material-Äquivalent von [dem Knoten der atomaren Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Es überblendet zwei vollständige Materialien (alle möglichen Kanäle) auf der Grundlage einer Graustufenmaske oder optional auf der Grundlage einer einzigen Farbe aus einer Farb-ID-Maske.

Dieser Knoten ist nützlich, wenn Sie zwei Material überblenden möchten und eine Graustufenzuordnung, aber kein vollständiges Farb-ID-Baking haben möchten. Wenn Sie über ein Farb-ID-Baking verfügen und mehr als zwei Materialien überblenden möchten, empfehlen wir Ihnen, [Überblendung mit mehreren Materialien](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) zu verwenden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Farbeingabe</i> | Optional: Baking geführt Farb-ID-Map. |
| <b>Graustufenmaske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie Material-Kanäle in dieser Gruppe ein und aus, wenn Sie Specular-/Glanz-Maps anstelle von z. B. Metallic/Rauheit verwenden. |
| <b>Diffuse</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Grundfarbe</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Normal</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Specular</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Emissive</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Glanz</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Rauheit</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Metallic</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Specular level</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Umgebungs-Verdeckung</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Height</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Deckkraft</b> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> |  |
| <b>Farb-ID-Maske</b> <i>False/True</i> | Verwenden Sie Farb-ID-Maske anstelle einer Graustufenmaske. Beachten Sie, dass dies nur für eine Farbe ist! |
| <b>Farbe</b> <i>(Farbwert)</i> | Welche Farbe ausgewählt und in Weiß konvertiert werden soll. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Der Grad, in dem die von Ihnen ausgewählte Farbe in die Nachbarfarben übergeht. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Übergangskontrast der ausgewählten Farbe. |

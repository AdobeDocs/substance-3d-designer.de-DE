---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialfarben-Überblendung , um Farbkanäle zwischen Materialien zu überblenden und so zusammengesetzte Materialeffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Color Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Material Color Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>In:</b> Materialfilter > Mischen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ermöglicht Anpassungen an einem Material mit mehreren Kanälen und voller Auflösung durch Mischen von Volltonfarben darüber. Dies ist der Hauptunterschied zur [Material Adjustment-Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), die nur [Tonwertkorrekturen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) an Kanälen zulässt, während dieser Knoten [Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)-Tonwertkorrekturen mit einer Volltonfarbe verwendet.

Dieser Knoten ist besonders hilfreich, wenn Sie einen einfachen Farbhinweis in Diffuse oder Grundfarbe einfügen oder andere Kanäle mit einem festgelegten Wert für die Volltonfarbe &quot;glätten&quot; möchten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Farbeingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Graustufenmaske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, wenn Sie z. B. Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Diffus</b> |  |
| <b>Farbe</b> <i>(Farbwert)</i> | Der Farbwert, der über dem Diffuse-Kanal überblendet werden soll. |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode Deckkraft zwischen Vorder- und Hintergrund. |
| <b>Füllmethode</b> <i>Normal, Hinzufügen, Subtrahieren, Multiplizieren, Hinzufügen/Sub, Max, Min, Switch</i> | Überblendung-Modus für den Betrieb. |
| <b>Grundfarbe</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Normal</b> |  |
| <b>Quelle</b> <i>Height, Maske</i> |  |
| <b>Füllmethode</b> <i>Zusammenführen, Überblendung</i> |  |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> |  |
| <b>Deckkraft des Heights</b> <i>0.0 - 1.0</i> |  |
| <b>Format</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Ausstrahlend</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Glossarität</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Raueit</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Metallisch</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Specular level</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Umgebungs-Verdeckung</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Height</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Deckkraft</b> | Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;. |
| <b>Farb-ID-Maske</b> <i>False/True</i> | Verwenden Sie Farb-ID-Maske anstelle einer Graustufenmaske. Beachten Sie, dass dies nur für eine Farbe gilt!<br><br>Aktiviert alle folgenden Optionen. |
| <b>Farbe</b> <i>(Farbwert)</i> | Welche Farbe ausgewählt und in Weiß konvertiert werden soll. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Der Grad, in dem die von Ihnen ausgewählte Farbe in die Nachbarfarben übergeht. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Übergangskontrast der ausgewählten Farbe. |

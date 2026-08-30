---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Luminanzüberblendung , um Texturen basierend auf Luminanzwerten zu überblenden, um helligkeitsbasierte zusammengesetzte Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminanz (Mischknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6507710c6005db383ba88ce9e5c6ad9c34d87c9f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Luminanz (Mischknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>In:</b> Filters > Blending

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt eine Füllmethode für die Luminanz durch, bei der Farbton und Chrominanz des Hintergrunds beibehalten werden, während die Luminanz des Vordergrunds übernommen wird.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vordergrund</b> <i>Farbeingabe</i> |  |
| <b>Hintergrund</b> <i>Farbeingabe</i> |  |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode Deckkraft zwischen Vorder- und Hintergrund. |
| <b>Alpha-Überblendung</b> <i>False/True</i> | Blendet die Alphakanäle für Vorder- und Hintergrund ein bzw. aus. Wenn der Wert auf &quot;Falsch&quot; gesetzt ist, wird der Alphakanal des Vordergrunds ignoriert. |

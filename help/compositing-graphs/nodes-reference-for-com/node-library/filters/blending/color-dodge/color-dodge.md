---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: Mit dem Mischknoten "Farbig abwedeln" kannst du Strukturen aufhellen, indem du den Kontrast verringerst und so Glanz- und Lichteffekte erzeugst.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbig abwedeln
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 9%

---


# Farbig abwedeln

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-dodge.resources/color-dodge-01.png){width="128px"}

<b>In:</b> Filters > Blending

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt eine Farbabwedler-Überblendung durch. Mathematisch ist die Formel Hintergrund / (1-Vordergrund).

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

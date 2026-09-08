---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: Mit dem Mischknoten "Farbig abwedeln" können Sie Texturen aufhellen, indem Sie den Kontrast für Glanz- und Lichteffekte reduzieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbig abwedeln
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 9%

---


# Farbig abwedeln

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-dodge.png){width="128px"}

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
| <b>Alpha-Überblendung</b> <i>False/True</i> | Schaltet die Füllmethode für den Vorder- und Hintergrund-Alphakanal um. Wenn der Wert auf &quot;Falsch&quot; gesetzt ist, wird der Alphakanal des Vordergrunds ignoriert. |

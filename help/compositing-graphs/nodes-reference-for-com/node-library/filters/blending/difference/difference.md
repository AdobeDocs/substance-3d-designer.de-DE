---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Differenz-Überblendung", um Texturen mithilfe des Differenzmodus zu überblenden und so Invertierungs- und Kontrasteffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Differenz
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Differenz

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

<b>In:</b> Filters > Blending

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Differenzüberblendmodus zwischen Vorder- und Hintergrund-Eingaben durch. Subtrahiert den Hintergrund vom Vordergrund und gibt ein absolutes Ergebnis zurück (niemals einen negativen Wert).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrund</b> <i>Farbeingabe</i> |  |
| <b>Vordergrund</b> <i>Farbeingabe</i> |  |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode Deckkraft zwischen Vorder- und Hintergrund. |
| <b>Alpha-Überblendung</b> <i>False/True</i> | Blendet die Alphakanäle für Vorder- und Hintergrund ein bzw. aus. Wenn der Wert auf &quot;Falsch&quot; gesetzt ist, wird der Alphakanal des Vordergrunds ignoriert. |

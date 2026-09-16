---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Richtungsverkrümmung", um Texturen eine Richtungsverkrümmung zuzuweisen und so Fluss- und Bewegungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsverzerrung
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 9%
---

# Richtungsverzerrung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Richtungsverkrümmung](directional-warp.resources/comp_directionalwarp_1.png "Atomarer Knoten: Richtungsverkrümmung"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Verschiebt Pixel in einer bestimmten Richtung entsprechend einer Intensitäts-Map, was zu Deformationen führen kann.

Verzerrt eine Eingabe in eine Richtung des Benutzersatzes, multipliziert mit einer vom Benutzer festgelegten Intensitätszuordnung. Die Funktion funktioniert ähnlich wie die Option &quot;Verformen&quot;, jedoch nur in eine bestimmte Richtung.

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="directional-warp.resources/directional-warp-tooltip.gif" alt="Richtungsverkrümmungs-QuickInfo" /></div>

Der Verformen-Knoten ist ein recht einfacher, aber nützlicher Knoten, der als gute Grundlage für andere, komplexere Effekte dient. Es gibt fortgeschrittenere Alternativen, z. B. die [Steigung-Weichzeichnung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) und die [Vektorverkrümmung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).



## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Gleitend* | Legt die Intensität der Verformung fest. |
| <b>Verkrümmungswinkel</b> *Gleitend* | Legt den Winkel des Verkrümmungseffekts in der Anzahl der Windungen fest. |
| <b>Eingangsfiltermodus</b> *Boolescher Wert* | Steuert, ob die nächste oder bilineare Filterung zum Sampeln der <b>Eingabe</b> verwendet wird. |
| <b>Offset der Intensitätszuordnung</b> *Gleitend* | Dieser Wert wird von den Bildwerten für <b>Intensitätseingabe</b> subtrahiert. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Das Graustufen- oder Farbeingabebild, auf das der Verkrümmungseffekt angewendet werden soll. |
| <b>Intensitätseingabe</b> *Graustufen* | Das Graustufenbild, das den Grad der Verformung definiert, der auf das <b>Eingabe</b>-Bild angewendet werden soll. |


## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungsverkrümmung - Beispiel 1](directional-warp.resources/dir-warp.gif "Richtungsverkrümmung - Beispiel 1"){width="20%"}{zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsverkrümmung - Beispiel 2](directional-warp.resources/dir-warp02.gif "Richtungsverkrümmung - Beispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsverkrümmung - Beispiel 3](directional-warp.resources/dir-warp03.gif "Richtungsverkrümmung - Beispiel 3"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Richtungsverzerrung", um Texturen eine gerichtete Verzerrung zuzuweisen, um Fluss- und Bewegungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsverzerrung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---


# Richtungsverzerrung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Richtungsverkrümmung](../../../../assets/comp_directionalwarp_1.png "Elementare Knoten: Richtungsverkrümmung"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Verschiebt Pixel in einer bestimmten Richtung entsprechend einer Intensitäts-Map, was zu Deformationen führen kann.

Verzerrt eine Eingabe in eine Richtung des Benutzersatzes, multipliziert mit einer vom Benutzer festgelegten Intensitätszuordnung. Die Funktion funktioniert ähnlich wie die Option &quot;Verformen&quot;, jedoch nur in eine bestimmte Richtung.

</td>
</tr>
</table>

Der Verformen-Knoten ist ein recht einfacher, aber nützlicher Knoten, der als gute Grundlage für andere, komplexere Effekte dient. Es gibt fortgeschrittenere Alternativen, z. B. die [Steigung-Weichzeichnung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) und die [Vektorverkrümmung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Fließkommazahl* | Legt die Intensität der Verformung fest. |
| <b>Verkrümmungswinkel</b> *Fließkommazahl* | Legt den Winkel des Verkrümmungseffekts in der Anzahl der Windungen fest. |
| <b>Eingabe-Filtermethode</b> *Boolesche Wert* | Steuert, ob zum Sampeln der <b>Eingabe</b> die nächsten oder bilinearen Filterungen verwendet werden. |
| <b>Offset der Intensitätszuordnung</b> *Fließkommazahl* | Dieser Wert wird von den Bildwerten für <b>Intensitätseingabe</b> subtrahiert. |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Das Graustufen- oder Farb-Eingabebild, auf das die Verkrümmung angewendet werden soll. |
| <b>Intensitätseingabe</b> *Graustufen* | Das Graustufenbild, das den Grad der Verformung definiert, der auf das <b>Eingabe</b>-Bild angewendet werden soll. |

## Ausgabe-Verbindungen

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungsverzerrung - Beispiel 1](../../../../assets/dir-warp.gif "Richtungsverzerrung - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsverzerrung - Beispiel 2](../../../../assets/dir-warp02.gif "Richtungsverzerrung - Beispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsverzerrung - Beispiel 3](../../../../assets/dir-warp03.gif "Richtungsverzerrung - Beispiel 3"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-5.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Dirt 5, um erweiterte Dirt-Muster zum Erstellen von verwitterten und gealterten Oberflächendetails zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt 5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: DIRT 5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---


# DIRT 5

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dirt 5 - Symbol](../../../../../../assets/dirt_5.png "Dirt 5 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der körnigen <b>Dirt</b>-Rauschen.

Siehe auch: [Dirt 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md), [Dirt 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md), [Dirt 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md), [Dirt 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-4/dirt-4.md), [Dirt-Verlauf](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-gradient/dirt-gradient.md)

</td>
</tr>
</table>

## Ausgaben

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Die generierte Rauschen als Graustufen-Bitmap. |

## Parameter

|  |  |
| --- | --- |
| <b>Skalierung</b> Ganzzahl | Die Unterteilung des Rasters, der zum Generieren der Rauschen-Kacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Fließkommazahl </b> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Fließkommazahl der Störungsgeschwindigkeit</b> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Anisotropie der Störung</b> Fließkommazahl | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Richtung wird durch den Parameter <b>Disorder anisotropy angle</b> gesteuert. |
| <b>anisotropy angle </b>-Fließkommazahl | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> Fließkommazahl2 | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> Boolesche Wert | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 5 - Beispiel 1](../../../../../../assets/dirt_5_1.png "Dirt 5 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 5 - Beispiel 2](../../../../../../assets/noise_dirt_5_v2_speed0.6_aniso0.gif "Dirt 5 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 5 - Beispiel 3](../../../../../../assets/noise_dirt_5_v2_speed0.6_aniso1.gif "Dirt 5 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 5 - Beispiel 4](../../../../../../assets/noise_dirt_5_v2_speed0.3_aniso0.6.gif "Dirt 5 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

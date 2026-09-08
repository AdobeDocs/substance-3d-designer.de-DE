---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-2.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Gaußsche Bereiche 2", um erweiterte Gaußsche Bereichsmuster zum Erstellen von Variationen organischer Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gaußsche Flecken 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78ee271bee643682c3815dd1657d66accb2f31c4
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# Gaußsche Flecken 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Symbol](../../../../../../assets/gaussian_spots_2.png "Gaußsche Flecken 2 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der glatten <b>Gaußschen Flecken</b> Rauschen.\
Basierend auf dem [Gaußschen Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)-Knoten, mit schmaleren Farbverläufen und höheren Frequenzen.

Siehe auch: [Gaußsche Flecken 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Die generierte Rauschen als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>Ganzzahl</i> | Die Unterteilung des Rasters, der zum Generieren der Rauschen-Kacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Fließkommazahl</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Anisotropie der Störung</b> <i>Fließkommazahl</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Beispiel 1](../../../../../../assets/gaussian_spots_2_1.png "Gaußsche Flecken 2 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Beispiel 2](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso0.gif "Gaußsche Flecken 2 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Beispiel 3](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso1.gif "Gaußsche Flecken 2 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Beispiel 4](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.3_aniso0.6.gif "Gaußsche Flecken 2 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

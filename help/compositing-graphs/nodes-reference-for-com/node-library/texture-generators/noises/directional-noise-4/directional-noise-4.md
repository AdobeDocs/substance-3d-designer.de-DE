---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-4.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Richtungsrauschen 4, um Richtungsrauschen-Muster mit vier Oktaven zu erzeugen, um anisotrope Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RICHTUNGSRAUSCHEN 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 93824555c1b2d3de289eaf470e6f929ebf90dd71
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# RICHTUNGSRAUSCHEN 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Richtungsrauschen 4 - Symbol](directional-noise-4.resources/directional_noise_4.png "Richtungsrauschen 4 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>Richtungsrauschen</b>-Geräusche.

Siehe auch: [Richtungsrauschen 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Richtungsrauschen 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Richtungsrauschen 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das erzeugte Rauschen als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>Integer</i> | Die Unterteilung des Rasters, das zum Erzeugen der Rauschkacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Anisotropie der Störung</b> <i>Gleitend</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Richtung wird durch den Parameter <b>Disorder anisotropy angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Fließkommazahl</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Winkel</b> <i>Fließkommazahl</i> | Der Winkel, der zum Festlegen der Richtung des Rauschen verwendet wird, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Fließkommazahl</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Kachelversatz</b> <i>Fließkommazahl2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungsrauschen 4 - Beispiel 1](directional-noise-4.resources/directional_noise_4_1.png "Richtungsrauschen 4 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsrauschen 4 - Beispiel 2](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.6_aniso0.gif "Richtungsrauschen 4 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungsrauschen 4 - Beispiel 3](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.6_aniso1.gif "Richtungsrauschen 4 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungsrauschen 4 - Beispiel 4](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.3_aniso0.6.gif "Richtungsrauschen 4 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

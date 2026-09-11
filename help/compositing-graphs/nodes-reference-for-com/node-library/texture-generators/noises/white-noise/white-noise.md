---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Weißer Rauschen", um Weiß-Rauschen-Muster zu generieren, um Variationen von Texturen und zufällige Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Weißes Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Weißes Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Weiße Rauschen - Symbol](white-noise.resources/white_noise_v2.png "Weiße Rauschen - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine weiße Rauschen mit einer von drei Methoden, die auf verschiedene Histogrammformen abzielen: einheitlich, Gaußsch und Dreieck.

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
| <b>Rauschen-Verteilung</b> <i>Integer</i> | Die Methode zur Verteilung der Inhaltsstoffe auf eine Histogrammform:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Einheitlich:</i> Ein flaches Histogramm.</li> <li data-preserve-html="true"><i>Gaußsch:</i> Ein Histogramm, das eine Normalverteilung darstellt, ähnlich einer Glockenkurve.</li> <li data-preserve-html="true"><i>Dreieck:</i> Ein dreieckiges Histogramm.</li> </ul> |
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![White Rauschen - Beispiel 1](white-noise.resources/white_noise_v2_1.png "White Rauschen - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![White Rauschen - Beispiel 2](white-noise.resources/white_noise_v2_speed0.6_aniso0.gif "White Rauschen - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

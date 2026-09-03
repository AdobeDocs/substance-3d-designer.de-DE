---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Gaußsche Flecken 1", um Gaußsche Fleckmuster zum Erstellen organischer Strukturvariationen und Details zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gaußsche Flecken 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# Gaußsche Flecken 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Gaußsche Flecken 1 - Symbol](gaussian-spots-1.resources/gaussian-spots-1-01.png "Gaußsche Flecken 1 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der glatten <b>Gaußschen Flecken</b>, die Geräusche verursachen.\
Basierend auf dem Knoten [Gaußsches Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md) mit engeren Verläufen.

Siehe auch: [Gaußsche Flecken 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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
| <b>Anisotropie der Störung</b> <i>Gleitend</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Gaußsche Flecken 1 - Beispiel 1](gaussian-spots-1.resources/gaussian-spots-1-02.png "Gaußsche Flecken 1 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Gaußsche Flecken 1 - Beispiel 2](gaussian-spots-1.resources/gaussian-spots-1-03.gif "Gaußsche Flecken 1 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Gaußsche Flecken 1 - Beispiel 3](gaussian-spots-1.resources/gaussian-spots-1-04.gif "Gaußsche Flecken 1 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Gaußsche Flecken 1 - Beispiel 4](gaussian-spots-1.resources/gaussian-spots-1-05.gif "Gaußsche Flecken 1 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

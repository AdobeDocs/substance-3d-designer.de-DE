---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Perlin Rauschen", um sanfte, natürlich aussehende Rauschen-Muster für die Erstellung organischer Texturen und Variationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Perlin Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Perlin Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Perlin Rauschen - Symbol](perlin-noise.resources/perlin_noise.png "Perlin Rauschen - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Perlin-Rauschen, eine weit verbreitete, gleichmäßige Verteilung von Graustufenwerten.

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
| <b>Kachelversatz</b> <i>Fließkommazahl2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Perlin-Rauschen - Beispiel 1](perlin-noise.resources/perlin_noise_1.png "Perlin-Rauschen - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Perlin-Rauschen - Beispiel 2](perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif "Perlin-Rauschen - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Anisotropes Rauschen", um Richtungsrauschen-Muster zum Erstellen anisotroper Textureffekte zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anisotropes Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Anisotropes Rauschen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Anisotropes Rauschen - Symbol](../../../../../../assets/anisotropic_noise_v2.png "Anisotropes Rauschen - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein horizontaler oder vertikaler Stapel von zufällig gefärbten Streifen, die ineinander übergehen.

Die Anzahl der Streifen ist einstellbar, ebenso wie die Smoothness ihrer Übergänge.

</td>
</tr>
</table>

## Ausgaben

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Das erzeugte Rauschen als Graustufen-Bitmap. |

## Parameter

|  |  |
| --- | --- |
| <b>X Betrag</b> Ganzzahl | Die Anzahl der Streifen auf der X-Achse. |
| <b>Y Betrag</b> Ganzzahl | Die Anzahl der Streifen auf der Y-Achse. |
| <b>Y Betrag nach Auflösung</b> Boolean | Wenn dieser Wert wahr ist, entspricht die Anzahl der Streifen auf der Y-Achse der Bildgröße auf dieser Achse. |
| <b>Rotieren</b> Boolescher Wert | Dreht das Rauschen um 90 Grad. |
| <b>Smoothness</b> Gleitend | Die Stärke der Überblendung zwischen den Streifen, wobei 0 keine Überblendung bedeutet und 1 über ihre gesamte Länge verblasst. |
| <b>Smoothness-Interpolation</b> Gleitend | Die Gewichtung der beiden Methoden der Interpolation angewendet, um die Streifen zu überblenden, wobei 0 linear und 1 Gauß ist. |
| <b>Störung</b> Float | Versetzt die Bestandteile des Rauschens.   So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> Gleitend | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.   Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Nicht quadratische Erweiterung</b> Boolescher Wert | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Anisotropes Rauschen - Beispiel 1](../../../../../../assets/anisotropic_noise_v2_1.png "Anisotropes Rauschen - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Anisotropes Rauschen - Beispiel 2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "Anisotropes Rauschen - Beispiel 2"){zoomable="yes"}

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

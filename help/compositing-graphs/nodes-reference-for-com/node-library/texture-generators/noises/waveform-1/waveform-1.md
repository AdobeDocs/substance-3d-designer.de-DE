---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Wellenform 1, um Wellenformmuster zum Erstellen organischer Texturen und prozeduraler Variationen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Waveform 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---


# Waveform 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Wellenform 1 - Symbol](../../../../../../assets/waveform_01_v2.png "Wellenform 1 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Horizontale Anordnung von vom Benutzer ausgewählten Mustern, die in einer Form ähnlich einer Wellenform gestapelt sind.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Ausgaben

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
<td style="border: 0;" valign="top">

### Beispiele

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
| <b>Beispiele</b> Ganze Zahl | Die Anzahl der Muster, die entlang der X-Achse platziert werden, um die Wellenform zu zeichnen, wobei ein niedrigerer Wert zu einer abgestuften Darstellung führt. |
| <b>Funktion</b> Ganzzahl | Die Funktion, mit der die Wellenform gezeichnet wird.   Dadurch wird die vertikale Größe des Musters gesteuert, das an jedem Sample platziert wird:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Wert-Rauschen:</i> Eine zufällige Verteilung der Werte</li> <li data-preserve-html="true"><i>Kosinus:</i> Die Werte folgen dem Verlauf einer Kosinusfunktion</li> <li data-preserve-html="true"><i>Benutzerdefinierte Funktion:</i> Verwenden Sie eine vom Benutzer verfasste Funktion zum Steuern der Werte.</li> </ul> |
| <b>Benutzerdefinierte Funktion</b> Float *Verfügbar, wenn &quot;Funktion&quot; auf &quot;Benutzerdefinierte Funktion&quot; festgelegt ist* | Berechnet die vertikale Größe des Musters, das an jedem Sample platziert wird.   Verfügbare Variablen:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) Die Position des Musters auf der X-Achse. Dies kann zur Auswahl von Mustern verwendet werden.</li> </ul> |
| <b>Unregelmäßigkeit</b> Unregelmäßigkeit | Interpoliert zwischen einer sauberen und glatten Wellenform mit einer raueren und gleichmäßigeren Wellenform.    Das kann man sich als klares Signal oder weißes Rauschen vorstellen. |
| <b>Skalierung</b> Ganze Zahl | Die horizontale Spanne der im Bild sichtbaren Wellenform. |
| <b>Amplitude min.</b>  Float | Der Mindestwert (oder die Thickness) der Wellenform. |
| <b>Maximale Amplitude</b>  Float | Der Maximalwert (oder die Thickness) der Wellenform. |
| <b>Rauschen</b> (schwebend) | Wendet Rauschen auf die Wellenform an, die zufällig von ihrer vertikalen Spanne subtrahiert. |
| <b>Position</b> Ganzzahl | Die Position der Wellenform im Bild:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Zentriert:</i> Der Ursprung befindet sich in der vertikalen Mitte des Bildes</li> <li data-preserve-html="true"><i>Unten:</i> Der Ursprung befindet sich am unteren Rand des Bildes.</li> </ul> |
| <b>Muster</b> Ganzzahl | Das Muster, das bei jedem Sample der Wellenform platziert wird. |
| <b>Mustervariation</b> Gleitkomma | Für einige Muster ist eine zusätzliche Anpassung verfügbar. |
| <b>Störung</b> Float | Verschiebt die Werte der Wellenform.    Mit dieser Option kannst du den Clip animieren. |
| <b>Störungsgeschwindigkeit</b> Gleitend | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation der Wellenform steuern. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Wellenform 1 - Beispiel 1](../../../../../../assets/waveform_01_v2_speed0.1_aniso0.gif "Wellenform 1 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den Node "Feuchtigkeit-Rauschen", um Feuchtigkeits- und Kondensationsmuster zu erzeugen, um Effekte auf der nassen Oberfläche zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Feuchtigkeit Rauschen 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---


# Feuchtigkeit Rauschen 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rauschen mit Feuchtigkeit 1 - Symbol](../../../../../../assets/moisture_noise_1.png "Rauschen mit Feuchtigkeit 1 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der reichen und schwammigen <b>Feuchtigkeit</b> Rauschen.

Festplatten unterschiedlicher Härte und Größe, die verstreut sind und von der unten stehenden Farbe subtrahiert oder addiert werden (ausgehend von einem grauen Grund).

Siehe auch: [Feuchtigkeits-Rauschen 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

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
| <b>Mustergröße</b> Float2 | Ein Multiplikator für die Größe eines gestreuten Musters., wobei 1,0 seine ursprüngliche Größe ist. |
| <b>Musterwinkel</b> Gleitend | Der Winkel, der verwendet wird, um die Richtung des gestreuten Musters festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Musterwinkel</b> Gleitkomma | Die maximale zufällige Schwankungsbreite, die auf den Wert <b>Musterwinkel</b> in Windungszahlen angewendet wird. |
| <b>Globale Deckkraft</b> Gleitend | Die Deckkraft aller Bestandteile des Rauschens, wobei 0,0 zu einem flachen grauen Grundton führt und 1,0 das Ergebnis der vollständigen Addition oder Subtraktion ist, die von den Bestandteilen angewendet wird. |
| <b>Kachelversatz</b> Gleitkomma2 | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> Boolescher Wert | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Feuchtigkeitsrauschen 1 - Beispiel 1](../../../../../../assets/moisture_noise_1_1.png "Feuchtigkeitsrauschen 1 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Feuchtigkeitsrauschen 1 - Beispiel 2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "Feuchtigkeitsrauschen 1 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Feuchtigkeitsrauschen 1 - Beispiel 3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "Feuchtigkeitsrauschen 1 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Feuchtigkeitsrauschen 1 - Beispiel 4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "Feuchtigkeitsrauschen 1 - Beispiel 4"){zoomable="yes"}

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

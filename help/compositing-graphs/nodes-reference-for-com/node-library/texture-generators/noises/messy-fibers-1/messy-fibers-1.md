---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-1.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Messy Fibers 1, um einfache Fasermuster zum Erstellen von Textil- und Textiltexturdetails zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unsaubere Fasern 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# Unsaubere Fasern 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Schmutzige Fasern 1 - Symbol](../../../../../../assets/messy_fibers_1.png "Schmutzige Fasern 1 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>chaotischen Fasern</b> strukturierten Geräusche.

Siehe auch: [Schmutzige Fasern 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md), [Schmutzige Fasern 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>Skalierung</b> Ganze Zahl | Die Unterteilung des Rasters, das zum Erzeugen der Rauschkacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Störung</b> Float | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> Gleitend | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Disorder Anisotropie</b> Float | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Winkel der Anisotropie der Störung</b> Gleitend | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Winkel</b> Gleitend | Der Winkel, der verwendet wird, um die Richtung der Fäden festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> Gleitend | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Zeilennummer</b> Gleitkomma | Die Menge der Kachelung, die auf die Grundfäden aufgebracht wird, wobei ein höherer Wert zu dichteren, dünneren Fäden führt. |
| <b>Kachelversatz</b> Gleitkomma2 | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> Boolescher Wert | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Schmutzige Fasern 1 - Symbol](../../../../../../assets/messy_fibers_1_1.png "Schmutzige Fasern 1 - Symbol"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Schmutzige Fasern 1 - Beispiel 2](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.gif "Schmutzige Fasern 1 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Schmutzige Fasern 1 - Beispiel 3](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso1.gif "Schmutzige Fasern 1 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Schmutzige Fasern 1 - Beispiel 4](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.6.gif "Schmutzige Fasern 1 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

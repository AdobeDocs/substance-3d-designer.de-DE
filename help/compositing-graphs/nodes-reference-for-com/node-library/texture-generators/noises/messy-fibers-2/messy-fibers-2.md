---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-2.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Messy Fibers 2, um Zwischenfasermuster zum Erstellen von gewebten und textilen Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unsaubere Fasern 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Unsaubere Fasern 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Schmutzige Fasern 2 - Symbol](messy-fibers-2.resources/messy-fibers-2-01.png "Schmutzige Fasern 2 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>chaotischen Fasern</b> strukturierten Geräusche.

Siehe auch: [Schmutzige Fasern 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Schmutzige Fasern 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Winkel</b> <i>Gleitend</i> | Der Winkel, der verwendet wird, um die Richtung der Fäden festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Gleitend</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Zeilennummer</b> <i>Gleitend</i> | Die Menge der Kachelung, die auf die Grundfäden aufgebracht wird, wobei ein höherer Wert zu dichteren, dünneren Fäden führt. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Schmutzige Fasern 2 - Beispiel 1](messy-fibers-2.resources/messy-fibers-2-02.png "Schmutzige Fasern 2 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Schmutzige Fasern 2 - Beispiel 2](messy-fibers-2.resources/messy-fibers-2-03.gif "Schmutzige Fasern 2 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Schmutzige Fasern 2 - Beispiel 3](messy-fibers-2.resources/messy-fibers-2-04.gif "Schmutzige Fasern 2 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Schmutzige Fasern 2 - Beispiel 4](messy-fibers-2.resources/messy-fibers-2-05.gif "Schmutzige Fasern 2 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

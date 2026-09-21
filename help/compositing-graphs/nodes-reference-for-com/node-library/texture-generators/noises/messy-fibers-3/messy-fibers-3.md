---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Messy Fibers 3, um komplexe Fasermuster für die Erstellung von Textil- und Textil-Textur-Effekten zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unsaubere Fasern 3
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%
---

# Unsaubere Fasern 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Schmutzige Fasern 3 - Symbol](messy-fibers-3.resources/messy_fibers_3.png "Schmutzige Fasern 3 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der <b>chaotischen Fasern</b> strukturierten Rauschen.

Siehe auch: [Schmutzige Fasern 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Schmutzige Fasern 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>Anisotropie der Störung</b> <i>Fließkommazahl</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Richtung wird durch den Parameter <b>Disorder anisotropy angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Fließkommazahl</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Winkel</b> <i>Fließkommazahl</i> | Der Winkel, der verwendet wird, um die Richtung der Fäden festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Fließkommazahl</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Luminanz zufällig</b> <i>Fließkommazahl</i> | Der Bereich der Luminanz, der zufällig von den Threads subtrahiert wird, wobei 1 der gesamte Bereich ist. |
| <b>Kachelversatz</b> <i>Fließkommazahl2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/messy_fibers_3_1.png" class="modal-image" alt="Schmutzige Fasern 3 - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.gif" class="modal-image" alt="Schmutzige Fasern 3 - Beispiel 2" />
        </td>
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso1.gif" class="modal-image" alt="Schmutzige Fasern 3 - Beispiel 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif" class="modal-image" alt="Schmutzige Fasern 3 - Beispiel 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>

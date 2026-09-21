---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-2.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Gaußsche Bereiche 2", um erweiterte Gaußsche Bereichsmuster zum Erstellen organischer Strukturvariationen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gaußsche Flecken 2
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%
---

# Gaußsche Flecken 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Gaußsche Flecken 2 - Symbol](gaussian-spots-2.resources/gaussian_spots_2.png "Gaußsche Flecken 2 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der glatten <b>Gaußschen Flecken</b>, die Geräusche verursachen.\
Basierend auf dem [Gaußschen Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)-Knoten mit engeren Gradienten und höheren Frequenzen.

Siehe auch: [Gaußsche Flecken 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md)

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
| <b>Disorder anisotropy angle</b> <i>Fließkommazahl</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> <i>Fließkommazahl2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="gaussian-spots-2.resources/gaussian_spots_2_1.png" class="modal-image" alt="Gaußsche Flecken 2 - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.6_aniso0.gif" class="modal-image" alt="Gaußsche Flecken 2 - Beispiel 2" />
        </td>
        <td style="border: 0;">
            <img src="gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.6_aniso1.gif" class="modal-image" alt="Gaußsche Flecken 2 - Beispiel 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Gaußsche Flecken 2 - Beispiel 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>

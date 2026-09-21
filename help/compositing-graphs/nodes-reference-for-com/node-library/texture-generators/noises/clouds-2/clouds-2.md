---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/clouds-2.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Wolken 2", um dazwischen liegende Wolkenmuster zu generieren, um atmosphärische und volumetrische Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Clouds 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Wolken 2
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%
---

# Wolken 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Clouds 2 - Symbol](clouds-2.resources/clouds_2.png "Clouds 2 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der groben <b>Wolken</b> Rauschen.

Siehe auch: [Clouds 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-1/clouds-1.md), [Clouds 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-3/clouds-3.md)

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
| <b>Anisotropie der Störung</b> <i>Fließkommazahl</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="clouds-2.resources/clouds_2_1.png" class="modal-image" alt="Clouds 2 - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="clouds-2.resources/noise_clouds_2_v2_speed0.6_aniso0.gif" class="modal-image" alt="Clouds 2 - Beispiel 2" />
        </td>
        <td style="border: 0;">
            <img src="clouds-2.resources/noise_clouds_2_v2_speed0.6_aniso1.gif" class="modal-image" alt="Clouds 2 - Beispiel 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="clouds-2.resources/noise_clouds_2_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Clouds 2 - Beispiel 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>

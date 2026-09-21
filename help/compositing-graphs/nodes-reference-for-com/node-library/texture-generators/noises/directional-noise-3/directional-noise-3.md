---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-3.html"
breadcrumb-title: ""
description: Verwenden Sie den Richtungsrauschen 3 -Knoten, um Richtungsrauschen-Muster mit drei Oktaven zum Erstellen von Richtungs-Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RICHTUNGSRAUSCHEN 3
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%
---

# RICHTUNGSRAUSCHEN 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Richtungsrauschen 3 - Symbol](directional-noise-3.resources/directional_noise_3.png "Richtungsrauschen 3 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der <b>Richtungsrauschen</b>-Rauschen.

Siehe auch: [Richtungsrauschen 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Richtungsrauschen 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Richtungsrauschen 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Winkel</b> <i>Gleitend</i> | Der Winkel, der verwendet wird, um die Richtung des Rauschens festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Gleitend</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="directional-noise-3.resources/directional_noise_3_1.png" class="modal-image" alt="Richtungsrauschen 3 - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="directional-noise-3.resources/noise_directional_noise_3_v2_speed0.6_aniso0.gif" class="modal-image" alt="Richtungsrauschen 3 - Beispiel 2" />
        </td>
        <td style="border: 0;">
            <img src="directional-noise-3.resources/noise_directional_noise_3_v2_speed0.6_aniso1.gif" class="modal-image" alt="Richtungsrauschen 3 - Beispiel 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="directional-noise-3.resources/noise_directional_noise_3_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Richtungsrauschen 3 - Beispiel 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>

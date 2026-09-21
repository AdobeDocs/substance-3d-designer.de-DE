---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-4.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Fraktalsumme 4, um mit vier Oktaven ein fraktales Rauschen zu erzeugen, um detaillierte organische Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FRAKTALSUMME 4
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%
---

# FRAKTALSUMME 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fraktalsumme 4 - Symbol](fractal-sum-4.resources/fractal_sum_4.png "Fraktalsumme 4 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>Fraktalsumme</b>-Störungen.

Siehe auch: [Fraktalsumme base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Fraktalsumme 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Fraktalsumme 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Fraktalsumme 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)

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
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="fractal-sum-4.resources/fractal_sum_4_1.png" class="modal-image" alt="Fraktalsumme 4 - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="fractal-sum-4.resources/noise_fractal_sum_4_v2_speed0.6_aniso0.gif" class="modal-image" alt="Fraktalsumme 4 - Beispiel 2" />
        </td>
        <td style="border: 0;"></td>
    </tr>
</table>

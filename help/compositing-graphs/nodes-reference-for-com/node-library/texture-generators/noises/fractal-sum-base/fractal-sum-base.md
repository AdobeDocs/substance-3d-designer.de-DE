---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Fraktalsumme Basis", um fraktale Grundrauschmuster zum Erstellen komplexer organischer Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fraktalsumme
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%
---

# Fraktalsumme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fraktalsumme Basis - Symbol](fractal-sum-base.resources/fractal_sum_base.png "Fraktalsumme Basis - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein anpassbares fraktales Rauschen mit einem einstellbaren Bereich und einer Balance von Oktaven.

Die Rauschfamilie <b>Fraktalsumme</b> basiert alle auf diesem Knoten.

Siehe auch: [Fraktalsumme 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Fraktalsumme 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Fraktalsumme 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Fraktalsumme 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Raueit</b> <i>Gleitend</i> | Die Balance der Rauschoktaven.    Ein höherer Wert macht die Oktaven mit höherer Frequenz sichtbarer. |
| <b>Min. Ebene </b> <i>Integer</i> | Die minimale Oktave, die im Rauschen verwendet wird.    Ein höherer Wert führt zu einer höheren Rauschfrequenz. |
| <b>Max. Ebene </b> <i>Integer</i> | Die maximale Oktave, die im Rauschen verwendet wird.    Ein höherer Wert führt zu einer höheren Rauschfrequenz. |
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Kontrast</b> <i>Gleitend</i> | Der Kontrast des Endergebnisses. |
| <b>Globale Deckkraft</b> <i>Gleitend</i> | Die Deckkraft der Rauschoktaven, die im Endergebnis addiert werden.    Ein hoher Wert kann dazu führen, dass Bereiche weiß verbrannt werden. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="fractal-sum-base.resources/fractal_sum_base_1.png" class="modal-image" alt="Fraktalsumme Basis - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="fractal-sum-base.resources/noise_fractal_sum_base_v2_speed0.6_aniso0.gif" class="modal-image" alt="Fraktalsumme Basis - Beispiel 2" />
        </td>
        <td style="border: 0;"></td>
    </tr>
</table>

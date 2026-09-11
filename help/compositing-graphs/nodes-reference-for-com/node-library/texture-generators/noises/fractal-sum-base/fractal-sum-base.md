---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Fraktalsumme-Basis, um fraktale Rauschen-Basismuster zum Erstellen komplexer organischer Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fraktalsumme
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Fraktalsumme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fraktalsumme Basis - Symbol](fractal-sum-base.resources/fractal_sum_base.png "Fraktalsumme Basis - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine anpassbare fraktale Rauschen mit einem anpassbaren Bereich und einer Oktavenbalance.

Die <b>Fraktalsumme</b>-Rauschen-Familie basiert alle auf diesem Knoten.

Siehe auch: [Fraktalsumme 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Fraktalsumme 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Fraktalsumme 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Fraktalsumme 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Rauheit</b> <i>Fließkommazahl</i> | Der Rest der Rauschen Oktaven.    Ein höherer Wert macht die Oktaven mit höherer Frequenz sichtbarer. |
| <b>Min. Ebene </b> <i>Ganzzahl</i> | Die Mindestoktave, die auf der Rauschen verwendet wird.    Ein höherer Wert führt zu einer höheren Rauschen-Frequenz. |
| <b>Max. Ebene </b> <i>Ganzzahl</i> | Die maximale Oktave, die auf der Rauschen verwendet wird.    Ein höherer Wert führt zu einer höheren Rauschen-Frequenz. |
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Fließkommazahl</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Kontrast</b> <i>Fließkommazahl</i> | Der Kontrast des Endergebnisses. |
| <b>Globale Deckkraft</b> <i>Fließkommazahl</i> | Die Deckkraft der Rauschen-Oktaven, die im Endergebnis addiert werden.    Ein hoher Wert kann dazu führen, dass Bereiche weiß verbrannt werden. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fraktalsumme Base - Beispiel 1](fractal-sum-base.resources/fractal_sum_base_1.png "Fraktalsumme Base - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fraktalsumme Base - Beispiel 2](fractal-sum-base.resources/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "Fraktalsumme Base - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

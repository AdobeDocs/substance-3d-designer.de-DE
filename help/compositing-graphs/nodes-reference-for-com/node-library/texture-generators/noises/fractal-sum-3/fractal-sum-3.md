---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-3.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Fraktalsumme 3, um eine fraktale Rauschen mit drei Oktaven zu erzeugen, um organische Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FRAKTALSUMME 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# FRAKTALSUMME 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fraktalsumme 3 - Symbol](fractal-sum-3.resources/fractal_sum_3.png "Fraktalsumme 3 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der <b>Fraktalsumme</b> Rauschen.

Siehe auch: [Fraktalsumme base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Fraktalsumme 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Fraktalsumme 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Fraktalsumme 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Fließkommazahl</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fraktalsumme 3 - Beispiel 1](fractal-sum-3.resources/fractal_sum_3_1.png "Fraktalsumme 3 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fraktalsumme 3 - Beispiel 2](fractal-sum-3.resources/noise_fractal_sum_3_v2_speed0.6_aniso0.gif "Fraktalsumme 3 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

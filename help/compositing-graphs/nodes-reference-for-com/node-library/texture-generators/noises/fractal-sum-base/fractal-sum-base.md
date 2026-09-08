---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Fraktalsumme Basis", um fraktale Grundrauschmuster zum Erstellen komplexer organischer Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fraktalsumme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Fraktalsumme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fraktalsumme Basis - Symbol](../../../../../../assets/fractal_sum_base.png "Fraktalsumme Basis - Symbol"){width="200px"}

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
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Fließkommazahl</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Kontrast</b> <i>Fließkommazahl</i> | Der Kontrast des Endergebnisses. |
| <b>Globale Deckkraft</b> <i>Fließkommazahl</i> | Die Deckkraft der Rauschen-Oktaven, die im Endergebnis addiert werden.    Ein hoher Wert kann dazu führen, dass Bereiche weiß verbrannt werden. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fraktalsumme Base - Beispiel 1](../../../../../../assets/fractal_sum_base_1.png "Fraktalsumme Base - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fraktalsumme Base - Beispiel 2](../../../../../../assets/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "Fraktalsumme Base - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

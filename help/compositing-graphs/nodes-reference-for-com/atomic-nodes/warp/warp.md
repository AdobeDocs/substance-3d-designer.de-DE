---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Verformen -Knoten, um Texturen Verzerrungen zuzuweisen, um Verzerrungs- und Versatz-Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verzerrung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# Verzerrung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Verformen](warp.resources/comp_warp_1.png "Atomknoten: Verkrümmen"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Verschiebt die Pixelwerte im Eingabebild entsprechend den Anstiegen, die aus einer separaten Verlaufseingabe berechnet werden, was zu Deformation führt.

Im Gegensatz zur Richtungsverkrümmung bewegt sich dieser Knoten gleichmäßig von weißen Bereichen weg, und zwar in einer Richtung, die durch die Steigung oder den Verlauf der Verlaufseingabe definiert wird.

</td>
</tr>
</table>

Der Knoten kann etwas schwierig zu bearbeiten sein, da das Ergebnis des Effekts sehr stark von der Verlaufseingabe abhängt: Kleine Anpassungen am Verlauf können bei gleicher Intensität einen großen visuellen Unterschied bewirken. Experimentiere mit Kontrast, Luminanz und Skalierung der Verlaufseingabe sowie dem Regler für die Intensität dieses Knotens.

Wenn Sie mit Normal-Maps vertraut sind, können Sie sich vorstellen, dass die Funktionsweise dieses Knotens der Konvertierung der Verlaufseingabe in eine [Normal-Map](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) ähnelt und die Basiseingabe dann in der durch die Normal-Map-Vektoren definierten Richtung verzerrt. Dasselbe lässt sich mit der [Vektorverkrümmung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) erreichen. Ähnliche Effekte finden Sie auch in [Steigung weichzeichnen](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Gleitend* | Legt die Intensität der Verformung fest. |
| <b>Eingangsfiltermodus</b> *Boolescher Wert* | Steuert, ob zum Sampeln der Eingabe die nächste oder bilineare Filterung verwendet wird. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Das Farb- oder Graustufenbild. |
| <b>Verlaufseingabe</b> *Graustufen* | Die Steigung des Farbverlaufs des Graustufeneingabebildes bestimmt den Verkrümmungseffekt im Ausgabebild. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

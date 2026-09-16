---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: Verwenden Sie den Verformen -Knoten, um Verzerrung-Effekte auf Texturen zum Erstellen von Verformen- und Versatz-Effekten anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verzerrung
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 9%
---

# Verzerrung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Verkrümmen](warp.resources/comp_warp_1.png "Elementare Knoten: Verkrümmen"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Verschiebt die Pixelwerte im Eingabebild entsprechend den Anstiegen, die aus einer separaten Verlaufseingabe berechnet werden, was zu Deformation führt.

Im Gegensatz zur Richtungsverzerrung schiebt dieser Knoten gleichmäßig von den weißen Bereichen weg, und zwar in einer Richtung, die durch die Steigung oder den Verlauf der Verlaufseingabe definiert wird.

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="warp.resources/warp-tooltip.gif" alt="Verkrümmen-QuickInfo" /></div>

Der Knoten kann etwas schwierig zu bearbeiten sein, da das Ergebnis des Effekts sehr stark von der Verlaufseingabe abhängt: Kleine Anpassungen am Verlauf können bei gleicher Intensität einen großen visuellen Unterschied bewirken. Experimentiere mit Kontrast, Luminanz und Skalierung des Reglers &quot;Verlaufseingabe&quot; sowie dem Regler &quot;Intensität&quot;.

Wenn Sie mit Normalen-Map vertraut sind, können Sie sich vorstellen, dass die Funktionsweise dieses Knotens der Konvertierung der Verlaufseingabe in eine [Normalen-Map](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) ähnelt und die Basiseingabe dann in der durch die Normalen-Map-Vektoren definierten Richtung verzerrt. Dasselbe lässt sich mit der [Vektorverkrümmung](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) erreichen. Ähnliche Effekte finden Sie auch in [Steigung weichzeichnen](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).



## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Fließkommazahl* | Legt die Intensität der Verformung fest. |
| <b>Eingabe-Filtermethode</b> *Boolesche Wert* | Steuert, ob zum Sampeln der Eingabe die nächstgelegenen oder bilinearen Filterungen verwendet werden. |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Die Farbe oder das Graustufenbild. |
| <b>Verlaufseingabe</b> *Graustufen* | Die Steigung des Farbverlaufs des Graustufen-Eingabebilds bestimmt die Verkrümmung im Ausgabebild. |


## Beispiele

*Demnächst verfügbar.*

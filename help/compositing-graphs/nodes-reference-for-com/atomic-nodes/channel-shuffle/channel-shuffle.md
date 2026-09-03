---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kanäle vertauschen", um Farbkanäle in Texturen neu anzuordnen, um Farbeffekte zu erstellen und Kanäle auszutauschen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kanäle mischen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# Kanäle mischen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Kanäle mischen](channel-shuffle.resources/channel-shuffle-01.png "Atomknoten: Kanäle mischen"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ordnet die Farbkanäle von einem oder zwei Eingabebildern im Ausgabebild neu an.

Das heißt, es werden zwei Eingänge verwendet und Sie können eine Ausgabe zurückgeben, bei der der Rot-, Grün-, Blau- und Alpha-Kanal vertauscht oder auf einen der Kanäle vom Eingang eingestellt wird.

Im Wesentlichen ermöglicht es Ihnen, RGB-Kanäle auf jede erdenkliche Weise zu verpacken und auszutauschen. Graustufen-Eingaben werden wie Farben behandelt: Rot, Grün, Blau und Alpha geben alle die gleichen Werte zurück.

</td>
</tr>
</table>

Channel-Shuffle bietet einfache Optionen, aber in den meisten Fällen von Channel-Packing oder Stripping und dem Festlegen von Alpha-Kanälen ist es schneller, [RGBA Merge](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), [RGBA Split](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), [Alpha Merge](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) und [Alpha Split](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md) zu verwenden. Sie sind für Standardaktionen eingerichtet, bei denen nicht mehrere Parameter geändert und danach in Graustufen konvertiert werden müssen. Wenn Sie nach einer erweiterten Version mit mehr Fülloptionen suchen, sehen Sie sich den [Kanalmixer](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md) an.

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
| <b>Roter Kanal</b> *Integer* | Wählen Sie den Quellkanal aus, der in den roten Kanal des Ausgabebilds eingefügt werden soll. |
| <b>Grüner Kanal</b> *Integer* | Wählen Sie den Quellkanal, der in den grünen Kanal des Ausgabebilds eingefügt werden soll. |
| <b>Blauer Kanal</b> *Integer* | Wählen Sie den Quellkanal aus, der in den Blaukanal des Ausgabebilds eingefügt werden soll. |
| <b>Alpha-Kanal</b> *Integer* | Wählen Sie den Quellkanal, der in den Alpha-Kanal des Ausgabebilds eingefügt werden soll. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe 1</b> *Farbe/Graustufen* PRIMÄR | Primäres Eingabebild. |
| <b>Eingabe 2</b> *Farbe/Graustufen* | Sekundäres Eingabebild. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

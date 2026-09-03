---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Pixelprozessor , um einzelne Pixel mit benutzerdefinierten Expressions für eine erweiterte Texturbearbeitung zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pixelprozessor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Pixelprozessor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Pixelprozessor](pixel-processor.resources/pixel-processor-01.png "Atomknoten: Pixelprozessor "){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Generiert ein Bild, bei dem der Wert jedes Pixels das Ergebnis des angegebenen [Substance-Funktionsdiagramms &#x200B;](../../../../function-graphs/the-function-graph/the-function-graph.md) ist.

Mit dem Pixelprozessor können Sie eine benutzerdefinierte Funktion für jedes Pixel ausführen, das als Ausgabe zurückgegeben wird, und zwar an einer optionalen Eingabe.

Es ist bei weitem der vielseitigste Knoten, da er es ermöglicht, jede mathematische Operation auszuführen und Ergebnisse innerhalb Ihres Diagramms zurückzugeben.

</td>
</tr>
</table>

Ähnlich wie [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) muss die interne Funktionalität eingerichtet werden, damit irgendetwas ausgeführt werden kann. Der Unterschied zwischen Pixel-Prozessor und FX-Map liegt darin, dass der Fokus nicht auf der Platzierung von Mustern liegt, da mehrere Funktionen die Form und Platzierung von Mustern steuern. Stattdessen wird für jedes Pixel eine einzige Funktion parallel ausgeführt, bei der jedes Pixel die Berechnungsergebnisse seiner Nachbarn nicht kennt.

Der Pixelprozessor ähnelt dem [Werteprozessor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), der nur mit einzelnen Werten ausgeführt wird und eine gute Optimierung im Vergleich zum Pixelprozessor bietet.

Für alle, die es gewohnt sind, [Shader](../../../../glossary/glossary.md)-Funktionen in knotenbasierten Editoren zu erstellen, sollte der Pixelprozessor eine vertraute Umgebung bieten.

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

>[!TIP]
>
> Eine mit Anmerkungen versehene Projektdatei, die die einfache Verwendung des Pixelprozessorknotens veranschaulicht, ist im Abschnitt [Beispiele für Substance-Grafiken](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) dieser Dokumentation verfügbar.
> 
> Der Knoten [Wertprozessor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) ist ein guter Ausgangspunkt für das Erlernen von [Substance-Funktionsdiagrammen](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Beachten Sie auch, dass die Arbeit mit dieser Art von Graphen und die Durchführung mathematischer Operationen zwingend erforderlich ist, um alles aus diesem Knoten herauszuholen.
> 
> Wir empfehlen außerdem, mit dem Konzept von [UVs](../../../../glossary/glossary.md), [Textursampling](../../../../glossary/glossary.md) und Vektoren vertraut zu sein.

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
| <b>Farbmodus</b> *Boolescher Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. |
| <b>Pro Pixelfunktion</b> *Gleitend/Gleitend4* | [Substance-Funktionsdiagramm &#x200B;](../../../../function-graphs/the-function-graph/the-function-graph.md) wird pro Pixel im Ausgabebild ausgewertet.   Verwenden Sie den Knoten [Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md), der auf die Variable <b>$pos</b> festgelegt ist, um auf die [normalisierte](../../../../glossary/glossary.md) Position des aktuellen Pixels zuzugreifen. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabebild #</b> *Graustufen/Farbe* | Verwenden Sie einen [Beispielfarbe](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)- oder [Beispielgrau](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)-Knoten, um auf die Werte in der Eingabe des angegebenen Index zuzugreifen. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

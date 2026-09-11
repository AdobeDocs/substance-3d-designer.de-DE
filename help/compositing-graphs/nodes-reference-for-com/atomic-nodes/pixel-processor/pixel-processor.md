---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Verwenden Sie den Pixelknoten, um individuelle Pixelprozessor mit benutzerdefinierten Expressions für die erweiterte Bearbeitung von Texturen zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pixelprozessor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Pixelprozessor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Pixelprozessor](pixel-processor.resources/comp_pixelprocessor_1.png "Elementare Knoten: Pixelprozessor"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Generiert ein Bild, bei dem der Wert jedes Pixels das Ergebnis des angegebenen [Substance-Funktions-Grafen ](../../../../function-graphs/the-function-graph/the-function-graph.md) ist.

Mit dem Pixelprozessor können Sie eine benutzerdefinierte Funktion für jeden Pixel ausführen, der als Ausgabe zurückgegeben wird, und zwar an einer optionalen Eingabe.

Es ist bei weitem der vielseitigste Knoten, da er es ermöglicht, jede mathematische Operation auszuführen und Ergebnisse innerhalb Ihres Grafen zurückzugeben.

</td>
</tr>
</table>

Ähnlich wie bei [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) muss die interne Funktionalität eingerichtet werden, damit irgendetwas ausgeführt werden kann. Der Unterschied zwischen dem Pixelprozessor und FX-Map liegt darin, dass der Fokus nicht auf der Platzierung von Mustern liegt. Mehrere Funktionen steuern die Form und Platzierung von Mustern. Stattdessen wird für jedes Pixel eine einzige Funktion parallel ausgeführt, bei der jedes Pixel die Berechnungsergebnisse seiner Nachbarn nicht kennt.

Der Pixelprozessor ähnelt dem [Wertprozessor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), der nur mit Einzelwerten ausgeführt wird und im Vergleich zum Pixelprozessor eine gute Optimierung bieten kann.

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
> Eine kommentierte Projektdatei, die die einfache Verwendung des Pixelprozessor-Knotens veranschaulicht, ist im Abschnitt [Beispiel-Substance-Graf](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) dieser Dokumentation verfügbar.
> 
> Der Knoten [Wertprozessor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) ist ein guter Ausgangspunkt für das Erlernen von [Substance-Grafen](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Beachten Sie außerdem, dass die Arbeit mit diesem Knotentyp und die Durchführung mathematischer Operationen zwingend erforderlich sind, um diesen Graf vollständig zu entfernen.
> 
> Wir empfehlen außerdem, mit dem Konzept von [UVs](../../../../glossary/glossary.md), [Textur Sampling](../../../../glossary/glossary.md) und Vektoren vertraut zu sein.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolesche Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. |
| <b>Pro Pixelfunktion</b> *Fließkommazahl/Fließkommazahl4* | [Graf der Substance-Funktion ](../../../../function-graphs/the-function-graph/the-function-graph.md) pro Pixel im Ausgabebild ausgewertet.   Verwenden Sie den Knoten [Get Fließkommazahl2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md), der auf die Variable <b>$pos</b> festgelegt ist, um auf die [normalisierte](../../../../glossary/glossary.md) Position des aktuellen Pixels zuzugreifen. |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Eingabebild #</b> *Graustufen/Farbe* | Verwenden Sie einen [Beispielfarbe](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)- oder [Beispielgrau](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)-Knoten, um auf die Werte in der Eingabe des angegebenen Index zuzugreifen. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

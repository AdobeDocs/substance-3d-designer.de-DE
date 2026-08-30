---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über Werttypen und Datenverarbeitung in Substance-Compositing-Graphen für eine effektive Materialerstellung.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Werte in Substance-Graphen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---


# Werte in Substance-Graphen

Seit der Einführung der [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html)-Engine v7 in Version 2019.1.0 ist es jetzt möglich, Werte im Substance-Diagramm und [nicht nur in Funktionen](../../function-graphs/function-graphs.md) zu verarbeiten. Wertedaten sind dieselben Daten, die in Funktionen verwendet werden ( Integers, Floats und Booleans usw.), wodurch sie sich deutlich von Farb- oder Graustufenbilddaten unterscheiden, die Pixelwerte für ein gesamtes Bild darstellen. Wenn Values-Daten erwähnt werden, bedeutet dies insbesondere *Integer 1, Integer 2, Integer 3 und Integer 4, Float 1, Float 2, Float 3 und Float 4 sowie Boolean*. Jede hat eine eigene Farbkodierung und wird meist nicht miteinander vertauscht.

Dafür gibt es einige Anwendungsfälle, z. B.:

* Zurückgeben und Verarbeiten von Nicht-Bild-Daten, z. B. von Materialeigenschaften mit einem Wert oder zusätzlichen Metadaten. Zum Beispiel der IOR-Wert eines Materials.
* Optimieren von Diagrammberechnungen, die nicht pro Pixel berechnet werden müssen (eine Alternative zum [Pixelprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)). Zum Beispiel eine zufällige Volltonfarbe.
* Verknüpfen von Eigenschaften eines Knotens mit anderen durch Verarbeitung von Bilddaten zu Werten. Zum Beispiel die Mindest- und Höchstwerte für ein Bild, mit denen die Tonwertkorrektur angepasst werden soll.

## Neue Wertknoten und Eingaben

Zwei neue Atomknoten funktionieren mit Werten:

|  |  |
| --- | --- |
| <div><img alt="Symbol für Werteprozessor-Knoten" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="values-in-substance-compositing-graphs.resources/valueprocessor.png" title="Symbol für Werteprozessor-Knoten" width="100px"/></div>  <b>[Value Processor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | Der [Werteprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) nimmt eine beliebige Anzahl von Graustufen- oder Farbeingaben an und ermöglicht es Ihnen, einen einzelnen Wert aus Berechnungen zurückzugeben, die auf diesen Eingaben basieren. |
| <div><img alt="Symbol für den Knoten &quot;Werteingabe&quot;" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="values-in-substance-compositing-graphs.resources/inputnumeric.png" title="Symbol für den Knoten &quot;Werteingabe&quot;" width="100px"/></div>  **[Werteingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)** | Mit der [Werteingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) können Sie einen Eingabeslot in Untergraphen erstellen, der explizit als Wert definiert ist. |

Darüber hinaus behandeln andere Knoten sie auf eine bestimmte Art und Weise:

Der [Ausgabeknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) wird automatisch angepasst, um eine Wertausgabe zu werden, wenn Sie eine Wertverbindung daran anschließen, genau wie zuvor bei Graustufen und Farbe.

![Ausgabewertknoten](values-in-substance-compositing-graphs.resources/values-output.gif "Ausgabewertknoten"){width="512px"}

Auf jedem einzelnen Knoten ([Atomic](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) und [Library](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/Instance) gibt es eine neue Registerkarte, auf der Sie Werteingaben definieren können.

![Eingabewerte für Knoten hinzufügen](values-in-substance-compositing-graphs.resources/values-inputs.gif "Eingabewerte für Knoten hinzufügen")

## Arbeiten mit Werten

Die Verwendung von Werten unterscheidet sich leicht von der normalen Arbeit mit Substance-Graphen:

Wertverbindungen können nur von einem [Wertprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), von einem [Werteingang,](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) oder von einem [Unterdiagramm](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) hergestellt werden. Das bedeutet, dass ein Value Processor die einzige Möglichkeit ist, eine Value-Verbindung von Grund auf neu zu erstellen. Es gibt keinen Knoten &quot;Statischer Wert&quot; oder Ähnliches. Erstellen Sie stattdessen einen Wertprozessor, platzieren Sie einen statischen Wert und legen Sie ihn als Ausgabe fest, um dasselbe Ergebnis zu erzielen.

Der Wertprozessor kann nur einen einzelnen Wert zurückgeben. Wenn Sie mehrere Werte oder Wertesätze oder Wertegruppen zurückgeben möchten, müssen Sie einen [Sub-Graph](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) erstellen.

Um herauszustellen, wo Werte angezeigt oder verwendet werden, wird jeder Knoten mit Werteingaben oder Wertausgaben mit einem dicken gelben Rahmen hervorgehoben:

![Arbeiten mit Werten](values-in-substance-compositing-graphs.resources/yellowhighlight.png "Arbeiten mit Werten")

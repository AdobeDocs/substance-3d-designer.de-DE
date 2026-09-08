---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Erfahre, wie du in Substance 3D Designer Compositing-Grafiken und MDL-Substance-Materialien für die Materialerstellung verwendest.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance-Grafiken und MDL-Materialien
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# Substance-Grafiken und MDL-Materialien

Auf dieser Seite werden die Synergien zwischen [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md) und MDL-Graphen beschrieben und es wird beschrieben, wie Texturen von Substance-Graph [Ausgaben](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) mit MDL-Graph-Eingängen verbunden werden.

## Überblick

Die Ausgaben von Substance-Graphen können *auf zwei Arten an exponierte Parameter* von MDL-Materialien übergeben werden, die auf dieser Seite beschrieben werden.

Wenn das derzeit in der 3D-Ansicht angewendete MDL-Material freigelegte Parameter mit dem Typ *[variierend](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)* enthält - dieser Typ kann mithilfe der Option <b>Typ-Modifizierer</b> in den Eigenschaften von [freigelegte Parameter](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) festgelegt werden -, können diese mit *Texturen* verbunden werden:

* Ein <b>Color</b>-Parameter kann mit RGBA-Texturen verbunden werden.
* einen <b>Float</b>-Parameter für Graustufenstrukturen

In diesen Fällen wird der einheitliche Rohwert durch einen Texturprobenehmer ersetzt, der einen unterschiedlichen Wert liefert. Diese Sampler haben ein <b>Verwendung</b>-Attribut, das im angezeigten Parameter definiert ist, und diese Verwendung ermöglicht es Designer, Texturen, die durch das Substance von Graphen ausgegeben werden, mit dem entsprechenden Parameter im MDL-Material zu verbinden, indem *Verwendungsarten zugeordnet werden*.

## Substance von Graphen in der 3D-Ansicht

Wenn Sie die Option <b>View ausgaben in 3D View</b> für ein Substance-Diagramm verwenden oder ein Substance-Diagramm aus dem Bedienfeld <b>Explorer</b> in die <b>3D View</b> ziehen, sind die Ausgaben mit den angezeigten Parametern von *übereinstimmenden Verwendungen* in dem MDL-Material verbunden, das derzeit in der 3D-angezeigt wird.

Einzelne Texturen aus einem Substance-Graphen können mit einem beliebigen MDL-Materialparameter verbunden werden, der die Texturabtastung unterstützt, unabhängig von der Kennung, indem RMB auf dem Substance-Graphknoten gedrückt und in die 3D-Ansicht gezogen wird. Es wird eine Liste der verfügbaren Samplerverwendungen angezeigt, und Sie können die Zielverwendung für die ausgewählte Textur auswählen.

![Verfügbare MDL-Diagrammeingaben](../../assets/mdl-graph-inputs-samplers.png "Verfügbare MDL-Diagrammeingaben")

*Die von einem Substance-Diagramm ausgegebenen Texturen sind mit den exponierten Parametern eines MDL-Diagramms in der 3D-Ansicht verbunden*

## Substance von Graphen in MDL-Graphen

Substance-Diagramminstanzen können direkt in MDL-platziert werden, indem sie aus dem Bedienfeld <b>Explorer</b> in das MDL-Diagramm gezogen werden. In MDL-Substance können Diagramme aus <b>Substance 3D-Dateien</b> (SBS) und <b>Substance 3D-Asset-Dateien</b> (SBSAR) verwendet werden.

+++Substance aus Substance 3D-Datei (SBS)
![Substance-Diagramm aus SBS-Datei im MDL-Diagramm](../../assets/mdl-sbs-instance-hl.png "Substance-Diagramm aus SBS-Datei im MDL-Diagramm")



*[Substance-Graph ](../../compositing-graphs/substance-compositing-graphs.md)-Instanz aus [Substance 3D-Datei ](../../getting-started/overview/overview.md) (SBS) im MDL-Graph*

+++

+++Substance-Diagramm aus Substance 3D-Element (SBSAR)
![Substance-Diagramm aus SBSAR-Datei im MDL-Diagramm](../../assets/mdl-sbsar-instance-hl.png "Substance-Diagramm aus SBSAR-Datei im MDL-Diagramm")



*[Substance Graf](../../compositing-graphs/substance-compositing-graphs.md) Instanz aus [Substance 3D Asset](../../getting-started/overview/overview.md) (SBSAR) in MDL-Diagramm*

+++

Wenn eine Substance-Grapheninstanz erstellt wird, wird sie als *Knoten* mit den folgenden Funktionen angezeigt:

* Eine *-typisierte Ausgabe*-Verbindung für jede Ausgabe des Grafen. Die Ausgabedaten werden wie folgt eingegeben:
  * RGBA-Bitmaps: Farbe (variierend)
  * Graustufen-Bitmaps: Fließkommazahl (variierend)
  * Werte: Mit Werttyp abgleichen (variierend)
* Eine *Eingabe* vom Typ &quot;UV-Koordinaten&quot;, um die UV-Koordinaten anzugeben, die zum Zuordnen der vom Substance-Graf ausgegebenen Texturen verwendet werden sollen. Wenn keine Verbindung besteht, ist der Standardwert ein klassischer linearer Verlauf von 0-1 in X und Y im UV-Raum.
* Der Graf ist *mit* gekennzeichnet, und zwar nach der Substance-Knotenbeschriftung - oder der Identifizierung, wenn keine Beschriftung definiert ist - und der ersten Bitmapausgabe als Miniaturansicht.

Mit den Knoteneigenschaften können Sie *alle dynamischen Eigenschaften* des Substance-Grafen ändern:

* Ausgabegröße
* Zufalls-Startwert
* Eingabeparameter
* …

Mit den Knoteneigenschaften können Sie auch Parameter festlegen, die festlegen, wie Texturen im MDL-Material *zugeordnet* werden:

* Kacheln
* Physische Größe verwenden
* Normalformat
* Tangentialraum

Der Ausgang des Substance-Grapheninstanz-Knotens kann mit jedem Knoteneingang des passenden Typs im MDL-Diagramm verbunden sein.

Beachten Sie, dass das Ändern eines Parameters im Abschnitt <b>SBSBasisparameter</b> das Neuberechnen einer oder mehrerer Substance-Graphausgaben beinhaltet, die das <b>Substance-Engine</b> verwenden und einen *Performance-Overhead* zusätzlich zu den MDL-Diagramm-Berechnungen umfassen. Erwarten Sie einen Leistungseinfluss, wenn *Sie einen Substance-Graf* ändern, der in einem MDL-Diagramm instanziiert wird, das in der 3D-Ansicht angewendet wird.

>[!WARNING]
>
> Wenn Sie einen Substance-Graf in einem MDL-Diagramm verwenden, müssen beim Exportieren des MDL-Diagramms die Substance-Graphausgaben in Bitmaps Baking geführt werden, die als Texturen exportiert werden, die mit der exportierten MDL-Datei gebündelt sind. Dies bedeutet, dass der Substance-Graf in der exportierten MDL-Datei *verloren* ist.

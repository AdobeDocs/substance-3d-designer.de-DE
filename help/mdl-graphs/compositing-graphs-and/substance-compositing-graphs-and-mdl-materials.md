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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
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

![Verfügbare MDL-Diagrammeingaben](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-01.png "Verfügbare MDL-Diagrammeingaben")

*Die von einem Substance-Diagramm ausgegebenen Texturen sind mit den exponierten Parametern eines MDL-Diagramms in der 3D-Ansicht verbunden*

## Substance von Graphen in MDL-Graphen

Substance-Diagramminstanzen können direkt in MDL-platziert werden, indem sie aus dem Bedienfeld <b>Explorer</b> in das MDL-Diagramm gezogen werden. In MDL-Substance können Diagramme aus <b>Substance 3D-Dateien</b> (SBS) und <b>Substance 3D-Asset-Dateien</b> (SBSAR) verwendet werden.

+++Substance aus Substance 3D-Datei (SBS)
![Substance-Diagramm aus SBS-Datei im MDL-Diagramm](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-02.png "Substance-Diagramm aus SBS-Datei im MDL-Diagramm")



*[Substance-Graph &#x200B;](../../compositing-graphs/substance-compositing-graphs.md)-Instanz aus [Substance 3D-Datei &#x200B;](../../getting-started/overview/overview.md) (SBS) im MDL-Graph*

+++

+++Substance-Diagramm aus Substance 3D-Element (SBSAR)
![Substance-Diagramm aus SBSAR-Datei im MDL-Diagramm](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-03.png "Substance-Diagramm aus SBSAR-Datei im MDL-Diagramm")



*[Substance Graf](../../compositing-graphs/substance-compositing-graphs.md) Instanz aus [Substance 3D Asset](../../getting-started/overview/overview.md) (SBSAR) in MDL-Diagramm*

+++

Wenn eine Substance-Grapheninstanz erstellt wird, wird sie als *Knoten* mit den folgenden Features angezeigt:

* Ein *-typisierter Ausgabe-*-Connector für jedes der Diagrammausgaben. Die Ausgabedaten werden wie folgt eingegeben:
  * RGBA-Bitmaps: Farbe (variierend)
  * Graustufen-Bitmaps: Float (variierend)
  * Werte: Mit Werttyp abgleichen (variierend)
* Eine *Eingabe* vom Typ &quot;UV-Koordinaten&quot;, um die UV-Koordinaten anzugeben, die zum Zuordnen der Texturen verwendet werden sollen, die vom Substance-Diagramm ausgegeben werden. Wenn keine Verbindung besteht, ist der Standardwert ein klassischer linearer Verlauf von 0-1 in X und Y im UV-Raum.
* Der Knoten ist *mit* gekennzeichnet, und zwar nach der Substance-Diagrammbeschriftung - oder der Kennung, wenn keine Beschriftung definiert ist - und der ersten Bitmapausgabe als Miniaturansicht.

Mit den Knoteneigenschaften können Sie *alle dynamischen Eigenschaften* des Substance-Diagramms ändern:

* Ausgabegröße
* Zufalls-Startwert
* Eingabeparameter
* …

Mit den Knoteneigenschaften können Sie auch Parameter festlegen, die angeben, wie Texturen im MDL-Material *zugeordnet* werden:

* Kacheln
* Physische Größe verwenden
* Normalformat
* Tangentialraum

Der Ausgang des Substance-Graph-Instanzknotens kann mit jedem Knoteneingang des entsprechenden Typs im MDL-Graph verbunden sein.

Beachten Sie, dass das Ändern eines beliebigen Parameters im Abschnitt <b>SBS Base Parameters</b> das erneute Berechnen eines oder mehrerer Substance-Diagrammausgaben beinhaltet, die das <b>Substance-Modul</b> verwenden und einen *Performance-Overhead* zusätzlich zu den MDL-Diagrammberechnungen beinhalten. Erwarten Sie einen Leistungseinfluss, wenn *ein Substance-Diagramm* geändert wird, das in einem MDL-Diagramm instanziiert wird, das in der 3D-angewendet wurde.

>[!WARNING]
>
> Wenn Sie ein Substance-Diagramm in einem MDL-Diagramm verwenden, müssen beim Exportieren des MDL-Diagramms die Substance-Diagrammausgaben in Bitmaps gesichert werden, die als Texturen exportiert werden, die mit der exportierten MDL--Datei gebündelt sind. Dies bedeutet, dass der Substance-Graph in der exportierten MDL-Datei *verloren* ist.

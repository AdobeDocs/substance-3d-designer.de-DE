---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/working-with-path-and-spline-tools.html"
breadcrumb-title: ''
description: Erfahre, wie du mit Pfaden und Spline-Werkzeugen prozedurale Muster und organische Formen in Grafen erstellst.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Working with Path  Spline tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arbeiten mit Pfad-Spline-Werkzeugen
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---


# Arbeiten mit Pfaden und Spline-Werkzeugen

Die Werkzeuggruppe &quot;Pfad und Splines&quot; umfasst eine Knotensammlung, mit der Sie Formen und Kurven mit unterschiedlichen Auflösungen erstellen und bearbeiten können, die zum Zeichnen, Zuordnen und Streuungen von Bildern verwendet werden.

## Überblick

### Was sind Pfade und Splines?

<b>Pfade</b> sind eine Reihe von Punkten, die in gerade Linien verbunden sind.

<b>Splines</b> sind glatte Kurven, deren Trajektorien durch Kontrollpunkte und die Tangenten dieser Punkte geformt werden.\
Jeder Punkt steuert auch die Height- und Thickness-Attribute eines Splines, die zum Steuern der Zuordnung, Verkrümmung und Streuung von Bildern verwendet werden.

Jede kann geschlossene oder offene Formen erstellen.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Knotenausgabe

Die Knoten geben Bilder aus, die <b> codierte Daten </b> enthalten, die Pfade und Splines darstellen.

Das Bild auf der rechten Seite stellt den Bildausgang beispielsweise durch einen Knoten vom Typ [Pfade Polygon](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) dar.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Ausgabe von Pfaden-Polygonen](working-with-path-and-spline-tools.resources/PathsPolygon_Data.jpg "Ausgabe von Pfaden-Polygonen")

</td>
</tr>
</table>

Daher sind die von ihnen erstellten Bilder nicht direkt als Grafikelement verwendbar. Sie müssen von anderen Nodes in der Toolset verarbeitet werden, die sie in ein grafisches Ergebnis konvertieren können, das dann mit den anderen Nodes verwendet werden kann, die für Substance-Graf verfügbar sind.

Während Sie mit Pfaden und Splines arbeiten, können Sie diese Objekte, die einem Bild zugeordnet sind, in der Vorschau anzeigen, indem Sie den dedizierten Knoten [Pfadevorschau](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) für Pfade und die dedizierte Ausgabe <b>Vorschau</b> für Splines verwenden.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Wechselwirkung zwischen 2D-Ansichten

Eine beträchtliche Anzahl von Knoten in der Toolset bietet die Möglichkeit, Änderungen direkt in der [2D-Ansicht](../../../../../interface/2d-view/2d-view.md) mithilfe von Kontroll-Gizmos durchzuführen. Diese Gizmos enthalten das Positions-Gizmo und die Transformationsmatrix.

Beispielsweise können Sie mithilfe von Spline-Generierungsknoten wie [Spline (Cubic)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) oder [Spline (Poly Quadratic)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) die Kontrollpunkte der Splines verschieben. Für Pfade hat [Quad Transformieren on Path](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md) ähnliche Steuerelemente, wenn es ausgewählt ist.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Spline Cubic in 2D-Ansicht](working-with-path-and-spline-tools.resources/SplineCubic-Demo.gif "Spline Cubic in 2D-Ansicht")

</td>
</tr>
</table>

### Leistung

Pfad und Spline-Werkzeuge erfordern umfangreiche Berechnungen, sodass Sie einige Einstellungen beachten sollten, um die beste Performance und Reaktionsfähigkeit bei der Arbeit mit den Tools sicherzustellen:

1. Das Toolset verwendet <b>Substance Engine</b>-Funktionen, die auf der GPU viel schneller ausgeführt werden, umfassend. Verwenden Sie daher bitte die GPU-Version des Engine für Ihr System: <b>Direct3D</b> (Windows) oder <b>OpenGL</b> (macOS).\
   Sie können das Engine wechseln, indem Sie die Taste <b>F9</b> drücken, oder indem Sie zu <b>Extras > Engine wechseln gehen...</b> in der Hauptmenüleiste.
1. Anschließend wird dringend empfohlen, die <b>Kontextabhängige Bearbeitung</b> im Abschnitt <b>Graf</b> der [Voreinstellungen](../../../../../interface/preferences-window/preferences-window.md) zu deaktivieren (navigieren Sie zu <b>Bearbeiten > Voreinstellungen...).</b> in der Hauptmenüleiste, um auf dieses Fenster zuzugreifen).\
   Bei der kontextbezogenen Bearbeitung können Sie Instanzknoten im Kontext des Host-Grafen öffnen, was zwar sehr praktisch ist, aber den Nebeneffekt hat, dass die Berechnungen, die für den Bildcache der Toolset erforderlich sind, exponentiell erhöht werden.

Wenn Sie eine dieser beiden Einstellungen in den empfohlenen Zustand ändern, sollten Sie eine deutliche Leistungsverbesserung bemerken.

![Pfadwerkzeuge in Bibliothek](working-with-path-and-spline-tools.resources/PathsTools.jpg "Pfadwerkzeuge in Bibliothek")

## Pfadwerkzeuge

### Generieren von Pfaden

Das [Pfade-Polygon](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) generiert einen Pfad in Form eines Polygons mit dem angegebenen Radius und der angegebenen Seitenanzahl.

Alternativ können Pfade aus einem Graustufenbild mithilfe des Knotens &quot;[Mask to Paths](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)&quot; extrahiert werden.\
Dies ist derzeit die einzige Möglichkeit, komplexe Formen zu erstellen. Sie können die gesamte Library von [Substance Graf Nodes](../../../../../compositing-graphs/nodes-reference-for-com/nodes-reference-for-substance-compositing-graphs.md) nutzen, um die Formen zu erstellen, die schließlich in Pfade konvertiert werden.

![Knoten zur Pfaderzeugung](working-with-path-and-spline-tools.resources/Paths_Generation.jpg "Knoten zur Pfaderzeugung"){width="600px"}

### Bearbeiten von Pfaden

Mit [Pfad 2D Transformieren](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Pfadverkrümmung](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) und [Quad Transformieren auf Pfad](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md) können Sie die Form von Pfaden bearbeiten.

Sie können unerwünschte Pfade auch entfernen, indem Sie Pfade nach Index oder Länge mithilfe des Knotens [Paths Select](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-select/paths-select.md) auswählen.

Eine komplexere Verarbeitung kann an jedem Punkt eines Pfades mithilfe des Scheitelpunkts [Paths Prozessor](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) erfolgen. Eine [einfachere Version](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md) ist für leichtere Anpassungen vorhanden.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Knoten &quot;Pfade in Vorschau anzeigen&quot;

Die Vorschau der Ergebnisse von Pfadeknoten erfolgt mithilfe des dedizierten [Pfadevorschau](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)-Knotens.\
Dieser Knoten hat keine Ausgaben. Doppelklicken Sie auf LMB auf dem Knoten, um die Vorschau in der [2D-Ansicht](../../../../../interface/2d-view/2d-view.md) anzuzeigen.

Separate Pfade haben in der Vorschau eine eindeutige Farbe, sodass sie jeden Pfad leicht voneinander unterscheiden können.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Pfadevorschau-Knoten](working-with-path-and-spline-tools.resources/PreviewPaths_Node.jpg "Pfadevorschau-Knoten")

</td>
</tr>
</table>

### Pfade zum Spline-Effekt

Sie können die gesamte für Splines mit Pfaden dedizierte Toolset nutzen, indem Sie Pfade mithilfe des Knotens [Pfade zu Spline](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) in Splines konvertieren.

Beachten Sie, dass Splines Kurven sind und daher die Schärfe von Pfaden nicht beibehalten können. Erwarten Sie eine Glättung von Formen, wenn Sie Pfade in Splines konvertieren.

Eine sehr nützliche Kombination, um das Splines-Toolset über Pfade hinweg zu nutzen, ist die folgende:

<b>Maske > Nach Pfaden maskieren > Pfade nach Spline</b>

![Pfad zu Spline](working-with-path-and-spline-tools.resources/Spline_PathToSpline.jpg "Pfad zu Spline")

### Spezifikationen für Pfadformate

Der Knoten &quot;Pfade in Vorschau anzeigen&quot; ist erforderlich, da Pfade die Daten von Pfaden ausgeben, die in einem Farbbild codiert sind.\
Diese Codierung folgt einer Spezifikation, die auf der Seite &quot;[Paths Format Specifications](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)&quot; beschrieben ist.

Sie können diese Spezifikation verwenden, um mithilfe dieses Formats eigene Knoten zu erstellen und die Knoten [Paths Vertex Processor](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) optimal zu nutzen.

![Spline-Werkzeuge in Library](working-with-path-and-spline-tools.resources/SplineTools.jpg "Spline-Werkzeuge in Library")

## Spline-Werkzeuge

### Splines generieren

Splines können mithilfe von Knoten wie [Spline Circle](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md), [Spline (Cubic)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) oder [Spline (Poly Quadratic)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) generiert werden. Mit diesen Knoten können Sie einen Spline einer beliebigen Trajektorie zeichnen, indem Sie verschiedene Steuerelemente verwenden, die vom Knoten abhängen.

Alternativ können Splines aus Pfaden mithilfe des Knotens [Pfade zu Spline](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) extrahiert werden.\
Beachten Sie, dass Splines Kurven sind und daher die Schärfe von Pfaden nicht beibehalten können. Erwarten Sie eine Glättung von Formen, wenn Sie Pfade in Splines konvertieren.

Eine sehr nützliche Kombination, um das Splines-Toolset über Pfade hinweg zu nutzen, ist die folgende:

<b>Maske > Nach Pfaden maskieren > Pfade nach Spline</b>

Splines können Ihnen auch helfen, mehr Splines zu generieren. Die [Spline Bridge (2 Splines)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) und [Spline Bridge (List)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) erzeugen beispielsweise Splines, die eine Liste von Splines in der richtigen Reihenfolge durchlaufen.

### Bearbeiten von Splines

Mit [Spline 2D Transform](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md) und [Spline Warp](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md) können Sie die Form der Splines bearbeiten.

Sie können auch unerwünschte Splines entfernen, indem Sie Pfade nach Index auswählen und Splines zuschneiden, indem Sie den Knoten [Spline Select](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md) verwenden.

Zusätzlich zu ihrer Trajektorie können die Height- und Thickness-Eigenschaften von Splines im Nachhinein mithilfe des [Spline Sample-Heights](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) und der [Spline Sample-Thickness](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md) angepasst werden.

Schließlich können mithilfe des Knotens [Spline Merge List](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) separate Splines zu einem einzigen Spline zusammengeführt werden.

### Anfügen von Splines

Beim Erstellen und Bearbeiten von Splines müssen Sie möglicherweise mehrere Splines kombinieren, um sie anzupassen oder alle gleichzeitig zu verwenden.

Beachten Sie unbedingt, dass Splines als <b>geordnete Liste</b> gespeichert und verarbeitet werden.

Das Kombinieren von Splines erfolgt mithilfe des Knotens &quot;[Spline Append](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md)&quot;. Anfügen ist der Vorgang, etwas am Ende einer geordneten Entität hinzuzufügen. Tatsächlich kombiniert der Knoten zwei Splines-Listen, indem er den zweiten Satz am Ende des ersten Satzes hinzufügt.

Daher ist es sehr wichtig, die Reihenfolge zu berücksichtigen, in der Sie Splines anfügen.

Dies wirkt sich auf Knoten aus, die Splines miteinander kombinieren müssen, z. B. [Spline Bridge (List)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), [Spline Bridge Mapper](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md) und [Spline Merge List](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md).

![Anfügen von Splines mit Link-Erstellungsmodi](working-with-path-and-spline-tools.resources/LinkCreationMode_Splines.gif "Anfügen von Splines mit Link-Erstellungsmodi")

### Spline-Eingänge und -Ausgänge

Splines werden mithilfe einer Gruppe von Verbindungen von einem Knoten an einen anderen übergeben:

* <b>Spline Coords </b>*Color* Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Spline-Punkte.
* <b>Spline-Daten </b>*Farbe* Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.
* <b>Spline-Betrag </b>*Ganzzahl* Die Anzahl der Eingabe-Splines.

Jede Verbindung des Ausgangsknotens sollte mit der Verbindung des Eingangs des entsprechenden Namens im Zielknoten verbunden sein.

Um diese Verbindungen zu beschleunigen, können Sie <b>Material</b> oder <b>Kompaktes Material</b> verwenden. [Link-Erstellungsmodi](../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md). So können Sie die drei Spline-Verbindungen in einem Arbeitsgang verbinden.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Ausgabevorschau

Die meisten Knoten bieten eine <b>Vorschau</b>-Ausgabe, die die Splines in einem Bild rendert, sodass Sie eine Vorstellung von ihren Trajektorien und Eigenschaften erhalten.

Diese Vorschau kann in den Knotenparametern mithilfe der Parameter in der Gruppe <b>Vorschau</b> angepasst werden.

</td>
<td style="border: 0;" valign="top">

![Vorschauausgabe auf Spline-Knoten](working-with-path-and-spline-tools.resources/Spline_PreviewOutput.jpg "Vorschauausgabe auf Spline-Knoten")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Als Segmente rendern

Splines sind Kurven ohne inhärente Auflösung. Sie können also unbegrenzt skaliert werden. Die einzige Grenze bei der genauen Darstellung besteht in der Präzision, die zur Speicherung der Daten verwendet wird.

Um Spline als Pixel zu zeichnen, werden sie von der Werkzeuggruppe in Linien oder Segmente unterteilt, die entlang der Bahn der Splines gezeichnet werden.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Spline als Segmente gerendert](working-with-path-and-spline-tools.resources/Spline_Segments.jpg "Spline als Segmente gerendert")

</td>
</tr>
</table>

Das bedeutet, dass du vielleicht auf die Anzahl der Segmente achten musst, die zum Zeichnen eines Splines in einem Bild verwendet werden, da diese Anzahl zu niedrig ist, um glatte Kurven zu zeichnen, oder zu hoch und für die Zielauflösung zu niedrig.

Knoten, die Splines in einem Bild zeichnen, verfügen über den Parameter &quot;<b>Segments Amount</b>&quot;, mit dem Sie diese Anzahl von Segmenten steuern können. Ein höherer Wert führt zu glatteren Kurven auf Kosten der Leistung.

### Erstellen von Bildern aus Splines

Wenn Sie mit dem Erstellen und Bearbeiten von Splines fertig sind, können Sie sie verwenden, um Bilder zu erstellen, die die restlichen Substance-Graf-Knoten nutzen können.

Es gibt drei Möglichkeiten, Splines zum Generieren von Grafiken zu verwenden:

* Rendern Sie den Spline mit seiner Form und seinen Eigenschaften mit dem Knoten [Spline Render](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) oder [Spline Fill](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md).
* Ordnen Sie Bilder entlang von Splines Zuordnungsknoten zu, z. B. [Spline Mapper](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md), [Spline Bridge Mapper](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md) und [Spline Flow Mapper](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-flow-mapper/spline-flow-mapper.md);
* Streuung entlang Splines mit der [Streuung auf Spline](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md).

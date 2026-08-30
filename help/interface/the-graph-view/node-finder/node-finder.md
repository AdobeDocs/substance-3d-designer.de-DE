---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/node-finder.html"
breadcrumb-title: ''
description: Verwenden Sie den Node Finder, um schnell nach Knoten in Ihren Substance-Graphen zu suchen und diese zu finden, um eine effiziente Navigation zu gewährleisten.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node finder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Knotensucher
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 0%

---


# Knotensucher

![Knotensuchersymbolleiste](node-finder.resources/node-finder-toolbar.png "Knotensuchersymbolleiste"){zoomable="yes"}

Mit dem Node Finder-Tool können Sie eine <b>Suche nach Knoten und Variablen</b> mithilfe einer Textabfrage durchführen. Alle Knoten, die nicht mit der Abfrage übereinstimmen, sind abgeblendet, damit die Ergebnisse hervorstechen.

Die Abfrage kann mit einem dieser Kriterien übereinstimmen:

* Ein <b>Bezeichner eines Diagramms </b>, auf das von einem Instanzknoten verwiesen wird
* Ein <b>-Bezeichner eines verfügbar gemachten Parameters oder einer Variablen </b>, die in einer Knotenparameterfunktion verwendet wird.
* <b>UID</b> eines Knotens (eindeutiger Bezeichner)
* Die <b>Bezeichnung</b> eines Knotens

Die Suche kann [Grapheninstanzen](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) rekursiv durchlaufen, sodass Knoten und Variablen in [Untergraph](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) gefunden werden können. Wenn Sie sich nicht sicher sind, welchen Begriff Sie genau suchen müssen, ist eine Fuzzy-Suchoption verfügbar, mit der Sie eine Toleranz auf die Abfrage anwenden können.

## Benutzeroberfläche

Der Knotenfinder kann auf zwei Arten aufgerufen werden:

Drücken Sie in der Diagrammansicht die Tasten <b>Strg+F</b> (Windows) bzw. <b>Cmd+F</b> (macOS), um die Symbolleiste des Knotenfinders anzuzeigen und den Fokus automatisch auf das Abfragefeld festzulegen. So können Sie eine schnelle Suche durchführen.

Klicken Sie in der Diagrammansichtssymbolleiste auf die Schaltfläche &quot;<b>Knotensuche&quot; ![](node-finder.resources/graph-node-finder.png)</b>, um die Knotensuche-Symbolleiste anzuzeigen. Nach der Anzeige wird die Symbolleiste nur durch Klicken auf diese Schaltfläche geschlossen.

<b>Durchsucht die Graphen</b>. Mit anderen Worten, eine Suche bleibt aktiv, wenn Diagramme durch diese Aktionen geöffnet werden:

* Instanzknoten: Verweis im Kontext öffnen (Strg+E / Cmd+E) (*Hinweis:* Die Diagrammbearbeitung im Kontext muss unter Bearbeiten > Voreinstellungen > Diagramm aktiviert werden)
* Pixelprozessor: Bearbeitungsfunktion (Strg+E / Befehl+E)
* Value-Prozessor: Bearbeitungsfunktion (Strg+E / Befehl+E)
* FX-Map: FX-Map-Diagramm bearbeiten (Strg+E/Befehl+E)
* Knotenparameter: Funktion bearbeiten

![Knotenfinder: Durchsuchen von Graf während der Suche](node-finder.resources/node-finder-traversal.gif "Knotenfinder: Durchsuchen von Grafen während der Suche"){zoomable="yes"}

### Suchanfrage

![Knotensuche-Abfragefeld](node-finder.resources/node-finder-query-field.png "Knotensuche-Abfragefeld"){zoomable="yes"}

Die Suchbegriffe können in dieses Feld eingegeben werden und die Pfeilschaltfläche öffnet eine Liste von Abfragevorschlägen, die einige der im aktuellen Kontext verfügbaren Variablen enthalten.

Weitere Informationen zu den Abfragen, die Sie ausführen können, finden Sie unten im Abschnitt [Suchanfrage](#search-query).

### Knotenart

![Knotentyp](node-finder.resources/node-finder-node-types.png "Knotentyp"){zoomable="yes"}

Mit diesem Kombinationsfeld können Sie Suchergebnisse filtern, um nur einen bestimmten Knotentyp beizubehalten.

Beachten Sie, dass alle Instanzknoten den Typ *des Knotens* aufweisen - tatsächlich den Typ &#39;instance&#39; -, während elementare Knoten jeweils einen eigenen Typ aufweisen.

+++Knotentyplisten
Die Liste ist kontextabhängig vom aktuellen Graf-Typ.

![Knotentypen (Compositing)](node-finder.resources/node-finder-types-compositing.png "Knotentypen (Compositing)"){zoomable="yes"}



*Knotentypen für Compositing-Graf*

![Knotentypen (Funktion)](node-finder.resources/node-finder-types-function.png "Knotentypen (Funktion)"){zoomable="yes"}



*Knotentypen für Funktions-Graf*

+++

+++Suchen nach elementaren Knoten
![Knotenfinder: Suche nach Typ &quot;Ebenen&quot; (Compositing)](node-finder.resources/node-finder-compositing-levels.png "Knotenfinder: Suche nach dem Typ &quot;Ebenen&quot; (Erstellen von Kompositionen)"){zoomable="yes"}



*Suchen nach dem Knotentyp &quot;Levels&quot; in einem Substance-Graf*

+++

+++Suchen nach Instanzknoten
![Knotenfinder: Suche nach &#39;Instance&#39;-Typ (Compositing)](node-finder.resources/node-finder-compositing-instances.png "Knotenfinder: Suchen nach dem Typ &quot;Instanz&quot; (Zusammenstellung)"){zoomable="yes"}



*Es wird nach dem Knotentyp &quot;Instanz&quot; in einem Substance-Graf gesucht*

![Knotenfinder: Suche nach &#39;Instance&#39;-Typ (Funktion)](node-finder.resources/node-finder-functions-instances.png "Knotenfinder: Suche nach Typ &quot;Instanz&quot; (Funktion)"){zoomable="yes"}



*Es wird nach dem Knotentyp &quot;Instanz&quot; in einem Substance-Funktions-Graf gesucht*

+++

### Suchoptionen

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Die Schaltfläche &quot;<b>Suchoptionen&quot; &quot;![](node-finder.resources/node-finder-search-options.png)</b>&quot; öffnet eine Liste von Einstellungen für die Suche, die aktiviert und deaktiviert werden können.

Weitere Informationen zu diesen Optionen finden Sie unten im Abschnitt &quot;Suchoptionen&quot;.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Knotensuche-Suchoptionen](node-finder.resources/node-finder-search-options-open.png "Knotensuche-Suchoptionen"){zoomable="yes"}

</td>
</tr>
</table>

## Suchanfrage

Um Knoten zu finden, wird eine Textabfrage mit den unten aufgeführten Knoteneigenschaften abgeglichen.

>[!NOTE]
>
> Die Eingabe der Abfrage sollte unter Berücksichtigung der folgenden Einschränkungen erfolgen:
> 
> * Bei der Suche wird nicht zwischen Groß- und Kleinschreibung unterschieden. Beispiel: &quot;my node label&quot; und &quot;My Node Label&quot; geben die gleichen Ergebnisse zurück.
> * Leerräume vor und nach der Abfrage werden ignoriert.
> * Es können nicht mehrere Abfragen gleichzeitig im selben Diagramm ausgeführt werden. Beispielsweise entspricht &quot;Ebenen weichzeichnen&quot; nicht den Knoten &quot;Ebenen&quot; und &quot;Weichzeichnen&quot;. Ebenso werden logische Operatoren nicht unterstützt.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Instanzdiagramm-Bezeichner

[Instanzknoten](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) können mit dem <b>Bezeichner</b> der Diagramme gefunden werden, auf die sie verweisen.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Knotenfinder: Suchen nach Diagrammbezeichner](node-finder.resources/node-finder-functions-identifier.png "Knotenfinder: Suchen nach Diagrammbezeichner "){zoomable="yes"}

*Zum Vergrößern auf Bild klicken*

</td>
</tr>
</table>

+++Bezeichner im Explorer
Diagramme werden nach ihrer Kennung im Explorer aufgelistet.

![Explorer: Paketinhalt](node-finder.resources/explorer-package-simple.png "Explorer: Paketinhalt"){zoomable="yes"}



+++

+++Kennung in der QuickInfo des Instanzknotens
Die QuickInfo von Instanzknoten enthält die Kennung ihres referenzierten Diagramms.

![Diagrammbezeichner in der QuickInfo des Instanzknotens](node-finder.resources/node-finder-compositing-identifier.png "Diagrammbezeichner in der QuickInfo des Instanzknotens"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Verfügbare Parameter und Variablen

Der Bezeichner von [verfügbar gemachten Parametern &#x200B;](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) oder eine andere Variable kann direkt durchsucht werden.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Knotenfinder: Knotenvariablen](node-finder.resources/node-finder-compositing-variable.png "Knotensuche: Knotenvariablen "){zoomable="yes"}

*Zum Vergrößern auf Bild klicken*

</td>
</tr>
</table>

+++Abfragevorschläge
Das Abfragefeld kann erweitert werden, um eine Liste mit Vorschlägen anzuzeigen.

Dazu gehören [integrierte Variablen](../../../function-graphs/variables/system-variables/system-variables.md), die für den aktuellen Diagrammtyp verfügbar sind, sowie die Bezeichner der exponierten Parameter des Diagramms.

![Vorschläge für Knotenfinder-Abfrage](node-finder.resources/node-finder-available-query-suggestions.png "Vorschläge für Knotenfinder-Abfrage"){zoomable="yes"}



Der Bezeichner der angezeigten Parameter kann auch direkt in die [Substance-Diagrammeigenschaften](../../../compositing-graphs/graph-parameters/graph-parameters.md) kopiert oder bearbeitet werden.

![Knotenfinder: verfügbar gemachte Parameter](node-finder.resources/node-finder-compositing-exposed-parameter.png "Knotenfinder: verfügbar gemachte Parameter"){zoomable="yes"}



*Zum Vergrößern auf Bild klicken*

+++

+++Suchen einer Variablen aus einer Konsolenwarnung/einem Konsolenfehler
Wenn ein Diagramm Fehler oder Warnungen enthält, die von einer <b>Variablen</b> ausgelöst wurden, die von einem Knoten verwendet wird, navigieren Sie zu <b>Windows > Console</b>, um die vollständige Fehler-/Warnmeldung anzuzeigen, die die Variable enthält. Anschließend können Sie diese Variable kopieren und in das Abfragefeld &quot;Knotensuche&quot; einfügen, um den Knoten zu finden, der das Problem verursacht.

Variablen können auch mit einem beliebigen Texteditor direkt aus den XML-Daten in der SBS-Datei kopiert werden.

![Knotenfinder: Suchvariable aus Konsolenwarnung/Fehler](node-finder.resources/node-finder-console-identifier.png "Knotenfinder: Suchvariable aus Konsolenwarnung/Konsolenfehler"){zoomable="yes"}



+++

+++Knoten abrufen/festlegen
Beim Durchsuchen einer Variablen in einem Diagramm - einschließlich der angezeigten Parameter - werden alle Knoten hervorgehoben, bei denen ein [Get](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)- oder [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)-Knoten diese Variable in einer der Parameterfunktionen des Knotens verwendet.

![Knotenfinder: Die Suche nach einer Variablen entspricht Get-Knoten, die sie verwenden](node-finder.resources/node-finder-exposed-parameter-01.gif "Node Finder: Das Durchsuchen einer Variable entspricht Get-Knoten, die sie verwenden"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Knoten-UID

Jeder Knoten in einem Diagramm hat eine eindeutige Identifizierungsnummer (UID), mit der nach diesem Knoten gesucht werden kann.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Knotenfinder: Suche nach UID](node-finder.resources/node-finder-compositing-uid-search.png "Knotenfinder: Suche nach UID"){zoomable="yes"}

*Zum Vergrößern auf Bild klicken*

</td>
</tr>
</table>

+++UID eines Knotens kopieren
Die UID eines Knotens kann über das Kontextmenü in die Zwischenablage kopiert werden.

Die Aktion kopiert die UID in diesem Format:

uid=1234567890

![Knotenfinder: Knoten-UID-Aktion kopieren](node-finder.resources/node-finder-compositing-uid-copy.png "Knotenfinder: Knoten-UID-Aktion kopieren"){zoomable="yes"}



+++

+++Durchsuchen einer Knoten-UID aus einer Konsolenwarnung/einem Konsolenfehler
Wenn ein Diagramm Fehler oder Warnungen enthält, die von einem Knoten ausgelöst wurden, rufen Sie Windows > Konsole auf, um die vollständige Fehler-/Warnmeldung anzuzeigen, die die <b>UID</b> des Knotens enthält. Anschließend können Sie diese UID kopieren und in das Abfragefeld &quot;Knotensuche&quot; einfügen, um den Knoten zu finden, der das Problem verursacht.

Knoten-UIDs können auch mit einem beliebigen Texteditor direkt aus den XML-Daten in der SBS-Datei kopiert werden.

![Knotenfinder: Knoten-UID wird über die Console gesucht](node-finder.resources/node-finder-console-uid.png "Knoten-Finder: Die Knoten-UID aus der Konsole wird gesucht"){zoomable="yes"}



+++

### Knotenbezeichnung

Knoten können auch mit ihren Beschriftungen gefunden werden.

Die Suche nach bestimmten Knoten ist besonders effektiv, wenn die exakte Bezeichnung mit deaktivierter Fuzzy-Suche verwendet wird.

## Suchoptionen

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Mit der <b>Schaltfläche für Suchoptionen ![](node-finder.resources/node-finder-search-options.png)</b> können Sie die <b>rekursiven</b>- und <b>Fuzzy</b>-Modi für die Suche nach Knoten umschalten.

Beide können gleichzeitig aktiviert werden.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Knotensuche-Suchoptionen](node-finder.resources/node-finder-search-options-open.png "Knotensuche-Suchoptionen"){zoomable="yes"}

</td>
</tr>
</table>

### Rekursiver Modus

Aktivieren Sie diese Option, damit Suchvorgänge [Grapheninstanzen](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) durchlaufen, um Ergebnisse von [Untergraphen](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) einzuschließen.

Diese Option kann bei der Fehlerbehebung in Diagrammen wesentlich sein, wenn Sie einen Knoten anhand seiner UID suchen müssen, die durch eine Warnung oder Fehlermeldung in der Konsole erworben wurde.

![Knotenfinder: rekursive Suche](node-finder.resources/node-finder-recursion-01.png "Knotensuche: rekursive Suche"){zoomable="yes"}

*In der Abfrage auf der rechten Seite wird der unten stehende Instanzknoten hervorgehoben, da sein referenziertes Diagramm auf der linken Seite Übereinstimmungen mit dieser Abfrage aufweist*

+++Beispiel 1
![Knotenfinder: rekursives Suchbeispiel 1](node-finder.resources/node-finder-recursion-01.gif "Knotenfinder: rekursives Suchbeispiel 1"){zoomable="yes"}



Ein Instanzknoten verweist auf ein Diagramm, in dem mehrere Knoten mit der Abfrage übereinstimmen.

+++

+++Beispiel 2
![Knotenfinder: rekursives Suchbeispiel 2](node-finder.resources/node-finder-recursion-02.gif "Knotenfinder: rekursives Suchbeispiel 2"){zoomable="yes"}



Wenn Sie die Option &quot;Rekursive Suche&quot; aktivieren, wird der Instanzknoten hervorgehoben, der auf ein Diagramm verweist, in dem ein Pixelprozessorknoten eine Variable verwendet, die der Abfrage entspricht.

+++

### Unscharfer Modus

Wenn Sie sich bei der genauen Schreibweise einer Abfrage nicht sicher sind, aktiviert diese Option eine <b>Toleranz</b> in den Ergebnissen.

Beachten Sie, dass die Verwendung dieser Option wahrscheinlich zu unerwünschten Übereinstimmungen führt.

![Knotenfinder: Unscharfer Modus](node-finder.resources/node-finder-functions-fuzzy.png "Knotenfinder: Unscharfer Modus"){zoomable="yes"}

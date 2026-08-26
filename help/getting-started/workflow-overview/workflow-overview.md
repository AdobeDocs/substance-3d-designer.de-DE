---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ''
description: Lernen Sie den grundlegenden Workflow zur Erstellung von Verfahrensmaterialien in Substance 3D Designer kennen.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Workflow-Übersicht
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 0%

---


# Workflow-Übersicht

Substance 3D Designer ist ein knotenbasierter Editor. Das bedeutet, dass fast jeder Projekt- oder Ressourcentyp Knoten (Bausteine) platziert und diese verbindet, um eine Kette von Vorgängen (einen Graph) zu erstellen. Auf dieser Seite wird das Konzept der knotenbasierten Workflows erläutert und eine Zusammenfassung der drei Haupttypen von Diagrammen bereitgestellt, die Sie in Designer erstellen können.

## Inhaltsverzeichnis

[Knotenbasierter Arbeitsablauf](#node-workflow)

[Arbeitsablauf für Grafikinstanzen](#instance-workflow)

[Benutzerdefinierte Parameter](#custom-parameters)

[Diagrammtypen](#graph-types)

![Datenfluss vereinfacht](../../assets/graph-direction.png "Datenfluss vereinfacht")

## Knotenbasierter Arbeitsablauf

Das Arbeiten in Designer unterscheidet sich von anderen 2D-Bildbearbeitungsprogrammen wie Photoshop. Anstatt eine Aktion manuell auszuführen (z. B. das Anpassen der Sättigung, indem Sie zu einer Menüoption wechseln und einen Schieberegler ändern), <b>konstruieren Sie die logischen Schritte</b> zum Bearbeiten oder Erstellen Ihres Bildes. Dies geschieht durch den Aufbau eines Netzwerks von kleinen Bausteinen, die &quot;Nodes&quot; genannt werden. Bilddaten werden von <b> links nach rechts</b> durch die Bausteine geleitet, die durch Verknüpfungen verbunden sind, die den Pfad der Informationen bestimmen. Jeder Knoten trägt, wenn er verbunden ist, zu den Endergebnissen bei.

Der Hauptvorteil besteht darin, dass Ihr Arbeitsablauf <b>nicht linear</b> wird. Im Gegensatz zu Aktionen, die manuell in einem Verlaufsstapel ausgeführt werden, können Sie einen Knoten jederzeit austauschen oder ändern. Wenn du feststellst, dass deine allererste Anpassung des Kontrasts, die das Ergebnis deines Bildes bis zum Ende beeinflusst, zu viel war, kannst du immer noch zurückgehen und sie anpassen oder sogar ganz ausschneiden, ohne die gesamte Arbeit zu verlieren, die du danach ausgeführt hast.

![Graph-Instanzen vereinfacht](../../assets/sub-graph.png "Graph-Instanzen vereinfacht")

## Arbeitsablauf für Grafikinstanzen

Das Instanziieren von Diagrammen ist ein wichtiger Prozess in Designer. Damit können Sie Ihre eigenen Knoten erstellen, indem Sie jede beliebige Größe oder jeden Diagrammtyp verwenden und diesen als neuen Knoten-Baustein verpacken. Diese Arten von Knoten werden als &quot;Graph-Instanzen&quot; bezeichnet. Dadurch können Sie viel effizienter sein, Zeit sparen und die Arbeit mit anderen teilen. Haben Sie zum Beispiel eine tolle Technik für Kantenverschleiß entwickelt? Erstelle eine Graph-Instanz daraus, und verwende sie selbst wieder, teile sie mit der Community oder deinem Team!

Weitere Informationen zu Graph-Instanzen in [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md) finden Sie in der Dokumentation in einem [dedizierten Abschnitt](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) darüber.

![Graph-Parameter vereinfacht](../../assets/parameters-5.png "Graph-Parameter vereinfacht")

## Benutzerdefinierte Parameter

Jeder Knoten in der Kette von Vorgängen hat irgendeine Form der Steuerung: -Schaltflächen, Schiebereglern und Einstellungen anpassen, die das Endergebnis beeinflussen. Wenn du ein Sub-Graph erstellst oder deine Substance-Datei in eine andere Anwendung exportieren möchtest, kannst du ein eigenes &quot;Control Panel&quot; für deine Dateien erstellen. Jeder, der das Graph verwendet, kann es mit einem völlig einzigartigen Control Panel optimieren und verändern, was unendliche Möglichkeiten bietet. [Informieren Sie sich hier über das allgemeine Konzept benutzerdefinierter Parameter](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md), oder gehen Sie in der Tiefe weiter, und [beginnen Sie mit dem Verfügbarmachen von Parametern](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

## Diagrammtypen

Im Folgenden finden Sie eine Zusammenfassung der drei Diagrammtypen, die Sie in Substance 3D Designer bearbeiten können, sowie einen Link zum entsprechenden Abschnitt in der Dokumentation.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance-Graphen

[Substance-Diagramme](https://substance3d.adobe.com/) sind der Haupttyp des in Substance 3D Designer erstellten Diagramms. Ihr Zweck ist es, <b>2D-Bilddaten</b> zu generieren und zu verarbeiten, die nicht auf eine festgelegte Auflösung, Farbe oder Form beschränkt sind. Sie sind als äußerst vielseitige Bildverarbeitungs- und Generierungswerkzeuge gedacht und nicht nur als statische, voreingestellte Ergebnisse.

Die Ergebnisse können in Form eines einfachen Schwarz-Weiß-Musters vorliegen, eines Filters, der nur auf anderen Bildern ausgeführt wird und keinen Inhalt für sich selbst generiert, oder sogar in Form eines vollwertigen prozeduralen Materials mit mehreren Kanälen.

Substance-Graphen sind [&#x200B; der am weitesten unterstützte Diagrammtyp &#x200B;](../../getting-started/overview/overview.md) und können exportiert und in einer Vielzahl von verschiedenen Workflows verwendet werden.

</td>
</tr>
</table>

#### Beispiele

Im Folgenden finden Sie einige typische Beispiele für häufige Anwendungsfälle.

+++Einfache Form
![Einfache Form im Substance-Diagramm](../../assets/simpleshape.png "Einfache Form im Substance-Diagramm"){width="512px"}



Eine einfache Maskenform für einen Aufkleber wird erstellt, indem [ein Textstück](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) und ein [Datenträgerform](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md) generiert werden, [die Kante](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) von der Festplatte extrahiert wird und diese schließlich [zusammengemischt werden](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), bevor sie als endgültige [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt werden.

Der Text mit der Nummer oder die Thickness der Kante kann extern belichtet werden, um das Diagramm dynamischer zu gestalten.

+++

+++Einstellungsfilter
![Korrekturfilter im Substance-Diagramm](../../assets/simplefilter.png "Korrekturfilter im Substance-Diagramm"){width="512px"}



Ein Filterdiagramm nimmt eine normale Karte als [Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) (mit einer benutzerdefinierten Vorschau), [konvertiert sie in Krümmung](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) und [passt den Kontrast](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) an, um eine Maske mit konvexen Kanten als endgültige [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) zu erstellen.

Die im Histogramm eingestellten Kontrastwerte können belichtet werden, was dies zu einem einfachen, aber nützlichen Filter in Kombination mit dem dynamischen Eingangs-Slot macht.

+++

+++Vollständiges Material
![Vollständiges Material im Substance-Diagramm](../../assets/simplematerial.png "Vollständiges Material im Substance-Diagramm"){width="512px"}



Ein komplizierteres Diagramm[fügt zwei Basismaterialien zusammen](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Eins[Basismaterial](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) ist einfach gehalten, das andere verwendet einige benutzerdefinierte Eingaben, um Interesse hinzuzufügen. Eine Maske wird verwendet, um zu bestimmen, welches der beiden Materialien an welcher Stelle angezeigt wird, bevor es als endgültige [Ausgaben](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt wird.

In diesem Beispiel werden [Verknüpfungserstellungsmodi](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) zur Vereinfachung der Verwendung mehrerer Verknüpfungen verwendet.

+++

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance-Funktionsdiagramme

Funktionen <b>verarbeiten einzelne Werte </b> (Ganzzahlen, Gleitkommawerte, Vektoren) anstelle von Bilddaten (ganze Pixelsätze). Funktionen sind auch Diagramme mit Knotennetzwerken, aber die [Nodes verwendet](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) und die Schnittstelle unterscheidet sich von [normalen Substance-Diagrammen](../../compositing-graphs/substance-compositing-graphs.md). Der Workflow basiert vollständig auf <b>mathematischen Vorgängen</b> und zeigt keine Bildvorschau-Miniaturansichten an. Dadurch wird die <b>Arbeit mit Substance 3D Designer </b> um einiges weiter entwickelt.

Funktionen können in vielen verschiedenen Kontexten verwendet werden, wobei die Hauptfunktionen darin bestehen, das Verhalten von [einem verfügbar gemachten Parameter](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) zu ändern, das Verhalten von [Pixelprozessoren](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) oder [FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) zu verfassen und [Werte](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md) in einem Substance-Diagramm zu verwenden.

</td>
</tr>
</table>

#### Beispiele

Im Folgenden finden Sie einige Beispiele aus gängigen Anwendungsfällen für Substance-Funktionsdiagramme.

+++Einfache Funktion
![Einfaches Funktionsdiagramm](../../assets/lerpfunction.png "Einfaches Funktionsdiagramm"){width="256px"}



Eine einfache Funktion im Kontext eines exponierten Parameters. Es erhält einen Eingangs-Gleitkommawert namens &quot;Intensität&quot;, der von 0 bis 1 geht (ein Bereich, der leicht zu verstehen ist) und weist ihn einem festgelegten Bereich von 0,1 bis 0,8 neu zu. Wenn der Benutzer die Intensität auf 0 setzt, wird intern 0,1 verwendet, wenn die Benutzeroberfläche auf 1 gesetzt ist, 0,8 wird verwendet und jeder Wert dazwischen wird linear interpoliert. Dieser Funktionstyp wird häufig verwendet, wenn [&#x200B; Parameter &#x200B;](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verfügbar macht, aber benutzerdefinierte Funktionen verwendet werden.

Diese Funktion könnte auch als *lerp(0.1, 0.8, Intensity)* in einem Pseudocode ähnlich wie HLSL oder GLSL geschrieben werden.

+++

+++Erweiterte Funktion
![Erweiterte Funktion](../../assets/pixel-function.png "Erweiterte Funktion"){width="512px"}



Diese erweiterte Funktion zeigt die inneren Funktionen eines [Pixelprozessors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), der zum Anpassen des Farbtons einer Farbmapeingabe basierend auf der Intensität einer zweiten Graustufenmaskeneingabe vorgesehen ist.

Es erfasst beide Eingaben mit der Variablen &quot;$pos&quot; des Systems, entfernt dann das Alpha, konvertiert den Farbwert in HSL und ändert die Farbtonkomponente, indem es mit dem aufgenommenen Graustufenwert multipliziert wird. Anschließend wird der Vektor neu zusammengestellt, der HSL-Farbton wird wieder in RGB konvertiert und das Alpha für die endgültige Ausgabe wieder hinzugefügt.

im Pseudo-Code wäre dies eine viel kompliziertere Funktion, die nicht auf eine einzelne Zeile passen würde.



+++

### MDL-Grafiken

Auf dieser Seite werden MDL-Diagramme in Substance 3D Designer angezeigt, mit denen Sie MDL-Materialien erstellen und in Echtzeit eine Vorschau ihres Verhaltens anzeigen können.

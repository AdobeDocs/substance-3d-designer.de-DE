---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ""
description: Lernen Sie den grundlegenden Workflow zur Erstellung von Verfahrensmaterialien in Substance 3D Designer kennen.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Workflow-Übersicht
user-guide-description: ""
user-guide-title: ""
source-git-commit: 21ee545724852c876444dcf3ed4a82af8d1e3715
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---

# Workflow-Übersicht

Substance 3D Designer ist ein knotenbasierter Editor. Das bedeutet, dass für fast jede Art von Projekt oder Ressource Knoten (Bausteine) platziert und verbunden werden, um eine Kette von Vorgängen (einen Graf) zu erstellen.\
Auf dieser Seite wird das Konzept knotenbasierter Arbeitsabläufe erläutert und eine Zusammenfassung der drei Haupttypen von Graf bereitgestellt, die Sie in Designer erstellen können.

![Datenfluss vereinfacht](workflow-overview.resources/graph-direction.png "Datenfluss vereinfacht"){zoomable="yes"}

## Knotenbasierter Arbeitsablauf

Das Arbeiten in Designer unterscheidet sich von anderen 2D-Bildbearbeitungsprogrammen wie Photoshop. Anstatt eine Aktion manuell auszuführen (z. B. die Sättigung anzupassen, indem Sie zu einer Menüoption wechseln und einen Schieberegler ändern), erstellen Sie das Bild in logischen Schritten. Dies geschieht durch den Aufbau eines Netzwerks von kleinen Bausteinen, die &quot;Nodes&quot; genannt werden. Bilddaten werden von <b> links nach rechts</b> durch die Bausteine geleitet, die durch Verknüpfungen verbunden sind, die den Pfad der Informationen bestimmen. Jeder Knoten trägt, wenn er verbunden ist, zu den Endergebnissen bei.

Der Hauptvorteil besteht darin, dass Ihr Arbeitsablauf **nicht linear** wird: Im Gegensatz zu Aktionen, die manuell ausgeführt werden und in einen Verlaufsknoten gehen, können Sie einen Stapel jederzeit austauschen oder ändern.
Wenn du feststellst, dass deine allererste Anpassung des Kontrasts, die das Endergebnis beeinflusst hat, zu intensiv war, kannst du immer noch zurückgehen und sie anpassen oder sogar ganz ausschneiden, ohne all die Arbeit zu verlieren, die du hinterher geleistet hast.

![Graph-Instanzen vereinfacht](workflow-overview.resources/sub-graph.png "Graph-Instanzen vereinfacht")

## Arbeitsablauf für Grafikinstanzen

Das Instanziieren von Grafen ist ein wichtiger Prozess in Designer. Sie können eigene Graf erstellen, indem Sie einen Knoten oder einen Teil eines Grafen als wiederverwendbaren Knoten verpacken. Diese werden [Instanzknoten](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) genannt und ermöglichen es Ihnen, effizienter zu arbeiten, indem Sie Graf wiederverwenden.\
Beispiel: Haben Sie eine tolle Technik für Kantenverschleiß entwickelt? Teilen Sie diesen in einen separaten Graf auf und verwenden Sie ihn in anderen Projekten wieder!

Weitere Informationen zu Grapheninstanzen finden Sie in einem [dedizierten Abschnitt &#x200B;](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) über ihre Verwendung in [Substance-Grafen](../../compositing-graphs/substance-compositing-graphs.md).

![Vereinfachte Graf-Parameter](workflow-overview.resources/parameters-5.png "Vereinfachte Graf-Parameter"){zoomable="yes"}

## Benutzerdefinierte Parameter

Jeder Knoten in der Kette von Vorgängen hat irgendeine Form von Steuerelementen: -Schaltflächen, Schiebereglern und Einstellungen, mit denen Sie das Endergebnis optimieren können.\
Wenn Sie einen Untergraph erstellen oder Ihre Substance-Datei in eine andere Anwendung exportieren möchten, können Sie ein eigenes &quot;Steuerungsfenster&quot; für Ihre Graf erstellen, damit andere Benutzer sie mit einem völlig eindeutigen Steuerungsfenster anpassen und ändern können.

Erfahren Sie hier mehr über das allgemeine Konzept der benutzerdefinierten Parameter &quot;[hier](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md)&quot;, oder gehen Sie in &quot;Tiefe&quot; vor, und [beginnen Sie mit dem leg der Parameter &quot;](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)&quot;.

## Graf

Im Folgenden finden Sie eine Zusammenfassung der drei Dokumenttypen, die Sie in Substance 3D Designer bearbeiten können, sowie einen Link zum entsprechenden Abschnitt in der Graf-Dokumentation.

<table>
<tr style="border: 0;">
<td style="border: 0;">

![](workflow-overview.resources/graph-5.png){width="120px"}

</td>
<td style="border: 0;">

### Substance-Graphen

</td>
</tr>
</table>

[Substance-Graf](https://substance3d.adobe.com/) sind der Haupttyp des in Substance 3D Designer erstellten Grafen. Ihr Zweck ist es, <b>2D-Bilddaten</b> zu generieren und zu verarbeiten, die nicht auf eine festgelegte Auflösung, Farbe oder Form beschränkt sind. Sie sind als äußerst vielseitige Bildverarbeitungs- und Generierungswerkzeuge gedacht und nicht nur als statische, voreingestellte Ergebnisse.

Die Ergebnisse können in Form eines einfachen Schwarzweißmusters, eines Filters, der nur auf anderen Bildern ausgeführt wird und keinen Inhalt für sich selbst erzeugt, oder sogar eines vollwertigen prozeduralen Materials mit mehreren Kanälen vorliegen.

Substance-Graf sind [&#x200B; der am weitesten unterstützte Graf &#x200B;](../../getting-started/overview/overview.md)-Typ und können exportiert und in einer Vielzahl von verschiedenen Workflows verwendet werden.

#### Beispiele

Im Folgenden finden Sie einige typische Anwendungsbeispiele.

+++ Einfache Form

![Einfache Form im Substance-Graf](workflow-overview.resources/simpleshape.png "Einfache Form im Substance-Graf"){width="512px" zoomable="yes"}

Eine einfache Maskenform für einen Aufkleber wird erstellt, indem [ein Textstück](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) und ein [Datenträgerform](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md) generiert werden, [die Kante](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) von der Festplatte extrahiert wird und diese schließlich [zusammengemischt werden](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), bevor sie als endgültige [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt werden.

Der Text mit der Nummer oder die Thickness der Kante kann extern gelegt werden, um den Graf dynamischer zu gestalten.

+++

+++ Einstellungsfilter

![Korrekturfilter im Substance-Graf](workflow-overview.resources/simplefilter.png "Korrekturfilter im Substance-Graf"){width="512px" zoomable="yes"}

Ein Graf nimmt eine Normalen-Map als [Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md) (mit einer benutzerdefinierten Vorschau), [konvertiert sie in Krümmung](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) und [passt den Kontrast](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) an, um eine Maske mit konvexen Kanten als endgültige [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) zu erstellen.

Die im Histogramm festgelegten Kontrastwerte können gelegt werden, sodass es sich um ein einfaches, aber brauchbares Filter in Verbindung mit dem dynamischen Eingangsschlitz handelt.

+++

+++ Material

![Vollständiges Material im Substance-Graf](workflow-overview.resources/simplematerial.png "Vollständiges Material im Substance-Graf"){width="512px" zoomable="yes"}

Ein komplizierterer Graf [&#x200B; überblendet zwei Basismaterial &#x200B;](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Ein [Basismaterial](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) ist einfach gehalten, das andere verwendet einige benutzerdefinierte Eingaben, um Interesse hinzuzufügen. Mit einer Maske wird bestimmt, welches der beiden Material an welcher Stelle angezeigt wird, bevor es als endgültige [Ausgaben](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt wird.

In diesem Beispiel werden [Verknüpfungserstellungsmodi](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) zur Vereinfachung der Verwendung mehrerer Verknüpfungen verwendet.

+++

<table>
<tr style="border: 0;">
<td style="border: 0;">

![](workflow-overview.resources/function-1.png){width="120px"}

</td>
<td style="border: 0;">

### Substance-Funktionsdiagramme

</td>
</tr>
</table>

Funktionen verarbeiten **Einzelwerte** (Ganzzahlen, Gleitkommawerte, Vektoren) und nicht Pixelsätze (Bilder). Funktionen sind auch Knotenknoten, aber die [Graf sind &#x200B;](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md), und ihre Benutzeroberfläche unterscheidet sich von Substance-Graf.

Der Arbeitsablauf basiert auf **mathematischen und logischen Vorgängen**, wodurch sie eine weitaus fortschrittlichere Arbeitsweise in Designer ermöglichen.

Funktionen können in vielen verschiedenen Kontexten verwendet werden, wobei die wichtigsten folgende sind:
* Das Verhalten von [einem freigelegte Parameter](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) wird geändert.
* Verfassen des Verhaltens von [Pixelprozessoren](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) oder [FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)
* Verwenden von [Werten](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md) anstelle von Bildern in Substance-Grafen zu bestimmten Zwecken

#### Beispiele

Im Folgenden finden Sie einige Beispiele aus gängigen Anwendungsfällen für Substance-Funktionsdiagramme.

+++ Einfache Funktion

![Einfaches Funktionsdiagramm](workflow-overview.resources/lerpfunction.png "Einfaches Funktionsdiagramm"){width="256px" zoomable="yes"}

Eine einfache Funktion im Kontext eines exponierten Parameters. Es erhält einen Eingangs-Gleitkommawert namens &quot;Intensität&quot;, der von 0 bis 1 geht (ein Bereich, der leicht zu verstehen ist) und weist ihn einem festgelegten Bereich von 0,1 bis 0,8 neu zu. Wenn der Benutzer also die Intensität auf 0 setzt, wird intern 0,1 verwendet, wenn die Benutzeroberfläche auf 1 gesetzt ist, wird 0,8 verwendet und jeder Wert dazwischen wird linear interpoliert. Dieser Funktionstyp wird häufig verwendet, wenn [&#x200B; Parameter &#x200B;](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verfügbar macht, aber benutzerdefinierte Funktionen verwendet werden.

Diese Funktion könnte auch als `lerp(0.1, 0.8, Intensity)` in einem Pseudocode ähnlich wie HLSL oder GLSL geschrieben werden.

+++

+++ Erweiterte Funktion

![Erweiterte Funktion](workflow-overview.resources/pixel-function.png "Erweiterte Funktion"){width="512px" zoomable="yes"}

Diese erweiterte Funktion zeigt die inneren Funktionen eines [Pixelprozessors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), der zum Anpassen des Farbtons einer Farbmapeingabe basierend auf der Intensität einer zweiten Graustufenmaskeneingabe vorgesehen ist.

Es erfasst beide Eingaben mit der Variablen &quot;$pos&quot; des Systems, entfernt dann das Alpha, konvertiert den Farbwert in HSL und ändert die Farbtonkomponente, indem es mit dem aufgenommenen Graustufenwert multipliziert wird. Anschließend wird der Vektor neu zusammengestellt, die HSL wieder in RGB konvertiert und das Alpha für die endgültige Ausgabe wieder hinzugefügt.

im Pseudocode wäre dies eine viel kompliziertere Funktion, die nicht auf eine einzelne Zeile passen würde.

+++

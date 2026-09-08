---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Verwendet Grapheninstanzen und Untergraphen, um wiederverwendbare Graf-Komponenten und modulare Material-Workflows zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grapheninstanzen und Untergraph
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# Grapheninstanzen und Untergraph

![](graph-instances-sub-graphs.resources/sub-graph.png)

Grapheninstanzen sind Knoten, die <b> auf einen anderen Graf </b> verweisen. Ein Graf, auf den ein Instanzknoten in einem Host-Graf verweist, kann als <b>Untergraph</b> des Host-Grafen bezeichnet werden.

Durch die Verwendung von Instanzen kann ein Graf in einem oder mehreren Grafen, auch in verschiedenen Paketen, mehrfach wiederverwendet werden.

## Warum sollte ich Grapheninstanzen verwenden?

<b>Durch das Aufteilen von Grafen in mehrere Untergraph</b> können Sie *viel* effizienter arbeiten<b>.</b>

Jedes Mal, wenn Sie eine Knotenkette in Designer duplizieren, können Sie diese Kette wahrscheinlich in einen Untergraph aufteilen, um die Wiederverwendung und Aktualisierung zu vereinfachen.

>[!NOTE]
>
> Eine Projektdatei, die eine einfache Einrichtung eines Unterfilters für einen *benutzerdefinierten*-Graf zeigt, ist im Abschnitt [Beispiel-Substance-Graf](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) dieser Dokumentation verfügbar.

### Wie erstelle ich eine Grapheninstanz?

Ziehen Sie einen Graf A vom Explorer in einen anderen Graf B, um einen <b>Instanzknoten</b> zu erstellen, der auf Graf A verweist.

Die Knoten können schnell in einen neuen Graf aufgeteilt werden, indem Sie die Knoten auswählen und im Kontextmenü &quot;Graf aus Auswahl erstellen&quot; verwenden. Sie werden dann aufgefordert, die Identifizierung des neuen Grafen festzulegen, der eindeutig sein sollte.

Beachten Sie, dass Sie, wenn die ausgewählten Graf mit anderen Knoten im Graf verbunden waren, auch [Eingangs-](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) und [Ausgangsknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) im neuen Knoten erstellen sollten, um diese Verbindungen mit dem Untergraph zu übertragen.

Außerdem sollten die Originalknoten durch einen Instanzknoten ersetzt werden, der auf den neuen Graf verweist.

Schließlich sollten Sie entscheiden, ob der Untergraph für Benutzer gelegt werden soll, wenn Sie Ihr Projekt in einer Sbsar-Datei veröffentlichen, die freigegeben werden kann. Siehe Parameter &quot;Gelegt in SBSAR&quot; in den Eigenschaften des [Grafen ](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Ein Wort zur Vererbung

Ein weiterer Vorteil bei der Verwendung von Untergraphen besteht darin, dass sich jede Instanz eines Untergraphen <b>an den Kontext </b> anpassen kann, in dem er verwendet wird. Mit anderen Worten, zwei Instanzen eines Grafen können unterschiedliche Ausgabeauflösungen, Bittiefen und Kachelungen haben.

Dies ist ein <b>grundlegendes </b>-Konzept für die Arbeit mit Grafen. Wir empfehlen Ihnen dringend, mehr über [Vererbung in Substance-Grafen](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) zu erfahren, wenn Sie bereit sind, mit Instanzen fortzufahren.

Beachten Sie, dass die Grapheninstanz- und Untergraph-Konzepte zwar auch für Substance-Grafen gelten, die auf dieser Seite erläuterte Vererbung jedoch nur für Substance-Grafen.

### Kann ich eigene Grapheninstanzen zur Knotenbibliothek hinzufügen?

<b>Ja, dies ist möglich </b>, erfordert jedoch eine bestimmte Einrichtung. Weitere Informationen finden Sie auf der Seite [Verwalten von benutzerdefiniertem Inhalt und Filtern](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dieser Dokumentation.

### Können Sie den Quell-Graf einer Grapheninstanz überprüfen?

![(tick)](graph-instances-sub-graphs.resources/check.svg) Ja, und *Nur* für Instanzen von Grafen, die aus einer **Substance 3D-Datei geladen wurden (SBS)**. Diese Instanzknoten haben eine *dunkelrote* Beschriftung.\
Klicken Sie mit der rechten Maustaste auf den Knoten, um das Kontextmenü zu öffnen, und wählen Sie die Option **Verweis öffnen** aus.

>[!NOTE]
>
> Beim Überprüfen des Quell-Grafen können Sie die Eingabedaten des Grafen der Instanz verwenden, wenn die Option **Kontextabhängige Bearbeitung** im Abschnitt **Graf** der [Voreinstellungen](../../../interface/preferences-window/preferences-window.md) *aktiviert* ist.

![(minus)](graph-instances-sub-graphs.resources/forbidden.svg) Es ist *nicht* möglich, Graf zu überprüfen, die von **Substance 3D Asset (SBSAR)**-Instanzen geladen wurden, da diese bereits kompiliert wurden. Sie dürfen das Element nur in das Bedienfeld &quot;**Explorer**&quot; laden, um die Liste der gelegt Graf und ihre Parameter zu überprüfen. Diese Instanzknoten haben eine *grüne*-Beschriftung.\
Klicken Sie mit der rechten Maustaste auf den Knoten, um das Kontextmenü zu öffnen, und wählen Sie die Option **Paket laden** aus.

>[!NOTE]
>
> **Elementare Knoten**
> 
> *Atomic*-Graf werden direkt über Code im Substance-Engine implementiert und sind *nicht*-Instanzen von Knoten, daher der Name atomic: Sie sind die *kleinsten Bausteine* für *alle* die anderen Graf in [Substance.](../../../compositing-graphs/substance-compositing-graphs.md).

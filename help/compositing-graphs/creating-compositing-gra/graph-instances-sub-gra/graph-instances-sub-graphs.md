---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Verwende Grafikinstanzen und Untergraphen, um wiederverwendbare Grafikkomponenten und modulare Material-Workflows zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diagramminstanzen und Untergraph
user-guide-description: ''
user-guide-title: ''
source-git-commit: b0053a42604f68604350a6bb3a2148970536c3c7
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---


# Diagramminstanzen und Untergraph

![](../../../assets/sub-graph.png)

Diagramminstanzen sind Knoten, die <b> auf ein anderes Diagramm </b> verweisen. Ein Diagramm, auf das von einem Instanzknoten in einem Hostdiagramm verwiesen wird, kann als <b>Untergraph</b> des Hostdiagramms bezeichnet werden.

Durch die Verwendung von Instanzen kann ein Diagramm in einem oder mehreren Diagrammen mehrfach wiederverwendet werden, selbst in verschiedenen Paketen.

## Warum sollte ich Instanzen von Diagrammen verwenden?

<b>Durch das Aufteilen von Graphen in mehrere Untergraph</b> können Sie *viel* effizienter arbeiten<b>.</b>

Jedes Mal, wenn Sie eine Knotenkette in Designer duplizieren, können Sie diese Kette wahrscheinlich in einen Untergraph aufteilen, um die Wiederverwendung und Aktualisierung zu vereinfachen.

>[!NOTE]
>
> Eine Projektdatei, die eine einfache Einrichtung eines Unterdiagramms für einen *benutzerdefinierten*-Filter zeigt, ist im Abschnitt [Beispiel-Substance-Diagramme](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) dieser Dokumentation verfügbar.

### Wie erstelle ich eine Grapheninstanz?

Ziehen Sie ein Diagramm A aus dem Explorer in ein anderes Diagramm B, um einen <b>Instanzknoten</b> zu erstellen, der auf Diagramm A verweist.

Knoten können schnell in ein neues Diagramm aufgeteilt werden, indem Sie die Knoten auswählen und die Option &quot;Diagramm aus Auswahl erstellen&quot; im Kontextmenü verwenden. Sie werden dann aufgefordert, den Bezeichner des neuen Diagramms festzulegen, der eindeutig sein sollte.

Beachten Sie, dass Sie, wenn die ausgewählten Knoten mit anderen Knoten im Diagramm verbunden waren, im neuen Diagramm auch [Eingangs-](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) und [Ausgangsknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) erstellen sollten, um diese Verbindungen mit dem Untergraph zu übertragen.

Darüber hinaus sollte das Ersetzen der ursprünglichen Knoten durch einen Instanzknoten, der auf das neue Diagramm verweist, anschließend manuell erfolgen.

Schließlich sollten Sie entscheiden, ob der Untergraph für Benutzer verfügbar gemacht werden soll, wenn Sie Ihr Projekt in einer SBSAR-Datei veröffentlichen, die freigegeben werden kann. Siehe Parameter &quot;In SBSAR verfügbar gemacht&quot; in den [Eigenschaften des Diagramms](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Ein Wort zur Vererbung

Ein weiterer Vorteil bei der Verwendung von Untergraphen besteht darin, dass sich jede Instanz eines Untergraphen <b>an den Kontext </b> anpassen kann, in dem er verwendet wird. Mit anderen Worten: Zwei Instanzen eines Graphen können unterschiedliche Ausgabeauflösungen, Bittiefen und Kachelmodi haben.

Dies ist ein <b>grundlegendes </b>-Konzept für die Arbeit mit Diagrammen. Wir empfehlen Ihnen dringend, mehr über [Vererbung in Substance-Diagrammen](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) zu erfahren, wenn Sie bereit sind, mit Instanzen fortzufahren.

Beachten Sie, dass die Graphinstanz- und Untergraph-Konzepte zwar auch für Substance-Funktionsdiagramme gelten, die Vererbung, wie auf dieser Seite erläutert, jedoch nur für Substance-Diagramme.

### Kann ich eigene Grapheninstanzen zur Knotenbibliothek hinzufügen?

<b>Ja, dies ist möglich </b>, erfordert jedoch eine bestimmte Einrichtung. Weitere Informationen finden Sie auf der Seite [Verwalten von benutzerdefiniertem Inhalt und Filtern](https://helpx.adobe.com/de/substance-3d/unlisted/documentation/sddoc/creating-library-filters-for-projects-170459772.html) dieser Dokumentation.

### Können Sie das Quelldiagramm einer Diagramminstanz überprüfen?

![(tick)](../../../assets/check.svg) Ja, und *Nur* für Instanzen von Graphen, die aus einer **Substance 3D-Datei (SBS) geladen wurden**. Diese Instanzknoten haben eine *dunkelrote* Beschriftung.\
Klicken Sie mit der rechten Maustaste auf den Knoten, um das Kontextmenü zu öffnen, und wählen Sie die Option **Verweis öffnen** aus.

>[!NOTE]
>
> Beim Überprüfen des Quelldiagramms können Sie die Eingabedaten des Diagramms der Instanz verwenden, wenn die Option **In-Context Editing** im Abschnitt **Graph** der [Voreinstellungen](../../../interface/preferences-window/preferences-window.md) *aktiviert* ist.

![(minus)](../../../assets/forbidden.svg) Es ist *nicht* möglich, Diagramme zu überprüfen, die von **Substance 3D Asset (SBSAR)**-Instanzen geladen wurden, da diese bereits kompiliert wurden. Sie dürfen das Element nur in das Bedienfeld &quot;**Explorer**&quot; laden, um die Liste der angezeigten Diagramme und ihre Parameter zu überprüfen. Diese Instanzknoten haben eine *grüne*-Beschriftung.\
Klicken Sie mit der rechten Maustaste auf den Knoten, um das Kontextmenü zu öffnen, und wählen Sie die Option **Paket laden** aus.

>[!NOTE]
>
> **Atomknoten**
> 
> *Atomic*-Knoten werden direkt über den Code im Substance-Modul implementiert und sind *nicht* Instanzen von Graphen, daher der Name atomic: Sie sind die *kleinsten Bausteine* für *alle* die anderen Knoten in [Substance-Graphen](../../../compositing-graphs/substance-compositing-graphs.md).

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Lernen Sie die wichtigsten Konzepte des Substance von Compositing-Graphen kennen, einschließlich Knoten, Verbindungen und Workflow-Grundlagen.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grundlagen zu Substance-Graphen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---


# Grundlagen zu Substance-Graphen

Auf dieser Seite werden die wichtigen Konzepte zum Arbeiten mit Substance-Graphen in Substance 3D Designer aufgeführt.

## Unterdiagramme/Veröffentlichen

[Das Veröffentlichen eines Diagramms](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) oder das Erstellen eines Unterdiagramms sind zwei sehr ähnliche, abstrakte Konzepte. Es bedeutet, dass jedes Diagramm oder Netzwerk von Knoten zusammen &quot;gepackt&quot; und in eine wiederverwendbare, eigenständige Ressource umgewandelt werden kann. Das Erstellen von [Unterdiagrammen](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) erfolgt meist innerhalb der Anwendung, um bestimmte Inhalte in einem effizienten, intelligenten Workflow wiederverwendbar zu machen, da dadurch ein Satz von Knoten nicht immer wieder dupliziert wird. Beim Veröffentlichen ist ein zusätzlicher Schritt zum Exportieren in das Substance 3D-Asset-Format (SBSAR) erforderlich, damit das Knotennetzwerkdiagramm außerhalb der Anwendung verwendet werden kann, z. B. wenn Sie Material für Unreal Engine erstellen.

Eingaben, Ausgaben und exponierte Parameter sind für dieses Konzept äußerst wichtig, da sie die einzige Möglichkeit darstellen, um mit dem Graphen zu interagieren, sobald es als Untergraph oder als veröffentlichtes Substance 3D-Element verwendet wird. Die Gründe dafür sind folgende:

* Keine Ausgaben würden bedeuten, dass Ihr Diagramm <b> nichts generiert,</b> überhaupt keine Daten.
* Keine verfügbar gemachten Parameter bedeuten, dass Ihr Diagramm <b> in keiner Weise angepasst werden kann</b>. Sie können keine Einstellungen vornehmen, wie z. B. die Intensität eines Effekts, die Deckkraft eines Bildes, das überblendet wird, die Farbe eines bestimmten Bereichs usw.
* &quot;Keine Eingaben&quot; bedeutet, dass Sie in einigen Fällen das Ergebnis eines Diagramms nicht mit <b> Ihren eigenen Bilddaten anpassen könnten</b>, z. B. mit Gittermasken, um Effekte aus einem Graphen zu generieren, mit einem Eingabebild, um eine Weichzeichnung auszuführen, oder mit einer benutzerdefinierten Maske, um bestimmte Bereiche eines Bildes zu isolieren.

## Ein- und Ausgänge

Eine [Ausgabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) ist ein Knoten, der ein einzelnes 2D-Ergebnis generiert. Es ist ein Endpunkt, ein Endpunkt für Ihr Diagramm, ein fertiges Ergebnis. Nur Daten, die mit einer Ausgabe verbunden sind, können außerhalb von Designer exportiert oder sogar in anderen Diagrammen verwendet werden.

Im Folgenden finden Sie einige Dinge, die Sie über Ausgaben wissen sollten:

* Sie können beliebig viele Ausgaben verwenden, aber Sie müssen <b>mindestens eine Ausgabe</b> haben.
* Eine Ausgabe kann <b>eine beliebige Auflösung</b> bis zu 8192px breit oder hoch sein, <b> Farbe oder Graustufen</b> sein und in jeden unterstützten Dateityp exportiert werden.
* Die Ausgaben können und sollten <b>eindeutig benannt</b> sein, um sie zu identifizieren. Dies ist beim Exportieren hilfreich.
* Jeder Connector auf der rechten Seite eines Knotens ist tatsächlich ein Output (siehe &quot;Sub-Graphen für weitere Informationen)

Eine [Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) ähnelt einer Ausgabe. Es handelt sich um einen leeren, offenen Steckplatz, mit dem Sie oder ein anderer Benutzer Ihre eigenen Daten verbinden können. Es ermöglicht die Erstellung eines Graphen, der in externen, benutzerdefinierten Bilddaten enthalten ist, z. B. ein Filter, der ein Eingabebild ändert (z. B. eine Weichzeichnungs- oder eine Kontrastkorrektur).

Im Folgenden finden Sie einige Dinge, die Sie über Eingaben wissen sollten:

* Die Eingaben sind vollständig <b>optional</b>. Sie sollten sie nur bei Bedarf hinzufügen. Es gibt keinen Mindest- oder Höchstbetrag.
* Eingaben haben eine festgelegte Auflösung (die im Allgemeinen mit dem Diagramm verknüpft ist), die Sie definieren, und es kann sich um Graustufen oder Farben handeln. Alles, was damit verbunden ist, wird entsprechend konvertiert.
* Eingaben können Bitmapdateien von Ihrer Festplatte, andere Grafiken, Ebenen von Painter oder Alchemist usw. sein.
* Jeder Connector auf der linken Seite eines Knotens ist ein Input (siehe &quot;Sub-graphs for more info)

## Vererbung

Wenn Bilder und Werte von Knoten an andere übergeben werden, werden einige *Attribute* dieser Bilder - d. h. ihre <b>Basisparameter</b> - ebenfalls *im Diagramm weitergegeben*, z. B. Auflösung, Präzision (d. h. Bittiefe), Unterteilung und Zufallswert.

Diese Weitergabe wird durch die [Vererbungsmethoden](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) definiert, die jeder Knoten für diese Attribute anwendet. Knoten können *Attribute* von anderen Knoten oder dem Diagramm erben, in dem sie vorhanden sind.\
Die Vererbungsmethoden können wie folgt lauten:

* *Relativ zu übergeordnetem Element*
* *Relativ zur Eingabe*
* *Absolut* - d. h. keine Vererbung

Die Vererbung kann abstrakt und schwierig zu verwalten sein. Daher wird dringend empfohlen, dass Sie einen Blick auf die [dedizierte Seite](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) werfen, auf der sie ausführlich erläutert wird.

## Parameter offenlegen

Das Verfügbarmachen von Parametern kann sehr ausführlich sein. Es kann aber auch so zusammengefasst werden, dass bestimmte Eigenschaften von Knoten in Ihrem Diagramm ausgewählt und ein dediziertes UI-Steuerelement für sie erstellt werden, das einfach verfügbar ist, wenn das Diagramm als Unterdiagramm verwendet oder als Archiv veröffentlicht wurde. Da Sie Knoten nicht mehr schnell oder einfach auswählen und ihre Eigenschaften optimieren können, besteht das Ziel darin, ein weiteres primäres Steuerungsfenster zu erstellen, in dem alle für dieses spezifische Diagramm relevanten Eigenschaften gruppiert werden.

Hier sind einige Dinge, die Sie über exponierte Parameter wissen sollten:

* Verfügbare Parameter &quot;<b>&quot; verschieben ein Steuerelement vom Knoten in das Diagramm &quot;</b>&quot;, im Wesentlichen eine Ebene in der Hierarchie nach oben.
* Die freigegebenen Parameter können somit nicht mehr auf dem Knoten, sondern nur noch auf dem Graphen geändert werden.
* Verfügbare Parameter können vollständig mit Namen, Beschriftungen, Werten und dem Typ des UI-Editors angepasst und sogar ausgeblendet und für bestimmte Bedingungen angezeigt werden.

Das Verfügbarmachen von Parametern ist ein abstraktes und schwieriges Konzept für Anfänger,[es gibt mehr spezielle Dokumentation zu diesem Thema](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), aber es wird empfohlen, sich mit anderen grundlegenden Aspekten der Software vertraut zu machen, bevor Sie sich mit dem Verfügbarmachen von Parametern beschäftigen.

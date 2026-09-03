---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Erfahre, wie du in Substance 3D Designer Diagramme für die Materialdefinitionssprache erstellst.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Erstellen eines MDL-Diagramms
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Erstellen eines MDL-Diagramms

Auf dieser Seite wird das Erstellen eines MDL-Diagramms zum Erstellen von MDL-Materialien in Substance 3D Designer beschrieben.

![MDL-Diagrammerstellungspfade](creating-an-mdl-graph.resources/creating-an-mdl-graph-01.png "MDL-Diagrammerstellungspfade")

*Pfade zum Erstellen eines neuen MDL-Diagramms in der Designer-Oberfläche*

## Methoden zum Erstellen eines MDL-Diagramms

Sie können ein MDL-Diagramm mit einer der folgenden Methoden erstellen:

* Wählen Sie die Option **Datei > Neu > MDL-Diagramm** in der *Hauptmenüleiste*.
* Klicken Sie auf die Schaltfläche ![](creating-an-mdl-graph.resources/creating-an-mdl-graph-02.png) **MDL-Diagramm hinzufügen** in der *Hauptsymbolleiste*.
* Klicken Sie im Bereich **Explorer** mit der rechten Maustaste auf ein *vorhandenes Paket* und wählen Sie die Option **Neu > MDL-Diagramm** aus.

Das Dialogfeld &quot;**Neues MDL-Diagramm**&quot; wird angezeigt (siehe unten).

![Neues Dialogfeld für MDL-Diagramm](creating-an-mdl-graph.resources/creating-an-mdl-graph-03.png "Neues Dialogfeld für MDL-Diagramm")

*Neues MDL-Diagramm-Dialogfeld*

## Neues MDL-Diagramm-Dialogfeld

Unabhängig von der Methode, die zum Erstellen eines neuen MDL-Diagramms verwendet wird, wird Ihnen immer das Dialogfeld <b>Neues MDL-Diagramm</b> angezeigt, mit dem Sie das neue Diagramm konfigurieren können.

### Vorlagen

Im Abschnitt <b> Vorlagen</b> können Sie eine Diagrammvorlage auswählen, die vorkonfigurierte Knoten enthält, damit Sie schneller mit dem Diagramm beginnen können. Die vorkonfigurierten Knoten umfassen Ausgabeknoten, einfache Knoten zur Übergabe von Werten an diese Ausgaben - z. B. einheitliche Farbe und Eingabeknoten, je nach Vorlage.

Wählen Sie die Vorlage <b>Leer</b> aus, um mit einem vollständig *leeren* Diagramm zu beginnen.

Mit der Option <b>Projekt</b> können Sie die Vorlagenliste nach Projektdatei filtern. Dadurch ist es leicht, die benutzerdefinierten Vorlagen in den Speicherorten zu finden, die im Abschnitt <b>Allgemein</b> der Projekteinstellungen für die Projektdatei hinzugefügt wurden.

>[!WARNING]
>
> Wenn Sie die falsche Vorlage auswählen, können Sie *nicht* zu einer anderen Vorlage wechseln, nachdem Sie das Diagramm erstellt haben.\
> Um Ihr vorhandenes Diagramm auf eine andere Vorlage zu portieren, können Sie ein neues Diagramm mit der entsprechenden Vorlage erstellen und das Diagramm kopieren und in die neue Vorlage einfügen. Stellen Sie die Knoten ggf. wieder her, einschließlich des Knotens [Root](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md).

Die Vorlagenliste kann in verschiedenen Modi mit den *Schaltflächen* neben dem Kombinationsfeld **Projekt** angezeigt werden:

* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-04.png)Anzeige zuletzt verwendet**: filtert die Liste, um die zuletzt verwendeten Vorlagen in der Reihenfolge von *zuletzt bis zuletzt* anzuzeigen, wobei das oberste Element das zuletzt verwendete ist
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-05.png)Diagramme anzeigen**: Vorlagen werden nur nach ihrer *Bezeichnung* in der Reihenfolge der [Substance 3D](https://www.adobe.com/de/products/substance3d/3d-augmented-reality.html)-Dateien im Vorlagenverzeichnis angezeigt
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-06.png)Substance 3D-Dateien anzeigen**: Vorlagen werden anhand ihrer Bezeichnung als *untergeordnete Elemente der Substance 3D-Datei, zu der sie gehören, angezeigt*. Die Reihenfolge der Dateien im Vorlagenverzeichnis ist dabei identisch.
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-07.png)Verzeichnisse anzeigen**: Vorlagen werden anhand ihrer Bezeichnung als *untergeordnete Elemente des Verzeichnisses angezeigt, zu dem sie gehören*, in der Reihenfolge der Dateien im Vorlagenverzeichnis.

### Eigenschaften

Im Abschnitt &quot;<b>Graph Properties </b>&quot; können Sie grundlegende Informationen zum neuen Diagramm einrichten. Jede dieser Einstellungen kann später jederzeit geändert werden, aber es ist sinnvoll, zunächst darauf zu achten und diese entsprechend für Ihren Anwendungsfall einzurichten.

* <b>Diagrammname</b>: den Bezeichner des Graphen. Sie muss für ein bestimmtes Paket eindeutig sein und darf keine Leerzeichen und einige Sonderzeichen enthalten.
* <b>Diagramm im Paket erstellen</b>: Mit diesem Kombinationsfeld können Sie ein *neues* Paket für das neue Diagramm erstellen oder das neue Diagramm einem *vorhandenen* Paket hinzufügen, das bereits im Explorer-Fenster geladen wurde.\
  Hinweis: Wenn der Erstellungsprozess mit der Methode <b>4</b> (siehe oben) gestartet wird, lautet dieser Parameter *preset* für das vorhandene Paket, von dem aus der Prozess gestartet wurde.
* <b>Vorlagendetails</b>: Dieser Abschnitt enthält einen kurzen Text, der die Merkmale und den Zweck der Vorlage erläutert.

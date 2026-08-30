---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie in Substance 3D Designer Graf für Material Definition Language erstellen und verwenden, um erweiterte Material-Workflows zu nutzen.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL-Grafiken
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# MDL-Grafiken

Auf dieser Seite werden MDL-Diagramme in Substance 3D Designer angezeigt, mit denen Sie MDL-Materialien erstellen und in Echtzeit eine Vorschau ihres Verhaltens anzeigen können.

![Malachite-MDL-Material](mdl-graphs.resources/mdl-malachite-example.jpg "Malachite-MDL-Material")

*Malachite mit Chrysocolla, MDL-Material von [Mark Foreman](https://www.artstation.com/oggyart)* *verfügbar auf unserer [Legacy-Substance share](https://share-legacy.substance3d.com/libraries/4043)* *Plattform*

>[!WARNING]
> 
> MDL-Diagramms und alle zugehörigen Funktionen wurden in Version 16.0.0 aus Designer entfernt.
> 
> Weitere Informationen: [MDL-Diagramm und Ende des Lebenszyklus von Iray](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++Inhaltsverzeichnis

* [Hauptkonzepte für MDL-Diagramme](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [Erstellen eines MDL-Diagramms](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDL-Bibliothek](/help/mdl-graphs/mdl-library/mdl-library.md)
* [Verfügbarmachen von Parametern in MDL-Diagrammen](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Substance-Grafiken und MDL-Materialien](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [MDL-Inhalte werden exportiert](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [Warnungen in MDL-Diagrammen](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL-Lernressourcen](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## Überblick

MDL steht für [Materialdefinitionssprache](http://www.nvidia.com/object/material-definition-language.html): &quot;eine Technologie, die von [NVIDIA](https://www.nvidia.com/) entwickelt wurde, um physikalisch basierte Materialien für physikalisch basierte Rendering-Lösungen zu definieren.&quot; (Quelle: [NVIDIA MDL-Dokumentation](https://raytracing-docs.nvidia.com/mdl/index.html))

Mit dieser Sprache ist eine vollständige Materialdefinition portabel und kann somit anwendungs- und rendererübergreifend für eine konsistente Ausgabe verwendet werden. Substance 3D Designer ist derzeit die *einzige*-Anwendung, die grafisch basiertes Knotenaustauschen von MDL-Materialien anbietet, indem die MDL-Funktionen und -Werttypen als Knoten in einem MDL-Diagramm verfügbar gemacht werden.

Beim Erstellen von Materialien können Sie den eigenen [Iray](../interface/3d-view/iray/iray.md)-Renderer von NVIDIA verwenden, der in Designer eingebettet und im Bedienfeld [3D view](../interface/3d-view/3d-view.md) verfügbar ist, um das Verhalten des Materials *interaktiv* in der Vorschau anzuzeigen.

MDL-Diagramm ergänzen [Substance-Graf](../compositing-graphs/substance-compositing-graphs.md) insofern, als letztere *Texturen* ausgeben, die vom MDL-Material *gesampelt* werden können, um dessen Verhalten und Aussehen zu beeinflussen.

Wir empfehlen, die Abschnitte dieser Dokumentation *in der Reihenfolge* für einen geführten Lernpfad zu durchlaufen, der mit den Eigenschaften einer MDL-Diagrammressource direkt unten beginnt.\
Bist du bereit reinzuspringen? Beginnen Sie mit MDL-Diagrammen im Abschnitt MDL-Lernressourcen!

>[!NOTE]
>
> Weitere Informationen über die technische Implementierung der Materialdefinitionssprache finden Sie in der [NVIDIA MDL-Dokumentation](https://raytracing-docs.nvidia.com/mdl/index.html), die Links zur MDL-Spezifikation und zum [MDL-Handbuch](http://mdlhandbook.com/) enthält, die alle von NVIDIA erstellt und gepflegt werden.

![MDL-Diagrammeigenschaften](mdl-graphs.resources/mdl-main.png "MDL-Diagrammeigenschaften")

*MDL-Diagramm-Eigenschaften im Eigenschaftenfenster*

## MDL-Diagrammeigenschaften

### Attribute

Dieser Abschnitt enthält Informationen über das MDL-Material zur Identifizierung, Klassifizierung und Feststellung der Urheberschaft.

* <b>Kennung</b>: Der Name dieser Ressource, der unter der übergeordneten Ressource im Paket eindeutig sein sollte
* <b>Anzeigename</b>: Der Name des MDL-Materials, der auf der Benutzeroberfläche angezeigt wird
* <b>Symbol</b>: Das Bild, das als Miniaturansicht für dieses Diagramm in der Designer-Bibliothek verwendet wird.
* <b>Verborgen\*</b>: Wenn auf* True* festgelegt, ist das MDL-Material nicht in einer MDL-Bibliothek sichtbar, ist aber intern weiterhin vorhanden und kann referenziert werden.
* <b>In Bibliothek anzeigen</b>: Wenn auf *True* festgelegt, wird das MDL-Diagramm in der Designer-Bibliothek angezeigt
* <b>Beschreibung</b>: Die Beschreibung des MDL-Materials, die in der QuickInfo von Instanzknoten angezeigt werden kann, die auf dieses Diagramm verweisen.
* <b>Kategorie\*</b>: Die Kategorie, zu der das MDL-Diagramm gehört - dies hat derzeit keine Auswirkungen darauf, wie das Diagramm in der [Library](../interface/the-library/the-library.md) von Designer sortiert wird.
* <b>In Gruppe\*</b>: Die Bibliotheksgruppe, zu der das MDL-Material gehört
* <b>Autor\*</b>: Der Autor des MDL-Materials
* <b>Mitwirkende\*</b>: Die Anbieter des MDL-Materials, die nicht der Autor sind
* <b>Schlüsselwörter\*</b>: Die Stichwörter, die zum Auffinden des MDL-Materials in einer Bibliothekssuche verwendet werden können
* <b>Copyright-Hinweis\*</b>: Der Copyright-Hinweis, der für die Urheberschaft und Nutzung des MDL-Materials relevant ist

Hinweis: Mit einem Sternchen (\*) markierte Eigenschaften sind MDL-Anmerkungen, die von MDL-Bibliotheksintegrationen verwendet werden sollen und* keine Auswirkungen* in Designer haben.

### Diagrammeingaben

In diesem Abschnitt werden die interaktiven Parameter aufgelistet, die mit den freigelegten Parametern des MDL-Diagramms verbunden sind, und ihre *Standardwerte* definiert. Sie können jederzeit *optimiert* und *neu angeordnet* sein.

Die Schnittstelle und das Verhalten dieser Eingaben sind durch den *Werttyp* und den *Bereich* der verfügbar gemachten Parameter definiert, mit denen sie verbunden sind. Beispiel:

* Ein exponierter Wert vom Typ &quot;<b>Float</b>&quot;, der auf einen weichen Bereich von [0,0,4,0] festgelegt ist, wird als *einzelner Schieberegler* angezeigt, der von 0,0 bis 4,0 reicht.
* Ein angezeigter Wert vom Typ <b>Color</b> wird als *Color-Widget* angezeigt, das einen Auswahlverlauf und eine Farbminiatur enthält.

Um die Diagrammeingaben neu anzuordnen, platzieren Sie den Cursor auf dem *dunklen Griff* links neben dem Parameter, klicken Sie auf *halten* <b>LMB</b> und ziehen Sie den Cursor nach oben oder unten. Diese benutzerdefinierte Reihenfolge wird verwendet, um die Eigenschaften des MDL-Materials in den folgenden Kontexten anzuzeigen:

* Instanzknoten, die auf das MDL-Diagramm für dieses Material verweisen
* Die Materialeigenschaften in der [3D-Ansicht](../interface/3d-view/3d-view.md)
* MDL-Integrationen von Drittanbietern

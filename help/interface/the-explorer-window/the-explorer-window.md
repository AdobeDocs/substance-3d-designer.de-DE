---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window.html"
breadcrumb-title: ''
description: Verwenden Sie das Explorer-Fenster in Substance 3D Designer, um Ihre Projektdateien und -ressourcen zu durchsuchen, zu organisieren und zu verwalten.
helpx_creative_field: ""
helpx_description: Designer > Interface > Explorer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Explorer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 2%

---


# Explorer

Auf dieser Seite wird das Explorer-Dock in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) beschrieben. In diesem Bedienfeld kannst du Pakete und die zugehörigen Ressourcen verwalten.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Überblick

Im Explorer-Dock verwalten Sie Ihre Dateien und Ressourcen, die derzeit in Substance 3D Designer geöffnet sind. Es wird eine Liste aller derzeit geöffneten Pakete angezeigt, wobei jedes Paket als Hierarchie erweitert wird, um [Ressourcen](../../resources/resources.md)darin anzuzeigen.

Im Explorer können Sie Ihre Projekte starten und beenden, da Sie damit jede Art von Ressource erstellen, speichern und exportieren können.

</td>
<td style="border: 0;" valign="top">

![Explorer-Dock](../../assets/explorer-3.jpg "Explorer-Dock")

</td>
</tr>
</table>

Im Explorer-Dock können Sie einige wichtige Aktionen ausführen:

* Erstellen neuer Pakete und Grafiken
* Vorhandene Pakete laden
* Speichern und Schließen von geladenen Paketen
* [Ressourcen importieren und verknüpfen](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)
* [Diagrammergebnisse in Texturen exportieren](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)
* [Erstellen eines Pakets als Substance 3D-Asset (SBSAR) in Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)
* [Senden von Paketen an andere Substance 3D-Anwendungen](send-to-interoperability/send-to-interoperability.md)
* [Karten aus einem Gitter backen](../../bakers/bakers.md)

## Obere Symbolleiste

Mit dieser Symbolleiste können Sie schnell Funktionen im Zusammenhang mit Ihrem gesamten Arbeitsablauf ausführen. Alle Schaltflächen sind *kontextabhängig*, d. h. sie aktivieren und ändern ihr Verhalten entsprechend Ihrer aktuellen Auswahl im Explorer.

![](../../assets/save.png) <b>Speichern</b> ausgewähltes Paket.

![](../../assets/sendto-icon.jpg) <b>Publish oder [senden](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)</b> ausgewählte Elemente:

* [Publish beliebiges ausgewähltes Paket zu einem Substance 3D-Asset (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md);
* Senden Sie das ausgewählte Paket an [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) oder [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html).

![](../../assets/republish.png) <b>Publish oder senden Sie wie zuvor:</b> Publish oder senden Sie die ausgewählten Elemente mit den gleichen Einstellungen wie zuvor. Diese Option ist nur für ein Paket verfügbar, das bereits *mindestens einmal* in der *aktuellen*-Sitzung veröffentlicht wurde.

![](../../assets/graph-cleaner.jpg) <b>Nicht verwendete Knoten entfernen</b> in ausgewählten Diagrammen. Das Tool befolgt die folgenden Regeln:

* Das Tool ist nur verfügbar, wenn die ausgewählten Elemente vom *gleichen Typ sind*: nur Diagramme, Ordner oder Pakete;
* Wenn die Auswahl Ordner oder Pakete enthält, bereinigt das Tool alle darin enthaltenen Diagramme *rekursiv*;
* Wenn eines der Zieldiagramme ein [Substance-Diagramm](../../compositing-graphs/substance-compositing-graphs.md) ist, ist eine zweite Option verfügbar, mit der Sie alle Parameterfunktionen auf Knoten in diesem Diagramm bereinigen können.

Erfahren Sie mehr über das Tool im Abschnitt &quot;Nicht verwendete Knoten entfernen&quot; auf der Seite [Diagrammansicht](../../interface/the-graph-view/the-graph-view.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dropdown-Menü &quot;Publish/Senden&quot;](../../assets/explorer-sendto-displayed.jpg "Dropdown-Menü &quot;Publish/Senden&quot;")

*Publish/Send*

</td>
<td style="border: 0;" valign="top">

![Dropdown-Menü für nicht verwendete Knoten entfernen](../../assets/explorer-graph-cleaner.jpg "Dropdown-Menü für nicht verwendete Knoten entfernen")

*Nicht verwendete Knoten entfernen*

</td>
</tr>
</table>

## Kontextmenüs

Der Großteil Ihrer Interaktion mit dem Explorer erfolgt über Kontextmenüs, die angezeigt werden, indem Sie in der Strukturansicht des Explorers auf ein Element im RMB-Format klicken.

Die verfügbaren Optionen hängen von den ausgewählten und angeklickten Elementen ab:

+++Leerer Bereich

Leerer Speicherplatz ist nur unter derzeit geöffneten Paketen verfügbar. Das Klicken neben vorhandenen Elementen gilt nicht als leerer Bereich.

<b>Neues Paket</b>: Erstellt ein neues leeres Paket.

<b>Paket öffnen</b>: Öffnet ein Dateidialogfeld zum Öffnen einer SBS-Datei.

+++

+++Paket

<b>Mit </b>Neu können Sie neue Diagramme ([Substance-Graph](../../compositing-graphs/substance-compositing-graphs.md), [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) und [Vektorgrafiken](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)-Ressourcen sowie *Ordner* zum Sortieren von Inhalten erstellen.

<b>Import</b> und <b>Link </b>ermöglichen das Einbringen von [Ressourcen](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

<b>Neu laden</b>, <b>Speichern, Speichern unter</b> und <b> Speichern einer Kopie als </b> ermöglicht das Speichern auf der Festplatte oder das Abrufen einer zuvor gespeicherten Version des Pakets von der Festplatte.

Mit <b>Publish .sbsar-Datei</b> und <b> .sbsar-Datei erneut veröffentlichen</b> können Sie Ihr nicht kompiliertes, nicht optimiertes Substance-Diagramm [veröffentlichen](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) in einer effizienten und portablen SBSAR-Datei für uns in anderen Substance-Anwendungen und Integrationen. Publish als &quot;Vorherige&quot; wiederholt die vorherige Publish-Aktion mit denselben Optionen und überspringt das Dialogfeld &quot;Optionen&quot;, um die Iteration zu beschleunigen. Die Symbolleiste enthält Schaltflächen mit derselben Funktionalität.

<b>Der Export mit Abhängigkeiten</b> unterscheidet sich vom Speichern und Veröffentlichen. Es nimmt Ihre SBS-Dateien, sammelt alle referenzierten Ressourcen und Abhängigkeiten und erstellt ein eigenständiges Paket. In diesem Dialogfeld können Sie auswählen, welche Bibliotheken erfasst werden sollen und ob die Datei ein komprimiertes Archiv sein soll (7-zip). Dies ist eine gute Wahl, um eine SBS-Datei mit jemand anderem zu teilen, ohne sich über fehlende Abhängigkeiten Gedanken zu machen.

<b>Senden an...</b> öffnet ein Untermenü, in dem Sie Ihr Paket direkt [senden](send-to-interoperability/send-to-interoperability.md) an [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html), [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html) oder [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

<b>Copy</b> kopiert das ausgewählte Paket.

Mit <b>Einfügen</b> werden kopierte Diagramme und/oder Ressourcen *in* das ausgewählte Paket eingefügt.

<b>Paket(e) schließen</b> schließt alle ausgewählten Pakete

<b>Ausgaben berechnen</b> erzwingt, dass Designer alle Ausgaben aller Graphen im Paket berechnet.

<b>In Explorer anzeigen...</b> öffnet den Speicherort des Pakets im Dateiexplorer Ihres Betriebssystems.

<b>Dependency Manager</b> öffnet das Fenster &quot;Dependency Manager&quot; für das ausgewählte Paket.

<b>Abhängigkeiten öffnen</b> öffnet alle Abhängigkeiten im Explorer (*[Substance nur Diagramme](../../compositing-graphs/substance-compositing-graphs.md)*).

+++

+++Substance-Graph

<b>Öffnen:</b> (Zurück) Öffnet dieses Diagramm in [der Diagrammansicht](../../interface/the-graph-view/the-graph-view.md).

<b>Kopieren:</b> *(Strg-C)* Kopiert das aktuelle Diagramm in die Zwischenablage.

<b>Entfernen:</b> (Löschen) Löscht das Diagramm aus diesem Paket.

<b>Umbenennen:</b> (F2) Benennen Sie dieses Diagramm um.

<b>Ausgaben in 3D-Ansicht anzeigen:</b> Sendet die Ausgaben dieses Diagramms an [die 3D-Ansicht](../../interface/3d-view/3d-view.md), um sie als Material anzuzeigen.

<b>Ausgaben berechnen:</b> Berechnet die Ausgaben dieses Diagramms und speichert sie im Speicher.

<b>Ausgaben exportieren...:</b> Öffnet das Dialogfeld für das [Exportieren in Bitmaps.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

+++

+++3D-Szenen

<b>Öffnen:</b> (Rückgabe) Verwendet dieses 3D-Mesh in [der 3D-Ansicht](../../interface/3d-view/3d-view.md) und ersetzt den Standardwürfel oder die Ebene.

<b>Kopieren:</b> (Strg-C) Kopiert diese Ressource in die Zwischenablage.

<b>Einfügen:</b> (Strg-V) Fügt Ressource aus Zwischenablage ein.

<b>Entfernen:</b> (Entf) Löscht die Ressource aus diesem Paket.

<b>Umbenennen:</b> (F2) Benennen Sie diese Ressource um.

<b>Erneutes Laden:</b> Erzwingen Sie das erneute Laden dieses Gitters von der Festplatte.

<b>In Explorer anzeigen:</b> Öffnen Sie ein Browserfenster für die Systemdatei am Speicherort der Ressource auf dem Datenträger.

<b>Verschieben:</b> Ändern Sie diese Ressource, um sie mit einer anderen Datei zu verknüpfen.

<b>Modellinformationen backen...:</b> Öffnet das [Dialogfeld &quot;Backen&quot;.](../../bakers/bakers.md)

+++

+++Ordner

<b>Neu:</b> Ermöglicht Ihnen, im Ordner neue Diagramme ([Substance-Diagramm](../../compositing-graphs/substance-compositing-graphs.md), [Substance-Funktionsdiagramm](../../function-graphs/function-graphs.md), [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) und [Vektorgrafiken](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) sowie *Ordner* zum Sortieren von Inhalten zu erstellen.

<b>Import</b> und <b>Link: </b>Sie können [Ressourcen](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) einbinden und in den Ordner einfügen.

<b>Kopieren:</b> (Strg-C) Kopiert den Ordner und seinen gesamten Inhalt in die Zwischenablage.

<b>Einfügen:</b> (Strg-V) Fügt den Ordner und seinen gesamten Inhalt aus der Zwischenablage ein.

<b>Umbenennen:</b> (F2) Benennen Sie diesen Ordner um.

<b>Entfernen:</b> *(Del)* Löscht den Ordner und seinen gesamten Inhalt aus dem Paket.

<b>Ausgaben berechnen:</b> Berechnet die Ausgaben aller im Ordner enthaltenen Diagramme und speichert sie im Speicher.

+++

## Untere Symbolleiste

Die Symbolleiste am unteren Rand des Explorer-Docks enthält Informationen zu einem Paket oder einer Paketressource:

<b>![](../../assets/explorer-dependencies.jpg) Abhängigkeiten:</b> Wenn ein Paket ausgewählt ist, werden seine Paketabhängigkeiten in einem dedizierten Bereich aufgelistet.

<b>![](../../assets/explorer-information.jpg)-Informationen: </b> Stellt Metadaten bereit, die sich auf das derzeit ausgewählte Paket oder die derzeit ausgewählte Ressource beziehen:

* Paket: den vollständigen Dateipfad des Pakets
* [Bitmapressource](../../resources/bitmap-resource/bitmap-resource.md): den vollständigen Dateipfad der Ressource, ihr [ICC-Profil](../../color-management/color-management.md), die Bildgröße und die [Importmethode](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) (d. h. *Verknüpft* oder *Importiert*)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Abhängigkeitsbereich](../../assets/explorer-dependencies-displayed.jpg "Abhängigkeitsbereich")

*Abhängigkeiten*

</td>
<td style="border: 0;" valign="top">

![Informationsbereich](../../assets/explorer-information-displayed.jpg "Informationsbereich")

*Informationen*

</td>
</tr>
</table>

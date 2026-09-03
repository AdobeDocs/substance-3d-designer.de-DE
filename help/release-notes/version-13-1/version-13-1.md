---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-13-1.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 13.1, um mehr über die Verbesserungen von Knotendiagrammen und die Unterstützung von AxF-Exporten zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 13.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---


# Version 13.1

<b>Substance 3D Designer 13.1</b> fügt dem Knotendiagramm viele Verbesserungen der Lebensqualität hinzu, hauptsächlich in Bezug auf Frames, um das Erlebnis bei der Materialerstellung zu verbessern. Außerdem wurde der AxF-Export hinzugefügt, der einen Interoperabilitätsarbeitsablauf für Benutzer ermöglicht, die mit dem AxF-Format arbeiten.

*Freigabedatum: 12. Dezember 2023*

![Substance 3D Designer 13.1-Banner](version-13-1.resources/version-13-1-01.png "Substance 3D Designer 13.1-Banner")

## Verbesserungen an Rahmen

Rahmen sind ein unverzichtbares Werkzeug, um das Diagramm gut organisiert und lesbar zu halten. Aus diesem Grund haben wir uns entschlossen, sie in dieser neuen Version aufzupolieren.

### Automatisch erweitern

Wenn das Diagramm wächst, muss der Inhalt der Rahmen möglicherweise neu angeordnet werden. Die Knoten können sich verschieben, um Platz für Ergänzungen zu schaffen, oder die Inhalte müssen möglicherweise weiter voneinander entfernt werden, um die Lesbarkeit zu verbessern. Um diese Anpassungen zu erleichtern, ist es jetzt möglich, einen Frame automatisch zu erweitern, wenn eingeschlossene Objekte verschoben werden: Halten Sie <b>Umschalt</b> an einem beliebigen Punkt gedrückt, während Sie ein Objekt verschieben, damit die Frameränder automatisch angepasst werden, damit das Objekt innerhalb seiner Grenzen bleibt.

![autoexpand](version-13-1.resources/version-13-1-02.gif)

### Größe an Inhalt anpassen

Wenn du in deinem Diagramm Anpassungen vornimmst, wird ein Frame möglicherweise nicht mehr elegant an seinen Inhalt angepasst. Mit diesem neuen Befehl können Sie die Position und die Größe des Frames automatisch anpassen, sodass er sich an die Spanne seines Inhalts anpasst. Der Abstand beträgt dabei eine Zelle mit mittlerem Raster. Wenn der Rahmen eine Beschreibung hat, wird er so angepasst, dass nach Möglichkeit ein leerer Bereich neben der Beschreibung verwendet wird.

![fitsize](version-13-1.resources/version-13-1-03.gif)

### Verbesserte Beschreibungen

Dank des HTML-Codes können Sie jetzt formatierten Text in der Beschreibung eines Rahmens haben. Dies gilt auch für Kommentare.

![richtext](version-13-1.resources/version-13-1-04.png)

### <b>...und vieles mehr!</b>

Viele Dinge wurden überdacht, z. B. die Toleranz von Zuordnungsregeln, Interaktionszonen zum einfachen Ändern der Größe von Frames, Ausrichtungsregeln, um Ihre Knoten im Raster nicht falsch auszurichten, und das visuelle Erscheinungsbild, um etwas Frische zu erzeugen. Weitere Informationen finden Sie in der [Dokumentation](../../interface/the-graph-view/graph-items/frame/frame.md) der Frames.

## Verbesserung der Lebensqualität

* Verbesserungen des <b>Knotenmenüs: </b> Um Zeit zu sparen, während Sie nach dem Knoten suchen, den Sie benötigen, haben wir das Knotenmenü ein wenig verbessert. Die Suche verzeiht jetzt mehr und gibt Ihnen ein Ergebnis, auch wenn es keine perfekte Übereinstimmung gibt. Darüber hinaus können Sie jetzt mit dem Pfeil nach oben direkt auf das letzte Element in der Liste zugreifen.
* <b>Knotenplatzierung: </b>Wenn du ein perfektes Layout für dein Diagramm haben möchtest, werden dir diese beiden kleinen Änderungen gefallen! Wenn Sie Knoten von einem Diagramm in ein anderes kopieren/einfügen, werden die eingefügten Knoten jetzt am Hauptraster ausgerichtet. Wenn Sie einen Knoten auf einem langen Link hinzufügen, wird dieser in der Mitte des sichtbaren Teils des Links platziert, damit er in jeder Situation sichtbar ist.
* <b>2D-Anzeigeoptionen: </b>Wenn Sie die [2D-Ansicht](../../interface/2d-view/2d-view.md) intensiv nutzen, sparen Sie Zeit, da Optionen wie &quot;Schachbrett anzeigen&quot;, &quot;Ansichtsgröße beibehalten&quot;, &quot;Physische Größe verwenden&quot; und &quot;Anzeigeunterteilung&quot; jetzt gespeichert werden. Sie müssen sie also nicht erneut festlegen, wenn Sie eine neue 2D-Ansicht erstellen oder Designer neu starten.

## AxF-Export

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![AxF-Dateisymbol](version-13-1.resources/version-13-1-05.png "AxF-Dateisymbol")

</td>
<td width="100.00%" style="border: 0;" valign="top">

AxF ist ein Format von [X-Rite](https://www.xrite.com/axf). Sie bietet eine Möglichkeit, komplexe Materialeigenschaften mithilfe von numerischen Daten im gesamten digitalen Design-Workflow zu erfassen, zu speichern, zu bearbeiten und zu kommunizieren. In früheren Versionen von Designer konnten Sie AxF-Dateien [importieren](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) und dann die Unterteilung verbessern oder prozedurale Effekte hinzufügen. Dann mussten Sie jedoch Änderungen als neue .sbsar-Datei exportieren.

In dieser neuen Version wird die Möglichkeit eingeführt, AxF-Materialien an Ort und Stelle zu bearbeiten, und dann [Ihre Änderungen &#x200B;](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) als neue Ebene in die importierte AxF-Datei zu exportieren.

</td>
</tr>
</table>

![Export AxF](version-13-1.resources/version-13-1-06.gif)

## API

Und schließlich verbessert diese Version 13.1 die Python-API weiter, indem sie zwei weitere Möglichkeiten hinzufügt:

* <b>-Eigenschaften &quot;Sichtbar, wenn&quot;: </b>Sie können diese Eigenschaft jetzt für Graphparameter, Eingaben und Ausgaben festlegen.
* <b>Reihenfolge der Diagramme Eingabe/Ausgabe:</b> verwenden sdsbscompgraph::reorderGraphInput und sdsbscompgraph::reorderGraphOutput, um die Parameter nach Bedarf zu organisieren.

>[!NOTE]
>
> Designer 13.1 ist die letzte Hauptversion, die auf Qt5 basiert. Die nächsten Hauptversionen werden auf Qt6 aktualisiert. Es kann Auswirkungen auf Ihre benutzerdefinierten Plug-ins haben.

## Versionshinweise

### 13.1.0

*(veröffentlicht am 12. Dezember 2023)*

### Hinzugefügt

* [Frames] Automatisch erweitern
* [Frames] Ändern Sie Regeln, um festzulegen, wann ein Objekt zu einem Frame gehört.
* [Frames] Deaktivieren der Textskalierung für die Rahmenbeschreibung
* [Frames] Größe an Inhalt anpassen
* [Frames] Neuer Standard-, Hover- und ausgewählter Status
* [Frames] Ausrichten an großem Raster
* [Frames] Unterstützung von HTML-Code für Frames-Beschreibung
* [Frames] Interaktionszonen aktualisieren
* [Frames] Visuelles Seitenverhältnis aktualisieren
* [Diagramm] Erstellen Sie den Knoten in der Mitte des sichtbaren Links anstelle der Mitte des Links.
* [Diagramm] Zeigt die Eigenschaften eines Elements an, wenn es das einzige Element ist, für das Eigenschaften in einer Auswahl verfügbar sind.
* [Diagramm] Option &quot;Skalierung&quot; für Kommentare im Diagramm entfernen
* [Graph] Ausrichten von Knoten auf dem Hauptraster beim Kopieren/Einfügen
* [UX] Fuzzy-Suche im Knotenmenü und in der Bibliothekssuche zulassen
* [UX] Knotenmenüliste in Schleife setzenN
* [AxF] Unterstützung des AxF-Exports
* [AxF] Deaktivieren von AxF unter Linux
* [API] Legen Sie die Eigenschaft &quot;Sichtbar wenn&quot; für Diagrammparameter, Eingaben und Ausgaben mithilfe der Python-API fest.
* [API] Festlegen der Reihenfolge von Diagramm-E/A mithilfe der Python-API
* [Abhängigkeiten] Update Boost auf 1.80.0
* [Abhängigkeiten] Update OpenSubdiv auf 3.5.x
* [Abhängigkeiten] Aktualisieren Sie das FBX SDK auf 2020.3
* [Abhängigkeiten] NGL auf 1.35.0.20 aktualisieren
* [Farbmanagement] Unterstützung für OCIO ICC-Displays hinzufügen
* [Ebenen] Möglichkeit zum Zurücksetzen des Histogramms hinzufügen
* [Python] Warnen Sie Benutzer, wenn QtForPython nicht importiert werden kann
* [2D-Ansicht] Speichern des Status der Ansichtsoptionen
* [3D-Ansicht] Hinzufügen von Positionstechnik zum Gitterinfo-Shader
* [Exportieren] Hinzufügen einer Schaltfläche &quot;Einstellungen speichern&quot;, um Änderungen an den Exportoptionen zu speichern

### Fehlerbehebungen

* [3D-Ansicht] Einer Eingabe vom Typ texture\_2d eines MDL-Materials kann keine Textur zugewiesen werden.
* [AxF] Diagrammbezeichner in der Vorlagenliste können leer sein.
* [AxF] Das Vorlagenfeld für Substance-Graphen ist standardmäßig leer.
* [Inhalt] Atlas Scatter: Fehlverhalten in bestimmten Fällen
* [Inhalt] Flood Fill Mapper: leere Ausgabe, wenn alle Formen die gleiche Box-Größe haben
* [Content] FloodFill zur Positionierung: Ungenauigkeiten in einigen Situationen
* [Inhalt] Falsche &quot;Specular&quot;-Ausgabe im Knoten &quot;BaseColor/Metallic/Roughness-Konverter&quot;
* [Inhalt] &quot;Auf Pfad maskieren&quot; funktioniert nicht in nicht quadratischen vertikalen Bereichen
* [Inhalt] Fehlende Beschreibung für Eingabewert, Graustufeneingabe, Eingabefarbe und Ausgabeknoten
* [Inhalt] Fehlende Beschreibung für Set- und Sequenzknoten
* [Inhalt] Formaufteilung: Ungenauigkeitsartefakte in der Ausgabe von &quot;Splatter data 2&quot;
* [Engine] Booleans in Value-Prozessoren werden immer als &quot;False&quot; ausgewertet (nur Apple Silicon)
* [Explorer] Die Reihenfolge der Symbolleistenschaltflächen ist zwischen den Betriebssystemen inkonsistent.
* [Frames] Ergreifen Sie keine Knoten, wenn Sie einen Frame mit dem STRG-Modifizierer verschieben
* [Verlaufsumsetzung] Alle zurücksetzen sollte auch das Verlaufs-Widget zurücksetzen
* [GraphRender] Einige Knoten werden beim Anpassen im Vorschaumodus schwarz gerendert
* [Graph] Die Vorschau für &quot;Eingabewert&quot; bleibt auf &quot;Falsch&quot; hängen, wenn der boolesche Standardwert angepasst wird (nur Apple Silicon)
* [Diagramm] Punktknoten in der Nähe der Rahmenkante werden nicht vom Frame verschoben
* [Interoperabilität] Symbol &quot;Erneut senden&quot; wird nach dem Senden an Substance 3D Stager nicht aktualisiert
* [MDL] Die Raueit kann in Knoten, in denen dieser Parameter verfügbar ist, nicht geändert werden.
* [MDL] Ungültige Verbindungen in der Vorlage &quot;AxF zu metallischer Raueit&quot;
* [UI] Fenster &quot;Ausgaben exportieren&quot; kann minimiert werden (nur Windows)
* [UI] Bilder werden im Bildschirm &quot;Info&quot; verpixelt angezeigt, wenn die Anzeigeskalierung verwendet wird
* [UI] Knotenausrichtungswerkzeuge in der Diagrammsymbolleiste erstellen mehrere Rückgängig-Schritte

### BEKANNTE FRAGEN

* [AxF OpenGL Shader] Falscher Ward für anisotrope Verteilung
* [AxF OpenGL Shader] Falsche Standardrauhigkeit
* [AxF OpenGL Shader] Falsche Schattierung-Basisrotation
* [AxF OpenGL Shader] Falscher Strahl unter Halbkugelerkennung
* [AxF OpenGL Shader] Erkennung falscher Beiträge
* [AxF] Die Zuordnungswerte für &quot;Specular-Farbe&quot; sind beim Export falsch
* [AxF] Vorschau und Texturen werden im Dialogfeld &quot;AxF importieren&quot; nicht korrekt angezeigt
* [AxF] Eigenschaft &quot;cc no refraktion&quot; wird in der AxF-Vorlage nicht korrekt in AxF injiziert

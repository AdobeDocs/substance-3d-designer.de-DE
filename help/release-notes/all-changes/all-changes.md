---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/all-changes.html"
breadcrumb-title: ''
description: Prüfe alle Änderungen und Updates in den verschiedenen Versionen von Substance 3D Designer, um die Entwicklung und Verbesserungen der neuen Funktionen verfolgen zu können.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > All changes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alle Änderungen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49d7d426f1b687cf6087bb1c9735a9060af48041
workflow-type: tm+mt
source-wordcount: '32039'
ht-degree: 0%

---


# Alle Änderungen

## Version 16

### 16.0.5

*(veröffentlicht am 26. August 2026)*

**Hinzugefügt:**

* [3D-Ansicht] Es wurde eine Schaltfläche zur Auswahl der aktuellen AOV hinzugefügt.
* [Inhalt] Perlin/Gaußsches Rauschen: Skalenparameter freigeben
* [Inhalt] Unnötige Bitmapressourcen aus der Bibliothek ausblenden
<!--
* &#91;Legal&#93; To meet generative AI transparency legal requirements, this version is updated to automatically attach Content Credentials to qualifying content created or edited with generative AI tools.  
-->

**Fest:**

* [3D-Ansicht] Änderungen an der Umgebungssichtbarkeit, die in OpenGL vorgenommen wurden, werden nicht auf Eclair-Renderer übertragen
* [Bäcker] Der Backkontext wurde nach dem Aktualisieren von Bäcken für eine gelöschte UDIM-Bitmapressource nicht zerstört.
* [Baker] Absturz beim Löschen einer UDIM-Bitmap-Ressource während der Aktualisierung der Backens behoben
* [Inhalt] Formspritzer v2: Height der Zylinderform ist nicht korrekt
* [Inhalt] Formspritzer v2: Dichte-Map funktioniert nicht ordnungsgemäß, wenn die Knotengröße 4096 überschreitet
* [Inhalt] Formspritzer v2: Die Verwendung des &#39;Rock&#39; SDF hinter einem If/Else kann zu einer Endlosschleife führen
* [Sicherheit] Es wurde eine NULL-Zeigerdereferenzlücke beim Analysieren von AXF-Dateien behoben.
* [Sicherheit] Es wurde eine NULL-Zeigerdereferenzlücke beim Analysieren von GLB-Dateien behoben.
* [Sicherheit] Sicherheitslücken beim Schreiben außerhalb des gültigen Bereichs beim Analysieren von SBSAR-Dateien behoben
* [Sicherheit] Es wurde eine Sicherheitslücke behoben, durch die beim Analysieren von DDS-Dateien ein Heap beschädigt wurde.
* [Sicherheit] Es wurde eine Sicherheitslücke aufgrund einer Heap-Beschädigung beim Analysieren von GLB-Dateien behoben.
* [Sicherheit] Es wurde eine Sicherheitslücke aufgrund einer Heap-Beschädigung beim Analysieren von TGA-Dateien behoben.
* [Sicherheit] Es wurde eine Sicherheitslücke behoben, durch die beim Analysieren von TIFF-Dateien ein Heap beschädigt wurde.
* [Sicherheit] Es wurde eine Sicherheitslücke aufgrund einer Heap-Beschädigung beim Analysieren von USDA-Dateien behoben.
* [Sicherheit] Bei der Analyse von WEBP-Dateien wurde eine Sicherheitslücke aufgrund einer Heap-Beschädigung behoben.
* [UI] Das Kontrollkästchen von Elementen in dauerhaften Kontrollkästchenmenüs erstreckt sich nur über den Elementtext.


### 16.0.4

*(veröffentlicht am 2. Juli 2026)*

**Hinzugefügt:**

* [3D-Ansicht] Klammern Sie die Renderauflösung auf 4096 in X und Y ein
* [Bäcker] Update bake-sdk auf 3.22.3
* [Engine] Aktualisieren der Substance-Engine auf Version 9.4.4
* [OpenGL]&#x200B;[OpenPBR] Reduzieren von Rauschen im Specular-Lappen für hohe Raueit + Anisotropie
* [Szenen] Beibehalten des Modus für die Interpolation von UV-Primärkomponenten

**Fest:**

* [3D-Ansicht] USD-Export: Ressourcenpfad wird mit dem absoluten Pfad gespeichert
* [Bäcker] Das Backen schlägt fehl, wenn das Laden des hohen Polygitters abgebrochen wird (Windows)
* [Bäcker] Liste der 3D-Szenen mit hohem Poly enthält keine Ressourcen mit demselben Bezeichner wie das niedrige Poly
* [Bäcker] Normaler Weltraum: Eine WS-Normale wird immer zurückgegeben, wenn eine Eingabe-Normale vorhanden ist.
* [Inhalt] Falsche Normale bei ungleichmäßiger Skalierung des Musters in der Formaufteilung V2
* [Inhalt] Formspritzer V2: Schwarze Normale für die Formen &quot;Plane&quot; und &quot;Disc&quot;
* [Inhalt] Formspritzer v2: Die erste Form wurde nicht korrekt mit dem Hintergrund überblendet.
* [Absturz] Zufälliger Absturz möglicherweise mit Video verknüpft (umfassende QuickInfos)
* [Graph] Absturz beim Einfügen eines Knotens, der aus einem neuen Graph mit leerem Bezeichner kopiert wurde
* [PSD] PSD-Dateien werden zu oft geladen

### 16.0.3

*(veröffentlicht am 29. Mai 2026)*

**Fest:**

* [Absturz] Beheben Sie eine Regression, die in Version 16.0.2 eingeführt wurde und bei einigen Benutzern beim Start einen Absturz verursachte.

### 16.0.2

*(veröffentlicht am 28. Mai 2026)*

**Hinzugefügt:**

* [OpenPBR] Unterstützung für Grundfarben-/AO-Konstanten hinzufügen

**Fest:**

* [3D-Ansicht] Leak of VRAM in GPU Path Tracer, wenn Versatz aktiviert ist
* [3D-Ansicht] Hauptthread bleibt belegt, wenn die 3D-Ansicht vorhanden ist
* [3D-Ansicht]&#x200B;[OpenPBR] OpenGL: Widgets vom Typ &quot;Gewicht&quot; scheinen festgeklemmt zu sein, akzeptieren aber Werte außerhalb des zulässigen Bereichs
* [Absturz] Absturz beim Verschieben referenzierter Eingaben um mehr als eine Stelle gleichzeitig
* [Absturz] Absturz beim Aufheben der Maximierung eines Fensters
* [Absturz] Absturz beim Schreiben von TARGA oder BMP vom Bäcker
* [Absturz] Zufälliger Absturz bei der Anzeige der 3D-Ansicht
* [Graph] Falsche Reihenfolge von I/O-Pins beim Verschieben von I/O nach dem Bearbeiten von Kennungen
* [Linux]&#x200B;[Export] Die Dialogfelder &quot;Publish sbsar&quot; und &quot;Senden an&quot; fügen keine Dateierweiterung hinzu.

### 16.0.1

*(veröffentlicht am 5. Mai 2026)*

**Hinzugefügt:**

* [Samples] Fügen Sie eine Materialprobe hinzu, die SDF/Shape Splatter gewidmet ist
* [Inhalt] 3D-Viewer: Standardstatus ändern
* [Inhalt] 3D-Viewer: Standardumgebung hinzufügen
* [Inhalt] Shape Splater v2 Mapper: Hinzufügen eines Mittelparameters für die Projektion pro Achse für die dreiplanare Abbildung
* [Inhalt] Shape Splater v2 Mapper: Anordnungsparameter hinzufügen
* [Inhalt] Formspritzer v2: Das Extrudieren von Formen standardmäßig aktivieren
* [3DView] Unterstützung von Intel Panther Lake-GPUs im Pathtracer
* [3D-Ansicht] Verbessern der Formatierung von Popup-QuickInfos für &quot;Versatz&quot;
* [Engine] Update auf Substance Engine 9.4.3
* [OpenPBR] geometry_tangent: Unterstützung für Konstanten hinzufügen
* [Voreinstellungen] Fügen Sie eine Option für TGA/BMP hinzu, um den Alphakanal zu schreiben, wenn er vollständig deckend ist
* [Drittanbieter] Update auf &quot;Adobe Color Engine&quot; (ACE) 7.0
* [UI] Fenster &quot;Plug-in-Manager&quot; immer sichtbar machen (modal)

**Fest:**

* [3D-Ansicht] Die Viewport-Skalierung wird bei Verwendung einer festen Auflösung angewendet
* [3D-Ansicht]&#x200B;[OpenPBR] Einfrieren beim Laden einer aus Designer exportierten GLTF-Szene und Verwenden eines OpenPBR-Materials
* [3D-Ansicht]&#x200B;[OpenPBR] Aus Painter exportierte Materialien können in Designer nicht überschrieben werden
* [Inhalt] 3D-Viewer: shape.id ist nicht initialisiert und generiert Meldungen in der Konsole
* [Inhalt] Form Splutter v2 Mapper Graustufen: Der Mustereingang 4 ist bei der triplanaren Projektion nicht belegt
* [Inhalt] Shape Splater v2 Mapper: SDF-ID wird bei Verwendung des Modus &quot;1 Bild pro Material-ID&quot; um -1 versetzt
* [Eclair]&#x200B;[USD] Falsches Ergebnis beim Anwenden eines Materials auf einen von Designer generierten USD
* [Engine] Berechnen eines neuen Levels-Knotens Shape Splatter V2 Hauptdiagramm verwürfelt folgende Berechnungen
* [Engine] Modul einer Variablen gegen ihren Gleichwert gibt in einigen Fällen mit der GPU-Engine nicht 0 zurück.
* [Engine]&#x200B;[Content] Arc tangent 2 gibt 0 oder Pi für X-Right-Vektoren in einem bestimmten Fall zurück.
* [Engine]&#x200B;[Ubuntu]&#x200B;[SSE2] Absturz beim Laden eines bestimmten SBSAR im Diagramm
* [Graph] Absturz beim Verbinden der Value Processor-Ausgabe mit der Bitmap-Eingabe
* [Graph] Absturz beim Einfügen von Werten in Bildeingaben in einigen Fällen
* [Graph] Graph wird automatisch bei jedem automatischen Speichern berechnet, wenn durch Baking erzeugte Map verwendet werden
* [GraphRender] Absturz beim Verbinden der Wertausgabe der Atlas Scatter mit der Bildeingabe des Atlas Splitters
* [Linux]&#x200B;[Export] Das bearbeitete Dateiformat wird in Dialogfeldern zum Speichern von Dateien ignoriert
* [Mac]&#x200B;[Steam] Sicherheits-Popup wird angezeigt, wenn Designer gestartet wird
* [Mesh] OBJ-Materialien werden nicht korrekt importiert
* [PSD] Der PSD-Importer fordert, bei jedem automatischen Speichern Ebenen aus der PSD-Datei zu extrahieren

### 16.0.0

*(veröffentlicht am 14. April 2026)*

**Hinzugefügt:**

* [Inhalt] Shape-Splatter v2-Knoten
* [Inhalt] Shape Splater v2 Mapper Color/Grayscale Nodes
* [Inhalt] Form Splint v2 zu Maskenknoten
* [Inhalt] Rasteratlas
* [Content] 3D-Viewer-Knoten
* [Content] 3D SDF-Operatorknoten
* [Content] 3D SDF primitive Knoten
* [Content] 3D SDF-Transformationsknoten
* [Content] 3D SDF-Materialknoten
* [Inhalt] Winkel zum Vektorknoten
* [Content] Knoten mit konstanten Werten
* [3D-Ansicht] OpenPBR-Shader für OpenGL-Renderer
* [3D-Ansicht] OpenPBR-Shader für Rasterizer und GPU-Pathtracer-Renderer
* [3D-Ansicht] Versatz-Fenster zum Festlegen der Height-Skalierung, der Height-Ebene und der Tesselierung
* [3D-Ansicht] Neuorganisieren der Symbolleistenelemente
* [3D-Ansicht] Legen Sie in der 3D-Ansicht OpenPBR als Standardansicht für das Materialmodell fest.
* [3D-Ansicht] Lassen Sie die 3D-Ansicht das Grafikattribut &quot;Materialmodell&quot; berücksichtigen.
* [3D-Ansicht] Synchronisieren von Materialmodellen beim Wechsel zwischen Rasterbildern/GPU-Pathtracer und OpenGL-Renderern
* [3D-Ansicht] Vergewissern Sie sich, dass das Materialmodell dauerhaft ist, wenn Sie 3D-Renderer wechseln und Änderungen an der Materialdefinition synchronisiert werden.
* [3D-Ansicht] GPU-Pathtracer: Pixelwiederholung für blaues Rauschen aktivieren
* [3D-Ansicht] Deckkraftsteuerung &quot;Umgebungs-Verdeckung belichten&quot;
* [3D-Ansicht] Stellen Sie den Parameterbereich &quot;Kacheln&quot; für alle Shader auf [0, 10] ein.
* [3D-Ansicht] Benennen Sie die Aktion &quot;Fokus&quot; in &quot;Frame&quot; um
* [3D-Ansicht] Verarbeiten Sie den neuen Parameter refineLevel, der tesselationFactor ersetzt.
* [3D-Ansicht] FPS-Zähler hinzufügen
* [3D-Ansicht] Verschieben Sie den Fortschrittsbalken in derselben horizontalen Symbolleiste wie den Farbraum unten
* [Bäcker] Anzeigen der UV-Werte des ausgewählten Bäckers in der Vorschau
* [Graph] Neues Materialmodell-Attribut zu Substance-Graphen hinzufügen
* [NewGraph] Hinzufügen von Trennlinien in der Miniaturansicht
* [Parameter] Definieren Sie einen standardmäßigen konstanten Wert für Eingabeparameter mit dem Editor &quot;Funktion&quot;
* [Parameter] Kombinationsfeld aus `Set` und `Is defined` Knotenparametern mit verfügbaren Variablen auffüllen
* [Voreinstellungen] Entfernen der veralteten Option &quot;Skalierungsfaktor deaktivieren&quot; auf der Registerkarte &quot;3D-Ansicht&quot;
* [Publish] Dialogfeld &quot;Publish&quot;: Materialmodell in Diagramminformationen einbeziehen
* [Python] Fügen Sie die neue Klasse SDMaterialModelDescription hinzu, um die Informationen eines Materialmodells abzurufen.
* [Python] Erlaubt das Abrufen/Festlegen der Materialmodell-Eigenschaft von SDSBSCompGraph-Objekten.
* [Python-Editor] Erhöhung der Schriftgröße auf 12
* [Vorlagen] OpenPBR-Vorlagen hinzufügen
* [Vorlagen] Materialproben in OpenPBR konvertieren
* [Drittanbieter] Update Boost auf Version 1.88
* [Drittanbieter] C++-API auf C++20 aktualisieren
* [Drittanbieter] NGL-Aktualisierung auf 1.42
* [Drittanbieter] OneTBB auf Version 2022.x aktualisieren
* [Drittanbieter] Update OpenColorIO auf Version 2.5.x
* [Drittanbieter] Update OpenEXR auf Version 3.4.x
* [Drittanbieter] Update Qt &amp; QtForPython auf 6.8.x und Python auf 3.13.x
* [Drittanbieter] Update TBB auf oneTBB 2021.x
* [Deprecation] Entfernen Sie Iray und den MDL-Editor.

**Fest:**

* [2D-Ansicht] Der Histogrammauswahlbereich wird nicht beibehalten, wenn die Breite des Widgets klein wird
* [3D-Export] Aus Designer exportierte Gitter werden in usdview nicht gleich gerendert
* [3D-Ansicht] Wenn der 3D-Ansicht Nicht-Audiomaterial zugewiesen wird, bleibt der Einzelkachel-Rendermodus erhalten.
* [3D-Ansicht] Eingeklemmtes Ergebnis bei Verwendung von OCIO
* [3D-Ansicht] Absturz beim Anwenden einer Diagrammtextur auf ein nicht überschriebenes Material für eine bestimmte Szene
* [3D-Ansicht] Absturz beim Erstellen von Frame-Puffern
* [3D-Ansicht] Eclair-GPU-Pathtracer: Fehlerhafte Geometrie und geringe Leistung beim Rendern eines bestimmten Modells
* [3D-Ansicht] Falsche Texturtransformation für bestimmte Szenen
* [3D-Ansicht] Inkonsistentes Framing von Szene/Auswahl bei Verwendung einer festen Renderauflösung
* [3D-Ansicht] Falsche diffuse Farbe beim Rendern bestimmter GLTF-Datei
* [3D-Ansicht] Unsichtbare Umgebung beim Wechseln von Renderern in einem bestimmten Fall
* [3D-Ansicht] Materialien werden beim Importieren einiger .fbx-Dateien nicht korrekt erkannt
* [3D-Ansicht] mehrmaliges Überschreiben von Materialien setzt die Kachelung auf 1 zurück
* [3D-Ansicht] Eigenschaften in der Kategorie &quot;UVs&quot; werden nicht in SBSSCN-Dateien gespeichert
* [3D-Ansicht] &quot;Ausgaben in 3D-Ansicht zurücksetzen und anzeigen&quot; aus Diagrammen mit einer Ausgabe setzt Materialien nicht zurück
* [3D-Ansicht] &quot;Rendering speichern&quot;: Das bearbeitete Bildformat bleibt nicht erhalten
* [3D-Ansicht] Auswahl funktioniert nicht auf AMD-GPUs
* [3D-Ansicht] Die eigenständige 3D-Szene wird nicht aktualisiert, wenn sie auf der Festplatte geändert wird
* [3D-Ansicht] Einige Farbmaterialeigenschaften werden beim Überschreiben nicht korrekt farbverwaltet
* [3D-Ansicht] UDIM-Texturen werden auf ein bestimmtes Gitter nicht korrekt angewendet
* [3D-Ansicht] USD-Szene mit Material aus MaterialX wird nicht mehr korrekt gerendert
* [Bäcker] Abstürze mit einigen Netzen
* [Bäcker] Texturübertragung: Absturz in bkBufferViewCopy
* [Cooker] Endlose Schleife im While-Schleifen-Knoten in einem Fall, der verhindert werden konnte
* [Engine] Beenden Sie die Substance-Engine beim Schließen der Anwendung.
* [Allgemein] Vermeiden von zufälligen Abstürzen beim Beenden der Anwendung (nur Windows)
* [Diagramm] Funktionsdiagramm: Typweitergabe funktioniert in einigen Situationen nicht richtig
* [Graph] Graph-Links werden gelöscht, wenn ein Bildeingabeknoten umbenannt wird
* [Diagramm] Verknüpfungen und Pins zeigen manchmal Artefakte an
* [Voreinstellungen] &quot;Viewport-Skalierung&quot; ist invertiert
* [Eigenschaften] Absturz beim Ändern der Diagrammeingabe-Optimierung beim Anzeigen der Instanzparameter
* [Python] PySide6-Module können nicht importiert werden (möglicher Konflikt mit der vorhandenen PySide6-Installation)
* [Python] Bestehende PySide- und Shiboken-Module stehen im Konflikt mit Designers
* [UI] Hover-Stil verschwindet bei Schaltflächen in bestimmten Fällen (nur Windows)
* [UI] Hover-Stil ist nicht auf Dropdown-Schaltflächen sichtbar, wenn darauf geklickt wird (nur macOS)
* [UI] Schaltfläche &quot;Weitere Informationen&quot; in &quot;?&quot; QuickInfo funktioniert nicht, wenn sich die QuickInfo außerhalb der Dialogfeldgrenzen befindet (nur Windows)

**Bekannte Probleme:**

* [Graph] Generierte Symbole für OpenPBR-Graphen sind ungenau
* [3D-Ansicht] Szenen mit animierten Grundelementen werden nicht ordnungsgemäß unterstützt.
* [3D-Ansicht] Pathtracer wird nicht auf allen AMD-Grafikkarten unterstützt

## Version 15

### 15.1.3

*(veröffentlicht am 10. März 2026)*

**Hinzugefügt:**

* [Bäcker] Hinzufügen von Makros für die Ausgabegröße des Dateinamens
* [Bäcker] Vermeiden Sie das Laden des Hochpoly-Gitters vor dem Backen
* [Bäcker] CLI: Aktualisieren der Beschreibung der Option &quot;output-size&quot; mit Makros für die Größe
* [Bäcker] Konvertieren des Eingabetexturformats in das angeforderte Format
* [Bäcker] Deaktivieren der Option &quot;Offset-Map&quot;, wenn &quot;Käfig verwenden&quot; aktiviert ist
* [Bäcker] Zeigt beim erneuten Öffnen des Backfensters bereits durch Baking erzeugte Map an
* [Bäcker] Halten Sie das Backfenster offen, bis alle Backvorgänge effektiv abgebrochen werden.
* [Baker] Funktion BindTexture migrieren
* [Bäcker] [Einstellungen] Legen Sie den Standardwert für den &quot;Namensfiltermodus&quot; auf &quot;Übergeordneter Name (veraltet)&quot; fest.
* [Bäcker] [QuickInfo] Fügen Sie der QuickInfo für den Parameter &quot;Entsprechen&quot; den Wert &quot;Name-Filtermodus&quot; hinzu.
* [Engine] Upgrade der Substance-Engine auf Version 9.3.4

**Fest:**

* [3D-Ansicht] &quot;Ausgaben in 3D-Ansicht anzeigen&quot; überschreibt nicht die vorhandene Zuweisung in Diagrammen mit einzelner Ausgabe
* [3D-Ansicht] UVs können in einigen Fällen nicht angezeigt werden
* [3D-Ansicht] Berechnete Tangenten erscheinen für USD defekt
* [3D-Ansicht] Absturz beim Öffnen des Renderer-Menüs
* [Bäcker] Der Abstand kann nicht größer als 1 festgelegt werden, wenn &quot;Relativ zu Box&quot; deaktiviert ist.
* [Bäcker] Die Fertigstellung des Farbbäckers dauert in bestimmten Fällen zu lange
* [Bäcker] Farbe: Absturz beim Backen von UV-Inseln
* [Bäcker] Die Bereiche der Abstands- und Radiusparameter sind zu eng, wenn der Wert absolut ist
* [Bäcker] Fehler beim Backen von hoher fehlender Poly-Tangente und Bitangenten, die nicht benötigt werden
* [Bäcker] Materialfarben in der Bäcker-Befehlszeile nicht korrekt
* [Bäcker] Mehrere hohe Polygitter werden in einigen Situationen ignoriert
* [Bäcker] Normal: Schwarze Ausgabe bei Verwendung von Anti-Aliasing und Diffusion (nur macOS)
* [Bäcker] Die Offset-Map-Pfadprüfung meldet unerwartete Fehler bei der Verwendung von Bitmap-Paketressourcen
* [Bäcker] Die QuickInfo für die Offsetzuordnung ist falsch
* [Bäcker] Das Platzieren der Ressource in einem netzspezifischen Ordner funktioniert nicht
* [Bäcker] Texturübertragung: Der Wert &quot;UV-Set&quot; wird nicht wie beim erneuten Öffnen des Backfensters wiederhergestellt
* [Bäcker] Texturübertragung: Eine Graustufeneingabe führt nicht zu einer Graustufenausgabe
* [Bäcker] Warnung für deaktivierten geerbten Bäcker wird nicht gelöscht, wenn die Texturquelle im Zielbaker geändert wird
* [Bäcker] [UDIM] Offset-Map wird nur auf UDIM 1001 angewendet
* [Graph] UDIM 1001 wird immer berechnet, unabhängig von der verwendeten UVTile.

### 15.1.2

*(veröffentlicht am 3. Februar 2026)*

**Fest:**

* [Engine] Ebenen: Gleitkommawerte werden immer auf [0, 1] eingespannt
* [Bäcker] Das Anpassen der Geometrie mit dem übergeordneten Namen (veraltet) funktioniert nicht für Subnetze
* [Bäcker] Farbe: Änderungen an Materialfarben in der Benutzeroberfläche werden ignoriert
* [3D-Ansicht]&#x200B;[Bäcker] Das Laden der OBJ-Datei dauert sehr lange

### 15.1.1

*(veröffentlicht am 20. Januar 2026)*

**Hinzugefügt:**

* [Beispiele] Fügen Sie zwei Beispiele hinzu, um Abschnitte zu erstellen, die dem Painter-Menüband-Tool zugeführt werden
* [Engine] Update auf Substance Engine 9.3.2
* [Engine]&#x200B;[Metal] Verbessern der Leistung
* [Engine] Bilineare Interpolation ganzzahliger Texturen wird jetzt mit erhöhter Präzision durchgeführt (CPU-Backend)
* [Bäcker] Protokollieren Sie eine Warnung, wenn die Scheitelpunktfarbe in einem hohen Polygonnetz fehlt.
* [Branding] Aktualisieren von Dateitypsymbolen
* [NewGraph] Anwenden von Hover-Formatvorlagen auf das Symbol (i) in den Ansichtsmodi &quot;Liste&quot;, &quot;Pakete&quot; und &quot;Verzeichnisse&quot;

**Fest:**

* [3DView] UDIM-Meshes rendern keine einzelne Kachel mehr.
* [3DView] Absturz, wenn kein renderDevice erkannt wird
* [Branding] Beheben von Symbolen für .SBS-Dateien unter Linux
* [Inhalt] RGB auf HSL-Funktion: Falsches Ergebnis für fast 0 Eingaben
* [Graph] Graph-Symbol/Miniaturbildgenerator funktioniert nicht
* [Graph] Node-Menü: gruppierte Elemente ohne Miniaturansicht ohne Einzug
* [Engine]&#x200B;[Inhalt] Farbe für Maske v2: Artefakte an der SSE2-Engine bei Verwendung des Lab-Distanz-Farbraums
* [Engine]&#x200B;[Inhalt] Farbe für Maske v2: Artefakte an arm64-GPU-Engines bei Verwendung des Lab-Distanz-Farbraums
* [Engine]&#x200B;[Metal] Schwarze Strahlungsleistung für PBR-Rendering-Node
* [Engine]&#x200B;[Mac] Falsches Ergebnis in einer Pixelprozessorfunktion unter Metal
* [Engine]&#x200B;[Mac] Verbessern der Genauigkeit einiger Anweisungen, die in Pixelprozessoren auf Apple Silicon M1/M2-GPUs verwendet werden
* [Engine] Größenänderung von Eingabebildern (oder eingebetteten Ressourcen) führt nicht mehr zu Randartefakten (CPU-Backend)
* [Engine] Der Pegelfilter klammert seine Gleitkomma-Eingangswerte nicht mehr ein, wenn 8I/16I-Texturen ausgegeben werden (CPU-Back-End)
* [Engine] Es wurde ein FxMaps-Fehler behoben, durch den Graustufen-Eingabebilder, die von FxMaps-Knoten verwendet wurden, falsch gesampelt wurden (CPU-Backend).
* [Engine] Einige Artefakte in der 1-Seed-Version des Distanzfilters (GPU-Backends) wurden behoben.

### 15.1.0

*(veröffentlicht am 11. Dezember 2025)*

**Hinzugefügt:**

* [NewGraph] Überarbeitung des neuen Diagrammfensters
* [NewGraph] Hinzufügen von Materialproben und erweiterten Proben
* [NewGraph] Fügen Sie ein neues Attribut für das Diagramm für die Vorlagendaten hinzu (Kategorie und Untertitel).
* [NewGraph] Option &quot;Ausgabeformat entfernen&quot;
* [Inhalt] Hashfunktionen hinzufügen
* [Content] Hinzufügen von Tonabbildungen zu functions.sbs
* [Inhalt] Anisotropes Rauschen v2: Standardausgabeformat hinzufügen, Störung hinzufügen
* [Inhalt] Anwenden von Groß- und Kleinschreibung auf Knoten- und Parameterbeschriftungen
* [Inhalt] BnW-Punkte 1 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] BnW-Punkte 2 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] BnW-Punkte 3 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Zellen 1,2,3,4 v2: Hinzufügen von Standardausgabeformaten, keine Kachelunterstützung, Unordnungsoptionen
* [Inhalt] Clouds 1 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Clouds 2 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Clouds 3 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Farbe für Maske v2
* [Inhalt] Richtungsrauschen 1 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Richtungsrauschen 2 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Richtungsrauschen 3 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Richtungsrauschen 4 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Richtungsabhängige Kratzer v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt 1 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt 2 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt 3 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt 4 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt 5 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Dirt-Verlauf v2: Standardausgabeformat hinzufügen, neue Unordnungsoptionen
* [Content] Fraktalsumme Base v2: Hinzufügen von Standardausgabeformat, Störung, keine Kachelunterstützung
* [Inhalt] Fraktalsumme 1,2,3,4 v2: Standardausgabeformat hinzufügen
* [Inhalt] Gaußsches Rauschen v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Gaußsche Flecken 1&amp;2 v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Messy Fasern 1,2,3 v2: Hinzufügen von Standardausgabeformaten, keine Kachelunterstützung, Unordnungsoptionen
* [Inhalt] Feuchtigkeitsrauschen v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Neuer Knoten &quot;Feuchtigkeitsrauschen 2&quot;
* [Inhalt] Geräusche: Aktualisieren, um das Standardausgabeformat hinzuzufügen
* [Inhalt] Perlin-Rauschen v2: Standardausgabeformat hinzufügen, keine Kachelunterstützung
* [Inhalt] Formzuordnung: Filtermodus hinzufügen
* [Inhalt] UV-Mapper: Filtermodus hinzufügen
* [Inhalt] Wellenform 1 v2: Verwenden des Standardausgabeformats + neue Optionen
* [Inhalt] Weißes Rauschen v2: Standardausgabeformat verwenden, Verteilungsoptionen hinzufügen
* [Bäcker] Zeigt nur die UVs aus dem ausgewählten Gitter an.
* [Bäcker] Fügen Sie eine Option hinzu, um die Methode zum Abgleichen der Geometrie nach Namen auszuwählen.
* [Bäcker] Wählen Sie den nächsten Bäcker aus, wenn ein Bäcker gelöscht wird
* [Bäcker] UDIM: eine Liste der UV-Kacheln für Backvorgänge definieren
* [Bäcker] Update bake sdk auf 3.15.4
* [3D-Ansicht/SceneBrowser] Vermeiden Sie die Auswahl einer UsdPrimitive, wenn Sie mit der rechten Maustaste darauf klicken.
* [ColorManagement] Unterstützung ACES 2.0
* [Compositing Graph] Ermöglichen das Festlegen eines Ausgabeknotens als &quot;Standardausgabe&quot;
* [Cooker] Warnung bei nicht verbundenen Eingängen von Funktionsinstanzen entfernen¬†
* [Functions] Add isDefined-Operator
* [Graph] Gruppieren Sie die Elemente nach &#39;group&#39;-Attribut im Knotenmenü.
* [Graph] Verbessern der Wiedergabe von Miniaturen

**Fest:**

* [3D-Ansicht] L16-Graustufenstruktur wird mit einem roten Farbton angezeigt, wenn sie an die Umgebung oder die baseColor angeschlossen ist
* [3D-Ansicht] Wenn Sie die Materialbindung einer Szene ohne Material ändern, wird ein neues &quot;Standardmaterial&quot; erstellt
* [3D-Ansicht] Berechnete Normale sind für bestimmte OBJ-Gitter nicht korrekt
* [3D-Ansicht] Benutzerdefinierte Umgebung von SBSSCN ist beim Laden in Pathtracer nicht sichtbar
* [3D-Ansicht] Fehler in der Konsole beim Drehen einer deaktivierten Umgebung
* [3D-Ansicht] Specular level wird nicht korrekt angewendet
* [3D-Ansicht] Specular edge color funktioniert nicht, wenn Eclair rasterer verwendet wird
* [3D-Ansicht] Vom Benutzer hinzugefügtes Material wird nicht auf Standardszenen angewendet
* [3D-Ansicht]&#x200B;[Bäcker] Die Materialfarbe ist zu dunkel, wenn sie einmal überschrieben wurde oder wenn ein &quot;Color&quot;-Bäcker verwendet wird
* [3D-Ansicht]&#x200B;[Bäcker] Keine Materialfarbe aus FBX-Datei
* [Bäcker] Materialfarben in FBX-Dateien werden nicht korrekt erkannt
* [Baker] Die Option &quot;recompute\_tangents&quot; ist in Exporten von JSON-Vorgaben immer &quot;false&quot;.
* [Bäcker] CLI: Absturz beim aufeinander folgenden Ausführen desselben Bakers über die JSON-Datei
* [Bäcker] Das Aktualisieren des Parameters &quot;Farbgenerator&quot; funktioniert nicht für &quot;Graustufen&quot;
* [Inhalt] Zu Pfaden maskieren: Fehler bei nicht quadratischen Verhältnissen
* [Inhalt] PBR-Rendering-/Symbolrenderer: Falsche Specular-Lappenfunktion
* [Inhalt] Pfade zum Spline: Legen Sie die Ausgabegröße standardmäßig auf &quot;Relativ zum übergeordneten Element&quot; fest.
* [Inhalt] Punktliste: Punkte sind nicht in der richtigen Reihenfolge, wenn die Datentextur nicht quadratisch ist
* [Inhalt] Spline-Mapper: 1px Leitungsstörung in zufälligen Fällen
* [Inhalt] Spline-Mapper: gedehnte UVs in einigen Fällen, wenn die Thickness 0 beträgt
* [Graph] Absturz beim Löschen der Ausgabe eines Funktions-Untergraphen
* [Graph] Der Farbtyp des Eingabeknotens kann in schreibgeschützten Paketen geändert werden
* [Graph] Primäre Eingabe kann in schreibgeschützten Paketen geändert werden
* [Eigenschaften] Die Farbe des Farbvorschau-Widgets stimmt nicht mit dem sRGB-Schaltflächenstatus überein
* [Szene] Kann keine OBJ-Datei laden, die größer als 2 GB ist
* [UI] Die Dockingstatus von Console und Dependency Manager werden nach einem Neustart nicht wiederhergestellt

### 15.0.3

*(veröffentlicht am 23. Oktober 2025)*

**Fest:**

* [Inhalt] Die Vorschauausgabe von Spline-Werkzeuge-Knoten wird standardmäßig nicht angezeigt
* [Graph] Absturz beim Löschen der Ausgabe eines Funktions-Untergraphen

### 15.0.2

*(veröffentlicht am 18. September 2025)*

**Hinzugefügt:**

* [3D-Ansicht/OpenGL] Entfernen Sie den Drahtgitter-Effekt, der auf das ausgewählte Mesh angewendet wurde.
* [3D-Ansicht] Verwenden der Taste &quot;F&quot;, um sich auf ein ausgewähltes Gitter zu konzentrieren, wenn der Szenenbrowser den Fokus hat
* [3D-Ansicht] Rendern wird beim Ändern der Normalen-Map-Format nicht aktualisiert
* [BakersCLI] Hinzufügen einer Option zum Steuern der Größe des Oberflächencaches
* [BakersCLI] Umbenennen der Option &quot;use\_cache&quot; in &quot;keep\_meshes\_in\_cache&quot;
* [UI] Symbol &quot;Aktualisieren&quot; für 3D-Szenen in der Bibliothek

**Fest:**

* [3D-Ansicht] Absturz beim Zuweisen eines Materialknotens zu einer Multimaterialszene
* [3D-Ansicht] Graph, der aus Textureingaben erstellt wurde, wird unabhängig von Voreinstellungen immer in der 3D-Ansicht angezeigt
* [3D-Ansicht] Falsche Verwendung bei einer Badge-QuickInfo &quot;In 3D-Ansicht angezeigt&quot; in einem bestimmten Fall
* [3D-Ansicht] Viele USD-Fehler beim Überschreiben bestimmter Szenen
* [3D-Ansicht] Schatten-Artefakte bei Verwendung von Versatz auf einer flachen Szene im Raster
* [3D-Ansicht] Einige bestimmte Szenen sind bei Verwendung des OpenGL-Renderers nicht sichtbar
* [3D-Ansicht] Das Dialogfeld, das zum &quot;Auswählen des Ziel-Substance-Grafen&quot; verwendet wird, enthält immer das Symbol &quot;Ausstehend&quot;.
* [3D-Ansicht] Das Kontextmenü des Ansichtsports wird für bestimmte Szenen nicht angezeigt
* [3D-Ansicht] Kennzeichen &quot;In 3D-Ansicht angezeigt&quot; werden nicht gelöscht, wenn in einem bestimmten Fall die Szene gewechselt wird
* [3D-Ansicht] Ausgewaschene Farbe in 3D-Ansicht bei Verwendung des Adobe ACE-Farbmanagements
* [3D-Ansicht]&#x200B;[Linux] Mehrere Szenen werden im OpenGL-Renderer schwarz dargestellt
* [3D-Ansicht]&#x200B;[Szenenbrowser] Pfeiltasten verschieben die Auswahl an der Wurzel
* [BakerCLI] Einige Parameter können nicht überschrieben werden.
* [Bäcker] Artefakte in Erweiterung bei Verwendung von normalen Bäckern mit Antialiasing
* [Bäcker] Der Backvorgang wurde in CLI abrupt gestoppt, während eine hohe Menge an UDIMs bei 4K gebacken wurde
* [Bäcker] Absturz beim Verschieben des Bäckers in der Bäckerliste in einem bestimmten Fall
* [Bäcker] Die Formatauswahl wechselt von .surface zu .dds
* [Bäcker] Einfrieren beim Backen einer großen Menge von UDIMs bei 4K
* [Bäcker]&#x200B;[macOS] Absturz beim Backen der Texturübertragung mit Antialisierung
* [Inhalt] Punktliste: Punkte sind nicht in der richtigen Reihenfolge, wenn die Datentextur nicht quadratisch ist
* [Inhalt] Farbpalette anzeigen: Interne Knoten werden mit zu hoher Auflösung berechnet
* [Daten] Absturz beim Umbenennen der Ausgabe, um die Ghost-Ausgabe in der Instanz zu korrigieren
* [Motor] Abstand: Luminanz der Eingabemaske wurde geändert
* [FxMap] $tiling hat keine Wirkung, wenn sich die FX-Map in einem Untergraph befindet
* [Diagramm] Unscharfe Suche gibt irrelevante Ergebnisse zurück
* [Python-Editor] Geladene Skripte werden nicht sitzungsübergreifend erneut geöffnet

### 15.0.1

*(veröffentlicht am 22. Juli 2025)*

**Hinzugefügt:**

* [3D-Ansicht] Ermöglichen Sie die Texturierung von USD-Meshes, die displayColor und keine Materialbindungen aufweisen.
* [3D-Ansicht] Erstellen Sie nicht automatisch ein Material pro Gitter, das keine Materialbindung hat
* [3D-Ansicht] Umbenennen von &quot;Konvergenz-Pixelproben&quot; in &quot;Samples&quot;
* [3D-Ansicht] Benennen Sie den Parameter &quot;UV-Skalierung aktiviert&quot; in &quot;Physische Größe aus Diagramm aktivieren&quot; um.
* [3D-Ansicht] Skalieren Sie die Intensität des Versatzes entsprechend dem Parameter &quot;Kacheln&quot;
* [3D-Ansicht/OpenGL/Iray] Hinzufügen einer Nachricht im Viewport, wenn die Standardumgebung deaktiviert ist
* [Bäcker] Verwenden Sie Symbole für Schaltflächen, um Linien in der Bäcker-Renderliste neu anzuordnen
* [Voreinstellungen] Fügen Sie eine Option hinzu, um den standardmäßigen 3D-Ansicht-Renderer zu definieren
* [Eigenschaften] Verwenden Sie für &quot;Auf Standard zurücksetzen&quot; die erstellten Standardwerte, falls vorhanden.

**Fest:**

* [3D-Ansicht] Artefakte an einer bestimmten Szene, wenn sie mit OpenGL gerendert werden
* [3D-Ansicht] Die Standardumgebung ist nicht deaktiviert, wenn eine USD-3D-Szenenressource geladen wird, die eine enthält.
* [3D-Ansicht] Die Anzeige des Kontextmenüs des Ansichtsports dauert in großen Szenen mehrere Sekunden
* [3D-Ansicht] &quot;Emissionsintensität&quot; ist 0, wenn nicht in USD enthaltene Materialien überschrieben werden, nur mit &quot;Emissionsfarbe&quot;.
* [3D-Ansicht] Rote und blaue Kanäle werden durch eine 8-Bit-Textur ersetzt, die als Umgebung verwendet wird
* [3D-Ansicht] RMB-Drag&amp;Drop funktioniert aufgrund des Registers mit Rechtsklick nicht konsistent
* [3D-Ansicht] &quot;Nur anzeigen&quot; für Untermenge blendet das übergeordnete Gitter aus
* [3D-Ansicht] Die aus einer Datei geladenen Standardszenen werden mit einer falschen Grundfarbe angezeigt
* [3D-Ansicht] Die Eigenschaft &quot;UV-Skalierung&quot; wird zurückgesetzt, wenn von OpenGL zu einem anderen Renderer und zurück gewechselt wird
* [3D-Ansicht]&#x200B;[Iran] Renderings sind oft verschwommen und pixelig
* [Bäcker] Artefakte bei Verwendung der Diffusion auf einer AMD-GPU
* [Bäcker] Das Backen schlägt mit einigen Szenen für andere UV-Sätze als 0 fehl
* [Bäcker] &#39;Transferierte Textur&#39;: Die Liste &quot;UV-Satz&quot; berücksichtigt nicht die Option &quot;Niedrig-Hoch-Poly verwenden&quot;
* [Bäcker] Die Auswahl der UV-Kacheln wird immer auf &quot;Alle&quot; zurückgesetzt
* [Graph] Absturz beim Löschen eines Knotens im Kontext
* [Mac OS]&#x200B;[3D-Ansicht] Falsche Renderauflösung auf Mac-Displays
* [Parameter] Geänderte Parameter werden bei der ersten Anzeige nicht stilisiert
* [UX] Deaktivierte Elemente im Dropdown-Menü sind nicht sichtbar

### 15.0.0

*(veröffentlicht am 15. Juli 2025)*

**Hinzugefügt:**

* [3D-Ansicht] Brandneuer Renderer mit Raster- und Pathtracer-Modi
* [3D-Ansicht] Hinzufügen eines Auswahlwerkzeugs, um ein Objekt in der 3D-Szene auszuwählen
* [3D-Ansicht] Fügen Sie eine neue &quot;Szene mit Ebenen exportieren...&quot; hinzu. Aktion im Menü &quot;Szene&quot;
* [3D-Ansicht] Hinzufügen neuer Symbolleistenschaltflächen
* [3D-Ansicht] Fügen Sie die Möglichkeit hinzu, zwischen mehreren Kameras in einer USD-Szene zu wechseln.
* [3D-Ansicht] Konzentrieren Sie sich auf das ausgewählte Objekt, wenn Sie im Darstellungsfenster &quot;F&quot; drücken.
* [3D-Ansicht] Generieren eines Substance-Compositing-Diagramms aus einem vorhandenen Material zulassen
* [3D-Ansicht] Erlaubt das Senden einer SBS-Kompositionskurve in der 3D-Ansicht und das Zuweisen ihrer eindeutigen Ausgabe zur Verwendung in der Umgebung/im Panorama.
* [3D-Ansicht] Löschen Sie die aktuelle Auswahl, indem Sie die Esc-Taste drücken.
* [3D-Ansicht] Eine importierte 3D-Szene mit Texturen anzeigen
* [3D-Ansicht] Unterscheiden Sie zwischen X- und Y-Texturwiederholungssteuerungen
* [3D-Ansicht] Aktivieren/Deaktivieren von Schatten
* [3D-Ansicht] Grundebene aktivieren/deaktivieren
* [3D-Ansicht] Fügen Sie im Menü &quot;Materialien&quot; die Option &quot;Entfernen&quot; nur für das Material hinzu, das manuell hinzugefügt wurde und nicht verwendet wird.
* [3D-Ansicht] Entfernen Sie im Menü &quot;Materialien&quot; die Aktion &quot;Alle entfernen&quot;.
* [3D-Ansicht] Macht exportierte USDZ-Dateien eigenständig
* [3D-Ansicht] Legen Sie die Eigenschaften des Renderers fest, wenn der Renderermodus gewechselt wird.
* [3D-Ansicht] Beibehalten der vorhandenen Materialeingaben beim Überschreiben eines Materials
* [3D-Ansicht] Neuanordnen von Kameraeigenschaften
* [3D-Ansicht] Aktionen entfernen &quot;Kamera/Screenshot speichern...&quot; und &quot;Kamera/Screenshot in Zwischenablage kopieren&quot;
* [3D-Ansicht] Menüaktion &quot;Material/Alle neu erstellen&quot; entfernen
* [3D-Ansicht] Entfernen Sie das Präfix &quot;Standard&quot; der Beschriftung der Standardkamera.
* [3D-Ansicht] Legen Sie die Menüaktion &quot;Auf Standardwert zurücksetzen&quot; als letzte im Hamburger-Menü der Materialeingabeeigenschaft fest.
* [3D-Ansicht] Korrekturen an Tastaturbefehlen
* [3D-Ansicht] Unterstützung von Schatten und Lichtdurchlässigkeit im Echtzeitmodus
* [3D-Ansicht] Unterstützung von MaterialX-Shadern aus einer importierten USD-Szene
* [3D-Ansicht / OpenGL] Benennen Sie den Parameter &quot;UV-Skalierung aktiviert&quot; in &quot;Physische Größe aus Diagramm aktivieren&quot; um.
* [3D-Ansicht / Post-Effekte] Blüte
* [3D-Ansicht/Post-Effekte] Tiefe des Felds
* [3D-Ansicht/Post-Effekte] Tonzuordnung
* [3D-Ansicht / Szenenbrowser] Ermöglicht die Anzeige der Materialeigenschaften bei der Auswahl im Szenenbrowser.
* [3D-Ansicht / Szenenbrowser] Spalte &quot;Material&quot; ausblenden
* [3D-Ansicht / Szenenbrowser] Fett formatieren die USD-Primitive, die von einer vordefinierten Entität gesteuert werden
* [Bäcker] Hinzufügen eines Kontextmenüs in der Baumstruktur mit den Aktionen &quot;Alle auswählen&quot;/&quot;Auswahl aufheben&quot;
* [Bäcker] Fügen Sie eine Option hinzu, um die bitangene Interpolation zu steuern.
* [Bäcker] Horizontaler Splitter in der Benutzeroberfläche hinzufügen
* [Bäcker] Fügen Sie UDIM-Makro standardmäßig im Ausgabenamen hinzu, wenn die Szene udim ist
* [Bäcker] Tangente neu berechnen lassen
* [Bäcker] Ermöglicht die Umbenennung eines Bäckers, ohne die Verknüpfungen zu trennen
* [Bäcker] Ändern der Standardgröße des mittleren Bereichs
* [Bäcker] Eingabetextur für UDIM-Workflow
* [Bäcker] 2D-Ansichtszuordnungen in der Reihenfolge der Baker-Renderlisten anpassen
* [Bäcker] Das Backfenster modal gestalten
* [Bäcker] Verwalten von Tonzuordnungsparametern
* [Bäcker] Auswahl des Tangentenraum-Zusatzmoduls entfernen
* [Bäcker] Speicherstatus &quot;aktiviert&quot; oder &quot;deaktiviert&quot; für Bäcker beim Speichern einer Vorgabe
* [Bäcker] Material standardmäßig im Widget &quot;Auswählen&quot; auswählen
* [Bäcker] Legen Sie die Standardausrichtung der Textur &quot;Normale Ausgabe&quot; relativ zu den Voreinstellungen fest
* [Bäcker] Legen Sie UV-Kacheln standardmäßig auf Alle fest
* [Bäcker] WordSpaceDirection add option FromTexture/FromValue
* [Bäcker] Welt zu Tangente: Standardeingabe auf &quot;Von Textur&quot; setzen
* [SBSBaker] Erstellen einer Option zur Steuerung der Backend-Reihenfolge
* [SBSBaker] Verbessern der Verwendung des StringList-Arguments
* [SBSBaker] Umbenennen von &quot;match\_source\_instance&quot; in &quot;match\_mesh\_name&quot;
* [SBSBaker] Umbenennen von &quot;Submesh&quot; in &quot;GeomSubset&quot;
* [SBSBaker] Umbenennen in substance3d\_baker
* [Inhalt] Hinzufügen der Form &quot;Hemisphere&quot; zu Generatorknoten, die Quadrantenformen freigeben
* [Interop] Unterstützung des GLTF-Dateiformats
* [Interop] Unterstützung des PLY-Dateiformats
* [Interop] Unterstützung des STL-Dateiformats
* [Library] Vereinheitlichte QuickInfos für atomare Knoten
* [Mac] Unterstützung für MacIntel-Plattform beenden
* [Knoten] Richtungstipps für atomare Knoten hinzufügen
* [Parameter] Schließen Sie den Abschnitt &quot;Attribute&quot; standardmäßig.
* [Parameter] Der Benutzer kann Standardwerte für Basisparameter für neue Instanzen angeben.
* [Voreinstellungen] Bäcker: Fügen Sie eine boolesche Option hinzu, um den Tangentenraum pro Fragment zu berechnen.
* [Voreinstellungen] Entfernen Sie die Tangentenraum-Plugins
* [Voreinstellungen] Speichern Sie die Voreinstellungen pro Nebenversion von SD (XX.X).
* [VFX] Update Boost auf 1.85.0
* [VFX] Aktualisieren der MacOS-Mindestversion auf 12.0
* [VFX] OpenColorIO auf 2.4.2 aktualisieren
* [VFX] OpenColorIO auf 2.4.x aktualisieren
* [VFX] Update OpenExr auf 3.3.x
* [VFX] Update Qt auf 6.5.8

**Fest:**

* [3D-Ansicht] Texturen in exportierter USD-Szene werden nicht korrekt angewendet
* [3D-Ansicht] [UDIM] UDIM-Diagrammausgaben können in der 3D-Ansicht nicht angezeigt werden, wenn die automatische Anzeige beim Öffnen des Diagramms in den Diagrammvoreinstellungen deaktiviert ist
* [Bäcker] &#39;Glätten.&#39; und &quot;Durchschn. Zellen von Normalen für nicht anwendbare Bäcker sind leer und bearbeitbar
* [Bakers] Die Aktion &quot;Aktualisieren&quot; verwendet Raytracing-Backend, wenn sie in den Einstellungen deaktiviert ist
* [Bäcker] Bäcker wurden nach einem Fehler während des Prozesses &quot;Alle durch Baking erzeugte Map aktualisieren&quot; als ausgelastet gesperrt.
* [Bäcker] Absturz bei mehr als 180 UDIMs beim Backen der OpenGL-Positions-Map auf einem bestimmten Gitter
* [Baker] Absturz beim mehrmaligen Öffnen des Dialogfelds &quot;Modellinformationen backen&quot; in einer Zeile (nur macOS)
* [Bäcker] Beim Export von JSON-Vorgaben wird der Wert &quot;udim&quot; durch &quot;1001&quot; ersetzt, wenn er auf &quot;Alle&quot; festgelegt wurde
* [Bäcker] Speicher wird unter Linux nicht korrekt erkannt
* [Bäcker] Fehlende Map-Eingabeabhängigkeit löst keine Warnung und/oder Blockrendering aus
* [Bäcker] Keine Fehlerbezeichnung, wenn der Ausgabename leer ist
* [Bäcker] Das Umschalten von High-Poly-Mesh aus einer Datei hat keine Auswirkungen
* [Bäcker] Zielbaker ist standardmäßig nicht ausgewählt, wenn die Aktion &quot;Erneut erstellen&quot; verwendet wird
* [Motor] Abstand: sichtbarer &quot;Schnitt&quot; in einigen Situationen
* [Engine] FX-Map: Negative Farben werden nicht unterstützt, wenn die Bittiefe 8 Bit beträgt (nur GPU-Engines)
* [Lokalisierung] Die Zeicheneingabe wechselt im Knotenmenü von Japanisch zu Lateinisch zurück
* [Sicherheit] Sicherheitslücke, die beim Analysieren von USDC-Dateien außerhalb des gültigen Bereichs auftritt
* [Sicherheit] Out-of-Bound WRITE Vulnerability II, beim Analysieren von NEF-Dateien
* [Sicherheit] Sicherheitslücke beim Lesen außerhalb des gültigen Bereichs III beim Analysieren von DNG-Dateien
* [Voreinstellungen] UX-Probleme in den Projekteinstellungen für schreibgeschützte Projekte
* [Ressourcen] Mehrere UV-Sets werden beim Öffnen von FBX-Dateien nicht angezeigt
* [UI] Überlappende Beschriftungen in der Statuszeile
* [UI] QuickInfos zum Dropdown-Menü &quot;Link-Erstellungsmodus&quot; werden nicht angezeigt.

## Version 14

### 14.1.2

*(veröffentlicht am 15. April 2025)*

**Hinzugefügt:**

* [Graph] Verwenden Sie die Standard-GPU-Engine, um Miniaturansichten für das aktuelle Diagramm zu generieren
* [Bibliothek] Verwenden Sie die Standard-GPU-Engine, um Miniaturansichten für die Bibliothek zu generieren

**Fest:**

* [Graph] Verbindungen können in einigen Fällen im Verbindungserstellungsmodus &quot;Standard&quot; nicht verschoben werden
* [Inhalt] Artefakte in der MLV-Filterausgabe in einem bestimmten Fall
* [Inhalt] Atlas Splitter/Streuung: Nur die erste Zelle wird korrekt gezeichnet (nur macOS + GPU-Engine)
* [Inhalt] Weiche Abschrägungen: -Format ist absolut 32f
* [Inhalt] Fasern 1: visuelle Artefakte bei der Konvertierung in eine normale Map
* [Inhalt] RT AO, Schatten, Gebeugte Normale werden in einigen Fällen falsch gerendert
* [Bäcker] Bei Menüpunkten mit Untermenüs fehlt ein Rand auf der rechten Seite des Textes
* [MacArm]&#x200B;[sbsrender] Falsche CPU-Engine, wenn die GPU-Engine nicht gefunden wurde
* [Mac/Linux]&#x200B;[sbsrender] Falsche Standard-GPU-Engine

### 14.1.1

*(veröffentlicht am 20. Februar 2025)*

**Hinzugefügt:**

* [Graph] Knotenausrichtungswerkzeuge: Tastaturbefehle wieder einsetzen, Stapelung standardmäßig aktivieren
* [MDL] Warnen Sie Benutzer, dass &quot;MDL-Diagramme&quot; in einer zukünftigen Version veraltet sind.
* [Voreinstellungen] Warnen Sie Benutzer, dass &quot;Plug-ins für benutzerdefinierte Tangentenräume&quot; in einer zukünftigen Version veraltet sind.

**Fest:**

* [2D-Ansicht] Zentrierte Pixelkoordinaten anstelle von oben links anzeigen
* [Inhalt] Anisotropes Kuwahara-Graustufen: Cooker-Warnung für fehlende Variable &quot;ignore\_alpha&quot;
* [Content] Cooker-Warnungen in einigen Schmutz-Nodes
* [Inhalt] Kochfehler für fehlenden Parameter im Knoten &quot;Auto-Tonwertkorrektur&quot;
* [Inhalt] Kochfehler in der Konsole beim Rendern von Miniaturansichten einiger Pakete
* [Inhalt] Kantenkerbe: Kochwarnung in der Konsole
* [Inhalt] MLV-Farbe: Anschnitt trotz Verwendung von &quot;Keine Kacheln&quot; in einem bestimmten Fall
* [Inhalt] Maske zu Pfaden: Pfade können zu viele, zu wenige oder in bestimmten Fällen von null Länge sein
* [Inhalt] PBR-Rendering v1: Einige Dienstprogrammdiagramme werden in der Bibliothek angezeigt
* [Inhalt] Streuung auf Spline: Ein Muster wird gezeichnet, obwohl kein Spline-Eingang vorhanden ist
* [Parameter] Beschriftung &quot;Geisterwert&quot; beim Einfügen des Listenparameters mit nicht übereinstimmendem Index
* [UI] Absturz beim Schließen von Designer durch die Aktion &quot;Beenden&quot; im macOS-Dock (nur macOS)
* [UI] Texturpfade in den Shader-Eigenschaften werden nicht auf die Breite des Docks beschnitten

### 14.1.0

*(veröffentlicht am 14. Januar 2025)*

**Hinzugefügt:**

* [2D-Ansicht] Hinzufügen einer fixierten Pixelanzeige im Informationsfenster
* [API] Zeigen Sie die Knoten in der Box-Größe in der Diagrammansichtsszene an.
* [Inhalt] &quot;Material Height Blend&quot;: Ausgabe für &quot;Height Mask&quot; hinzufügen
* [Content] &quot;Path Vertex Processor&quot;: Schaltfläche &quot;Funktion bearbeiten&quot; für Parameter &quot;Funktion pro Vertex&quot; verwenden
* [Inhalt] Automatische Tonwertkorrektur: Nicht verwendete Parameter bereinigen, Beschriftungen und QuickInfo anpassen
* [Inhalt] Maske auf Pfade v2
* [Inhalt] Neuer Mittelwert des Knotens mit der geringsten Abweichung (MLV)
* [Inhalt] Neuer Medianfilterknoten
* [Inhalt] Farbe quantisieren: Filteroption &quot;Nächste&quot; hinzufügen
* [Inhalt] Spline Bridge-Liste: Hinzufügen zufälliger Spline-Offset-Parameter
* [Inhalt] Spline-Werkzeuge: Neuer Spline-Knoten (quadratisch)
* Triangle Grid [Inhalt]: Dreiecksänderungsverfahren und Verwendung von Schleifen
* [Inhalt] Knoten &quot;Neue Streuung-Splines auf Splines&quot;
* [Cooker] Stellen Sie den Basisparameter &quot;Pixelverhältnis&quot; als statische Variable &quot;$pixelratio&quot; bereit.
* [CrashReport] Neues Absturzbericht-Fenster integrieren
* [Engine] Fügen Sie die Vulkan/Metal-Version der Blend Engine hinzu.
* [Diagramm] Materialmodus: Verbindung ohne Verwendung zulassen, wenn ein einzelner Link ausgewählt ist
* [Diagramm] Materialverknüpfung: Standardverbindungen zulassen, wenn die Verbindung nicht mehrdeutig ist
* [Graph] Knotenausrichtungswerkzeuge: horizontale/vertikale Verteilungen hinzufügen, linke/rechte/obere/untere Ausrichtung festlegen und gestapelte Knoten unterstützen
* [Bibliothek] Textfarbe in Kontextmenüs korrigieren
* [Parameter] Kopieren von Parametern von einem Knoten in einen anderen
* [Eigenschaften] Alle zurücksetzen: Entfernen Sie das Bestätigungs-Popup-Fenster.
* [Ressourcen] Legen Sie im Dialogfeld &quot;Bitmap verknüpfen&quot; das Format auf &quot;Alle Formate&quot; fest.
* [Suche] Hinzufügen einer Möglichkeit zum Aktivieren/Deaktivieren eines rekursiven Modus
* [Suche] Fügen Sie eine Möglichkeit hinzu, die Fuzzy-Suche zu aktivieren/deaktivieren
* [Suche] Bei Aktivierung von Node Finder über den Tastaturbefehl immer den Fokus auf das Suchbegrifffeld anzeigen und festlegen
* [Suche] Filteroption erneut bearbeiten
* [Tastaturbefehle] Zuweisung der Tasten &quot;V&quot;, &quot;H&quot; und &quot;S&quot; zulassen
* [Drittanbieter] Upgrade auf Qt 6.5.7
* [UX] Modale Dialogfelder sollten nicht minimierbar sein.
* [UX] Horizontalen Bildlauf im Warndialogfeld entfernen

**Fest:**

* [Inhalt] Abgeflachte Kante: Das Normalformat wird von der globalen Voreinstellung nicht beeinflusst.
* [Inhalt] Der Knoten &quot;Farbe in Maske&quot; ignoriert Alpha nicht
* Richtungsabstand [Inhalt]: Falsches Ergebnis, wenn die Eingabe ein vertikales Bildverhältnis aufweist
* [Inhalt] Flood Fill Mapper: Warnung bei fehlender Variable ausgelöst
* [Inhalt] Histogramm Berechnen: Das Ergebnis ist 16-mal so, wie es sein sollte
* [Inhalt] RT-Kaustik funktioniert nicht bei nicht quadratischer Auflösung
* [Inhalt] Spline Bridge-Liste: Falsches Ergebnis bei Verwendung von Start-/End-Versätzen
* [Inhalt] Spline-Auswahl: Der Ausgangs-Spline-Betrag kann größer sein als der Eingangs-Spline-Betrag.
* [Inhalt] Spline-Warp erzeugt ein schwarzes Ergebnis mit SSE-Engine
* Triangle Grid [Inhalt]: Muster ist nicht richtig gekachelt
* Triangle Grid [Inhalt]: Kachelung ist in einem bestimmten Fall fehlerhaft
* [Daten] Absturz beim Ändern der Diagrammeingabe-ID in einem bestimmten Fall
* [Funktionsdiagramm] Lange Werte werden überlappend auf &#39;Float&#39;-Knoten angezeigt
* [Fx-Map] Absturz beim Anzeigen von Quadrant-Knoteneigenschaften
* [Graph] [UDIM] Mit einer Bildlaufleiste in der UDIM-Liste werden 1.1 1.2 Einträge generiert.
* [Graph]&#x200B;[Shortcuts] Knoten, der mit einem Shortcut erstellt wurde, wird nach dem Duplizieren des Knotens nicht auf dem vorhandenen Link platziert.
* [Eigenschaften] Falsche Parameteranzeige, wenn der Wert ungültig ist
* [Publish] Gegenseitige Abhängigkeiten führen beim Veröffentlichen eines Pakets zu einer Endlosschleife.
* [Publish] Unbeaufsichtigter Fehler bei Verwendung der Aktion &quot;Publish&quot; für ein Paket mit entladener Abhängigkeit
* [UI] Widget &quot;Übergeordnete Größe&quot; wird nicht korrekt angezeigt, wenn es erweitert wird, und kann die Benutzeroberfläche blockieren (nur macOS)
* [UI] Das Hauptfenster liegt in einigen Fällen hinter anderen Anwendungen (nur Windows)

### 14.0.2

*(veröffentlicht am 10. Oktober 2024)*

<b>Hinzugefügt:</b>

* [Funktionsdiagramm] Verbessern der Textausrichtung innerhalb von Knoten
* [MacOS] Installation auf BigSur-Version (11.0) erneut zulassen
* [Windows] Installation unter Windows 10 19H2 erneut zulassen

<b>Fest:</b>

* [Bitmap] Malstriche auf Bitmapressourcen markieren das Hostpaket nicht als geändert.
* [Funktionsdiagramm] Absturz beim Schließen des Pakets mit Funktionsdiagramm, das einen Instanzknoten hostet
* [Funktionsdiagramm] Absturz beim Rückgängigmachen von zwei Sample Color-Knoten-Änderungen in einer Zeile

### 14.0.1

*(veröffentlicht am 24. September 2024)*

<b>Hinzugefügt:</b>

* [Engine] Update auf Substance Engine 9.1.4
* Triangle Grid [Inhalt]: Dreiecksänderungsverfahren und Verwendung von Schleifen

<b>Fest:</b>

* [API] Ungeladene Plug-ins können nicht erneut geladen werden
* [Inhalt] Histogramm Berechnen: Das Ergebnis ist 16-mal so, wie es sein sollte
* Triangle Grid [Inhalt]: Muster ist nicht richtig gekachelt
* [Daten] Absturz beim Ändern der Diagrammeingabe-ID in einem bestimmten Fall
* [Engine] Knoten &quot;Entfernung&quot; erzeugt Artefakte bei Verwendung sehr niedriger Pixelgrößen
* [Engine] Ungültiges Ergebnis des Knoten-Abstands bei 8K-Auflösung auf SSE2-Engine
* [Funktionsdiagramm] Lange Werte werden überlappend auf &#39;Float&#39;-Knoten angezeigt
* [Graph]&#x200B;[Shortcuts] Knoten, der mit einem Shortcut erstellt wurde, wird nach dem Duplizieren des Knotens nicht auf dem vorhandenen Link platziert.
* [Eigenschaften] Falsche Parameteranzeige, wenn der Wert ungültig ist

### 14.0.0

*(veröffentlicht am 30. Juli 2024)*

<b>Hinzugefügt:</b>

* [Inhalt] Neuer anisotroper Kuwahara-Filter
* [Inhalt] Neuer Knoten &quot;Weiche Abschrägung&quot;
* [Inhalt] Neuer Kurvenglätter v2-Knoten
* [Inhalt] Neuer Richtungsabstand
* [Inhalt] Neue Histogramm-Werkzeuge: Berechnen, Ausgleichen, Rendern
* [Inhalt] Neue ID für Maskenknoten
* [Inhalt] Neuer Knoten Normal Nicht kombinieren
* [Inhalt] Neue Palettenknoten: Erstellen, Anwenden, Ändern, Anzeigen
* [Inhalt] Neuer Knoten &quot;Farbe quantisieren&quot;
* [Inhalt] Uneinheitliche Richtungsverkrümmung: Festlegen des Standardwerts für die Intensitätszuordnung auf 1
* [Content] Hinzufügen des Suffixes &quot;Color&quot; oder &quot;Grayscale&quot; zu allen Knotenbeschriftungen, die diese Versionen aufweisen
* [Inhalt] Veraltetes &quot;weißes Rauschen&quot; nur &quot;weißes Rauschen schnell&quot; beibehalten
* [Inhalt] Veralteter Knoten &quot;Negate Float1&quot; im Substance-Funktionsdiagramm
* [Inhalt] Benennen Sie &quot;Farbe quantisieren&quot; in &quot;Farbe quantisieren (einfach)&quot; um.
* [2D-Ansicht] Anzeigen von Werten im Informationenbedienfeld für Pixel außerhalb des Bereichs 0-1
* [Engine]&#x200B;[Text] Neues Kerning für einige Schriftarten
* [Graph] Verbessern der Invalidierungszeit bei der Bearbeitung von Deep Untergraphen bei Verwendung der In-Context-Edition
* [Linker] Bitmaps in SBSASM nicht duplizieren
* [Parameter] Fügen Sie ein neues Funktions-Widget für alle Eingabeparametertypen hinzu.
* [Eigenschaften] Verbessern der Anzeige geerbter Parameter
* [UX] Verbesserte Trackpad-Unterstützung (nur Mac)
* [UX] Modernisieren Sie das Verschieben, wenn Sie beim Auswählen den Rand des Diagramms erreichen
* [UX] Entfernen der Funktion &quot;High DPI deaktivieren&quot;
* [Branding] Neues Branding für Splash Screen und Fenster &quot;Info&quot;
* [Verlaufsumsetzung] Fügen Sie eine Möglichkeit hinzu, alle Tasten und die Schleife zu verschieben
* [Library] Alle Standardfilter auf Satzschreibweise umstellen
* [API] Hinzufügen einer Methode zum Framing eines bestimmten Knotens im Viewport der Diagrammansicht
* [API] Add-Methode zum Öffnen einer Paketressource in ihrem Editor (z. B. ein Substance-Diagramm in der Diagrammansicht)
* [API] Add-Methode zum Auswählen einer Paketressource im Explorer (z. B. ein Substance-Diagramm)
* [API] Hinzufügen von Methoden zum Abrufen und Festlegen des Diagrammtyps eines Substance-Compositing-Diagramms
* [Drittanbieter] Empfehlungen für VFX-Plattformen 2023 befolgen
* [Drittanbieter] Empfehlungen für VFX-Plattformen 2024 befolgen
* [Third Party] Update Boost auf 1.82.0 + USD auf 23.08
* [Drittanbieter] NGL-Aktualisierung auf 1.38
* [Drittanbieter] Update OpenColorIO auf 2.3.x
* [Drittanbieter] Update OpenExr auf 3.2.x
* [Drittanbieter] Update OpenSubdiv auf 3.6.x
* [Drittanbieter] Update Python auf 3.11.x
* [Drittanbieter] Update Qt auf 6.5.x
* [Drittanbieter] Aktualisieren Sie gcc auf 11.2.1
* [ThirdParty] Update glibc auf 2.28
* [ThirdParty] Update libstdc++ ABI auf C++11 one
* [Dokumentation] Neue Seite &quot;Glossar&quot;

<b>Fest:</b>

* [Bäcker] Absturz beim Umbrechen einer Szene, deren Dateiname geändert wurde
* [Bäcker] Absturz beim Speichern der Bäcker-Voreinstellung in der JSON-Datei
* [Inhalt] &quot;Streuung auf Spline&quot;: Alpha-Parameter für Eingabebild verfügbar machen
* [Inhalt] &quot;Sampler Color anordnen&quot;: Expression &quot;missing visibleif&quot;
* [Inhalt] Anisotropes Rauschen: Negativer Wert für X/Y-Betrag führt zu falschem Ergebnis
* [Inhalt] Anisotropes Rauschen: Problem beim Anordnen, wenn ein ungerader Wert als X-Wert und keine Smoothness verwendet wird
* [Inhalt] Funktion &quot;Normale Verteilung&quot;: falsch platzierte max() kann zu NaN führen
* [Inhalt] RTAO, Bent Normal und RT Shadows funktionieren auf einigen Plattformen nicht ordnungsgemäß.
* [Inhalt] Farbe für Form-Farbspritzer: OpenGL-Normalmaps werden nicht korrekt überblendet
* [Inhalt] Unzulässiger Speicherplatz nach dem Präfix &quot;Multi&quot; in den Knotenbeschriftungen
* [Abhängigkeiten] Absturz beim Verschieben des Diagramms innerhalb oder zwischen Paketen
* [Engine] Genauigkeitsfehler in Verkrümmungsknoten, die sich auf die Steigung-Weichzeichnerknoten auswirken
* [Engine] SBSAR-Ebene in SD kann SBSAR mit SBSASM-Inhalt > 2 GB nicht lesen
* [Funktionsdiagramm] Falsches Ergebnis für 0^n
* [Graph] Option &#39;Display node size&#39; ist falsch beschriftet
* [Graph] Absturz beim Kopieren eines übergeordneten Kommentars in ein anderes Diagramm
* [Graph] Einfrieren beim Alt-Ziehen eines Punktknotens
* [Graph] Knotensuche kann offensichtliche Übereinstimmungen in einigen Fällen verpassen
* [Graph] Leistungsproblem beim Bearbeiten eines Funktionsdiagramms, das mehrmals mit geöffnetem Supergraph installiert wurde
* [Graph] Zu viele Ungültigkeiten beim Erstellen einer Ausgabe
* [Sicherheit] ICO analysiert Schreibfehler außerhalb des gültigen Bereichs
* [Sicherheit] Nicht verwendete Bildformate verwerfen
* [Parameter] Der Bitmap-PKG-Ressourcenpfad sollte nicht bearbeitbar sein.
* [Parameter] Beheben von Problemen im Zusammenhang mit der Belichtung/Batch-Belichtung des Parameters eines Wertprozessors
* [Parameter] Zeichenfolgenparameter werden ignoriert, wenn Batch-Daten angezeigt werden.
* [Eigenschaften] Leistungsproblem beim Bearbeiten eines Funktionsdiagramms, das mehrmals mit geöffneten Eigenschaften instanziiert wurde
* [SVG] Bearbeitungen an Formen werden nicht auf gerasterte Bilder angewendet
* [UI] Beheben einiger Fehler/Inkonsistenzen mit scrollbaren Widgets (nur Windows)
* [UI] Inkonsistente Reihenfolge der 3D-Szenendateiformate in Import-/Exportlisten
* [UI] Fensteraktionen werden in der Benutzeroberfläche dupliziert
* [Versionskontrolle] Das Skript &quot;perforce.py&quot; funktioniert nicht auf Python 3

## Version 13

### 13.1.2

*(veröffentlicht am 16. April 2024)*

<b>Hinzugefügt:</b>

* [Graph] Platzieren Sie keine duplizierten Knoten auf dem ursprünglichen Knoten.
* [Graph] Verbessern der Ausrichtung von Kommentaren, die an Knoten angehängt sind
* [Graph] Verbessern der Kommentarbewegung
* [Graph] Eingefügte/duplizierte Frames und Kommentare am Raster ausrichten
* [Frames] Ausrichten neuer Frames und Kommentare am Raster
* [Inhalt] &quot;Glatte Krümmung&quot;: Fügen Sie in der Beschreibung einen Hinweis zur Untertitelunterstützung hinzu
* [3DView]&#x200B;[IRay] Die Zuweisung der int-Ausgabe zum enum-Parameter zulassen
* [AxF] Hinzufügen von Eigenschaften zum Klarlack-Modell
* [AxF] Verbessern des Fehlermanagements beim Export
* [AxF] Verbessern von GLSLFX- und MDL-Materialien für die &quot;SVBRDF&quot;-Darstellung, wie sie in einer AXF-Datei gespeichert ist
* [AxF] Entfernen der Eigenschaft &quot;CC No Refraction&quot; aus der Vorlage &quot;AxF to AxF&quot;
* [AxF] Umbenennen von Eigenschaften &quot;properties.has\_xxx&quot; in &quot;properties.has\_xxx&quot;
* [AxF] Aktualisieren Sie die Vorlage, um alle Eigenschaften einzubeziehen, die von unseren SVBRDF-Shadern verwendet werden

<b>Fest:</b>

* [3D-Ansicht] Absturz beim Zurücksetzen eines Int MDL-Parameters, der einer MDL-Enumeration zugeordnet ist
* [3D-Ansicht] Falsche Widgets für SVBRDF-Shader-Eigenschaften, wenn Material nach dem Ändern der 3D-Szene zurückgesetzt wird
* [3D-Ansicht] Falsche Widgets für SVBRDF-Shader-Eigenschaften, wenn kein Diagramm angewendet wird
* [3D-Ansicht] Schaltfläche &quot;Umgebung anzeigen&quot; ist deaktiviert für neue Ansichten ohne standardmäßige SBSSCN-Datei
* [3D-Ansicht] Beim Wechsel von Iray zum OpenGL-Renderer wird eine Diagrammausgabe getrennt
* [AxF] Die Fresnel-Variante wird nicht durch die Diagrammausgabe aktualisiert
* [AxF] Beschriftungen von AxF-Shader-Eigenschaften werden inkonsistent formatiert
* [AxF] Warnung vor unveränderten Ressourcen wird nur in der Konsole angezeigt
* [Inhalt] &quot;Nicht einheitlich&quot; wird nicht konsistent in alle Knoten geschrieben
* [Inhalt] Streuung auf Spline: Fehlende Muster bei Brückenzweigen
* [Inhalt] Spline Mapper: Einfrieren beim Festlegen eines negativen Segmentbetrags
* [Inhalt] &quot;Symmetrie&quot;: Beschriftungen fehlen und sind inkonsistent.
* [Diagramm] Vorhandene Kommentare sind leicht versetzt.
* [Sicherheit] Sicherheitslücke bei RAS-Datei beim Analysieren von Lesevorgängen außerhalb des gültigen Bereichs

### 13.1.1

*(veröffentlicht am 8. Februar 2024)*

<b>Hinzugefügt:</b>

* [AxF] Hinzufügen von booleschen Eigenschaften hasClearCoat, hasSheen usw.
* [AxF] Fehlende Eigenschaften hinzufügen
* [AxF] Importieren von EP-SVBRDF zulassen
* [AxF] Umbenennen von Eigenschaften in &quot;anisotropic&quot;, &quot;fresnel&quot; und &quot;fresnel variant&quot;
* [AxF] Update auf AxF-Editing 1.0.0
* [Graph] Auf Mausposition einfügen, wenn Position innerhalb der Diagrammansicht
* [UX] Height des Textfelds &quot;Beschreibung&quot; von Rahmen und Kommentar vergrößern
* [UX] Konzentrieren Sie sich beim Erstellen von Frames, Kommentaren oder Pins auf Texteditionsfelder

<b>Fest:</b>

* [AxF] Die Zuordnungswerte für &quot;Specular-Farbe&quot; sind beim Export falsch
* [AxF] Vorschau und Texturen werden im Dialogfeld &quot;AxF importieren&quot; nicht korrekt angezeigt
* [AxF] Eigenschaft &quot;CC No Refraction&quot; wird in der Vorlage &quot;AxF to AxF&quot; nicht korrekt injiziert
* [Inhalt] &quot;Flood Fill in Position&quot; ist in der Bibliothek nicht vorhanden.
* [Inhalt] &#39;Platterkreis&#39;: Negative &#39;Pattern Amount&#39;-Werte führen zu sehr langen und intensiven Berechnungen
* [Inhalt] &#39;Spline Merge-Liste&#39;: Falsche Eingabefolge
* [Abhängigkeiten] Die Abhängigkeit wird ihrer Kopie neu zugeordnet, nachdem sie als Kopie gespeichert wurde
* [Frames] Die Schaltfläche &quot;HTML-Markup aktivieren&quot; ist nicht aktiviert, wenn die Verwendung rückgängig gemacht wird
* [Frames] Die Auswahlmarkierung eines Frames und seines Inhalts führt dazu, dass der gesamte Frame-Inhalt verschoben wird, während er automatisch erweitert wird
* [Diagramm] Kommentare, die aus übergeordneten Kommentaren dupliziert werden, werden immer am Diagrammursprung platziert
* [Graph] Zeilenumbruch in Comment ist bei der Erstellung härter
* [Publish] Festlegen des Standardpfads für die SBSAR-Veröffentlichung im Ordner &quot;Meine Dokumente&quot;
* [SBSAR] Durch Wiederholen des SBSAR-Ladevorgangs ist es editierbar und die Daten können verloren gehen.

### 13.1.0

*(veröffentlicht am 12. Dezember 2023)*

<b>Hinzugefügt:</b>

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
* [UX] Schleife der Knoten-Menüliste erstellen
* [AxF] Unterstützung des AxF-Exports
* [AxF] Deaktivieren von AxF unter Linux
* [API] Legen Sie die Eigenschaft &quot;Sichtbar wenn&quot; für Diagrammparameter, Eingaben und Ausgaben mithilfe der Python-API fest.
* [API] Festlegen der Reihenfolge von Diagramm-E/A mithilfe der Python-API
* [Abhängigkeiten] Update Boost auf 1.80.0
* [Abhängigkeiten] Update OpenSubdiv auf 3.5.x
* [Abhängigkeiten] Aktualisieren Sie gcc auf 11.2.1 - Problem mit Iray/MDL C++20
* [Abhängigkeiten] Aktualisieren Sie das FBX SDK auf 2020.3
* [Abhängigkeiten] NGL auf 1.35.0.20 aktualisieren
* [Farbmanagement] Unterstützung für OCIO ICC-Displays hinzufügen
* [Ebenen] Möglichkeit zum Zurücksetzen des Histogramms hinzufügen
* [Python] Warnen Sie Benutzer, wenn QtForPython nicht importiert werden kann
* [2D-Ansicht] Speichern des Status der Ansichtsoptionen
* [3D-Ansicht] Hinzufügen von Positionstechnik zum Gitterinfo-Shader
* [Exportieren] Hinzufügen einer Schaltfläche &quot;Einstellungen speichern&quot;, um Änderungen an den Exportoptionen zu speichern

<b>Fest:</b>

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

### 13.0.2

*(veröffentlicht am 27. Juli 2023)*

<b>Hinzugefügt:</b>

* [Funktionsdiagramm] Hinzufügen der Systemvariable $getPhysicalSize
* [Startbildschirm] Unterstützung beim Öffnen von SBS-Dateien per Drag &amp; Drop
* [Inhalt] Spline Mapper/Spline Flow Mapper : Parameter &quot;Nicht-quadratische Korrektur&quot; hinzufügen

<b>Fest:</b>

* [Startbildschirm] Startbildschirm nicht anzeigen, wenn eine Datei von einer anderen Software gesendet wird
* [Startbildschirm] Falscher Status für das Designer-Symbol in der Windows-Symbolleiste
* Atlas Splitter [Inhalt]: Die Beschreibung ist falsch
* [Inhalt] Falscher Referenzwert in der Funktion &quot;Linear zu sRGB (Luminanz)&quot;
* [Inhalt] Das Werkzeug zur Anzeige von Zahlen unterstützt keine nicht quadratischen Auflösungen
* Punktliste [Inhalt]: Der Parameter &quot;Punktzahl&quot; hat einen falschen Mindestwert.
* [Inhalt] Form-Schlagschatten: Der Schatten kann verschwinden, wenn die Unterteilung deaktiviert ist
* [Inhalt] Spline (Poly Quadratic): Falsche Vorschau-Tangenten und Thickness in nicht korrigierten nicht quadratischen Auflösungen
* [Inhalt] Spline (Poly Quadratic): Punktbeschriftungen werden bei Verwendung der Start-/Endoptionen von Connect nicht ausgeblendet
* [Inhalt] Spline Bridge (Liste): Der Parameter &quot;Nicht-quadratische Korrektur&quot; hat keine Auswirkungen
* [Inhalt] Spline Cubic: Der Parameter &quot;Nicht-quadratische Korrektur&quot; hat keine Auswirkungen auf die Vorschauausgabe
* [Inhalt] Spline Mapper: Falsches Rendering, wenn der Spline eine sehr kleine Thickness hat
* [Inhalt] Spline-Knoten: Umgekehrte Alpha-Zeichenbeschreibung in der Spline-Code-QuickInfo
* [Inhalt] Spline-Knoten: Der Parameter &quot;Nicht-quadratische Korrektur&quot; hat keine Auswirkungen auf die Vorschauausgabe
* [Inhalt] Spline-Rendering: Das Ausgabeformat ist absolut 32F.
* [Inhalt] Spline-Rendering: Ausgabe wird im Bereich [0, 1] eingespannt
* [Inhalt] Spline-Beispiel-Thickness: Spline kann in negative Werte subtrahiert werden
* [Inhalt] Spline-Auswahl: Splines werden standardmäßig mit einem einzelnen Segment geschlossen
* [Absturz]&#x200B;[Cooker] Absturz beim Laden bestimmter Diagramme
* [Absturz]&#x200B;[UI] Absturz beim Aktivieren von Menüs nach dem Laden des Pakets vom Startbildschirm
* [API] Link &quot;Benutzerdokumentation&quot; in der Skriptreferenz ist veraltet
* [Eigenschaften] Die Wertprozessorfunktion kann in einem gesperrten Diagramm nicht geöffnet werden.
* [Publish] Pakete mit MDL-Graphen können nicht veröffentlicht werden
* [UI] &quot;Mein Konto verwalten...&quot; ist im Hilfemenü deaktiviert
* [UI] Fehlende Einträge im Hilfemenü beim Öffnen von Designer durch eine Datei

### 13.0.1

*(veröffentlicht am 27. Juni 2023)*

<b>Hinzugefügt:</b>

* [Inhalt] Spline (Poly Quadratic), Punktliste: Namen von Punkten in der Vorschau hinzufügen
* [Inhalt] Spline Mapper: Hinzufügen eines Parameters, um den Mittelpunkt des Zylinderprofils zu verschieben
* [DotNode] Sortiert die Liste der Eingabeportale alphabetisch.

<b>Fest:</b>

* [Inhalt] Falsches Ergebnis in mehreren Spline-Knoten bei Verwendung der einheitlichen Verteilung
* [Inhalt] Geringfügige Fehler in den QuickInfos der Spline- und Path-Knoten
* [Inhalt] Quad-Transform auf Pfad: Die Standardwerte p01 und p10 werden umgeschaltet
* [Inhalt] Quad Transform: das Ergebnis in einer bestimmten Situation falsch ist
* [Inhalt] Spline Circle: Das Ergebnis &quot;Richtung spiegeln&quot; ist falsch, wenn keine einheitliche Verteilung verwendet wird
* [Inhalt] Spline Circle: Tangenten sind beim Anpassen der Spiral- und Größenparameter falsch
* [Inhalt] Spline-Flusszuordnung: schwarze Streifen ergeben sich bei Verwendung hoher Spiralleistung in Spline Circle
* [Inhalt] Spline Mapper / UV Mapper: Hintergrundfarbe funktioniert nicht
* [Inhalt] Spline Mapper: Das Basis-Height ist 0, was zu einer Übersteuerung führt
* [Inhalt] Spline Mapper: Spline-Height wird durch einen Eingangsmultiplikator modifiziert, auch wenn dieser Eingang nicht angeschlossen ist
* [Inhalt] Spline Mapper: Splines-Extremitäten, die auf eine Bildkante treffen, werden nicht zugeordnet
* [Inhalt] Spline Mapper: UV-Skalierung Y hat keine Auswirkungen, wenn eine Nicht-Ebene-Form verwendet wird
* [Inhalt] Spline Mapper: Z-Kämpfen beim Rendern überlappender Splines desselben Heights
* [Inhalt] Spline Poly Quadratic: Das Ergebnis &quot;Richtung spiegeln&quot; ist falsch, wenn keine einheitliche Verteilung verwendet wird
* [Inhalt] Spline-Rendering: Gelenke werden nicht konsistent über Spline-Stil-Optionen hinweg behandelt
* [Inhalt] Spline-Rendering: letztes Segment wird nicht gezeichnet
* [Inhalt] Spline-Rendering: Nicht-quadratische Korrektur wird nicht richtig angewendet
* [Inhalt] UV Mapper-Farbe wird zweimal in der Bibliothek angezeigt
* [DotNode] Der Bereich zum Ausrichten der Verbindung wird nach dem Deaktivieren der Textskalierungsbeschränkung nicht aktualisiert
* [DotNode] Erstellung über Kontextmenü ist unterbrochen
* [DotNode] Die Position des Eingabeportalnamens wird nach dem Rückgängigmachen/Wiederholen einer Namensänderung nicht angepasst.
* [GraphRender] Zu viele Ungültigkeiten beim Ändern eines Funktionsdiagramms
* [Diagramm] Die Position des Transformations-Widgets wird visuell nicht korrekt aktualisiert
* [Lokalisierung] &quot;Soft Range&quot; und &quot;Hard Range&quot; sind nicht in MDL-Graphen lokalisiert.
* [Parameter] Aufeinander folgende Textänderungen werden nicht im Verlaufsstapel protokolliert.
* [Parameter] Hitbox zum Verschieben von Diagrammeingabeparametern in der Liste ist unzuverlässig
* [Eigenschaften] Ein einfacher Klick wird als doppelter Klick auf ein Spin-Box-Widget bei großen Projekten betrachtet
* [Publish] Die Reihenfolge der im Paket enthaltenen Ressourcen wird im veröffentlichten Element nicht beibehalten.

### 13.0.0

*(veröffentlicht am 6. Juni 2023)*

<b>Hinzugefügt:</b>

* [Graph] Portal-Knoten
* [Onboarding] Neuer Startbildschirm
* [Inhalt] Spline-Knoten (kubisch)
* [Inhalt] Spline-Knoten (Poly Quadratic)
* [Inhalt] Spline Circle-Knoten
* Knoten &quot;Punktliste&quot; [Inhalt]
* [Inhalt] Spline Bridge-Knoten (2 Splines)
* [Inhalt] Spline Bridge-Knoten (Liste)
* [Inhalt] Spline-Append-Knoten
* [Inhalt] Spline-Auswahlknoten
* [Inhalt] Knoten &quot;Spline Merge-Liste&quot;
* [Inhalt] 2D-Spline-Transformationsknoten
* [Inhalt] Spline-Warp-Knoten
* [Inhalt] Spline-Beispiel-Height-Knoten
* [Inhalt] Spline-Beispiel-Thickness
* [Inhalt] Spline-Renderknoten
* Streuung [Inhalt] im Spline-Farbknoten
* [Inhalt] Streuung auf dem Spline-Graustufenknoten
* [Inhalt] Spline Mapper-Farbknoten
* [Inhalt] Spline Mapper Graustufen-Knoten
* [Inhalt] Spline Bridge Mapper-Farbknoten
* [Inhalt] Spline Bridge Mapper Graustufen-Knoten
* [Inhalt] Spline-Flow-Mapper-Knoten
* Knoten &quot;UV-Mapper-Farbe&quot; [Inhalt]
* [Inhalt] Knoten &quot;UV Mapper Graustufen&quot;
* [Inhalt] Knoten &quot;Pfade zu Splines&quot;
* [Inhalt] Knoten &quot;Masken zu Pfaden&quot;
* [Content] Paths 2D Transform node
* [Inhalt] Knoten &quot;Pfade Polygon&quot;
* [Inhalt] Knoten &quot;Pfade in Vorschau anzeigen&quot;
* [Inhalt] Knoten &quot;Pfade verformen&quot;
* [Inhalt] Pfade Knoten auswählen
* [Inhalt] Knoten &quot;Pfade, Scheitelpunkt&quot;
* [Inhalt] Pfade Vertex Prozessor Einfacher Knoten
* [Inhalt] Knoten &quot;Quad Transform on Path&quot;
* [Inhalt] Raytraced Ambient-Verdeckung v2
* [Inhalt] Raytraced Bent Normal v2
* [Inhalt] Raytraced Shadows v2
* [Engine] Update auf Version 9
* [Engine] Schleifenknoten in Funktionsdiagrammen
* [Engine] Hinzufügen des Volltonmodus zum Verlauf
* [Engine] Atomic pow() node in Function Graph
* [Engine] Hinzufügen von Optionen zum Einschließen von Rändern (Klemmen an Kante/Wiederholen) im Knoten Sampler
* [Engine] Nächstliegendes Sampling im Knoten &quot;Verformen&quot; und &quot;Richtungsverkrümmung&quot;
* [Engine] Hinzufügen eines &quot;Punch-Through-Alpha&quot;-Modus zum Scharfzeichnungsfilter für Farbeingaben
* [Engine] FxMap: Halbkugelmorphlet
* [Engine] Atomic Get/Set-Vorgänge in Funktionsdiagrammen
* [Engine] Funktionen: genaue Funktion von log/log2/exp, 2pow verwenden - Vereinheitlichen Sie Funktionen zwischen Herd und Engine
* [Engine] Hinzufügen eines Parameters &quot;Intensitätsversatz&quot; zum Filter &quot;Richtungsverkrümmung&quot;
* [API] Unterstützung der Vorgabenverwaltung für Compositing-Graphen
* [Funktionen] Ändern des Eingabenamens für Funktionen atomare Knoten
* [Lokalisierung] Portugiesisch (Brasilien), Italienisch (Italien) und Spanisch (Spanien) hinzufügen
* [Lokalisierung] Respektregel &quot;Sprache (Land)&quot; in der Liste der Sprachen
* [Vorgaben] Deaktivieren der Bereiche &quot;Vorschau&quot; und &quot;Vorgaben&quot; in den Diagrammeigenschaften bei Verwendung der kontextbezogenen Bearbeitung
* [Substance-Modelldiagramm] Ende der Unterstützung für Substance-Modelldiagramme

<b>Fest:</b>

* [3D-Ansicht] Anzeige langer Zeichenfolgen in der Szenenstatistik ist abgeschnitten (nur macOS)
* [API] Das Modul &quot;structure::structure&quot; ist weiterhin in der API-Referenz enthalten.
* [API] Punktknoten in MDL-Graphen haben keine Definition und keine Eigenschaften
* [API] Falsches Verhalten beim Festlegen des Parameters von Funktionsknoten
* [Content] 3D Voronoi und 3D Voronoi Fractal Nodes erzeugen eine Kochwarnung
* [Engine] Der Parameter &quot;Offset der Intensitätszuordnung&quot; hat keine Auswirkungen auf Graustufendaten in der SSE2-Engine
* [Explorer] Graph i/o kann gelöscht werden.
* [Graph] Bitmap wird ignoriert, wenn sie in Instanzen verwendet wird
* [Graph] Falsche Punktknotenposition beim Erstellen eines Knotens aus einem Knoten
* [Graph] Falscher Fokus im Dialogfeld &quot;Parameter verfügbar machen&quot; bei Verwendung der Eingabetaste
* [Graph] Falsches Ergebnis beim Histogrammscan mit Bitmap bei der Kontextbearbeitung
* [Lokalisierung] Beheben verschiedener Schnittprobleme
* [Parameter] Absturz beim Löschen eines Eingabeparameters
* [Publish] Grafiken in Ordnern werden in den Stammordner im veröffentlichten Paket verschoben
* [Resources] Absturz beim Aktualisieren einer geladenen Ressource auf dem Datenträger
* [VisibleIf] Beheben von Regressionen in der Bewertung der bedingten Sichtbarkeit

## Version 12

### 12.4.1

*(Freigegeben: 30. März 2023)*

**Hinzugefügt:**

* [Cooker]&#x200B;[Graph] EXIF-Transformations-Tags in JPEG-Datei berücksichtigen
* [Sicherheit] Upgrade auf 23,02 USD
* [Sicherheit] Entfernen Sie die Unterstützung für den Import von Dateiformaten in Collada (.date)
* [Substance-Modelle] Warnung vor dem Ende der Lebensdauer von Substance-Modellgrafiken in der nächsten Hauptversion

**Fest:**

* [3D-Ansicht]&#x200B;[ASM] Beschichtungsrauheitsartefakt bei Verwendung von CoatNormal
* [Inhalt] Parameter &quot;Mit Verlauf gefüllte Zellen&quot; des Alveolus-Knotens ist invertiert
* [Inhalt] Eingabe Anzahl der Multiswitch-Knoten ist nicht fest
* [Inhalt] Kochwarnung im Knoten Scratches Generator Normal
* [Daten] Absturz beim manuellen Laden des Pakets nach Rückgängigmachen des vorherigen Ladens
* [Daten] Absturz beim schnellen Rückgängigmachen mehrerer Diagrammvorgänge bis zum Laden des Pakets

### 12.4.0

*(Freigegeben: 31. Januar 2023)*

**Hinzugefügt:**

* [3D-Ansicht] Hinzufügen aller Optionen im Menü &quot;Anzeige&quot; als Symbolleistenschaltflächen
* [API] Hinzufügen von Aktionen zu Symbolleisten der Diagrammansicht zulassen
* [API] Erstellen, Bearbeiten und Bewerten eines Substance-Modelldiagramms über die API zulassen
* [Farbmanagement] Verbessern der Qualität von gebackenen 3D-LUTs im ACE-Modus
* [Dokumentation] Beispielprojekte für Substance Compositing-Graphen
* [Dokumentation] Beispielprojekt für Funktionsdiagramme
* [Explorer] Verschieben von Diagrammen und Ressourcen von einem übergeordneten Element in ein anderes zulassen, ohne Widgets zu schließen oder zu ungültig zu machen
* [Verlaufseditor] Wählen Sie bei der Anzeige des Verlaufseditors den angeklickten Pin aus.
* [Graph] Option hinzufügen im Kontextmenü eines Knotens, um alle untergeordneten Knoten auszuwählen
* [Graph] Bereinigen Sie das Graph-Werkzeug, um nicht verwendete Knoten in allen Graphentypen und Eigenschaftendiagrammen zu erkennen und zu entfernen.
* [Graph] Transformieren der Bildeingabe in Farbe/Graustufen
* [Parameter] Eine Sperre für Ganzzahl2-Widgets hinzufügen
* [Parameter] Einfache Formeln können als Parameter eingegeben werden
* [Substance-Modell] Umschalten zwischen Werten und Symbolen für Wertknoten
* Schaltfläche [UI] zum Generieren eines zufälligen Werts, wenn ein zufälliger Seed erforderlich ist
* [UI] Das fokussierte Element wird im Szenenbrowser nicht hervorgehoben.
* [UX] Zurücksetzen von Schiebereglerbereichen, wenn ihr Wert zurückgesetzt wird

**Fest:**

* [API] SDProperty.getDefaultValue() gibt fast immer None zurück.
* [3D-Ansicht] Der Eigenschaftswert &quot;DirectX Normal&quot; wird nicht für alle Renderer freigegeben
* [3D-Ansicht] Die Anzeige der Szenenstatistik wird erweitert, wenn der Viewport klein ist
* [3D-Ansicht] Drahtgitter-Anzeigeeigenschaft wird nicht gespeichert
* [Inhalt] Die Parameter für die radiale Weichzeichnungsfarbe haben keine Auswirkungen auf den Alphakanal
* [Lokalisierung] Zusätzliche Schieberegler und Schaltflächen werden in den OpenGL-Eigenschaften der Umgebung angezeigt.
* [MDL]&#x200B;[Substance-Modell] Absturz beim Löschen exponierter Knoten
* [Voreinstellungen] Die Datei Default\_config wird nie neu erstellt, wenn sie gelöscht wird
* [Substance-Modell] Parameter für die Neuanordnung von Abstürzen, der nicht auf Instanzebene angezeigt wird

### 12.3.1

*(Freigegeben: 24. November 2022)*

**Hinzugefügt:**

* [3DView] Optimiertes Rendering für Szenen mit vielen Materialien
* [3DView] Anzeigen der Ausgaben eines Substance-Modelldiagramms beim Ablegen aus Explorer
* [Lizenz] Bereinigen Sie ältere Systeme für Linux-Benutzer
* [Onboarding] Hintergrundtransparenz aktualisieren
* [Substance-Modelle] Zeigt eine Warnung in der Diagrammansicht an, wenn Eingabe und Ausgabe dieselbe Kennung verwenden.

**Fest:**

* [3D Assets] &quot;Hilfe > Substance 3D Assets&quot; zielt fälschlicherweise auf Creative Cloud Desktop unter Linux
* [3D-Ansicht] Materialien werden nicht erstellt, wenn das Gitter geladen wird
* [3D-Ansicht] Die Materialliste wird geöffnet, wenn das Substance-Modelldiagramm im Ansichtsfenster abgelegt wird
* [Explorer] Die Auswahl mit der Tastatur kann nicht gelöscht werden, wenn ein Substance-Modelldiagramm enthalten ist
* [Explorer] Absturz beim Öffnen des Kontextmenüs des Materialelements einer Gitterressource in Mac
* [Graph] Instanzen, deren Eingabebilder von Werten abhängen, erzeugen ein falsches Ergebnis in nachfolgenden Knoten.
* [Graph] Falsches Ergebnis bei Verwendung der Kette von Untergraphen mit aktivierter kontextbezogener Diagrammbearbeitung
* [MDL] Absturz beim Laden eines MDL-Diagramms, das auf ein Compositing-Diagramm mit veralteten Ausgaben verweist
* [MDL] Der 2D-Texturknoten funktioniert nicht mehr.
* [Onboarding] Beschnittene und nicht lokalisierte Texte
* [Onboarding] Fenster werden beim Starten der App durch Öffnen einer Datei nicht korrekt angezeigt
* [Voreinstellungen] Der Bildcache ignoriert den vom Benutzer festgelegten Speicherort für temporäre Dateien
* [Eigenschaften] Änderungen in Vorschau-/Vorgabenfenstern werden im Rückgängig-Stapel zusammengeführt
* [Tastaturbefehl] Tastaturbefehl, der veralteten Knoten zugewiesen ist, verursacht Konflikte und kann nicht bereinigt werden.
* [Substance-Modelle] Absturz beim Schließen eines Pakets nach Ausführung bestimmter Aktionen
* [Substance-Modelle] Instanzknoten und Verknüpfungen von verlagerten Paketen werden nicht korrekt aktualisiert
* [Substance-Modelle] Das Rückgängigmachen des Löschens von Untergraph aktualisiert Instanzknoten und Verknüpfungen nicht konsistent
* [Substance-Modelle] Der Wert steigt auf dem Transformationsknoten plötzlich zu schnell an
* [UI] Die Warnsymbole für die Eigenschaft &quot;Sichtbar, wenn&quot; enthalten keine QuickInfo.
* [UI] Der Bildinformationstext im Viewport der 2D-Ansicht ist zu dunkel
* [Rückgängig] Verschieben eines Positions-Widgets im Vorschaumodus speichert alle Zwischenwerte

### 12.3.0

*(Freigegeben: 6. Oktober 2022)*

**Hinzugefügt:**

* [Allgemein] Onboarding-Bereich zur Aufnahme neuer Benutzer
* [Allgemein] Neues Fenster zur Verbesserung der Auffindbarkeit neuer Funktionen
* [Substance-Modell] Unterstützung von Unterdiagrammen und Instanzen
* [Substance-Modell] Unterstützung von &quot;Sichtbar wenn&quot; für exponierte Parameter
* [Substance-Modell] Hinzufügen von Unterstützung für Ausgabeknoten
* [Substance-Modell] Kurvenversatzknoten
* [Substance-Modell] Kurvenwiederherstellungsknoten
* [Substance-Modell] Kurvenglättungsknoten
* [Substance-Modell] Unterteilungsknoten für Kurven
* [Substance-Modell] Graft-Knoten
* [Substance-Modell] Knoten &quot;Filterszene&quot; aktualisieren
* [Substance-Modell] Erkennen von nicht atomaren Knoten im Knotenmenü
* [Substance-Modell] Fügen Sie die Aktion &quot;Open Reference&quot; im Kontextmenü eines Instanzknotens hinzu.
* [Substance-Modell] Hinzufügen einer &quot;View in 3DView&quot;-Aktion im Kontextmenü von Knoten, die an 3DView gesendet werden können
* [Substance-Modell] Zeigt automatisch die Eigenschaften eines Knotens an, nachdem er verfügbar gemacht wurde.
* [Substance-Modell] Fenster &quot;Neues Substance-Modelldiagramm&quot; mit Vorlagenliste erstellen
* [UI] Verbessern der Konsistenz von Bildspeicheroptionen in der 2D- und 3D-Ansicht
* [UI] Benennen Sie &quot;Link > 3D-Mesh&quot; im Kontextmenü des Explorers in &quot;Link > 3D-Szene&quot; um.
* [UI] Layout zurücksetzen wird jetzt auf alle schwebenden Fenster angewendet
* [UI] Verwenden Sie die Beschriftung &quot;Ausgaben in 3D-Ansicht anzeigen&quot; in Kontextmenüs für Diagramme
* [Library] Unterstützung von nicht-atomaren Substance-Modellgrafiken
* [SBSAR] Beschreibung der Support Graph-Ausgaben im SBSAR
* [Shader] Setzen Sie den Standardwert für den Tesselierungsfaktor für alle Shader auf 1.
* [UI] Anzeige des Widgets &quot;2 Schaltflächen&quot; für boolesche Parameter
* [Engine] Update auf Version 8.6.4
* [Steam] Optimierter Build für Apple Silicon Chipsatz (Apple M1 / M2)

**Fest:**

* [UI] Beheben von Skalierungsproblemen für Bildschirme mit hoher DPI
* [UI] &#39;$(udim)&#39;-Vorlage fehlt in der Liste im Backing-Fenster
* [UI] Absturz bei Anzeige des Knotenmenüs am rechten Rand des Bildschirms (nur macOS)
* [UI] Erweiterungsschaltfläche im Menü &quot;3D-Ansicht&quot; ist nicht sichtbar
* [UI] Erweiterungsmenü der Diagrammsymbolleiste ist unvollständig
* [UI] Falscher Parameter-Widget-Wert nach Rückgängigmachen der Aktivierung des harten Bereichs
* [3D-Ansicht] Die nicht standardmäßige Shader-Einstellung geht auf dem Iran von einer Sitzung zu einer anderen verloren
* [Bäcker] Absturz beim Laden des Backfensters mit einer Szene ohne Gitter
* [Funktion] Absturz beim Kopieren einer Instanz in das referenzierte Diagramm
* [Funktion] Beheben eines möglichen Absturzes beim Manipulieren von Knoten
* [Globalization] Italic ist nicht immer korrekt auf Japanisch/Koreanisch/Chinesisch deaktiviert
* [Graph] Falsche Fallback-ID für neue MDL- und Substance-Modelldiagramme
* [Graph] Geerbte Parameter, die von Werten gesteuert werden, werden manchmal falsch berechnet
* [GraphRender] Absturz beim Wechseln von Engines während der Berechnung des hochauflösenden Diagramms (nur macOS)

### 12.2.1

*(Freigegeben: 04. August 2022)*

**Fest:**

* [Graph] Falsche Ergebnisse beim Ändern der übergeordneten Größe des Diagramms
* [Absturz] Absturz beim Berechnen des Substance-Compositing-Diagramms mit sehr hoher Auflösung
* [Absturz] Absturz, wenn beim Laden des Pakets nicht mehr genügend Speicher zur Verfügung steht
* [Absturz] Absturz bei Verwendung von Klammern in den Anmerkungen des angezeigten Parameters in einem Substance-Modelldiagramm
* [Absturz] Verbessern der Stabilität beim Rendern von Substance-Compositing-Graphen
* [Iray] Update auf Version 2021.1.6

### 12.2.0

*(Freigegeben: 19. Juli 2022)*

**Hinzugefügt:**

* [Apple] Unterstützung für natives Apple-Chip (M1) (nur Creative Cloud-Version)
* [Substance-Modelldiagramm] Anzeigen von Knoten-QuickInfos in der Diagrammansicht
* [Substance-Modelldiagramm] Anzeigen von Knoten-QuickInfos in Library
* [Substance-Modelldiagramm] Hinzufügen eines Kontextmenüeintrags zu Vorschauknoten
* [Substance-Modelldiagramm] Benutzer kann Verknüpfungen für Knotenerstellung erstellen
* [UI] Hinzufügen der Option &quot;Ausgabe in 2D-Ansicht anzeigen&quot; im Kontextmenü des Compositing-Graphen
* [UI] Teilen Sie die Einstellung &quot;Automatische Anzeige der Ausgaben&quot; in spezifische Einstellungen für 2D-Ansicht/3D-Ansicht auf.
* [UI] Hinzufügen eines Dropdown-Pfeils und einer QuickInfo zur Schaltfläche &quot;Ausgabe anzeigen&quot; in der Symbolleiste der 2D-Ansicht
* [UI] Elemente im Bedienfeld &quot;Informationen&quot; des Explorers umformulieren und neu ordnen
* [Farbmanagement] Fügen Sie &quot;Linear Adobe RGB (1998)&quot; und &quot;Adobe RGB (1998)&quot; hinzu, um Farbräume für Adobe ACE zu exportieren
* [Farbmanagement] Hinzufügen des &quot;Linear Adobe RGB (1998)&quot;-Arbeitsfarbraums für Adobe ACE
* [Farbmanagement] Unterstützung für OCIO ICC-Displays hinzufügen
* [Farbmanagement] Adobe RGB-Arbeitsfarbraum in ACE-Voreinstellungen ausblenden
* [Farbmanagement] Verbessern der Qualität von gebackenen 3D-LUTs im ACE-Modus
* [Farbmanagement] Verwenden Sie das neue GPU-Backend im 3D-Viewer
* [Lokalisierung] Vollständige Aktualisierung der koreanischen Sprache
* [Engine] Update auf Version 8.6.0
* [Graph] Weisen Sie einen Standarddiagrammbezeichner zu, wenn diese Eigenschaft leer gelassen wird
* [Bibliothek] Deaktivieren von QuickInfo-Hyperlinks für Nicht-Instanzknoten
* [NewProject] Standardauflösung aktualisieren
* [Vorlagen] CLO-Vorlage hinzufügen
* [API] Stellen Sie die defaultParentSize-Eigenschaft für SDSBSCompGraph-Objekte bereit.
* [Abhängigkeiten] Aktualisieren Sie Alembic auf Version 1.8.3
* [Abhängigkeiten] Aktualisieren von AXF auf Version 1.9.0
* [Abhängigkeiten] Update Boost auf Version 1.76
* [Abhängigkeiten] Aktualisieren Sie FBX auf Version 2020.2.1
* [Abhängigkeiten] Aktualisieren von IRay auf Version 2021.1.0
* [Abhängigkeiten] Update OpenColorIO auf Version 2.1.1
* [Abhängigkeiten] Update OpenEXR auf Version 3.1.5
* [Abhängigkeiten] Update TBB auf Version 2020.3
* [Abhängigkeiten] Aktualisieren Sie USD auf Version 0.22.3
* [Entfernen] Deaktivieren der Post-Effects-Funktion (Yebis)
* [Entfernen] Entfernen des Befehls &quot;Rendering in Artstation speichern&quot; aus dem Menü &quot;3D-Ansicht&quot;

**Fest:**

* [Substance-Modelle] Der für den angezeigten Parameter festgelegte Hartbereich wird beim Aufheben der Belichtung gespeichert
* [Substance-Modelle] Bezeichner ist auf Konstantknoten nicht benutzerfreundlich
* [Substance-Modelle] Verbessern der Suche basierend auf Knotenkompatibilität
* [UI] Die Reihenfolge des Untermenüs &quot;Neu&quot; ist für Ordnerressourcen falsch
* [UI] Die Standardgröße des Hauptfensters ist sehr klein
* [UI] Symbolleisten sind nicht von der Option &quot;Layout zurücksetzen&quot; betroffen
* [UI] Sichtbares Transparenzraster auf dem Schriftenressourcensymbol im Explorer
* [Cooker] Compositing-Graphen, die im MDL-Graphen instanziiert werden, werden immer vollständig wiederhergestellt.
* [Graph] Absturz beim Einfügen eines Knotens, der aus einem Diagramm mit leerem Bezeichner kopiert wurde
* [MDL] Absturz beim Schließen eines bestimmten MDL-Diagramms
* [Leistung] Anwendung reagiert nicht, wenn sehr große Pakete geladen werden
* [Ressourcen] 3D-Szenenressource kann in einem bestimmten Fall importiert werden

### 12.1.1

*(Freigegeben: 7. Juni 2022)*

**Fest:**

* [Content] Die Ressource &quot;bluenoise\_256&quot; hat in einigen Knoten das Attribut &quot;colorspace&quot; definiert.
* [Inhalt] Knoten &quot;Größe abrufen&quot; werden nicht in der Bibliothek angezeigt und die Graustufenversion ist falsch bezeichnet
* [Inhalt] Der Parameter &quot;Random Color Seed&quot; in 2D Voronoi-Knoten hat keine Auswirkungen
* [SBSRender] Exportieren eines Diagramms in EXR erzeugt nicht den gleichen bpc wie Designer
* [Substance-Modelle] &quot;Gamma-Typ&quot; sollte nicht in den Eigenschaften des angezeigten Parameters angezeigt werden
* [Substance-Modelle] Absturz bei Verwendung von Klammern in den Anmerkungen des angezeigten Parameters

### 12.1.0

*(Freigegeben: 26. April 2022)*

**Hinzugefügt:**

* [Main] Neuer Inhalt für Materialdiagramme
* [Main] Materialien an Stager senden
* [Main] Unterstützung von USD-Dateien
* [Main] Verbessern der Fehlerberichterstattung in der Benutzeroberfläche
* [Main] Szenenmanagement-Knoten für Modellgrafiken
* [Inhalt] Weitere Optionen zu 3D-Perlin-Rauschen hinzufügen (Kacheln, Absolut...)
* [Inhalt] Neuer Fraktalknoten &quot;3D-Ridge Noise&quot;
* [Inhalt] Neuer Knoten &quot;3D-Texturversatz&quot;
* [Inhalt] Neuer Knoten 3D-Texturposition
* [Inhalt] Neuer Knoten 3D-Struktur rendern Oberfläche
* [Inhalt] Neuer Knoten &quot;3D-Textur-Rendervolumen&quot;
* [Inhalt] Neuer 3D-Textur-Vorzeichenbehaftetes Abstandsfeld-Knoten
* [Inhalt] Neuer Knoten für automatisches Freistellen
* [Inhalt] Neue Beschleunigungsfunktionen
* [Inhalt] Neue Extend Shape-Knoten
* [Content] Neue Schmutz Maps
* [Inhalt] Neuer Knoten für ungleichmäßige Drehung
* [Inhalt] Neuer Tabellenfilter für summierte Bereiche
* [Inhalt] Neuer Kachel-Zufallsgenerator 2
* [Inhalt] Neuer Triangle Grid-Mustergenerator
* [Inhalt] Neue Version des Knotens &quot;Graustufen quantisieren&quot;
* [Inhalt] Neue Voronoi- und Voronoi-Fraktalrauschen (2D/3D)
* Schwellenwert [Inhalt]: Vergleichsmodus &quot;Unterer&quot; und &quot;Unterer und gleicher&quot; hinzufügen
* [Inhalt]&#x200B;[3D-Ansicht] Fügen Sie den ausgelieferten Ressourcen eine Gitteranpassung für die Anzeige von Stoffen hinzu.
* [Substance-Modelle] Neuer Knoten &quot;Gruppeninstanzen erweitern&quot;
* [Substance-Modelle] Neuer Fuse-Knoten
* [Substance-Modelle] Neuer Knoten Umbenennen
* [Substance-Modelle] Neuer übergeordneter Knoten
* [Substance-Modelle] Neuer Set Pivot-Knoten
* [Substance-Modelle] Update auf SDK 1.6.0
* [UI] Verbessern des Verhaltens des Knotenmenüs bei Fehlklick
* [UI] Öffnen Sie Untergraph auf derselben Registerkarte, auch wenn sie angeheftet sind
* [UI] Schaltfläche &quot;Pin entfernen&quot; in der Titelleiste des Explorer-Bedienfelds
* [UI] Speichern Sie die Option &quot;Nicht mehr anzeigen&quot; auf dem Begrüßungsbildschirm in allen Versionen
* [ThirdParty] Upgrade Qt (und QtForPython) auf 5.15.8
* [Drittanbieter] Upgrade von Python auf 3.9.9
* [Drittanbieter] Upgrade von OpenSSL auf 1.1.1m
* [3D-Ansicht] Die Rastereinheit im Viewport anzeigen, wenn der &quot;Achsen&quot;-Helfer aktiviert ist
* [Automatisierung] Bereitstellen des Absbaker-Befehlszeilentools mit Designer
* [Farbmanagement] Implementieren eines neuen GPU-Backends für Adobe ACE
* [Cooker] Fügen Sie eine Option hinzu, um ein Paket ohne Zeitstempel zu kochen
* [Graph] Hinzufügen von Abzeichen im FxMap-Diagramm
* [Library] Neuen Filter für Easings-Funktionen hinzufügen
* [Player] USD-Unterstützung
* [Eigenschaften] Hinzufügen eines Warnfehlers für den Parameter &quot;PKG-Ressourcenpfad&quot; eines Bitmap-Knotens, wenn die Ressource nicht gefunden wird
* [Substance Engine] Upgrade auf 8.4.1
* [Yebis] Warnen Sie den Benutzer, dass Yebis-Post-Effekte in der nächsten Version entfernt werden
* [Dokumentation] Neue Seite &quot;Warnungen und Fehler&quot;
* [Dokumentation] Neue Seite zur Beschreibung der Vererbung in Substance-Kompositionsdiagrammen
* [Dokumentation] Abschnitt &quot;Iray&quot; aktualisieren
* [Dokumentation] Abschnitt &quot;MDL-Diagramme&quot; aktualisieren

**Fest:**

* [UI] Beschneidungsprobleme in den QuickInfos für Vorlagen im neuen Diagrammfenster
* [UI] Schwer lesbarer weißer Text in Knoten bei Verwendung des Dunkelmodus in macOS
* [UI] Layoutproblem in einigen Dialogfeldern
* [UI] Beim Erstellen eines Substance-Funktionsdiagramms im Explorer wird eine Warnmeldung angezeigt, die abgeschnitten ist.
* [UX] Der Farbwähler bewegt sich bei jeder neuen Öffnung nach unten
* [UX] Das Fenster des Verlaufseditors bewegt sich bei jedem Start nach oben
* [UX] Diagrammeigenschaften werden für geladene Pakete nicht automatisch angezeigt
* [Inhalt] Flood Fill Mapper: Falsche Eingabeauswahl in einem bestimmten Fall
* Flood Fill [Inhalt]: Anschnittbereich in Schaltflächen für boolesche Parameter
* [Inhalt] Falscher Bereich für den Parameter &quot;Erster Lichtwinkel&quot; des Knotens &quot;Mehrere Winkel&quot; bis &quot;Normal&quot;
* [Substance-Modelle] Eigenschaften des Knotens zeigen Bezeichner anstelle der Bezeichnung an
* [Substance-Modelle]&#x200B;[3D-Ansicht] Aktualisierungsproblem beim erneuten Öffnen eines Projekts
* [Substance-Modelle]&#x200B;[3Dview] Aktualisierungsproblem bei Verwendung der Drahtgitter-Vorschau
* [Parameter] Absturz beim Löschen von Diagrammeingaben in schneller Abfolge in einem bestimmten Fall
* [Parameter] Absturz beim Zurücksetzen eines Instanzparameters während der Bearbeitung seiner Referenzbeschreibung
* [Bitmap] UDIM-Erkennung wird nicht für Bitmap-Dateien ausgelöst, die im Diagramm abgelegt wurden
* [Graph] Bitmap-/SVG-Knoten werden nicht ungültig, wenn die Ressource nach dem Laden des Pakets auf der Festplatte geändert wird
* [GraphRender] Speicherleck, wenn die Substance-Diagrammauswertung abgebrochen wird
* [Localization] Die Zeichenfolge &quot;Alle Maps für diese Ressource erneut erstellen&quot; wird nicht lokalisiert angezeigt.
* [MDL] Verfügbarer Parameter initialisiert auf 0, wenn der Eingang mit einem nicht verbundenen Punktknoten verbunden ist
* [Voreinstellungen] QuickInfos werden auch dann angezeigt, wenn sich der Cursor in einem leeren Bereich befindet
* [Eigenschaften] Durch Rückgängigmachen einer Änderung des Farbraumwerts wird der Standardwert in einem bestimmten Fall festgelegt
* [Text] Der Schriftartwechsel kann nicht rückgängig gemacht werden, um eine fehlende Schriftartenressource zu erhalten

## Version 11

### 11.3.3

*(Freigegeben: 1. Februar 2022)*

**Fest:**

* [Substance-Modelle] Bereiche können in einigen Fällen verloren gehen
* [Substance-Modelle]&#x200B;[Exportieren] Die Skalierung variiert je nach Dateityp.
* [Substance-Modelle]&#x200B;[Exportieren] Gitter werden dupliziert.

### 11.3.2

*(Freigegeben: 25. Januar 2022)*

**Hinzugefügt:**

* [Dokumentation] Abschnitt &quot;Iray&quot; aktualisieren

**Fest:**

* [Substance-Modelle] Paket, das Substance-Modelldiagramme enthält, kann nicht veröffentlicht werden
* [Substance-Modelle] In bestimmten Fällen kann ein Modelldiagramm nicht exportiert werden.
* [Substance-Modelle] Konsistentere Parameterbereiche
* [MDL] Absturz beim Exportieren der MDLE-Datei
* [MDL] Falsche MDL-Datei generiert, wenn ein MDL-Diagramm Punktknoten enthält, die mit den verfügbaren Parametern verbunden sind
* [2D-Ansicht] Optimieren der Anzeige von Malwerkzeugen
* [Inhalt] Inkonsistente Einrichtung von Parametern für die Ausgabegröße in den Quelldiagrammen der Vorlage
* [Eigenschaften] Beschriftungen von Soft-/Hard-Bereichen sind im Eigenschaftenfenster für MDL- und Substance-exponierte Knoten falsch
* [Vorlagen] Aktualisieren Sie die Standardwerte der Eingaben in der Vorlage &quot;Sampler-Filter&quot;

### 11.3.1

*(Freigegeben: 13. Dezember 2021)*

**Hinzugefügt:**

* [Graph] Hinzufügen einer Warnung beim Löschen eines Graphen, der in einem anderen Graph/Paket verwendet wird

**Fest:**

* [UI] Der Farbeditor ist zu klein, wenn ein bestimmtes UI-Layout verwendet wird
* [UI] Absturz beim Aktualisieren der Liste der zuletzt verwendeten Vorlagen
* [UI] Falsche Markierung in den Voreinstellungen für Tastaturbefehle
* [UI] Die Größe des Hauptfensters ist nach dem Neustart einer Sitzung in einem Fenster zu klein (nur macOS)
* [UI] Maximiertes Dock wird beim Beenden nicht minimiert (nur Windows)
* [UI] Fehlender Platz in der Tooltip für den Parameter &quot;Level Out High&quot;[3DView] Achse in der 3D-Ansicht ist zu klein, wenn der Begrenzungsrahmen der Szene dünn ist
* [UI] Stilproblem bei einigen Texten in den Projekteinstellungen für die französische Sprache
* [Substance-Modelle] Das Klemmen auf belichteten Parametern wird nicht sitzungsübergreifend gespeichert
* [Substance-Modelle] Der Umschalt-Modifizierer ist nach Verwendung des Knotenvorschau-Kurzbefehls weiterhin aktiviert
* [Substance-Modelle] Einige gelöschte Knoten verbleiben im exportierten SBSM
* [Substance-Modelle] Zielknoten der Auswertung akkumulieren und werden nicht gelöscht[API] Absturz beim Rendern des Kurvenknotens, welche Eigenschaften über API festgelegt wurden
* [Bäcker] Widget &quot;Materialfarbe&quot; ist nicht sichtbar und funktioniert nicht wie erwartet
* [Content] PBR-Rendering-Node: interne Berechnung, die nicht mit der Auflösung des Knotens durchgeführt wird
* [Funktionsdiagramm] Meldungen, die die erwarteten Typen anzeigen, sind in einigen Fällen falsch
* [Graph] Eingabe relativ zur Eingabe: geerbte Parameter sind bei verbundenen Instanzen falsch
* [MDL] Substance-Graph-Instanzen werden in MDL-Graphen nicht zuverlässig aktualisiert
* [Publish] Veröffentlichen des Diagramms mit zirkulären Abhängigkeiten ist fehlgeschlagen.
* [Tastaturbefehle] Umschalt+Leertaste sollte kein zuweisbarer Tastaturbefehl für Knoten sein
* [Vorlagen] Das Ausgabeformat benutzerdefinierter Vorlagen wird ignoriert.

### 11.3.0

*(Freigegeben: 24. November 2021)*

**Hinzugefügt:**

* [Substance-Modelle] Hinzufügen von QuickInfos für Knotenparameter
* [Substance-Modelle] Anzeigen des Ergebnisses eines Zwischenknotens im Overlay im 3D-Viewport zulassen
* [Substance-Modelle] Verbessern der Anzeige von Basis
* [Substance-Modelle] Behalten Sie die Hierarchie der Objekte beim Exportieren eines Substance-Modelldiagramms nach .fbx bei
* [Substance-Modelle] Unterstützung mehrerer Materialien beim FBX/OBJ-Export aus dem Substance-Modelldiagramm
* [Substance-Modelle]&#x200B;[Inhalt] Partikelknoten
* [Substance-Modelle]&#x200B;[Inhalt] Knoten &quot;Generative Transformation&quot;
* [Substance-Modelle]&#x200B;[Inhalt] Organic Pattern node
* [Substance-Modelle]&#x200B;[Inhalt] Knoten &quot;Partikel aus Instanzen&quot;
* [Substance-Modelle]&#x200B;[Inhalt] Particle Pruning node
* [Substance-Modelle]&#x200B;[Inhalt] Drehknoten
* [Substance-Modelle]&#x200B;[Inhalt] Shell-Knoten
* [Substance-Modelle]&#x200B;[Content] Projektionsknoten
* [Substance-Modelle]&#x200B;[Inhalt] Knoten &quot;Kurven zuschneiden&quot;
* [Substance-Modelle]&#x200B;[Inhalt] Kurve aktualisieren Sampler-Knoten
* [Substance-Modelle]&#x200B;[Inhalt] Mesh Sampler-Knoten aktualisieren
* [Substance-Modelle]&#x200B;[Inhalt] Jitter-Knoten aktualisieren
* Schaltfläche [UX] zum Maximieren der aktuellen Ansicht
* [UX] Neues Diagrammfenster aktualisieren
* [UX] Option &quot;Player herunterladen&quot; im Menü &quot;Extras&quot; hinzufügen und mit &quot;Player suchen&quot; aggregieren
* [UX] Hinzufügen des Eintrags &quot;Alle schließen&quot; zum Dateimenü
* [UX] Konsistente Groß- und Kleinschreibung im gesamten Hauptmenü anwenden
* [UX] Automatische Anzeige der Eigenschaften von duplizierten Diagrammelementen
* [UX] Hinzufügen von Schaltflächen in der Diagrammsymbolleiste, um die konstante Bildschirmgröße für Frame-Titel/Kommentare/Pins zu deaktivieren
* [UX] Schaltflächen zum Kopieren von Versionsinformationen in die Zwischenablage im Dialogfeld &quot;Info&quot;
* [Materialien] Eingänge relativ zu Eingängen
* [Inhalt] Option &quot;Kacheln&quot; für 3D-Perlin-Rauschen hinzufügen
* [Inhalt] Neuer Diffusionsprozessknoten
* [Inhalt] Neue PBR-Rendering-Knotenversion
* [Interoperabilität] SBS und SBSAR von Sampler erhalten
* [Interoperabilität] SBSM an Stager senden
* [3D-Ansicht] Fügen Sie eine Option hinzu, um die Rückseitenschälung zu deaktivieren.
* [3D-Ansicht] Fügen Sie eine Option hinzu, um den Tangentenraum &quot;Scheitelpunkt&quot; anzuzeigen.
* [Explorer] Diagramm im Explorer markieren, wenn Sie auf den Hintergrund der Diagrammansicht doppelklicken
* [Explorer] Entfernen der Option &quot;Durchsuchen&quot; in Kontextmenüs
* [Bäcker] Veraltete Bäcker ausblenden
* [Farbmanagement] Unterstützung für OCIO v2-Konfigurationsdateiregeln hinzufügen
* [Bibliothek] Umbenennen von Kategorien nach Diagrammtypen
* [Voreinstellungen] Automatische Deaktivierung der CPU in den Iray-Hardware-Voreinstellungen, wenn unterstützte CUDA-GPU erkannt wird

**Fest:**

* [Substance-Modelle] Absturz auf Mac bei Verwendung der Option &quot;as sudb&quot; auf .fbx
* [Substance-Modelle] Absturz beim Exportieren nach SBSM in einem bestimmten Fall
* [Substance-Modelle] Exportfehler beim Exportieren von angezeigten Parametern, deren Widgets nie erstellt wurden
* [Substance-Modelle] Zufälliger Absturz beim Öffnen eines Diagramms, der sich auf mehrere .fbx-Dateien bezieht
* [Substance-Modelle] Bereiche werden in den Widgets der angezeigten Parameter nicht dynamisch angewendet.
* [Substance-Modelle] Die Option &quot;Gitter neu laden&quot; funktioniert nicht für Ressourcen, die im Diagramm &quot;Substance-Modelle&quot; verwendet werden
* [Substance-Modelle] In einem bestimmten Fall werden Szenen nicht in einer verfügbaren 3D-Ansicht angezeigt
* [UI] Der Bereich &quot;Deaktivieren&quot; ist in den Materialoptionen zu groß
* [UI] Stilproblem im Dialogfeld &quot;Paketdatei nicht gespeichert&quot;
* [UI] Die Tabulatortaste muss zweimal gedrückt werden, um zwischen Werten zu navigieren
* [UI] Das Zoomen mit der Maus wird zwischen der 3D-Ansicht und anderen Viewports umgekehrt
* [UI] Das Laden eines bereits geöffneten SBS mithilfe der Liste &quot;Zuletzt verwendete Dateien&quot; löst fälschlicherweise die Aufforderung &quot;Paket nicht gefunden&quot; aus.
* [UI]&#x200B;[macOS] Falsches Standard-UI-Layout nach dem Starten der Anwendung
* [UI] Pakete können nicht im Stammverzeichnis eines Laufwerks gespeichert werden (nur Windows)
* [Diagramm] Die Option &quot;In 2D-Ansicht automatisch anzeigen&quot; ist in einem bestimmten Fall inkonsistent
* [Graph] Option &quot;Open Reference&quot; ist für SBSAR-Instanzknoten verfügbar
* [Diagramm] Pin-Eigenschaften werden nur angezeigt, wenn ein Element erstellt wird
* [Graph] Zeichenfolgenregeln werden inkonsistent erzwungen
* [Graph] Absturz beim Speichern eines leeren Diagramms
* [3D-Ansicht] Der Anisotropie-Winkel wird im ASM-Shader invertiert
* [3D-Ansicht] ASM Shader: Linearisierungsprobleme mit SSS-bezogenen Karten
* [3D-Ansicht] Fehlerhaftes OpenGL-Rendering nach dem Schließen zusätzlicher 3D-Ansichten in einem bestimmten Fall
* [3D-Ansicht] Die vordefinierten Kamerapositionen sind in der 3D-Ansicht mit einigen .fbx-Dateien nicht korrekt
* [MDL] &quot;Knoten hinzufügen&quot; aus dem Kontextmenü funktioniert nicht für MDL-Diagramme
* [MDL] Fehler: Die Verbindung des Knotens schlägt fehl, wenn float2.x-Komponenten und Ähnliches verwendet werden (SD 11.1.2)
* [MDL] Absturz beim Öffnen der Datei specific.sbs
* [MDL] Szeneneinheiten pro Meter in Irak sind beim Start der Rendersitzung nicht festgelegt
* [MDL] Einfrieren beim Anpassen eines Lerp-Knotens im MDL-Diagramm
* [MDL] Reihenfolge der Parameter im exportierten MDL-Code
* [Explorer] Leerer Ressourcenordner wird nach Abbruch der Ressourcenerstellung erstellt
* [Explorer] Nur das erste Element eines Pakets kann an den unteren Rand der Liste verschoben werden.
* [Content] RT Bent Normal und RT AO lösen Knotenberechnung in verschachtelten Graphen aus
* [Eingabeknoten] Bitmap in Eingabeknoten wird nicht aktualisiert, wenn sich UDIM ändert
* [Iray] Es wird viel Zeit in Anspruch genommen, wenn versucht wird, eine Substance-Modellszene mit vielen Instanzen anzuzeigen.
* [Voreinstellungen] Leere Zeile beim Abbrechen des Hinzufügens einer Projektdatei
* [Python-Editor] Die Option &quot;Schließen&quot; bleibt nach dem Schließen des letzten Skripts aktiviert und enthält weiterhin seinen Namen æ

### 11.2.2

*(Freigegeben: 28. September 2021)*

**Hinzugefügt:**

* [Eigenschaften] Neue Diagrammtypen für Aufkleber, Atlanten, Umgebungslichter und Lichtstrukturen hinzufügen

**Fest:**

* [UI] Falsches Schnittstellenlayout nach dem Starten der Anwendung
* [Stabilität] Abstürze beheben, wenn Sie den Energiesparmodus unter Windows beenden und Bildschirme anschließen/trennen
* [3D-Ansicht] Das Erstellen einer 3D-Szenenressource aus dem Substance-Modelldiagramm &quot;Szene&quot; hat keine Auswirkungen
* [Angleichen] Enumerationswerte fehlen, wenn der Mischmodus angezeigt wird
* [Exportieren] Der Szenenexport von Substance-Modellen führt zu duplizierter Geometrie
* [MDL] Absturz beim Öffnen einer bestimmten SBS-Datei
* [Gitter] Absturz beim Verknüpfen eines bestimmten Gitters mit fehlerhafter Geometrie
* [Substance-Modelle] Export schlägt fehl, wenn der Standardwert des angezeigten Parameters außerhalb des Soft-Range liegt

### 11.2.1

*(Freigegeben: 27. Juli 2021)*

**Hinzugefügt:**

* [Substance-Modell] Update auf Version 1.0.3
* [Substance-Modell] Vervollständigen und verbessern Sie die Dokumentation der Substance-Modelldiagramme
* [Substance-Modell] Protokolle in der Konsole anzeigen
* [Substance-Modell]&#x200B;[ScatterOnCurves] Ändern des Standardwerts für den Abstand
* [Substance-Modell]&#x200B;[ScatterOnCurves] Entfernen des nicht benötigten Parameters &quot;HalfSpaceOddEven&quot;
* [Substance-Modell]&#x200B;[Transformieren] Aktualisieren des weichen Bereichs der Euler-Drehung
* [Publish] Einstellungen im Publish-Fenster speichern
* [Publish] Warnen Sie den Benutzer, wenn mindestens eine Abhängigkeit nicht gespeicherte Änderungen enthält
* [Publish] Feld &quot;Dateipfad&quot; initialisieren
* [Publish] Visuelles Feedback während der Veröffentlichung hinzufügen
* [Interoperabilität] Hinzufügen des Befehls &quot;An Player senden&quot; zum Menü &quot;Senden an&quot;
* [Interoperabilität] Vereinfachen Sie den Arbeitsablauf zum Senden/erneuten Senden an Sampler und Painter
* [API] Fügen Sie SDApplication.getVersion() hinzu, damit die Version der Hostanwendung abgerufen werden kann.
* [Explorer] Hinzufügen einer Open-Aktion zu Substance-Modelldiagrammelementen
* [Graph] Deaktivieren der Aktionen &quot;In 3D-Ansicht anzeigen&quot; für Ghost-Instanzknoten

**Fest:**

* [Substance-Modell] Absturz beim Löschen einer Sequenz
* [Substance-Modell] In einigen Fällen werden die Grundlagen nicht korrekt gezeichnet
* [Substance-Modell] Fehler beim Exportieren bestimmter Projekte
* [Substance-Modell] Materialzuordnung beim Öffnen eines Projekts mit aktiviertem Iran funktioniert nicht
* [Substance-Modell] Der minimale Bereich funktioniert unter bestimmten Umständen nicht richtig
* [Substance-Modell]&#x200B;[Primitiv] Die erste Stufe der Unterteilung in der Icosphäre funktioniert nicht
* [Substance-Modell]&#x200B;[RandomFloat] Korrigieren Sie den Fall, dass Min >= Max.
* [3D-Ansicht] Absturz beim Ziehen und Ablegen von Karten
* [3D-Ansicht] Verfügbare Zeichenfolgen in MDL-Materialien verwenden das Farbraum-Widget.
* [3D-Ansicht]&#x200B;[Bäcker] Übergeordnete Objekte werden nicht korrekt behandelt
* [3D-Ansicht] Warnmeldung zum Verwendungsnamen &quot;heightScale&quot; für ältere .glslfx-Dateien
* [Inhalt] Kochwarnungen im Knoten &quot;Höhenextrusion&quot;
* [Inhalt] RT-Strahlungsknoten wird nicht in der Bibliothek angezeigt
* [Inhalt] RT-Schatten: Warnmeldungen zum Kochen in der Konsole
* [Graph] Absturz beim Öffnen einer Datei mit einigen deaktivierten Knoten
* [Graph] Der Punktknoten funktioniert im MDL-Graph nicht ordnungsgemäß, wenn eine Verknüpfung ausgewählt ist
* [Diagramm] Die Diagrammansicht wird nach dem erneuten Laden eines Pakets nicht automatisch erneut geöffnet
* [Interoperabilität] Fehlerdialogfeld bei Auswahl von &quot;Herunterladen...&quot; beim Senden an den Player
* [Interoperabilität] Das erneute Löschen aller Ausgaben führt zu API-Fehlern.
* [Interoperabilität] Das erneute Schließen unmittelbar nach dem Schließen der Zielanwendung führt zu API-Fehlern
* [Explorer] [Graph] Nach dem erneuten Laden eines Pakets ist das erste geöffnete Diagramm nicht das erste Diagramm des Pakets.
* [Explorer] Neue Diagramme in einem Paket werden je nach Typ nicht auf die gleiche Weise platziert.
* [Explorer] Ein Substance-Modelldiagramm oder eine Szenenressource kann nicht geöffnet werden, nachdem sie in den Explorer verschoben wurde
* [Explorer] Absturz/Einfrieren beim Verschieben eines Substance-Modelldiagramms in die Pakethierarchie
* [Library] SBSAR-Dateien verbleiben am Speicherort für temporäre Dateien.
* [Library] XML-Dateien verbleiben im Speicherort für temporäre Dateien.
* [Player] Material hat keine Auswirkungen in der 3D-Ansicht, wenn die Sprache auf Japanisch eingestellt ist
* [Player] Download-Link für Substance Player ist veraltet
* [Farb-Widget] Das Farbeditor-Fenster wird an den oberen Rand des Bildschirms verschoben.
* [IRay] Beheben Sie das Laden des IRay-Moduls unter Windows, wenn das App-Verzeichnis Nicht-ASCII-Zeichen enthält
* [Voreinstellungen] Das MDL-Bedienfeld wird im Projekt zweimal angezeigt
* [API] FxMap-Knoten unterstützen getPropertyGraph() nicht.

### 11.2.0

*(Freigegeben: 23. Juni 2021)*

**Hinzugefügt:**

* [Branding] Substance Designer wird zu Adobe Substance 3D Designer
* [Substance Models] Neue Substance-Modellgrafiken zur Erstellung prozeduraler 3D-
* [Inhalt] Neue HDR-Umgebungszuordnungen hinzufügen
* [Inhalt] Neuer Knoten Gebogenes Normal
* [Inhalt] Neuer Knoten &quot;RT Ambient Verdeckung&quot;
* [Inhalt] Neuer RT-Kaustikknoten
* [Inhalt] Neuer RT-Kaustikknoten
* [Inhalt] Neuer RT-Bestrahlungsknoten
* [Inhalt] Neuer Knoten &quot;RT Shadows&quot;
* [Interoperabilität] Element an Painter senden startet Painter und fügt das Element der Bibliothek hinzu oder aktualisiert es (Adobe Substance 3D erforderlich).
* [Interoperabilität] Element an Sampler senden startet Sampler und fügt das Element der Bibliothek hinzu oder aktualisiert es (Adobe Substance 3D erforderlich).
* [Interoperabilität] Durchsuchen Sie Ihr Asset in Adobe Bridge und starten Sie Bridge am Speicherort des Assets (erfordert ein Adobe Substance 3D-Abo).
* [ASM] Unterstützung des neuen Adobe-Standardmaterials (ASM) in Substance-Grafen und MDL Graph
* [ASM] ASM-Vorlagen hinzufügen
* [ASM] OpenGL-Shader für ASM hinzufügen
* [ASM] ASM-Shader als Standard-Shader festlegen
* [Allgemein] Aggregieren aller temporären Dateien in das vom Benutzer festgelegte temporäre Verzeichnis
* [Allgemein] Neuer Befehl &quot;Kopie speichern unter&quot;
* [Allgemein] Menü &quot;Datei aktualisieren&quot;
* [Allgemein] Menü &quot;Hilfe aktualisieren&quot;
* [Publish] Neues Veröffentlichungsfenster
* [Publish] Fügen Sie in den Einstellungen die Option hinzu, um die SBS-Datei beim Veröffentlichen einer SBSAR-Datei nicht zu speichern
* [Eigenschaften] Hinzufügen eines Diagrammtypfelds zu den Diagrammeigenschaften
* [Eigenschaften] Ordnen Sie die Eigenschaften von Graphen relevanter an
* [Branding] Fenster &quot;Neues Info&quot;
* [Branding] Anwendungsstil aktualisieren
* [GLSLFX] Hinzufügen eines Labels zu Techniken
* [GLSLFX] Fügen Sie die Möglichkeit hinzu, die Beschriftung eines GLSLFX-Shaders festzulegen.
* [Metadaten] Hinzufügen von Metadaten zu den Paketressourcen
* [Metadaten] Metadaten-Edition für Diagramme, Eingaben, Ausgaben und Ressourcen zulassen
* [Lokalisierung] Neue Übersetzungen in Deutsch, Französisch und vereinfachtem Chinesisch
* [UX] Zoom in der 3D-Ansicht bei Ziehen mit der Maus umkehren
* [AXF] Update auf Version 1.8.0
* [Protokolle] Hinzufügen installierter Plug-ins zu den Protokollen
* [VFX] ACES 1.2 OpenColorIO-Konfiguration hinzufügen
* [Python-API] Hinzufügen einer Methode zum Abfragen des in den Einstellungen angegebenen TMP-Verzeichnisses
* [Python-API] Hinzufügen einer isModified-Methode zu SDPackage, um zu überprüfen, ob ein Paket gespeichert ist
* [Python-API] Hinzufügen einiger Farbkonvertierungsmethoden zu SDColorManagementEngine
* [Python API] Löschen von Diagrammobjekten (Kommentare, Pins, Rahmen, ...)
* [Python-API] Eigenschaft &quot;Physische Größe verfügbar machen&quot; für Knoten der Grapheninstanz
* [Python API] Verfügbarmachen und Speichern einer Kopie als
* [Python-API] SDPackageMgr.savePackage-Methode reparieren
* [Python API] Liste der ausgewählten Diagrammobjekte abrufen
* [Python-API] Einführung neuer Methodennamen für die Arbeit mit Diagrammauswahlen
* [Python-API] Plug-ins können dem zuerst erstellten Explorer-Bedienfeld keine Aktionen hinzufügen

**Fest:**

* [Parameter] Negative Werte bei Dropdown-Integer1-Parametern führen zu inkongruentem Verhalten in der Instanz
* [Parameter] Problem beim Erhöhen eines Werts auf einem Winkel-Widget
* [Graph] Timing-Probleme bei der Anzeige der Ausgabe in der 2D- oder 3D-Ansicht.
* [Internationalisierung] Einige bestimmte Zeichen werden in Leerzeichen in Dateikennungen geändert.
* [Voreinstellungen] Die Dateibezeichnung &quot;Benutzerprojekt&quot; wird nicht aus dem Japanischen zurückübersetzt
* [Python-API] RecursionError beim Ausführen der SDUIMgr.getCurrentGraphSelectedNodes()-Methode
* [Python-API] SDApplication.getPath(SDApplicationPath.InstallationDir) gibt nichts zurück.
* [Python-API] SDSBSARExporter sendet keine Benachrichtigungen zum Speichern von Dateien

### 11.1.2 (2021.1.2)

*(Freigegeben: 17. März 2021)*

**Fest:**

* [Bibliothek] Miniaturansichten werden nicht konsistent aktualisiert
* [Content] Die Eigenschaft &quot;Vektormorphkurven&quot; der Eigenschaft &quot;Pixelverhältnis&quot; ist auf &quot;Dehnen (Absolut)&quot; festgelegt.
* [Inhalt] Bitmaps, die in Malwerkzeugen verwendet werden, werden im Knotenmenü angezeigt
* [Inhalt] NaN-Ausgabe für flache Farbeingabe im Knoten &quot;Auto-Tonwertkorrektur&quot; mit Gleitkomma-Präzision
* [Engine]&#x200B;[SSE2] &#39;Level in mid&#39;-Wert (anderer Wert als 0,5) führt zu Ausgabe von 1,0
* [Miniatur] Eingabemaps werden auf 256 skaliert
* [UI] Atomic Nodes Tooltips haben falschen Zeilenumbruch

### 11.1.1 (2021.1.1)

*(Freigegeben: 10. Februar 2021)*

**Fest:**

* [3D-Ansicht] Renderproblem bei Verwendung von SBS, die hohe Frequenzen in der normalen Karte haben
* [3D-Ansicht] Bilder werden nicht angewendet, wenn die Ausgabeeigenschaft &quot;Komponente&quot; nicht auf RGBA oder RGB festgelegt ist
* [3D-Ansicht] Szenen werden in bestimmten Situationen nicht korrekt geladen
* [UI] Das Eingabefeld &quot;Texturdatei&quot; im Pinsel-Editor wird vertikal skaliert
* [UI] Schaltflächen zum Anheften und Andocken verschwinden von der Registerkarte, wenn die aktive Registerkarte geschlossen ist
* [Bäcker] Falsches Ergebnis, wenn die globale Bbox von hohen Poly-Netzen den Szenenursprung nicht enthält
* [Farbmanagement] Die Materialeigenschaft &quot;sRGB-Grundfarbtextur&quot; wird im benutzerdefinierten Szenenzustand nicht überschrieben.
* [Console] Die Protokollmeldung &quot;Verfügbare GPUs&quot; listet die GPUs nicht auf und wird nach dem Zufallsprinzip angezeigt
* [Console] Falsche Zeichenfolge bei Verwendung des Batch-Exports protokolliert
* [Inhalt] Der Parameter &quot;Normales Eingabeformat&quot; des Atlas Splitters wirkt sich auf den roten Kanal anstelle des grünen aus
* [Cooker] Absturz oder NaN-Ausgabe bei Verwendung von \*.surface-Bitmaps in SBSAR
* [Engine] Die Ausgabewerte der Verlaufsumsetzung außerhalb des Bereichs werden in einer Schleife auf 0 umgeschaltet, wenn das Ausgabeformat einen Bereich von 0 bis 1 aufweist
* [Parameter] Min-/Max-/Standard-Schieberegler werden im Fenster &quot;Belichtungsparameter&quot; nicht automatisch angepasst
* [SBSAR] Absturz beim Importieren einiger SBSAR
* [SVG] Absturz beim Abbrechen des Ressourcenimports

### 11.1.0 (2021.1.0)

*(Freigegeben: 28. Januar 2021)*

**Hinzugefügt:**

* [Volltonfarben] Unterstützung von Pantone-Farben in Designer
* [Graph] Knoten deaktivieren
* [3D-Ansicht] Exportieren von Tesselierten Meshes aus dem Viewport
* [Internationalisierung] Japanische Version aktualisieren
* [3D-Ansicht] Optimieren Sie den Speicherverbrauch, wenn Sie Iray nicht verwenden.
* [Python-API] Fügen Sie die Methode SDResource.delete() hinzu, um eine SDResource zu löschen.
* [Python-API] Unterstützung für Volltonfarben zur Python-API hinzufügen
* [Python-API] Neuer Rückruf, der ausgelöst wird, wenn ein Paket geschlossen wird
* [2D-Ansicht] Konvertieren der Pinseldatenbank aus SQLite in das Json-Format
* [2D-Ansicht] Verbessern der Rendering-Leistung und -Zuverlässigkeit (CPU-Berechnung)
* [Library] Option &quot;Muster ausschließen&quot; in den Projekteinstellungen hinzufügen
* [Library] Benennen Sie &quot;Muster ausschließen&quot; in &quot;Dateierweiterungen ausschließen&quot; in den Projekteinstellungen um.
* [UX] &quot;?&quot; entfernen in Fenstertitelleisten auf Windows
* [UX] Verschieben Sie die Tastenkombination Strg+E auf &quot;Referenz öffnen&quot;, wenn die kontextbezogene Bearbeitung deaktiviert ist
* [Bäcker] Vorschaucache löschen, wenn ein Bäcker in der Backliste gelöscht wird
* [Leistung] Verbessern des Image-Cache-Budgets für Hardware mit GPU mit gemeinsam genutztem Speicher
* [Voreinstellungen] Anpassen des Werts &quot;GPU-Cache-Grenze&quot; an den verfügbaren Speicherpool
* [Eigenschaften] Physische Größe-Attribut auf Knoteninstanz anzeigen
* [Scripting] Externes Skripterstellungssystem als veraltet markieren
* [Freigeben] Entfernen der Funktionen &quot;Auf Substance share exportieren&quot;

**Fest:**

* [Content] Inkonsistente E/A-Reihenfolge auf Materialknoten
* [Inhalt] Primäre Eingabe auf Warp-Knoten ist inkonsistent
* [Inhalt] Beheben Sie Cooker-Warnungen vom Knoten &quot;Radial-Weichzeichner&quot;.
* [Exportieren] Batch-Export mit CPU-Engine verwendet VRAM zur Bestimmung des Speicherbudgets
* [Exportieren] Exportieren in einen Pfad, der nicht vorhanden ist, erstellt die Ordner
* [Export] Das Arbeitsspeicherbudget ist zu niedrig, wenn Batch-Export verwendet wird
* [2D-Ansicht] Artefakte/Banding beim Kopieren von HDR-Bildern in die Zwischenablage
* [2D-Ansicht] Exportieren von Bildern aus Ressourcen exportiert immer 8 Bit
* [3D-Ansicht] Irak: Ändern des Normalwerts mit dem Editor gibt ein seltsames Ergebnis
* [3D-Ansicht] Irak: Das Deaktivieren des normalen Kanals führt nicht zum richtigen Ergebnis
* [Library] Das Filtern nach URL funktioniert nicht richtig
* [Library] Ressourcen, die einem aus der Bibliothek ausgeschlossenen Muster entsprechen, können nicht manuell importiert werden.
* [Baker] Das Umbenennen eines Bäckers hat keine Auswirkungen auf seinen Eintrag in der 2D-Ansicht-Vorschauliste
* [Explorer] Verlust der Synchronisierung zwischen Explorer und Diagrammdaten
* [Funktionsdiagramm] Absturz beim Festlegen des Funktionsknotens mit nicht übereinstimmendem Ausgabetyp als Ausgabe
* [MDL] SBS-Instanzknoten haben keine Vorschau, Ausgabe 0 und lösen keine Diagrammberechnung aus
* [Python-API] Die Eigenschaft &quot;editor&quot; des Eingabeparameters kann nicht geändert werden
* [Python] Das Zurücksetzen des Layouts setzt von Python erstellte Docks nicht korrekt zurück
* [Ressourcen] 32-Bit-PSD-Dokument kann nicht verknüpft/importiert werden.

## Version 10

### 10.2.2 (2020.2.2)

*(Freigegeben: 17. Dezember 2020)*

**Hinzugefügt:**

* [3D-Ansicht] Wiederherstellen der in einer Szenenressource gespeicherten Kameraposition
* [Graph] Entfernen Sie &quot;Eingabeknoten&quot; im Kontextmenü für FXMap und den Wertprozessor.

**Fest:**

* [Content] Inkonsistente E/A-Reihenfolge auf Materialknoten
* [Inhalt] PBR-Rendering: fehlerhafte IBL-Probenahme für den Specular-Beitrag
* [Inhalt] PBR-Rendering: Einige Pixel sind immer transparent.
* [Inhalt] PBR-Rendering: Die UV-Ausgabe ist für die Zylinderform falsch
* [Inhalt] Der Parameter &quot;Musterspezifisch&quot; des Splatter Circular hat keine Auswirkungen
* [MDL] Absturz beim Erstellen und Verbinden eines Knotens
* [MDL] Absturz beim Duplizieren eines color[]-Array-Konstruktors mit angeschlossenem Sichtwerteingang
* [MDL] Absturz beim erneuten Verbinden einer ungültigen Verbindung
* [MDL] Exportierte MDLs haben duplizierte Parameter
* [MDL] Verfügbare Parameter werden nicht in eine MDL-Datei exportiert.
* [Parameter] Ein Knotenparameter kann im SBS in einem bestimmten Fall zweimal definiert werden.
* [Parameter] Absturz beim Abrufen des Ausgabetyps des Funktionsdiagramms eines Parameters
* [Parameter] Absturz beim Auswählen der Option &quot;Belichtete Diagrammeingabe bearbeiten&quot;, wenn keine übereinstimmende Eingabe vorhanden ist
* [3D-Ansicht] Die Verwendung von &quot;Umgebung&quot; wird vom OpenGL-Renderer nicht korrekt berücksichtigt
* [3D-Ansicht] IOR ist 0 und muss in einem bestimmten Fall zurückgesetzt werden
* [3D-Ansicht] UVs von Plane/Plane Hi-res sind versetzt
* [Bitmap] Absturz beim Abbrechen des Ressourcenimports
* [Bitmap] Absturz beim Erstellen eines neuen Bitmap-Knotens mit einem nicht unterstützten Dateityp
* [Abhängigkeiten] Absturz beim Rückgängigmachen von &quot;Relocate&quot; zum Lösen einer Geisterinstanz
* [Funktionsdiagramm] Absturz beim Öffnen des Funktionsdiagramms für einen Parameter
* [Verlaufseditor] Verschieben von Reglern und Tasten protokolliert zu viele Aktionen im Verlaufsstapel
* [Lizenz] Absturz beim Analysieren einer ungültigen license.key-Datei
* [SBSAR] SBSAR-Instanzknoten können nicht aus der Bibliothek erstellt werden, wenn sich exponierte Diagramme in Ordnern befinden.

### 10.2.1 (2020.2.1)

*(Freigegeben: 04. November 2020)*

**Fest:**

* [Allgemein] Absturz beim Verlassen des Windows-Ruhemodus
* [Allgemein] Absturz beim Rückgängigmachen nach dem Laden einer 3D-Szenenressource
* [Engine] Artefaktlinien werden in der Ausgabe des Knoten &quot;Entfernung&quot; in Direct3D angezeigt
* [Engine] Absturz beim Auswählen des Verlaufsumsetzungs-Knotens in einem aktualisierten Diagramm
* [Engine] Keine Warnung, wenn im Kompatibilitätsmodus von Engine v7 ein anderer Standardwert als 0 eingegeben wird
* [3D-Ansicht] &quot;Alle entfernen&quot; hinterlässt Gitter mit vordefinierten Materialien ohne angewendetes Material
* [3D-Ansicht] &quot;Szene zurücksetzen&quot; entfernt alle Texturen aus dem Gitter in Irak
* [3D-Ansicht] OpenGL: Das Ändern des Standardwerts eines Samplers in einer .glslfx-Datei wird in der Benutzeroberfläche nicht korrekt dargestellt
* [3D-Ansicht] Rote und schwarze Pixel am rechten Rand von OpenGL-gerenderten Bildern
* [Abhängigkeiten] Fehlende Abhängigkeiten vom Typ &quot;Andere&quot; können nicht verschoben werden.
* [Abhängigkeiten] Absturz beim Beenden, wenn Dependency Viewer geöffnet ist
* [Graph] Absturz beim Duplizieren eines Ghost Instance-Knotens
* [Diagramm] Die kontextbezogene Bearbeitung ist über Tastenanschlag verfügbar, wenn sie in den Voreinstellungen deaktiviert ist
* [UI] Das Warnfenster &quot;Player suchen&quot; hat einen falschen Titel.
* [UI] Der Aktivierungsassistent hat ein falsches Verhalten.
* [Explorer] Paketdateien können unter Windows immer bearbeitet werden
* [MDL] Absturz beim Laden des Diagramms aus der vorherigen Version mit jetzt ungültigen Verbindungen
* [Eigenschaften] Standardfarbe des Eingabeknotens wird beim Rückgängigmachen nicht aktualisiert
* [SBSRender] ICC-Profile von injizierten Bitmaps werden nicht verwendet.

### 10.2.0 (2020.2.0)

*(Freigegeben: 12. Oktober 2020)*

**Hinzugefügt:**

* [Inhalt] Knoten &quot;Querschnitt&quot; hinzufügen
* [Inhalt] Hinzufügen der Funktion &quot;Cross product vec2&quot; zu functions.sbs
* [Inhalt] Hinzufügen des Werteknotens &quot;Größe abrufen&quot;
* [Inhalt] Hinzufügen der Funktion &quot;Orthogonal vec2&quot; zu functions.sbs
* [Content] Hinzufügen von Durchschnittfunktionen zu functions.sbs
* [Inhalt] Filter &quot;Schwellenwert hinzufügen&quot;
* [Inhalt] Farbabgleich: Hinzufügen einer Maskeneingabe, um anzugeben, wo der Filter angewendet werden soll
* [Inhalt] Tile Generator/Sampler: neue Optionen zur Steuerung der Mustergröße hinzufügen
* [Content] PBR-Rendering-Knoten mit Standardwert für Bildeingaben aktualisieren
* [Parameter] Fügen Sie Warnsymbole hinzu, um Probleme in Instanzparametern hervorzuheben
* [Parameter] Sichtbare If-Anweisungen für Ein-/Ausgänge ignorieren, die Parameter enthalten, auf die eine Funktion angewendet wurde
* [Parameter] Verbessern der UX für die Gruppenzuordnung
* [Parameter] Überarbeitung der Methode zum Anzeigen eines einzelnen Parameters
* [Parameter] Belichtete Parameter hervorheben
* [Parameter] Verbessern Bereinigung nicht verwendeter Parameter
* [Engine] Kurvenknoten: Neue Option zum Ausgeben der Kurvenstruktur
* [Engine] Standardwerte für Eingabebilder
* [Engine] Distanzknoten: neue Entfernungsmodi (Entfernungen Manhattan und Chebyshev)
* [Engine] Verlaufsknoten: Neuer Interpolationsmodus für natürlichere Farbmischung
* [UX] Einige Parameter sind jetzt abhängig von anderen Parametern ausgegraut
* [UX] Akzeptieren Sie 6-stellige RGB-Farben im Hexadezimalfeld des Farbwählers
* [UX] Vermeiden Sie, Kommentareigenschaften anzuzeigen, sobald sie ausgewählt sind
* [UX] Relevante Gruppen anzeigen, wenn mit dem Schreiben eines Gruppennamen begonnen wird
* [UX] Verknüpfung zum erneuten Exportieren von Diagrammausgaben
* [UX] Aussehen aller Dropdown-Textfeld-Kombinationsfelder anders als in regulären Kombinationsfeldern
* [GraphRender] Zeigen Sie Knoten-Miniaturansichten nacheinander an, nicht nur, wenn sie alle berechnet werden.
* [GraphRender] Verbessern der Abbruchverzögerung beim Rendern von Diagrammen
* [GraphRender] Verbessern der Genauigkeit der Rendering-Fortschrittsleiste
* [Miniaturansichten] Automatische Berechnung der Miniaturansichten (Symbol)
* [Miniaturansichten] Überarbeitung der UX, um einem Paket eine Miniaturansicht (Symbol) hinzuzufügen
* [Voreinstellungen] GPU-Raytracing standardmäßig für neue Benutzer aktivieren
* [Voreinstellungen] 3DView / OpenGL / Qualität: Schieberegler zum Ersetzen der Sampleanzahl durch eine intuitivere Auswahlliste
* [Bäcker] Verbessern der Leistung von Nachbearbeitungsprozessen
* [Farbmanagement] Anzeigen des aktuellen Arbeitsfarbraums im Dialogfeld &quot;Voreinstellungen&quot;.
* [Iray] Automatischer Wechsel in den CPU-Modus, wenn keine kompatible GPU vorhanden ist
* [Leistung] Verbessern Sie die Reaktionszeit, um den Knoten zu berechnen, an dem wir interessiert sind (jetzt zuerst berechnet).
* [Python-API] Neue Methode addActionToExplorerToolbar zum Hinzufügen von Symbolen zur Explorer-Symbolleiste
* [Ressourcen] Upgrade auf FBX 2020.0.1
* [iRay] Update für Irak 2020.1.0
* [API] Hinzufügen von Python-Zugriff auf Farbmanagementeinstellungen und -eigenschaften

**Fest:**

* [Diagramm] Das Ändern der übergeordneten Größe oder der UV-Kachel bricht das aktuelle Rendering nicht ab
* [Graph] Absturz beim Verschieben einer Ausgabeverbindung und anschließendem Drücken von Alt+LMB
* [Graph] Absturz beim Verschieben von Verbindungen im Modus &quot;Material&quot; oder &quot;Kompaktes Material&quot;
* [Graph] Eingabeknoten können keine Vorschau von Bitmapressourcen anzeigen
* [Graph] Knotenkompatibilität bei Instanzen unterbrochen
* [Graph] Zu viele Knoten werden ungültig, wenn ein Diagrammparameter geändert wird
* [Inhalt] Die Ausgabeform &quot;Shape Extrude&quot; wird in bestimmten Fällen gespiegelt: neue Version erforderlich, alte Version ist veraltet
* [Inhalt] Falsches Ergebnis bei Verwendung der benutzerdefinierten Farbvariation im Knoten &quot;Farbabgleich&quot;
* [Inhalt] Das Größenverhältnis x x/y in der Atlas Scatter hat den entgegengesetzten Effekt.
* [Inhalt] Das Größenverhältnis x x/y in der Formaufteilung hat den entgegengesetzten Effekt
* [3D-Ansicht] Absturz beim Rückgängigmachen nach dem Laden einer Szenenressource aus einem Paket
* [3D-Ansicht] Benutzerdefinierte Umgebung wird nicht in SBSSCN gespeichert, wenn der Pfad Alias mit Sonderzeichen enthält
* [3D-Ansicht] Das Wechseln des Normalformats in den Materialeinstellungen führt zu gespiegelten Zuständen
* [UI] Schaltflächentext &quot;Als primär festlegen&quot; fließt vom Anzeigebereich über.
* [UI] Die Position des Hauptfensters wird beim Arbeiten im Fenstermodus nicht korrekt wiederhergestellt
* [UI] Text in der Statusleiste wird versetzt, wenn das Fenster im Vollbildmodus angezeigt wird oder wenn der Text in die Nähe des Bildschirmrandes gezogen wird
* [Iray] Absturz mit der Meldung &quot;Ungültiges Tag&quot; beim Hin- und Herschalten zwischen Renderern
* [Iray] Sichtbare Gesichter auf nicht-opaken Oberflächen
* [Vorgaben] Absturz beim Anwenden von Vorgaben in Instanzen einiger Substance Source-Graphen
* [Vorgaben] falscher Name nach Rückgängigmachen auf SBS-Instanz
* [Rendern] Falsches Rendering beim Anpassen eines Parameters im Vorschaumodus
* [Bäcker] Das Aktualisieren mehrerer durch Baking erzeugte Map führt dazu, dass Warnungen einige Backen blockieren.
* [Cooker] Das Anpassen von SBSAR-Knoten in SBS-Instanzen führt zu einer 0-Ausgabe von der Instanz
* [Explorer] Benutzerdefinierte Aliase werden bei Verwendung von &quot;Speichern und auf Substance Player öffnen&quot; nicht weitergegeben
* [Verlaufseditor] Die absolute Farbauswahl wirkt sich nicht auf alle ausgewählten Tasten aus

### 10.1.3 (2020.1.3)

*(Freigegeben: 11. Juni 2020)*

**Hinzugefügt:**

* [Inhalt] Parameter &quot;Matte Farbe&quot; im Knoten &quot;Sicheres Transformieren von Graustufen&quot; anzeigen
* [Inhalt] PBR-Rendering: Option &quot;Hintergrundeingabe&quot; hinzufügen
* [Inhalt] Panorama Lichtknoten: neue Option zum Aufnehmen der Farbe aus dem Hintergrundbild
* [Parameter] Ausblenden von Parametern mit dem Flag &quot;not-supported&quot; aus der Liste des Fensters &quot;Exposé-Parameter&quot;

**Fest:**

* [3D-Ansicht] Absturz beim Wechseln benutzerdefinierter Meshes in einem bestimmten Fall
* [3D-Ansicht] Normalformat ist beim Start immer DirectX
* [Inhalt] 3D-Worley-Rauschen: Artefakt bei Verwendung eines hohen Rastergrößenwerts rendern
* [Inhalt] Die Überblendung von Knoten ist falsch.
* [Inhalt] PBR-Rendering: Cooker-Warnung entfernen
* [Inhalt] PBR-Rendering: result enthält in einigen Fällen negative Farben
* [Cooker] Cache-Injection-Problem für Knoten mit mehreren Ausgabeinstanzen
* [Explorer] Absturz beim Schließen eines Pakets, das ein angezeigtes MDL-Diagramm enthält
* [Schaubild] 2 Durchgänge kochen: Knotentypänderung löst keine Wiederherstellung aus
* [Graph] Absturz beim Löschen von Eingaben während der Verwendung der Verbindung
* [Graph] Link-Endpunkte können in einen leeren Raum verschoben werden.
* [MDL] Absturz beim Abbrechen des MDL-Exports aus dem MaterialX-Diagramm
* [MDL] Fehler beim Abbrechen des Exports nach MDLE
* [Vorgaben] Absturz auf der Registerkarte &quot;Vorgaben&quot; nach dem Ändern des Parametertyps in der Vorgabe
* [Ressourcen] Die Materialliste ist im Kontextmenü des Diagramms für als Nicht-UDIM verknüpfte Gitter leer

### 10.1.2 (2020.1.2)

*(Freigegeben: 27. April 2020)*

**Hinzugefügt:**

* [Inhalt] Alchemist-Filtervorlage hinzufügen
* [Inhalt] PBR-Rendering: Parameter hinzufügen, um die Intensität der Diffus-/Specular-Schatten zu steuern
* [Inhalt] Shape Light-Knoten: Kamerapositionsparameter hinzufügen
* [News] Der Stil &quot;Pfeil&quot; der Gruppe wird bei der ersten Anzeige des Fensters beschädigt
* [Bäcker] Fügen Sie den Z-Shortcut zur 2D-Ansicht hinzu, um das Bild bei 1:1 anzuzeigen.
* [Project] Alias $(PROJECT\_DIR) in der Liste ausblenden
* [Explorer] Erstellen Sie keine benutzerdefinierte Ressource für Ressourcen, die keine Datei auf dem Datenträger sind.

**Fest:**

* [Player] Fehlende Aliase beim Laden von SBS-Paketen melden
* [Player] Zeigt den Wert für Zufallsverteilung in der Dezimalbasis an.
* [Player] Bündelung aller im Substance Designer enthaltenen Umgebungskarten
* [Player] Absturz beim Beenden in macOS High Sierra
* [Player] Pakete, die sbs:// verwenden, können nicht geladen werden.
* [Inhalt] 3D-Worley-Rauschen: Artefakt bei Verwendung eines hohen Rastergrößenwerts rendern
* [Content] Die Eingabe &quot;größer als Null&quot; im Knoten &quot;Welle&quot; wird nicht verwendet.
* [Inhalt] Flächenlicht: Der Weltraumpositionsmodus funktioniert nicht
* [Inhalt] Sphäre Licht: Innenbeleuchtungsposition funktioniert nicht richtig
* [Baker] Absturz beim Backen mit dem Backfenster, während ein &quot;Alle durch Baking erzeugte Map aktualisieren&quot; ausgeführt wird
* [Bäcker] Backen schlägt bei Optix für AO aus Mesh fehl, wenn &quot;Niedrig bis Hoch&quot; mit einer normalen Karte verwendet wird
* [Bäcker] Die Auflösung der Vorschau der UVTiles entspricht nicht der Bildschirmgröße
* [3D-Ansicht] Zugewiesene Bitmaps werden beim Laden einer MDL überschrieben, wenn der Standardwert nicht texture2d ist
* [3D-Ansicht] Widgets für Materialeigenschaften ändern sich, nachdem eine Eigenschaft zurückgesetzt wurde
* [3D-Ansicht] Globale Voreinstellung Normalformat funktioniert nicht mehr
* [MatX] Bibliothek: Die Kategorie &quot;MaterialX-Diagramm&quot; zeigt nicht alle verfügbaren Knoten an.
* [MatX] Das Kontextmenü eines benutzerdefinierten Diagramms kann leere Unterordner im Ordner &#39;Knoten hinzufügen&#39; enthalten
* [SBSAR] Primäre Eingabe wird auf die erste Eingabe in der Liste zurückgesetzt
* [Bibliothek] Nur das erste Diagramm ist von SBSAR mit mehreren Diagrammen enthalten.
* [CustomGraph] Knoten, die nicht Teil des aktuellen Diagrammtyps sind, werden in einigen Fällen automatisch erstellt
* [Iray] Der Parameter &quot;Tiefe&quot; der Box-Projektion funktioniert nicht ordnungsgemäß.
* [Voreinstellungen] Verbessern des Layouts in den Projekteinstellungen
* [Parameter] Absturz beim Verschieben eines Positions-Widgets nach dem Löschen eines Parameters
* [UI] Absturz beim Ändern der Benutzerhierarchie im Ausgabeknoten
* [Graph] Absturz bei Verwendung eines Auswahlfelds für Kommentar und einen gekennzeichneten Knoten

### 10.1.1 (2020.1.1)

*(Freigegeben: 10. April 2020)*

**Fest:**

* [3D-Ansicht] Die Speichernutzung ist zu hoch, wenn an einem Compositing-Diagramm gearbeitet wird
* [Inhalt] Unerwartete Formen in nicht quadratischer Ausgabe von &#39;Polygon&#39;-Knoten
* [Inhalt] PBR-Rendering: Die orthogonale Kamera funktioniert bei Verwendung einer nicht quadratischen Auflösung nicht korrekt
* [Inhalt] PBR-Rendering: Wirbelndes Bokeh erhöht die Helligkeit des Bildrands
* [Farbmanagement] Der Farbwähler im Dialogfeld &quot;Neue Bitmap&quot; ist nicht farbverwaltet.
* [Farbmanagement] Farbwähler in Mal- und Vektorwerkzeugen in der 2D-Ansicht sind nicht farbverwaltet.

### 10.1.0 (2020.1.0)

*(Freigegeben: 9. April 2020)*

**Hinzugefügt:**

* [Shortcuts] Shortcuts-Manager für Knotenerstellung
* [Content] Neuer PBR-Rendering-Knoten
* [Inhalt] Neuer FXAA-Filter
* [Inhalt] Neuer Hald CLUT-Filter
* [Inhalt] Filter in Knoten &quot;Zuschneiden&quot; verfügbar machen
* [3D-Ansicht] Verbessern der Shader-Parameter / Arbeitsablauf für die Texturzuweisung
* [3D-Ansicht] Neuer unbeleuchteter Shader
* [3D-Ansicht] Hinzufügen eines &quot;Skalaren Nullwerts&quot; zu den Versatz-Shadern
* [3D-Ansicht] Fügen Sie eine Option hinzu, um die Viewport-Auflösung herunterzuskalieren, wenn &quot;Hohe DPI&quot; aktiviert ist.
* [3D-Ansicht] GLSLFX: Erlaubt das Festlegen von GUI-Informationen für Sampler (Standard, Min, Max, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup).
* [3D-Ansicht] Fügen Sie &quot;Ladezustand mit Gitter...&quot; hinzu. im Menü &quot;Szene&quot;
* [3D-Ansicht] Hinzufügen der tonemapped ACES-Ausgabetransformation im Legacy-Farbmanagementmodus
* [Bäcker] Neue Sampling-Methode in AO, Krümmung, Biegung Normal, Thickness Bäcker
* [Bäcker] Neue Normalisierungsoptionen in Height- und Thickness-Bäcker
* [Farbmanagement] Integrieren von Adobe ACE (Adobe Color Engine)
* [Farbmanagement] Hinzufügen von Optionen zum Festlegen des Standardverhaltens, wenn das ICC-Profil fehlt
* [Parameter] Konsistente Inkrementierung der Regler für Substance Painter
* [Verpacken] Bundle so viele Qt dlls wie möglich für Python-Skripte
* [Projekt] Deaktivieren Sie die Einstellungen für schreibgeschützte Projektdateien, und stellen Sie diesen Status klar
* [Voreinstellungen] Ausblenden spezifischer unklarer Einstellungen im Zusammenhang mit Reaktionszeiten und Berechnungszeiträumen
* [UI] Pow2 umbenennen -> 2Pow
* [Eigenschaften] Anzeige der Compositing-Eigenschaften von Graphen optimieren
* [AXF] Aktualisierung auf AXF SDK 1.7.1

**Fest:**

* [3D-Ansicht] Umgebungslichtparameter sind nicht sichtbar, obwohl sie aktiviert sind
* [3D-Ansicht] glslfx: Das Farb-Widget ist immer ein vec3 ohne Alpha
* [3D-Ansicht] Die Umgebungszuordnung, die aus einer Ressource festgelegt wurde, wird nicht in der Szenenressource gespeichert
* [3D-Ansicht] Irak: Umgebungslicht wird am Ursprung der Szene in ein Punktlicht konvertiert
* [3D-Ansicht] glslfx: Das Farb-Widget ist immer ein vec3 ohne Alpha
* [Parameter] Die URL des Instanzpakets ist in der Attributgruppe nicht korrekt.
* [Parameter] Absturz beim Verfügbarmachen von Parametern
* [Parameter] Symbole werden in den Parametern von Kurvenknoten nicht korrekt ausgerichtet.
* [Parameter] Die Knotenzeichenfolge &quot;Text&quot; wird nur im Vorschaumodus angezeigt, wenn sie angezeigt wird.
* [Parameter] Absturz beim Umbenennen eines in der Anweisung &quot;Visible If&quot; verwendeten Eingabeparameters
* [Parameter] Absturz beim Löschen eines Levels-Knotens, der eine in einem seiner Parameter festgelegte Funktion aufweist
* [UI] Warnsymbol in der Liste der Eingabeparameter wird oben auf einer vorhandenen Schaltfläche platziert
* [UI] Warnungen werden für das richtige Eingabeparameterelement in einem bestimmten Fall nicht gelöscht.
* [UI] Verhindern des &quot;Is mesh UDIM ?&quot;- Popup, das angezeigt wird, wenn sich die Gitter-UVs ausschließlich in der Kachel [0,1] befinden
* [UI] Dropdown-Listen mit Vorgaben können mit dem Mausrad bei einfachem Mauszeiger verschoben werden
* [UI] Option zur Berechnung der Ausgabe(en) in Diagrammattributen ist falsch benannt
* [MDL] Absturz beim Platzieren einer SBS-Diagrammressource in einem MDL-Diagramm
* [MDL] SBS-Knoten mit Bildeingabe funktioniert nicht ordnungsgemäß.
* [MDL] Falsche Texturbindungen und Verwendungsnamen
* [Graph] Eingabewertgruppe und Verwendung werden im Modus &quot;Material&quot; für die Erstellung von Verknüpfungen ignoriert.
* [Graph] Eingabewerte verwenden den Standardwert anstelle von Eingabedaten für Booleans
* [Bäcker] Falsche Normale im World Space Normale Bäcker, der eine tangente Normalmap in bestimmten Fällen verwendet
* [Bäcker] Übermäßige Speichernutzung beim Backen mit geöffnetem Vorschaufenster
* [Vorgaben] Beschädigte Voreinstellung führt zum Absturz beim Rendern
* [Vorgaben] Boolescher Parameter aus altem SBS wird von der Vorgabe nicht beeinflusst.
* [Library] Ressourcen aus dem ersten geöffneten Paket werden im Floating-Menü zur Knotenerstellung aufgeführt.
* [Publish] Veröffentlichung auf SBSAR gibt Fehlercode 13 in SBSCooker auf macOS zurück
* [Publish] Veraltete Argumentwarnung in SBSCooker beim Veröffentlichen in SBSAR
* [API] Die Metadaten können nicht von einem Paket abgerufen werden, das aus einer .sbsar-Datei stammt
* [Exportieren] Im Legacy-Modus wird die Farbraumoption für bestimmte Ausgaben auf die Standardeinstellungen zurückgesetzt
* [2D-Ansicht] Beim Kopieren in die Zwischenablage wird der Farbmanagement-Status nicht berücksichtigt
* [Unix] Designer ignoriert Systemsignale
* [Library] Einige Filter in der Bibliothek funktionieren aufgrund übersetzter Tags nicht richtig
* [Herd] Quadratische Wurzel negativer Zahlen sollte 0 anstelle von NaN zurückgeben
* [2D-Ansicht] Rote und blaue Kanäle werden ausgetauscht, nachdem der erste Malstrich rückgängig gemacht wurde
* [Console] Zu viele Warnmeldungen in der Konsole &quot;QPixmap::scaled: Pixmap ist NULL-Pixelmap&quot;
* [Inhalt] &quot;Glühen in Form&quot;: Kochwarnung
* [Abhängigkeiten] Das Zuweisen eines Diagramms, das sich in einem anderen Paket befindet, zu einem Gitter erzeugt keine Abhängigkeiten
* [Iris] Materialeigenschaften werden nach dem Wechsel der Geometrie inaktiv

## Version 9

### 9.3.3 (2019.3.3)

*(Freigegeben: 14. Februar 2020)*

**Hinzugefügt:**

* [Batch Tools] Versand von Standard-OCIO-Profilen mit Batch Tools

**Fest:**

* [Inhalt] Atlas Scatter: Probleme bei der Verwendung von zufälliger Farbe/Normal in einigen Situationen

### 9.3.2 (2019.3.2)

*(Freigegeben: 04. Februar 2020)*

**Hinzugefügt:**

* [SBSRender] Unterstützung für das Hinzufügen von Farbmanagement

**Fest:**

* [Inhalt] Linearer sRGB-Knoten zu ACEScg: E/A-Beschriftungen sind falsch
* [Inhalt] ACEScg zu sRGB-Knoten: Ausgabebeschriftungen sind falsch
* [Inhalt] Panorama Lichtknoten: Temperaturbereich einstellen
* [Graph] Schwerer Leistungsabfall und Einfrieren beim Anpassen eines verschachtelten Diagramms mit aktiver &quot;In-Context Editing&quot;-Bearbeitung
* [Graph] Absturz beim Löschen mehrerer Knoten in FX-Map
* [Vorstellungen] Der Designer-Prozess kann nach dem Beenden lebendig bleiben

### 9.3.1 (2019.3.1)

*(Freigegeben: 27. Januar 2020)*

**Fest:**

* [Graph] Schwerer Leistungsabfall und Einfrieren beim Anpassen eines verschachtelten Diagramms mit aktivierter Option &quot;Kontextabhängige Bearbeitung&quot;
* [Graph] Von [0, 99] kann kein enum-Wert in Integer1 tweak eingegeben werden.
* [Diagramm] Kommentar wird nicht verschoben, wenn der entsprechende Frame verschoben wird
* [Graph] Eingabenamen fehlen im Knoten der benutzerdefinierten Instanz
* [Diagramm] Miniaturansichten können beim Laden des Diagramms gerendert werden, auch wenn die entsprechende Option in den Voreinstellungen deaktiviert ist
* [2D-Ansicht] Negatives Alpha zeigt Checker an, unabhängig von der Anzeigeoption
* [2D-Ansicht] Die Konvertierung von 32f in 8 Bit schlägt mit hohen Werten fehl.
* [2D-Ansicht] Verzerrung oben/links und &quot;Platz erstellen&quot; legen einige Koordinaten auf große Werte in Vorwärtstransformationsmatrizen fest
* [2D-Ansicht] UVs aller Mesh-Objekte werden nur auf &quot;0&quot;-UV-Sätzen angezeigt.
* [Inhalt] Abgeflachte Kante: Angular-Modus funktioniert nicht ordnungsgemäß auf Kachelmaske
* [Inhalt] Flood Fill zu Verlauf: Der Bildwert der Steigung wird nicht in der Mitte der Form aufgenommen
* Funktion [Inhalt]; &quot;Boolescher Wert für Gleichheit&quot; ist defekt
* [Bäcker] Artefakte bei Verwendung der automatischen Tonzuordnung im Bäcker &quot;Krümmung aus Mesh&quot; in bestimmten Fällen
* [Bäcker] Absturz in DXR beim Backen, während kein Material ausgewählt ist
* [Bäcker] Leistungsproblem in der 2D-Ansicht bei Aktivierung der &quot;Info&quot;
* [Engine] Die Funktion &quot;Pow&quot; gibt bei Verwendung eines sehr niedrigen Eingangswerts und eines hohen Exponenten auf der SSE2-Engine enorme Werte aus.
* [Engine] Absturz bei Verwendung einer hohen JPG-Komprimierung auf Bitmap-Ressourcen
* [Engine] Der Wertprozessor gibt einen falschen $size-Wert zurück, wenn er sich in einem Untergraph befindet.
* [Parameter] Bei Auswahl eines Instanzknotens mit einer hohen Anzahl von Parametern wird ein leeres Popup angezeigt.
* [Parameter] Der Ganzzahlwert wird in Dropdown-Parameterelementen nicht angezeigt.
* [Parameter] Die Schaltfläche &quot;Bearbeiten&quot; der Transformationsmatrix ist im Vorschaumodus nicht verfügbar.
* [Cooker] $size in ValueProcessor ist falsch, wenn innerhalb einer Diagramminstanz
* [Cooker] Die Ausgabegröße ist falsch, wenn der Wert-Link über einen Punktknoten zu einem atomaren Knoten führt
* [UI] Schaltfläche zum Anzeigen aller Elemente in der unteren Leiste der 2D-Ansicht ist nicht sichtbar
* [UI] Die Vorschau ausgewählter RGB-Werte zeigt bei Verwendung des Farbmanagements falsche Zahlen an
* [Exportieren] 16f RGBA-Bilder werden als Graustufen exportiert
* [3D-Ansicht] OBJ mit mehreren Leerzeichen kann nicht importiert werden
* [Farbmanagement] Die OCIO-Konfiguration wird beim Veröffentlichen von SBSAR nicht berücksichtigt.
* [Farb-Widget] Farbschieberbereiche können in einem bestimmten Fall exponentiell erweitert werden
* [Dok] Der Abschnitt &quot;paramValue&quot; ist in der Sbs-Formatreferenz unvollständig
* [MDL] Farb-Widget in SBSAR-Instanzen ist nicht korrekt
* [Vorgaben] Absturz beim Aktualisieren von Vorgaben in einem bestimmten Fall
* [PSD] FreeImage-Fehler beim Laden von PSD-Dateien aus aktuellen Versionen von Photoshop
* [Ressourcen] Absturz beim Rückgängigmachen der Bitmapverknüpfung direkt im Diagramm
* [SVG] SVG-Knoten werden bei Verwendung der Vektorwerkzeuge nicht automatisch aktualisiert

### 9.3.0 (2019.3.0)

*(Freigegeben: 19. Dezember 2019)*

**Hinzugefügt:**

* [Allgemein] Unterstützung des Farbmanagements mithilfe der OpenColorIO-Konfigurationsdatei
* [Vorgaben] Verbessern der Vorgaben-Verwaltung
* [Vorgaben] Synchronisieren von 2D-Ansicht-Gizmos und Vorschau-Schiebereglern
* [Vorgaben] Wiederherstellen von Vorschauwerten beim Wechseln in den Vorschaumodus
* [Vorgaben] Beibehalten des Vorschaumodus beim Bearbeiten anderer Knoten, Ressourcen oder Diagramme
* [Vorgaben] Rückgängig funktioniert reibungslos, wenn Sie zwischen den drei Vorgaben-Registerkarten navigieren
* [Vorgaben] Ermöglicht das Zurücksetzen von Parametern auf den Standardwert des Diagramms oder den Wert der Vorgabe im Vorschaumodus.
* [Vorgaben] Verbesserung des Anheftens von Parametern
* [Vorgaben] Importieren/Exportieren aller Vorgaben eines Diagramms in eine Datei
* [Bäcker] Neuer Bäcker für &quot;Krümmung aus Gitter&quot; auf Basis von Raytracing
* [Bäcker] Fügen Sie die Option &quot;Grundebene&quot; im Bäcker &quot;AO from Mesh&quot; hinzu
* [Bäcker] Fügen Sie die Option &quot;Match by Name&quot; hinzu, um die Rückseite in &quot;AO from Mesh&quot;-Bäcker zu ignorieren
* [Inhalt] Neuer Atlas Scatter-Knoten
* [Inhalt] Neue Farbraum-Konvertierungsknoten und -funktionen (ACEScg)
* [Content] Verbessern der Namenskonsistenz für Knoten mit Farb-/Graustufenversionen
* [Graph] Verbessern der Leistung im Vorgabenvorschaumodus
* [Graph] Hinzufügen eines $(Farbraum)-Makros zum Exportieren der Diagrammausgabeoption
* [Parameter] Wenn ein Parameter auf &quot;unsichtbar&quot; eingestellt ist, blenden Sie das entsprechende Gizmo in der 2D-Ansicht aus.
* [Parameter] Fügen Sie &#39;Graph input group&#39; nicht als Präfix hinzu, wenn Parameter angezeigt werden.
* [Parameter] Hinzufügen einer QuickInfo für &quot;VisibleIf&quot; in Diagrammparametern
* [AXF] AXF SDK auf Version 1.6 aktualisieren

**Fest:**

* [Linux] Designer wird auf CentOS 8 aufgrund eines Qt-Plattformladefehlers nicht gestartet.
* [Linux] WARNUNG: Die Freetype-Bibliothek wurde aus der SD-Anwendung entfernt: Benutzer mit CentOS-Version &lt;= 7.5 müssen sie manuell installieren.
* [AxF] Absturz beim Importieren von Dateien, die mit neueren AxF-Versionen erstellt wurden
* [2DView] Pinseltexturen, die von einer Ressource zugeführt werden, werden nicht angewendet
* [2DView] Absturz beim Ändern der Eingaben des instanzierten Diagramms mit Positionsanpassung
* [3DView] Absturz beim Abbrechen von &quot;Laden...&quot; Aktion
* [3DView] Option &quot;Farbraum hinzufügen&quot; für Emissionstexturen in GLSLFX-Shadern
* [Bäcker] Karten, die durch Ressourcen gespeist werden, werden während des Backens ignoriert.
* [Bäcker] Optionen für &quot;Weltraumrichtung&quot; sind falsch gesperrt
* [Bitmap] EXR-Bitmaps mit Gleitkommawerten werden als schwarzes Bild dargestellt
* [Inhalt] Flood Fill zu indizieren: Formerkennung schlägt in einem bestimmten Fall fehl
* [Inhalt] Freistellen: Sampling-Problem, wenn der Zuschneideknoten eine niedrigere Auflösung als die Eingabe hat
* [Allgemein] Absturz beim Schließen von Designer beim Generieren der Bibliothek
* [Graph] Bitmap-Knoten spiegeln die Komprimierung der zugeordneten Bitmap nicht wider
* [Graph] Cache wird nicht gelöscht, wenn Knoten-Miniaturansichten nach dem ersten Rendern gelöscht werden
* [Graph] Die Knotengröße wurde fälschlicherweise ungültig gemacht.
* [Graph] Absturz, wenn in einigen Fällen Eingangsverbindungen an einem Pixelprozessorknoten geändert werden
* [MDL Graph] Fehler beim Wiederherstellen eines Funktionsaufruf-Standardwert
* [Eigenschaften] Die Schaltflächen &quot;Bearbeiten&quot; und &quot;Transformationsmatrix&quot; in Matrixparametern sind verwirrend.

### 9.2.3 (2019.2.3)

*(Freigegeben: 26. November 2019)*

**Hinzugefügt:**

* [MacOS] Beglaubigen Sie der Software, die neuen MacOS Catalina-Verteilungsanforderungen zu folgen

**Fest:**

* [Bäcker] Absturz beim Backen mit einer Skew-Map-Ressource mit einem ungültigen Link
* [Bäcker] UV-Sets außer 0 werden bei Embree nicht berücksichtigt
* [Bäcker] &quot;Gebeugte Normale aus Mesh&quot; gibt falsche Ergebnisse mit anderen UV-Sätzen als 0 auf DXR aus
* [Bäcker] Die Parameter &quot;UV Set&quot; werden beim erneuten Öffnen des Backfensters auf den Wert &quot;0&quot; zurückgesetzt.
* [Baker] &quot;Position&quot; gibt ein schwarzes Bild mit anderen UV-Sätzen als 0 aus.
* [Inhalt] Smart Auto Tile: Probenahme in 8k
* Atlas Splitter [Inhalt]: Die Formerkennung schlägt in einigen Fällen fehl, der Genauigkeitsparameter sollte angezeigt werden.
* [Content] Pow gibt in einigen Fällen nicht den richtigen Wert zurück.
* [Inhalt] Flood Fill zu indizieren: Falsches Ergebnis bei Veröffentlichung in SBSAR
* [Library] Absturz beim Laden des ersten SBS-Pakets der Sitzung
* [Bibliothek] Die Einstellung &quot;Ressourcen standardmäßig in der Bibliothek anzeigen&quot; wird bei Ressourcen ignoriert, die direkt in das Explorer-Bedienfeld importiert werden
* [Console] Unerwartete Meldung in der Konsole bei Verwendung des Knotenmenüs
* [Parameter] Ein einzelner Eintrag in der Ausgabenverwendungsliste kann nicht entfernt werden.
* [3DView] Die Szene wird nicht korrekt neu geladen, wenn die Szenendatei auf der Festplatte geändert wird[Graph] Die Knotenmenü-Filterung ist falsch, wenn Werteausgaben verwendet werden.

### 9.2.2 (2019.2.2)

*(Freigegeben: 23. Oktober 2019)*

**Fest:**

* [Graph] Die Knotenmenüfilterung ist falsch, wenn Wertausgaben verwendet werden
* [Graph] Absturz bei Anzeige des Knotenmenüs
* [Diagramm] Suchwerkzeug wird angezeigt, wenn ein Umschaltbefehl verwendet wird
* [Graph] Absturz beim aufeinander folgenden Starten von Knotenmenüs aus dem Werteingabe-Connector
* [Diagramm] Kommentare, die lange Zeichenfolgen enthalten, werden beschnitten
* [Graph] Die Flow-Hervorhebung ist falsch, wenn ein Knoten mit dem Ziehen aus dem Konnektormenü erstellt wird
* [Graph] Absturz beim Entfernen aller Diagrammelemente aus der Szene beim Laden eines anderen Diagramms
* [Graph] Absturz bei Verwendung zum Erstellen eines Knotens bei Verwendung von Klick- und Ziehvorgängen vom Connector
* [Graph] Absturz bei Verwendung des Tools &quot;Node Finder&quot;
* [Graph] Ausgabe-Pin-Farbe ist im Modus &quot;Material Compact&quot; falsch
* [Cooker] Knoten hinter Knoten mit mehreren Ausgängen werden nicht korrekt aktualisiert
* [Cooker] Problem mit Value-Ausgaben und Passthrough-Knoten
* [Cooker] Value Processor gibt falsche Ergebnisse aus, wenn nur ein Get-Knoten verwendet wird.
* [Inhalt] Der Knoten &quot;Kontrast/Luminanz&quot; gibt einen Alpha-Wert von 1,0 aus.
* [Inhalt] Vorlage &quot;Studio Panorama&quot; hat keine Beschreibung
* [Inhalt] Flood Fill zu indizieren: Falsches Ergebnis, wenn die Eingabe eine Umbruchform enthält
* [Inhalt] &quot;HDR-Zusammenfügung&quot;: interne Expositionsberechnung ist falsch
* [Punktknoten] Absturz bei Verwendung einer Ebene und eines Punktknotens
* [Abhängigkeits-Manager] Die Aktion &quot;Gehe zu&quot; funktioniert nicht mehr.
* [PSD] Absturz beim Rückgängigmachen des Löschens mehrerer Knoten, die im PSD Exporter enthalten waren
* [UI] Absturz beim Schließen des Diagramms über das Menü &quot;Fenster&quot; und beim erneuten Öffnen, während ein Diagramm angeheftet ist
* [Verlaufseditor] Die Schaltfläche &quot;Taste entfernen&quot; ist zu groß
* [Engine] Genauigkeitsproblem mit sqrt() acos() und asin()
* [Bäcker] AO aus Mesh: Der Schieberegler &quot;Überstreichungswinkel&quot; hat einen falschen Wertebereich, wenn er optimiert wird

### 9.2.1 (2019.2.1)

*(Freigegeben: 20. September 2019)*

**Hinzugefügt:**

* [Vorlagen] Hinzufügen von Standardeingabeknoten zu Specular/Glossiness und zu anderen Vorlagen
* [Vorlagen] Vorlage für PBR-Anisotropie hinzufügen
* [3D-Ansicht] Automatische Clipebene über weite Entfernungen vergrößern
* [3D-Ansicht] PBR-beschichtet: Ändern des Standardwerts für die normale Vererbung von Coat
* Atlas Splitter [Inhalt]: Hinzufügen der Option für die Funktion &quot;Auto-Freistellung&quot;
* [Knotenmenü] Knoten nicht ohne Eingabe filtern

**Fest:**

* Atlas Splitter [Inhalt]: Einige Ausgaben werden bei Verwendung der Option &quot;Auto-Freistellung&quot; nicht korrekt zugeschnitten
* [Inhalt] Material Height Blend: Kochfehler in Zusammenhang mit nicht vorhandenem Parameter
* [Inhalt] &quot;Flächenlicht&quot;: Muster-UV-Modus funktioniert nicht richtig
* [Content] &quot;Height to Normal World Unit&quot;: Eingang wird auf 16 Bit erzwungen
* [Inhalt] Unerwartete Formen bei Verwendung des angular-Knotens &quot;Abgeflachte Kante&quot; ohne Unterteilung in kleine Formen
* [Library] Symbole für SBSAR sind in der Bibliothek nicht sichtbar
* [Bibliothek] Verwenden von &quot;\&quot; zum Filtern der URL funktioniert nicht mehr
* [Library] Bei Filterwerten wird Groß- und Kleinschreibung unterschieden
* [Library] Suchfilter funktioniert nicht, wenn &quot;Compositing&quot; aktiviert ist
* [Bäcker] Durch Doppelklicken auf bestimmte Zellen und Schließen der Änderung werden sie auf falsche Werte zurückgesetzt
* [Baker] Der Backend-Statustext im Baker-Fenster zeigt immer &quot;GPU-Beschleunigung : enable&#39;
* [Cooker] Absturz beim Verarbeiten einer &quot;Hochstapler&quot;-Abhängigkeit in einem Diagramm
* [Cooker] Graustufen-Konvertierung hat falsche Ausgabegröße, wenn Wert verwendet wird
* [Explorer] Absturz beim Verarbeiten von &quot;Publish auf Freigeben&quot;
* [Graph] Absturz beim Öffnen eines bestimmten Pakets
* [MDL] Absturz bei Verwendung des Casting-Operators
* [Vorlagen] Ausgabe-IDs sind in der mit PBR beschichteten Vorlage nicht korrekt.

### 9.2.0 (2019.2.0)

*(Freigegeben: 29. August 2019)*

**Hinzugefügt:**

* [Inhalt] Neue Formen für &quot;Panorama Light&quot;
* [Inhalt] Neuer Filter &quot;Panorama-Nadir Patch&quot;
* [Inhalt] Neuer Filter &quot;Panorama-Nadir Extract&quot;
* [Inhalt] Neuer Filter &quot;Panorama-Horizont begradigen&quot;
* [Inhalt] Neuer Filter &quot;Panorama-Drehung&quot;
* [Inhalt] Neuer Knoten &quot;Panoramaposition&quot;
* [Inhalt] Neuer Knoten &quot;Panorama Physical Sun and Sky&quot;
* [Inhalt] Neue Knoten &quot;Panoramaverläufe&quot;
* [Inhalt] Neuer HDR-Zusammenführungsfilter
* [Inhalt] Neuer Filter &quot;HDR-Vorschau&quot;
* [Inhalt] Neuer Filter &quot;Color Temperature Adjustment&quot;
* [Inhalt] Neuer &#39;Blackbody&#39;-Knoten
* [Inhalt] Neuer Belichtungsfilter
* Menü zur Knotenerstellung [UI]: Anzeigen und Verwalten von Favoriten im Menü
* [UI] Hinzufügen/Entfernen eines Knotens aus den Favoriten aus dem Knotenerstellungsmenü
* Menü zur Knotenerstellung [UI]: Das Menü beim Klicken auf/Ziehen eines Links in einer Ausgabe aufrufen
* Menü zur Knotenerstellung [UI]: den Inhalt nach dem aktuellen Auswahltyp filtern
* [3D-Ansicht] Support-Anisotropie
* [3D-Ansicht] Effekt &quot;Beschichtung unterstützen&quot;
* [3D-Ansicht] Unterstützung von Untergrundstreuung
* [Graph] Punktknoten
* [Graph] Optimieren Sie das Rendern von Graphen durch Zwischenspeichern von Kochergebnissen
* [Voreinstellungen] Ändern Sie den Standardwert für die Begrenzung der Kochgröße auf 8192.
* [Voreinstellungen] Fügen Sie einen Schalter hinzu, um die neue Funktion der Tabulatortaste zu aktivieren/deaktivieren.
* [API] Add SDResource.getPackage()-Methode
* [Iray] Update für NVIDIA Iray RTX 2019.1.3 SDK (317500.3714)
* [Explorer] Verknüpfen eines beliebigen Dateityps als Ressource im Paket zulassen
* [GradientNode] Drücken Sie ESC, um die Auswahl des Verlaufs abzubrechen.
* [Parameter] Automatische Groß-/Kleinschreibung für Bezeichner entfernen
* [Projekt] Fügen Sie eine Option hinzu, um anzugeben, ob Diagramme und Ressourcen standardmäßig &quot;In Bibliothek sichtbar&quot; sind.
* [Vorgaben] Automatische Fixierung geänderter Parameter

**Fest:**

* [MDL] Modul kann aufgrund eines Problems mit dem Parametertyp nicht exportiert werden
* [MDL] Beim Laden ist die exponierte int nicht sichtbar.
* [MDL] Absturz beim MDL-Export
* [MDL] Absturz beim Ändern der Farbe eines Materialoberflächenknotens
* [MDL] void MDLGraphNodeControllerSelector::updateSelectorCurrentMember(const DataMessage&amp; msg) ist beschädigt
* [Graph] Falsche Link-Thickness in der Diagrammanzeige
* [Graph] Beim Anpassen von Parametern werden zu viele Invalidierungen ausgelöst
* [Graph] Absturz beim Schließen eines Pakets, während zwei Fenster davon geöffnet sind, und bei Verwendung der kontextbezogenen Bearbeitung
* [Funktionsdiagramm] Beim Schließen der Funktionsansicht wird keine Warnung angezeigt
* [3D-Ansicht] Absturz bei der Initialisierung der 3D-Ansicht, wenn die Kameraprojektion als &quot;orthografisch&quot; als Standardszenenstatus festgelegt ist
* [3D-Ansicht] DOF-Aufenthalte nach FX in Irak aktiviert
* [2D-Ansicht] Pinselauswahlfenster verschwindet beim Ändern der Pinselgröße
* Informationsbereich [2D-Ansicht]: werden mit einem bestimmten Layout beschnitten
* [2D-Ansicht] Das Bild wird versetzt, wenn das Hauptfenster minimiert und wiederhergestellt wird.
* [Bäcker] Auswahlliste &quot;Aus Ressource&quot; wird nicht richtig gefiltert
* [Bäcker] Absturz beim Verketten von &quot;Farbkarte aus Mesh&quot;- und &quot;Normale Karte aus Mesh&quot;-Bäkern auf Embree
* [Bäcker] Krümmung pro Scheitelpunkt Backen führt zu schweren Artefakten
* [Explorer] Kann UDIM-Ressourcen nicht importieren, indem Sie sie in den Explorer ziehen und ablegen
* [Explorer] Explorer-Fenster wird beim Verknüpfen von Gittern und Schriften nach dem Verknüpfen ungewöhnlicher Dateiformate nicht korrekt gefiltert
* [Explorer] Ressourcen sind sichtbar, wenn im Diagramm &quot;In Bibliothek anzeigen&quot; auf &quot;Nein&quot; gesetzt ist
* [Inhalt] Die Eingaben &quot;Pow&quot; und &quot;clip&quot; sind nicht in der richtigen Reihenfolge.
* [Inhalt] RGBA Merge-Knoteneingaben sind nicht beschriftet
* [Cooker] Ungültige Verbindungen von numerischen Werten werden trotzdem ausgewertet
* [Cooker] Assert beim Verbinden einer Bildeingabe mit einem Eingabewert
* [UI] Der Maus-Cursor bleibt in bestimmten Fällen im Zustand &quot;Skalieren&quot; hängen
* [UI] Beim Rechtsklick in der Paketansicht wird unter Linux nicht das richtige Menü angezeigt
* [Abhängigkeiten] Der Dateipfad der temporären Ressourcen ist nicht korrekt.
* [Abhängigkeiten] Warnung zu fehlenden Bitmapressourcen bleibt nach der Verschiebung aktiv.
* [Bibliothek] Einige Miniaturansichten werden nicht generiert.
* [Library] MDL-Dateien werden in der Bibliothek angezeigt
* [Parameter] Absturz beim Verfügbarmachen von Parametern
* [Parameter] Absturz nach dem Neuerstellen eines neuen Elements in der Dropdown-Liste
* [Export] Fehler beim Export von 8K-Stapeln
* [Vorgaben] Absturz beim Anwenden einer Vorgabe mit booleschen Werten in SBS-Instanzen
* [Scripting] Der Begrüßungsbildschirm wird weiterhin angezeigt, wenn das Befehlszeilenargument &quot;—quit&quot; verwendet wird.

### 9.1.3 (2019.1.3)

*(Freigegeben: 19. August 2019)*

**Fest:**

* [Bäcker] Absturz in DXR, wenn Seitenverhältnisse von Backausgabe und Skew-Map nicht übereinstimmen
* [Bäcker] Der Bäcker &quot;Ambient Verdeckung From Mesh&quot; gibt bei Verwendung einer Normalmap falsche Ergebnisse mit Optix oder DXR aus
* [Bäcker] Der Bäcker &quot;Krümmung&quot; gibt falsche Ergebnisse aus, wenn die Einstellung &quot;Pro Scheitelpunkt&quot; verwendet wird
* [Bäcker] Fehlermeldungen geben das Backend an, das anstelle der Fehlerursache fehlgeschlagen ist
* [Bäcker] Absturz beim Verarbeiten eines Detail-Map-Bäckerers ohne ein hohes Polygitter
* [Bäcker] Schrägzuordnung scheint sich nicht auf die gesamte Ausgabe mit aktiviertem DXR zu auswirken
* [Inhalt] mg\_lecks: Typo in Parametername
* [Content] &quot;Shape&quot; gibt eine Kochwarnung zurück
* [Inhalt] Polygon 1 und 2 unterstützen keine zufälligen Funktionen
* [Inhalt] Polygon 1 und 2 können weniger als 3 Seiten haben
* [Inhalt] &quot;Normal&quot; bis &quot;Height HQ&quot; funktioniert nicht korrekt in nicht quadratischen
* [Parameter] Ganzzahlen-Eingabeparameter: In der Dropdown-Liste werden die Werte nicht angezeigt

### 9.1.2 (2019.1.2)

*(Freigegeben: 2. Juli 2019)*

**Fest:**

* [3D-Ansicht] 3D-Ansicht-Export mit aktivierter Tiefe des Felds sieht falsch aus
* [3D-Ansicht] Der Bildkanal von PSD-Alphas ist falsch, wenn Render speichern verwendet wird
* [3D-Ansicht] PNG und PSD werden beschädigt, wenn die Option zum Speichern des Renderings mit Iran verwendet wird
* [3D-Ansicht] Das DDs-Format funktioniert beim Speichern des Renderings nicht
* [Diagramm] Knoten werden versetzt, wenn Sie Rechts- und Linksklick kombinieren und auf bestimmte Weise ziehen
* [Graph] Das Ändern einer Funktionsinstanz aktualisiert das Knotenergebnis nicht mehr.
* [Graph] Absturz bei Anzeige des Menüs &quot;Leertaste&quot;
* [Inhalt] Form-Extrudieren: Qualitätsproblem, wenn die Form keine Drehung hat
* [Inhalt] Der Shape-Schlagschatten (und Graustufen) erzeugt keinen Schatten ohne H- und V-Kachelung
* [Inhalt] Normales Problem mit Material Crop
* [Bäcker] JSON-Bäcker-Vorgaben werden nicht korrekt geladen
* [Bäcker] Absturz beim Backen schwerer Meshes mit Optix oder DXR (jetzt kann es aufgrund von unzureichendem Vram fehlschlagen, aber es wird nicht abstürzen)
* [Bitmap-Editor] Bitmap-Malwerkzeuge versetzen Striche und zeichnen im Strichbegrenzungsrahmen neu
* [Bitmap Editor] Fehlerhafte Bitmap-Malwerkzeuge in OSX
* [UI] Einige Schaltflächenmenüs sind kaum erreichbar
* [UI] Absturz beim Ziehen und Ablegen einer Bäckerinstanz
* [SVG] Eingebettete SVG-Bearbeitungswerkzeuge sind unzuverlässig
* [Parameter] Absturz beim Anwenden einer Voreinstellung mit booleschen Parametern in einer SBSAR-Instanz
* [Netzwerk] Absturz manchmal, wenn ein Fehler in einer SSL-verschlüsselten Verbindung aufgetreten ist

### 9.1.1 (2019.1.1)

*(Freigegeben: 28. Mai 2019)*

**Hinzugefügt:**

* [PythonIntegration] Speichern und Wiederherstellen des Plug-In-Manager-Status
* [Voreinstellungen]&#x200B;[Abhängigkeiten] Fügen Sie eine Option hinzu, um festzulegen, wie der Abhängigkeitsdateipfad gespeichert wird.
* [Inhalt] Flood Fill Mapper: Option &quot;An Formrahmen anpassen&quot; hinzufügen

**Fest:**

* [Inhalt] Flood Fill Mapper: &quot;Drehung Auto-Skalierung&quot; bewirkt das Gegenteil
* [Inhalt] Die Eingabe für &quot;luminance\_offset\_map&quot; wird von &quot;Flood Fill Mapper Color&quot; nicht verwendet.
* [Inhalt] Der Flood Fill &quot;Graustufen-Knotenzuordnung&quot; generiert Stepping-Artefakte.
* [Inhalt] Höhenextrusionen können nicht veröffentlicht werden.
* [Parameter] Eingebettete Vorgaben in SBSAR werden nicht in Designer geladen
* [Bäcker] Bäckername wird in der Bäckerliste nicht korrekt angezeigt
* [3D-Ansicht] &quot;Ausgaben in 3D-Ansicht anzeigen&quot; funktioniert nicht für Werte
* [Cooker] Absturz bei Korrektur eines falschen Parametertyps
* [API] SDResource.setInputPropertyFromId-Funktion funktioniert nicht mit SDSBSCompGraph-Eingabeparametern
* [Updater] einige SBS können in 2019 nicht aktualisiert werden
* [Explorer] Absturz beim Importieren einer bestimmten .obj-Datei
* [PythonIntegration] Backslashes werden bei der Initialisierung von PYTHONPATH unter Windows nicht richtig maskiert
* [UI]-Werteproblem mit einigen Reglern in Bäckereien
* [Linux] Designer kann unter CentOS &lt; 7.6 nicht ausgeführt werden.

### 9.1.0 (2019.1.0)

*(Freigegeben: 09. Mai 2019)*

**Hinzugefügt:**

* [API] Fügen Sie der SDPackageMGR.loadUserPackage()-Methode den Parameter &quot;updatePackages&quot; hinzu, um zu steuern, ob die Updater beim Laden angewendet werden sollen oder nicht.
* [API] Möglichkeit zum Trennen einer SDC-Verbindung hinzufügen
* [API] Klasse SDSBSARExporter hinzufügen, um ein SDPackage zu veröffentlichen
* [API] Fügen Sie eine SDHistoryUtils-Klasse hinzu, um rückgängig zu machende Befehle zu verwalten
* [API] Hinzufügen einer Graustufen-Eingabeknotendefinition im Substance-Kompositionsdiagramm (sbs::compositing::input\_grayscale)
* [API] Werteingabeknotendefinition im Substance-Kompositionsdiagramm hinzufügen (sbs::compositing::input\_value)
* [API] SDProperty.isFunctionOnly()-Methode hinzufügen
* [API] Unterstützung benutzerdefinierter Eingabeparameter für SDSBSCompNode hinzufügen
* [API] Fügen Sie der SDPackageMGR.loadUserPackage()-Methode den Parameter &quot;reloadIfModified&quot; hinzu, um zu steuern, ob ein Paket bei einer Änderung neu geladen werden muss.
* [API] SDPackageMgr.getPackages()-Methode hinzufügen
* [API] Hinzufügen der Möglichkeit zum Abrufen/Hinzufügen/Entfernen von Stammpfaden aus SDModuleMgr
* [API] Abrufen des Zeigers des Pixelpuffers und der Tonhöhe einer SDTexture
* [API] Abrufen des Zeigers des MainWindow
* [API] Benutzerdefinierte Menüs im Hauptmenü erstellen
* [API] Erstellen benutzerdefinierter DockWidgets im Hauptfenster zulassen
* [API] Verwenden von Objektnamen zum Suchen von Menüs in Symbolleisten
* [API] Bereitstellung eines Systems zur Verwaltung von Anwendungsbenachrichtigungen für die API
* [PythonIntegration] Fügen Sie eine Standard-Umgebungsvariable hinzu, um nach Python-Plug-ins zu suchen
* [PythonIntegration] Hinzufügen von Textsuche und Ersetzen zum Python-Editor
* [PythonIntegration] Instanziieren von Python-Plug-ins beim Start
* [PythonIntegration] Berücksichtigung der PYTHONPATH-Umgebungsvariable
* [PythonIntegration] Erstellen von Symbolleisten in Grafik-Widgets zulassen
* [PythonIntegration] Unterstützung von Python-Threads
* [PythonIntegration] Plug-in-Manager hinzufügen (im Menü &quot;Extras&quot;)
* [Inhalt] Normale Vektordrehung: Hinzufügen einer optionalen Bildeingabe, um den Winkel zu steuern
* [Inhalt] Neuer Min/Max-Filter
* [Inhalt] Neuer Filter &quot;Flood Fill zu Index&quot;
* [Inhalt] Neuer Filter &quot;Flood Fill Mapper&quot;
* [Inhalt] Neuer Atlas Splitter-Filter
* [Inhalt] Verbessern des dreidimensionalen Filters
* [Inhalt] Neuer Non Uniform Directional Warp-Filter
* [Inhalt] Neue multidirektionale Verkrümmung
* [Inhalt] Neuer Datenfilter
* [Engine] FXMAP: Neues Muster &quot;Abstufung mit Versatz&quot;
* [Engine] Unterstützung für die Verarbeitung einheitlicher Werte (neuer Value-Prozessorknoten)
* [3D-Ansicht]&#x200B;[Bäcker] Verbessern der Leistung des OBJ-Laders
* [3D-Ansicht] Die Ebenenabstände des Kameraclips erhöhen
* [Voreinstellungen] Hinzufügen von Einstellungen für Bäcker
* [Graph] Schnellere Invalidierung durch Vermeiden von Zeichenfolgenvergleichen
* [MDL] Unterstützung von MDL-Arrays
* [UI] Verbesserungen an der Benutzeroberfläche für die Modulauswahl
* [IRay] Upgrade auf IRay SDK 2018.1.4
* [Abhängigkeitsmanager] Verwenden Sie &quot;letzten Pfad&quot; beim Verschieben einer Ressource.
* [Kochen] Hinzufügen von Unterstützung für boolesche Beschriftungen im Unterfenster
* QT 5.12.2 integrieren

**Fest:**

* [Graph] Verbindungen werden unterbrochen, wenn der Name der Eingabe geändert wird
* [Graph] Beim Anpassen von Parametern werden zu viele Invalidierungen ausgelöst
* [Diagramm] Die Aktion &quot;In Zwischenablage kopieren&quot; funktioniert nicht, wenn Sie mit der rechten Maustaste auf ein Abzeichen klicken
* [Diagramm] Das Verschieben eines Frames mit Alt wird nicht in der SBS-Datei gespeichert
* [MDL] Farbprofil wird im MDL-Editor nicht automatisch aktualisiert
* [MDL] Absturz beim Exportieren eines Moduls, das ein bestimmtes Setup enthält
* [MDL] Fehler beim Exportieren eines MDL-Diagramms, das ein LightProfile oder eine MBSDF-Ressource enthält.
* [UI] Verknüpfungen werden nicht mehr in Kontextmenüs angezeigt
* [UI] Gleitendes Fenster wird nach einem Neustart andockfähig
* [Scripting] Abbrechen-Option funktioniert nicht im Python-Editor
* [Skripterstellung] &quot;Yes to all&quot;-Option im Speichermenü funktioniert nicht
* Die Dropdown-Liste [Parameter] wird nach dem Kopieren nicht korrekt angezeigt
* [Explorer] Beim Verschieben von Ressourcen sollte standardmäßig der zuletzt verlagerte Pfad geöffnet werden.
* [Bibliothek] Der Inhalt der Bibliothek wird beim Wechsel von einer Version zu einer anderen immer neu erstellt.
* [Library] Importierte Bitmaps werden beim Speichern ungültig.
* [IRay] Der Tangentenraum wird nicht korrekt berechnet/falsche Normalzuordnung
* [Funktion] Absturz oder Fehler beim Erstellen eines neuen Diagramms aus der Auswahl
* [API] Standardwert von Eigenschaften ist nicht definiert

## Version 8

### 8.3.4 (2018.3.4)

*(Freigegeben: 12. April 2019)*

**Hinzugefügt:**

* [Inhalt] Normale Transformation/Materialtransformation: Fügen Sie eine Option hinzu, um die Transformation &quot;Skalieren&quot; und &quot;Neigen&quot; zu aktivieren

**Fest:**

* [Inhalt] Der Wirbelfilter funktioniert nicht ordnungsgemäß, wenn zufällige Funktionen in Parameterfunktionen verwendet werden
* [Inhalt] Normale Transformation/Materialtransformation: Normal wird nach einer Skalierungstransformation nicht normalisiert
* [Inhalt] Wirbel gibt falsche Ergebnisse aus, wenn der Betrag zufällig ist
* [Graph] Absturz beim Ziehen einer Ausgabe mit Umschalttaste und anschließendem Wechseln zu Strg-Ziehen
* [Graph] Absturz beim Bearbeiten von Teilungspunkten
* [Graph] Leistungsabfall bei der Anzeige von Knoten-Badges
* [Skripterstellung] Die Verwendung benutzerdefinierter Aktionen kann nach 30 Sekunden abstürzen
* [Voreinstellungen/Projekte] Aktivierte Skripte aus allen Projekten sollten ausgeführt werden (im Abschnitt &quot;Skripterstellung&quot;).
* [MDL] Absturz beim Verknüpfen eines MDL-Diagramms mit einem anderen MDL-Diagramm
* [Parameter] Knoten werden nicht aktualisiert, nachdem die Zufallszahl des Graphen auf einen exponierten Parameter gesetzt wurde
* [PSD] Das Zuweisen von Farbknoten ändert die Größe der Ebenenminiaturen, das Zuweisen eines Graustufenknotens ändert sich nicht
* [API] Unbehandelte Ausnahme mit SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Freigegeben: 19. Februar 2019)*

**Fest:**

* [Inhalt] PBR-Basismaterial-Ausgaben haben nicht den richtigen Gruppennamen

### 8.3.2 (2018.3.2)

*(Freigegeben: 19. Februar 2019)*

**Hinzugefügt:**

* [Bäcker] Fügen Sie eine Beschriftung hinzu, die die aktuelle Suffixeinstellung für &quot;Nach Name abgleichen&quot; angibt.

**Fest:**

* [Graph] Absturz beim Bearbeiten von Teilungspunkten
* [Graph] Ungültigkeitsproblem, wenn die Bittiefe des Eingabeknotens geändert wird
* [Graph] Optionen zur Berechnung von Miniaturansichten funktionieren nicht mehr
* [Diagramm] Unter dem Breadcrumb wird ein leerer Bereich mit einem bestimmten UI-Layout angezeigt.
* [Graph] Die Verknüpfungsformatvorlage ist im Kontext falsch
* [Graph] Miniaturansichten werden in Funktions-/MDL-Graphen auf Hi DPI-Bildschirmen nicht korrekt angezeigt
* [Inhalt] Farbe für Form-Farbspritzer: Keine Option zum Angeben der Normalen-Map-Format
* [Inhalt] Rechtschreibfehler in der QuickInfo für lineare Interpolation
* [Inhalt] &quot;Normale Transformation&quot; verarbeitet die Spiegelungs- und Neigungstransformation nicht korrekt
* [Inhalt] Farbverlauf axial, radial, kreisförmig unterstützen keine zufälligen Funktionen
* [Inhalt] Radialer Verlauf funktioniert nicht korrekt in nicht quadratischen
* [API] output\_exporting.sbs muss immer aktualisiert werden, wenn das Skript export\_output verwendet wird.
* [API] Absturz nach Verwendung des export\_output-Skripts
* [API] Fehler beim Festlegen des numerischen Werts von Anmerkungen für Compositing-Graph-Eingaben
* [Explorer] Zufälliger Absturz beim Speichern eines Projekts
* [Explorer] Kann SBS mit Großbuchstabenerweiterung nicht öffnen
* [UI] Fenstergröße &quot;Neue Substance&quot; ist nicht dauerhaft
* [UI] Kontextmenü auf Funktionsinstanz stimmt nicht mit Compositing-Diagramm überein
* [Bäcker] Absturz beim Öffnen der Bäcker auf einem bestimmten Gitter
* [Bäcker] Falsche Berechnung für DXR-Bäcker, wenn UVs einen Ordinatenwert von 0 haben
* [Updater] Absturz beim Abbrechen des Updaters
* [3D-Ansicht] Die UVs der Sphere primitive werden um 1 Einheit versetzt.
* [Cooker] Zufallsdithering beim Kochen von Bitmaps
* [Player] Schaltflächen zur Fenstersteuerung sind klein
* [Player] Schaltflächensymbole sind defekt

### 8.3.1 (2018.3.1)

*(Freigegeben: 20. Dezember 2018)*

**Hinzugefügt:**

* [API] Add SDConnection.getOutputProperty() and SDConnection.getOutputPropertyNode()
* [API] Dokument über alle Ressourcendefinitionen hinzufügen
* [API] SDSBSCompNode-Anmerkungseigenschaft &quot;visibleif&quot; zur Konsistenz in &quot;visible\_if&quot; ändern

**Fest:**

* [Graph] Wenn Sie die TAB-Taste ein zweites Mal drücken, wird das Knotenmenü nicht geschlossen.
* [Diagramm] 3D-Ansicht-Badges funktionieren in einigen Situationen nicht richtig
* [Graph] Schreibgeschützte Pakete können geändert werden
* [Bäcker] Der Fortschrittsbalken wirkt beim Laden eines sehr hohen Polygitters seltsam
* [Bäcker] Artefakte am Gitter mit nach innen gerichteten Normalen
* [Bäcker] Bäcker-Ausgabe- und Parameter-Widget kann nicht entsperrt werden
* [Explorer] 3D-Ressourcen werden beim Öffnen eines Pakets geladen
* [CmdLineArgs] &quot;—news hide\_changelog:true&quot; funktioniert nicht mehr.

### 8.3.0 (2018.3.0)

*(Freigegeben: 05. Dezember 2019)*

**Hinzugefügt:**

* [Diagramm] Hinzufügen eines Breadcrumbs beim Bearbeiten von Unterdiagrammen/Funktionen
* [Graph] Fügen Sie TAB als Kurzbefehl zum Starten des &quot;Knotenmenüs&quot; hinzu.
* [Graph] Knotenmarkierung für übergeordnete Auswahlknoten
* [Graph] Fügen Sie Strg+E als Verknüpfung hinzu, um die Pixelprozessorfunktion und -Untergraph zu öffnen.
* [Graph] Verbinden eines neuen Knotens mit der ersten sichtbaren Ausgabe des ausgewählten Knotens
* [Graph] Knoten &quot;Badges&quot; hinzufügen
* [Graph] Hinzufügen von Warnungen auf Compositing-Knoten über Badges
* [Graph] Fügen Sie die Möglichkeit hinzu, einen Knoten nach seinem Namen, seinen Attributen oder seiner UID zu suchen.
* [API] Erstellen und Ändern von Daten zulassen
* [API] SDPackage und SDMDLGraph können in MDL-Module exportiert werden (siehe SDMDLExporter)
* [API] Abrufen aller Knoten, Enumerationen und Strukturdefinitionen zulassen (siehe SDModuleMgr)
* [3D-Ansicht] Wechseln Sie zu Cubemaps für den OpenGL-Renderer
* [3D-Ansicht] Exportieren Sie ein lineares HDR-Bild beim Speichern in .exr oder .hdr
* [Bäcker] Integration der DXR-Raytracing-Technologie
* [IRay] Integrieren von IRay SDK 2018.1
* [Engine] SSE (CPU) Engine-Unterstützung für HDR-Gleitkommabildverarbeitung
* [Engine] Fügen Sie eine Befehlszeilenoption (—gpu x) hinzu, um das der Substance-Engine zugeordnete GPU-Gerät anzugeben.
* [Inhalt] Neuer PBR-Rendering-Knoten
* [UI] Registerkarten und Titelleiste überarbeiten
* [Abhängigkeitsmanager] Aktualisierung der Abhängigkeitsliste verhindern, wenn Benutzeraktionen keine Abhängigkeiten betreffen

**Fest:**

* [Graph] Absturz beim Instanziieren eines Diagramms in sich selbst
* [Graph] Duplizierter Knoten ist nicht ausgewählt
* [Graph] Computing-Problem bei Verwendung derselben Knoteninstanz in 2 verschiedenen MDL-Graphen
* [Diagramm] Die Z-Taste sollte die Ansicht in der Szenenfeldmitte zentrieren.
* [Diagramm] Farbraum in den Verbindungsregeln ignorieren, wenn Materialverknüpfung verwendet wird
* [Diagramm] Vermeiden Sie das Öffnen von Ausgaben in der 3D-Ansicht, wenn Sie ein Diagramm in conli öffnen
* [Graph] Einfügen von Knoten ist langsam, wenn &quot;Neu erstellten Knoten öffnen&quot; aktiviert ist
* [3D-Ansicht] Assert beim Ziehen und Ablegen eines bestimmten Gitters
* [3D-Ansicht] Die Option &quot;UV-Skalierung aktiviert&quot; funktioniert nicht in der Height-Map
* [Inhalt] Dreidimensional: Verschiedene Probleme mit Achsen und Transformationen
* [Inhalt] Steigung Weichzeichnen Graustufen: eine der Samples nicht die richtige Füllmethode hat, wenn min oder max verwendet wird
* [Inhalt] Verlauf linear 2 falsch Ergebnis bei niedriger Auflösung
* [API] SDPackage.findResourceFromUrl() kann auch Ressourcen abrufen, die sich in einem anderen SDPackage befinden.
* [API] SDPackage.getChildrenResources() gibt immer das erste Element im nicht rekursiven Modus zurück.
* [API] [Dokumentation] Aufzählungen, Strukturen im Ordner &quot;generiert&quot; werden in der Dokumentation nicht wiedergegeben
* [UI] Die Breite der 2D-Ansicht sollte nicht eingeschränkt werden
* [Verlauf] Absturz beim Auswählen auf Mac
* [Explorer] Absturz beim Schließen und erneuten Öffnen eines Diagramms
* [Mac] Farbwähler funktioniert nicht auf mehreren Bildschirmen
* [Parameter] Drehfeld für Ganzzahlparameter funktioniert nicht
* [Cooker] Absturz beim Erstellen bestimmter Knoten unter OSX 10.13
* [Kurvenfilter] Tasten und Kontrollpunkte können mit einem Wert von -0,0 oder einem merkwürdigen Wert von &quot;fast null&quot; im Kurveneditor enden.
* [2D-Ansicht] Positions-Widget ist nicht für Graphen vom SBSAR verfügbar
* [PSD] Ebenenproblem nach Export mit Abhängigkeiten

### 8.2.2 (2018.2.2)

*(Freigegeben: 04. Oktober 2019)*

**Fest:**

* [Inhalt] Der Formschatten funktioniert nicht ordnungsgemäß, wenn die Unterteilung deaktiviert ist
* [Inhalt] Flutfüllung in Zufallsgrau/Farbe funktioniert in einigen Fällen nicht richtig
* [Inhalt] Flood Fill ist nicht korrekt in nicht quadratisch
* [Inhalt] Flood Fill zu Farb-/Graustufendarstellung funktioniert nicht
* [Inhalt] QuadTransform ist in der CPU zackig
* [Inhalt] Sternform gibt einen &quot;Keine Kachelung&quot;-Kachelmodus aus
* [Inhalt] Ausgabe der Form-Farbspritzer-Angleichungsfarbe absolut 32f Bittiefe
* [Inhalt] Die Füllfarbe für Shape-Farbspritzer kann lange berechnet werden, wenn ihr Format nicht auf 32F festgelegt ist
* [Graph] Absturz beim Verknüpfen eines Bildes als Eingabe einer Fx-Map, während Iterate-Eigenschaften angezeigt werden
* [Graph] Das Timing scheint falsch zu sein, wenn das Diagramm im Kontext bearbeitet wird
* [Graph] Zufälliger Absturz beim Speichern des Diagramms
* [Diagramm] Materialmodus funktioniert nicht mit SBSAR
* [3D-Ansicht] Materialzuordnung wird nicht korrekt wiederhergestellt
* [3D-Ansicht] Einige Einstellungen für die 3D-Ansicht-Statusdatei werden nicht korrekt geladen
* [2D-Ansicht] Alpha-Anzeige immer schwarz
* [2D-Ansicht] Die Schaltfläche &quot;Bild in Graustufen anzeigen&quot; funktioniert nicht für Bilder mit Alpha
* [UI] Abhängigkeitsmanager-Lawn beim Start, auch wenn er nicht in Mac aktiviert ist
* [UI] Einige Schaltflächen führen Aktionen aus, auch wenn die Maus außerhalb des Fensters losgelassen wird
* [API] Absturz beim Versuch, ein Arrayelement außerhalb des Bereichs des Arrays zu halten, aus dem es stammt
* [MDL Graph] Knotenvorschau auf dem Kopf
* [MDL Graph] Der Versatz des Vorschauknotens unterscheidet sich von dem in 3DView.
* [Konsole] Die Leistung wird sehr langsam, wenn die Konsole viele Meldungen enthält.
* [Console] Qt-Warnungen beim Starten von Designer unter CentOS
* [FX-Map] Absturz beim Löschen von Verknüpfungen zwischen Eingaben und FX-Map
* [Funktionen] Ein Zeichenfolgentypknoten kann nicht als Ausgabe in der Funktionsressource festgelegt werden.
* [Voreinstellungen] Das Menü &quot;Voreinstellungen&quot; enthält keinen Fokus. Der Benutzer kann beim Scrollen versehentlich einen Wert ändern.
* [FX-Map] Eingabebildindex-Kombinationsfeld wird beim Hinzufügen/Entfernen von Eingaben nicht korrekt aktualisiert
* [Abhängigkeiten] Absturz beim Löschen von UDIM-Ressourcen, die in einem Diagramm verwendet werden
* [API] SDLocationContext.getCurrentGraph() gibt immer null zurück.
* [Publish] Falsche URL für Substance Player-Downloadseite

### 8.2.1 (2018.2.1)

*(Freigegeben: 17. August 2018)*

**Hinzugefügt:**

* [UI] Fügen Sie eine Nachricht in der Taskleiste hinzu, wenn die Kontextbearbeitung aktiviert ist
* [Voreinstellungen] Umformung der Optionsbeschriftung &quot;Im Kontext bearbeiten&quot;

**Fest:**

* [Diagramm] Einfügen ohne Verknüpfungs-Shortcut funktioniert im Compositing-Diagramm nicht
* [Graph] Die Invalidierung ist sehr lang, wenn die Kontextbearbeitung aktiviert ist
* [Graph] Absturz beim Verknüpfen von Knoten
* [Graph] Absturz Neuverknüpfungsknoten
* [Graph] Absturz bewegter Frames
* [Graph] Absturz beim Wechseln von UVTile in Graph und Gitter ist nicht mehr udim
* [Graph] Absturz bei Verwendung von Strg+z nach dem Einfügen von Knoten
* [Graph] Übergeordnete Knoten auswählen ist sehr langsam
* [Bäcker] Durch Verschieben von Karten nach oben/unten kann der Benutzer die Größe der Zeile ändern
* [Bäcker] Pfad zum Speichern oder Laden der Voreinstellung wird nie gespeichert
* [Bäcker] Käfig wird auch dann verwendet, wenn er nicht im Backfenster ausgewählt ist
* [Bäcker] Neigungskorrektur funktioniert nicht richtig
* [Bäcker] Sehr langsame Leistung, wenn negativer UV-Raum in der Ansicht ist
* [Baker] Durch Klicken auf die Schaltfläche Abbrechen wird das Laden des Gitters nicht abgebrochen.
* [Bäcker] Kann nicht mit einem Käfig gebacken werden, wenn die Schrägzuordnung leer und auf &quot;true&quot; gesetzt ist
* [Inhalt] Flood Fill ist in 4K langsam
* [Inhalt] Funktion &quot;Linear zu sRGB&quot; ist defekt
* [Inhalt] Kachel Zufälliger Graustufen-Hintergrund wird von einem float4 anstelle eines float gesteuert, verhindert Kochen
* [Inhalt] Formaufteilung: Position/Vektorzuordnungsvervielfacher funktioniert nicht richtig
* [Skripterstellung] Strg + o funktioniert nicht im Python-Editor
* [Scripting] Der Python-Editor fragt auch nach dem Schließen immer wieder nach
* [Skripterstellung] Einfrieren beim Erstellen mehrerer neuer Skripte
* [UI] Symbole in der Bibliothek sind verpixelt
* [UI] Standardmäßig schwebende Bedienfelder verhalten sich nicht korrekt.
* [Explorer] Absturz beim Importieren eines Gitters unter CentOS
* [Explorer] UDIM-Gitter wird zweimal geladen
* [Cooker] Kein Timing für Knoten im Kontext
* [Cooker] Stapelüberlauf beim Kochen
* [Lizenz] Fehlerhafte Authentifizierung mit gültigen Anmeldedaten
* [Lizenz] Gleitende Lizenz wurde mehr als einmal für denselben Benutzer gemeldet.
* [3D-Ansicht] V-Standardwert des UV-Kachelmaterials ist falsch
* [3D-Ansicht] Leistungsrückgang im Vergleich zu 2018.1.x
* [Voreinstellungen] Absturz bei Verwendung einer Konfigurationsdatei von einem Server
* [Library] Absturz beim Löschen eines Filters innerhalb der Bibliothek
* [SVG] Abhängigkeitsproblem bei Verwendung des Alias
* [Ebenen] 32-Bit-HDR-Bitmaps bringen den Level-Editor zum Blinzeln, während die Widget-Position verschoben wird
* [PSD] Das Fenster für die verknüpfte Import-PSD wird zweimal angezeigt
* [Iray] Szene wird aktualisiert, wenn eine deaktivierte Anzeige geändert wird
* [MDL] Absturz beim Löschen aller Knoten einer MDL-Vorlage
* [Engine] Riesiger Offsetbetrag in FX-Map kann SD einfrieren
* Crashpad stürzt beim Start ab
* Python-Umgebungsvariable führt zum Absturz von Designer beim Start

### 8.2.0 (2018.2.0)

*(Freigegeben: 19. Juli 2018)*

**Hinzugefügt:**

* [UI] Neue Formatvorlage
* [UI] Neue Regler
* [UI] Schwebende Fenster wirklich schwebend machen
* [UI] Layout des Fensters &quot;Voreinstellungen&quot; ändern
* Bibliothek [UI]: Filterleiste herausnehmen
* Bibliothek [UI]: Auswahlauswahlanzeigeüberlagerung entfernen
* [UI] Hinzufügen einer Meldung in der Taskleiste, wenn die Anwendung ein Paket automatisch speichert
* [UX] Eigenschaften: Menüs &quot;function&quot; und &quot;reset to default&quot; zusammenführen
* [Inhalt] Neue Formaufteilungsknoten (+ Begleitfilter)
* [Inhalt] Hinzufügen von Flood Fill zu Farb-/Graustufenfiltern
* [Inhalt] Unterstützung für neue Flood Fill: Stützformen mit Löchern
* [Inhalt] Flood Fill zu Verlauf: Hinzufügen der Steigung- und Winkelbildeingabe
* [Inhalt] Optimieren des Filters &quot;Auto-Level&quot;
* [Inhalt] Neuer Formextrusionsfilter
* [Inhalt] Materialtransformation: Unterstützung für gedrehte Normalmaps hinzufügen
* [Inhalt] Neue Filter &quot;Normale Vektordrehung&quot; und &quot;Normale Transformation&quot;
* [Inhalt] Normal normalisieren: die Ergebnisqualität zu verbessern.
* [Inhalt] Neuer Filter &quot;Trapezoid transformieren&quot;
* [Inhalt] Neuer Quad Transform-Filter
* [Inhalt] Halbkugelmuster zum Formknoten hinzufügen
* [Inhalt] Hinzufügen neuer Farbverläufe mit Steuerelementen in der 2D-Ansicht
* [Inhalt] Hinzufügen von UV-Ausgabe zum Knoten &quot;Cube GBuffers&quot;
* [Graph] Frame: Titeltext ignorieren, der größer als das Rahmenfeld für die Auswahl ist
* [Graph] Hinzufügen von Unterstützung für in der Kontextausgabe von Unterdiagrammen (experimentell)
* [Graph] Das Erstellen von Rahmen/Kommentar sollte den Knoten unter dem Cursor betreffen, wenn RMB verwendet wird
* [Graph] Frame: Titeltext ignorieren, der größer als das Rahmenfeld für die Auswahl ist
* [Diagramm] Vorhandene Registerkarte wiederverwenden, wenn eine bereits geöffnete Funktion geöffnet wird
* [Graph] Erstellen einer neuen Registerkarte, wenn &quot;Open Reference&quot; verwendet wird
* [Graph] Funktion: keine Funktionseigenschaften anzeigen, wenn auf den Hintergrund geklickt wird
* [Parameter] Schaltfläche &quot;Expose&quot; aus fxmap-Graphen entfernen
* [Parameter] Ebene: Schaltfläche &quot;Umkehren&quot; hinzufügen
* [Parameter] Erweitern Sie die Gruppe &quot;Eingabeparameter&quot;, wenn Sie einen neuen Eingabeparameter erstellen
* [Eigenschaften] Fügen Sie die Paket-URL-Informationen in den Graph-Attributen hinzu
* [Eigenschaften] Erhöhen Sie die Größe des Beschreibungsfelds für Ausgabeknoten
* [Eigenschaften] Erlaubt die Eingabe von Pro-Pixel-Funktionen des Pixelprozessors auch für schreibgeschützte Pakete.
* [Skripterstellung] Neue Python-API/neuer Python-Editor (erste Iteration)
* [Bäcker] Optimieren der Geometrieübertragung während des Renderns
* [3D-Ansicht] Wechsel zu OpenGL-Kernprofil
* [3D-Ansicht] Unterstützung von Tesselation/Versatz auf Mac
* Funktionsressource: Listen-Bildeingaben in Samplerknoten

**Fest:**

* [Graph] Absturz beim Verknüpfen eines Knotens mit einem anderen
* [Graph] Das Abrufen von Variablen in der Graphen-Zufallswertfunktion funktioniert nicht
* [Graph] Absturz beim Ziehen und Ablegen von Rauschen in einem Diagramm
* [Graph] Absturz beim Öffnen eines bestimmten Diagramms
* [Inhalt] Das Ergebnis unterscheidet sich zwischen Kachelzufälliger Farbe und Graustufen
* [Inhalt] Kachel zufällig: Ergebnisänderungen beim Ändern des &quot;Symmetrie-Zufallsmodus&quot;
* [Inhalt] Edge Detect funktioniert nicht mit nicht quadratischen Auflösungen
* [Bäcker] Artefakte beim Backen der Krümmung mit einem UDIM-Gitter
* [Bäcker] Umgebungskarte Verdeckung aus Mesh wird invertiert, wenn eine Normalkarte verwendet wird
* [Bäcker] Liste der UV-Sätze sollte auf verfügbare UV-Sätze beschränkt werden
* [Explorer] Absturz beim Löschen von Ressourcen während des Backens
* [Transform2D] Absturz beim Freigeben der Parameter &quot;MIP-Map-Ebene&quot; und &quot;Hintergrundfarbe&quot;
* [Transform2D] Fehlverhalten beim Anzeigen einer Transformieren-Mipmap-Stufe
* [PSDExport] PSD-Exporter exportiert Graustufen 32F nicht ordnungsgemäß.
* [2D-Ansicht] Histogrammberechnung funktioniert nicht mit 16F-Knoten
* [PSD] Verknüpftes PSD ist defekt
* [Cooker] Funktion im Parameter &quot;outputsize&quot; wird nicht korrekt ausgewertet
* [Export] Der Ausgabepfad für den Export sollte mit dem Paketpfad übereinstimmen.
* [Export] Der Exportpfad wird nicht mit einem leeren Muster gespeichert
* [Vorlagen] Fehlende Gruppe für Position in Painter-Vorlage
* [Help] Befehlszeilenhilfe zeigt in Mac keine —news an
* [Abhängigkeiten] Das doppelte Exportieren nach dem Ändern eines Ordnernamens funktioniert nicht

### 8.1.2 (2018.1.2)

*(Freigegeben: 31. Mai 2018)*

**Hinzugefügt:**

* [3D-Ansicht] Legen Sie den Standardlichtstatus in den Projekteinstellungen fest.
* [Versionskontrolle] Entfernen Sie die Zeitüberschreitung von 30s beim Aufrufen der Python-Skripte

**Fest:**

* [Content] Fraktalsumme Basis: Falsches Ergebnis mit der dritten Ebene (neues Diagramm wurde hinzugefügt)
* [Inhalt] Das 3D-Perlin-Rauschen-Fraktal wird auf 32 Bit erzwungen
* [Inhalt] Verlauf Linear 3 gibt bei Verwendung einer ungleichmäßigen Größe nicht das richtige Ergebnis.
* [Content] Normal Sobel unterstützt keine Kacheloptionen
* [Inhalt] Checker\_1 ist auf 8 Bit gezwungen
* [Inhalt] Multiangle to Normal: interner Rechenfehler
* [Inhalt] Stripe-Muster unterstützt keine negativen &quot;Shift&quot;-Werte (Absturz des Motors)
* [MDL] Absturz beim Öffnen eines bestimmten MDL-Projekts
* [MDL] MDL-Diagramm wird nach einem geschlossenen/erneuten Öffnen nicht berechnet.
* [Exportieren] Ausgaben aus nicht zugewiesenen Diagrammen werden mit dem Stapelwerkzeug exportiert
* [Exportieren] Beim Exportieren von C16F in EXR wird ein Graustufenbild erzeugt
* [Bäcker] Neigungsfunktionen sind in der Benutzeroberfläche beim Backen mit einem Käfig nicht deaktiviert
* [Bäcker] Absturz, wenn der Käfig nicht über den entsprechenden UV-Satz verfügt
* [Cooker] bscooker: Kochfehler in Zusammenhang mit &quot;blend\_switch.sbs&quot;
* [Cooker] Veröffentlichtes Diagramm wird nicht korrekt gerendert
* [Motor] Transformation 2D: Maskenfarbe ist nicht korrekt
* [Explorer] Absturz beim erneuten Importieren eines FBX-Gitters
* [Color Widget] Graustufen-Farbwähler wählt nur den roten Kanalwert aus
* [3D-Ansicht] Verwendung &quot;textcoordN&quot; funktioniert nicht mehr
* [Iray] Normalmap wird zweimal für Dielektrika angewendet

### 8.1.1 (2018.1.1)

*(Freigegeben: 12. April 2018)*

**Hinzugefügt:**

* [3D-Ansicht] Stellen Sie den Standardbereich des &quot;Tesselierungsfaktors&quot; auf [0, 16] ein.

**Fest:**

* [3D-Ansicht] Seltsames visuelles Artefakt mit bestimmter AMD-GPU
* [3D-Ansicht] Einfrieren mit bestimmten AMD-GPUs
* [3D-Ansicht]&#x200B;[Bäcker] Generierte Normale von .obj haben harte Kanten an der UV-Naht
* [3D-Ansicht] Absturz beim Berechnen kugelförmiger Harmonien
* [Bäcker] Ressource kann nicht als &quot;eingebettet&quot; festgelegt werden
* [Bäcker] Absturz beim Backen
* [Bäcker] Backen von 2 verschiedenen Versionen einer Karte aus dem UDIM-Gitter ist unterbrochen
* [Bäcker] Absturz beim Wechsel zwischen kontextabhängigem und nicht kontextabhängigem Diagramm
* [Bäcker] Wenn sie den gleichen Bäcker zweimal haben, werden sie synchronisiert
* [Bäcker] Das Umbenennen des Makros $(custom) verhindert ein korrektes Backen
* [Bäcker] Das Aktualisieren eines durch Baking erzeugte Map sollte die Benutzeroberfläche blockieren
* [Bäcker] Alle durch Baking erzeugte Map aktualisieren erstellt leere Ressourcen
* [Bäcker] Drücken der &quot;Eingabetaste&quot;, um einen Parameterwert zu bestätigen, entfernt das hohe Poly
* Tile Generator [Inhalt]: Fehler &quot;Drehung zufällig&quot;, wenn X- und Y-Betrag unterschiedlich sind
* [Inhalt] Einige Schmutz Maps enthalten Geisterinstanzen
* [Inhalt] Cube 3d: Verwenden von Zufallsfunktionen in Parametern führt nicht zu einem erwarteten Ergebnis
* [Inhalt] Fraktale Störungen werden nicht korrekt gerendert, wenn die Quadratische Ausbreitung deaktiviert ist
* [Inhalt] Zellen 2 und Zellen 4 verhalten sich nicht korrekt, wenn die Quadratische Ausbreitung deaktiviert ist
* [Graph] Beim Aktualisieren einer SBSAR-Instanz wird ein Geisterdiagramm erstellt.
* [Diagramm] Zuweisung durch Rechtsklick sollte Untermenü &quot;UV-Kacheln&quot; für Nicht-UDIM-Gitter nicht anzeigen
* [Graph] Wiederveröffentlichte Unterfenster werden nicht korrekt aktualisiert
* [Graph] Knoten werden nicht korrekt ungültig, wenn sich die Ressource ändert
* [Cooker] Der Parameter für die Alpha-Überblendung von Premult wird nicht ordnungsgemäß von sbsar abgerufen.
* [Cooker] Pegelfilter klemmt Werte nicht, wenn sie in einem SBSAR gekocht werden
* [Cooker] Implizite Transformationen werden vor FX-Map-Knoten durchgeführt
* [Explorer] Durch Drücken der Entf-Taste auf einem Paket wird der Benutzer gefragt, ob er es löschen möchte
* [Explorer]&#x200B;[Bäcker] Problem beim Verschieben
* [Kurve] Zufälliger Absturz beim Bearbeiten von Schlüsseln im Kurveneditor
* [MDL] Gamma-Typ wurde nicht korrekt für die benutzerdefinierte Verwendung festgelegt
* [Parameter] Absturz beim Freigeben eines Parameters mit demselben Bezeichner wie eine vorhandene Eingabe
* [Eigenschaften] Die Verwendung der Ausgabe wird ohne Berücksichtigung der Groß-/Kleinschreibung bearbeitet

### 8.1.0 (2018.1.0)

*(Freigegeben: 09. März 2018)*

**Hinzugefügt:**

* [Bäcker] Optimieren des High-Poly-Backens
* [Bäcker] Verbessern Sie das Ergebnis an Nähten für Kurvenbäcker
* [Bäcker] Bake Maps für UDIM-basiertes Mesh
* [Bäcker] Hinzufügen einer dedizierten 2D-Ansicht im Fenster &quot;Bäcker&quot;
* [Graph] Unterstützung für UDIMs
* [Graph] Optimieren der Leistung von Cookern
* [Graph] Verbessern der Generierungsgeschwindigkeit von Knoten-Miniaturansichten
* [Graph] Node-Cache nur für geöffnete Diagramme beibehalten
* [Diagramm] Fügen Sie im Compositing-Graphen die Symbolleiste hinzu, um den Miniaturansichtserstellungsmodus zu steuern.
* [3D-Ansicht] Fügen Sie einen Geometrie-Cache hinzu, um die Anzeige von hochauflösenden Netzen zu optimieren
* [3D-Ansicht] Unterstützung der UDIM-Anzeige (zeigt die aktuelle Kachel an)
* [3D-Ansicht] Abgerundeten Cube mit einheitlicher Topologie aktualisieren
* [3D-Ansicht] Vermeiden Sie es, die Szene ständig zu speichern
* [Content] Hinzufügen von 3D-Noises (Perlin, Perlin, Fraktal, Worley, Simplex)
* [Inhalt] Knoten &quot;3D-Volumenmaske hinzufügen&quot;
* [Inhalt] Knoten &quot;3D Linear gradient&quot; hinzufügen
* [Content] Knoten &quot;3D-Cube-Puffer&quot; hinzufügen (nützlich zur Vorabvisualisierung von 3D-basierten Knoten)
* [Inhalt] 3D-Knoten &quot;Planare Projektion&quot; hinzufügen
* [Inhalt] Radialen Weichzeichnungsfilter hinzufügen
* [Parameter] Anzeige der Bildeingabe-/-ausgabeeigenschaften in den Diagrammeigenschaften
* [Parameter] Edition des Ressourcenpfads zulassen
* [Engine] Unterstützung von Texturen mit bis zu 8k mit der CPU (SSE2)-Engine
* [Engine] Verwenden von HDR-Gewichtungen für die HDR-Engine durch den Graustufen-Konverter zulassen
* [Voreinstellungen] Fügen Sie eine Option hinzu, um die automatische Konvertierungsknotenerstellung zu deaktivieren.
* [Voreinstellungen] Legen Sie die Standardkomprimierung für png auf &quot;Beste Geschwindigkeit&quot; fest.
* [UI] Unterstützung für HTML-Link in den Diagrammeigenschaften
* [UI] Die Schaltflächen &quot;Ja/Nein/Abbrechen&quot; im Dialogfeld zur Speicherbestätigung zentrieren
* [Explorer] Verbessern der Anzeige der Gitterhierarchie
* [IRay] Integrieren von IRay SDK 2017.1.4

**Fest:**

* [Bäcker] Durch Hinzufügen eines Makros im Feld &quot;Ausgabename&quot; wird es nicht an der Cursorposition hinzugefügt
* [Bäcker] Es werden keine Materialien in der Liste angezeigt, wenn das Objekt kein Material enthält
* [Bäcker] Drücken der Eingabetaste zum Bestätigen der Bäckerparameter öffnet ein Dropdown-Menü
* [Bäcker] Backtexturen sollten keine Befehle im Rückgängigstapel generieren.
* [Bäcker] Absturz beim Backen einer übertragenen Textur aus dem Gitter ohne Angabe einer Textur
* [Explorer] &quot;Speichern unter&quot; sollte den vorhandenen Dateinamen anstelle des ersten Ressourcennamens verwenden.
* [Explorer] Falsches Verhalten beim Ziehen und Ablegen einer Ressource von einem Paket in ein anderes
* [Explorer] Mit der rechten Maustaste sollten die Daten nicht in den Eigenschaften geöffnet werden.
* [Explorer] Symbol für Szenenelemente hat nicht den richtigen Hintergrund
* [Graph] Strg + D funktioniert nicht unter Linux
* [Diagramm] Multi-Relink-Funktion kann nur einen Link schließen
* [Diagramm] Strg+Umschalt+D sollte nur externe, nicht interne Links entfernen
* [Diagramm] Verknüpfung zwischen Graustufen und Farbe ist nicht korrekt
* [3D-Ansicht] Eine Ressource kann nicht als Env-Map festgelegt werden.
* [3D-Ansicht] Mesh-Info-Shader zeigt Ergebnisse nicht im richtigen Farbraum an
* [Parameter] Nicht exponierbare Parameter können weiterhin mit STRG+P exponiert werden.
* [Parameter] Textfelder werden beim Rückgängigmachen/Wiederholen nicht korrekt aktualisiert
* [Inhalt] Artefakte in Schmutz Map 003
* [Inhalt] Die primäre Graustufeneingabe des Vektors erscheint falsch.
* [Cooker] sbscooker generiert einen Fehler, wenn eine Ressource fehlt
* [Kochen] Absturz mit Stapelüberlauf, wenn die Knotenkette zu lang ist
* [UI] Schaltfläche &quot;Beenden&quot; in der Lizenzverwaltung funktioniert nicht

## Version 7

### 7.2.5 (2017.2.5)

*(Freigegeben: 19. Februar 2018)*

**Hinzugefügt:**

* [Content] Tippfehler in function.sbs
* [Inhalt] Reduzieren des Standardbereichs von Perlin- und Gaußgeräuschen
* [3D-Ansicht] Anpassen des Standardbereichs für den Parameter &quot;Height skalieren&quot;
* [AXF] Aktualisieren von MDL-Vorlagen

**Fest:**

* [3D-Ansicht]&#x200B;[Bäcker] Normale werden nicht neu berechnet, wenn das Modell keine Normalen hat
* [Graph] Nicht-quadratische Bitmapressource ist leer, sobald sie instanziiert wurde
* [Content] Perlin-Rauschen führt zu unterschiedlichen Ergebnissen zwischen CPU und GPU-Engine

### 7.2.4 (2017.2.4)

*(Freigegeben: 08. Februar 2018)*

**Hinzugefügt:**

* [AXF Import] Festlegen des Filtermodus für Eingabebitmaps
* [2D-Ansicht] Ändern Sie nicht das Bildverhältnis in der 2D-Ansicht, wenn die Physische Größe aktiviert ist.

**Fest:**

* [Library] Absturz beim Aktivieren/Deaktivieren des Pfads in den Einstellungen
* [Baker] Passende Namen ignorieren einige Gitter mit bestimmten Namen
* [Inhalt] Alphakanal wird durch den Filter &quot;Prämult zu gerade&quot; entfernt.

### 7.2.3 (2017.2.3)

*(Freigegeben: 19. Januar 2018)*

**Fest:**

* [Content] Typ im Knoten &quot;PBR Basecolor Validate&quot;
* [Inhalt] Der Störungsparameter wurde in Zellen 2 unterbrochen.
* [Inhalt] Zellen 3 wird invertiert, wenn bestimmte Werte in Parametern verwendet werden
* [Inhalt] Polygon 2: Visuelle Artefakte mit bestimmten Einstellungen
* [Inhalt] Tile Generator-Graustufen sind standardmäßig in 8 Bit.
* [Inhalt] Mustergenerator: musterspezifischer zufälliger Parameter funktioniert nicht
* [Inhalt] Formzuordnung: zufällige Funktionen können nicht verwendet werden, um Mustergröße, Radius, Breite usw. zu steuern
* [Inhalt] Polygon 2: zufällige Funktionen können nicht verwendet werden, um den Seitenwert zu steuern
* [Inhalt] Einige Geräusche/Mustergeneratoren generieren Warnungen in der Konsole.
* [Inhalt] Non-Square-Transform-Grayscale generiert eine falsche Pixelgröße
* [Inhalt] Der Wirbelfilter berücksichtigt nicht den Kachelmodus
* [Graph] Ziehen und Ablegen der Bitmapressource auf den Bildeingabeknoten funktioniert nicht mehr
* [Graph] STRG+R (neu laden) funktioniert nicht mehr
* [Graph] Problem bei der Verwendung eines Frames in einem anderen Frame
* [Graph] Absturz beim Verschieben von Frames, die Pins enthalten
* [Graph] Die Instanz &quot;Shape (Legacy)&quot; wird beim Speichern in &quot;Shape&quot; umgewandelt
* [Baker] Absturz bei Verwendung von nicht leistungsfähigen 2 Bildern
* [Bäcker] Farbe aus Gitter: Polygroup, Submesh ID gibt immer ein schwarzes Bild zurück
* [Bäcker] AO aus Mesh: Okklusionsabstand wird unabhängig vom Eingangswert auf 1 geklemmt
* [Iray] Absturz beim Wechsel nach Iray
* [Iray] Der Kachelwert sollte die HöhenSkalenintensität beeinflussen.
* [Iray] Laden von IRay auf einem Windows-Computer, auf dem VCCOMP110.dll nicht vorhanden war, fehlgeschlagen
* [3D-Ansicht]&#x200B;[Bäcker] UVs können nicht von einem aus Modo exportierten Objekt decodiert werden
* [3D-Ansicht] Die Intensität des Versatzes ist zwischen Opengl und Iray nicht konsistent.
* [3D-Ansicht] Die Intensität der Versatz-/Parallax-Verdeckung ist doppelt so hoch wie sie sein sollte
* [2D-Ansicht] Versatz bei Anzeige von Alpha-Bild
* [Cooker] Konstanter Parameter ($tiling) wird nicht gefunden, wenn er innerhalb einer Diagramminstanz verwendet wird
* [Cooker] Falsche Auswertung von Variablen in verketteten Instanzen
* [Parameter] Der Bitmap-PKG-Ressourcenpfad sollte nicht bearbeitbar sein.
* [Parameter] Parameter in derselben Gruppe sind unsichtbar, wenn nur ein Parameter die Sichtbarkeit &quot;false&quot; hat.
* [PSD] Eine PSD-Datei kann nicht aus einem Ordner importiert/verknüpft werden, der mit Sonderzeichen benannt ist
* [Funktionen] Parameter in Funktionen sollten keine Sichtbarkeitsoption haben.
* [LicenseService] Ausnahme beim Abrufen von Informationen über Knoten
* [UI] Wenn Sie Text im Beschreibungsfeld auswählen, bleibt er hervorgehoben.

### 7.2.2 (2017.2.2)

*(Freigegeben: 23. November 2017)*

**Fest:**

* [Inhalt] Tippfehler in &quot;Richtung ...&quot; Nodes
* [Inhalt] Verschiedene Tippfehler
* [Inhalt] Kachel Sampler ist auf &quot;Absolut 32 Bit&quot; festgelegt
* [Inhalt] Formzuordnung: sichtbare Artefakte an der Formbegrenzung in einigen Fällen
* [Inhalt] Die Parameter &quot;Unterteilung&quot; und &quot;Nicht-quadratische Erweiterung&quot; in Polygon 1 sind fehlerhaft.
* [Inhalt] &quot;Random Seed&quot; und &quot;Non-Square Expansion&quot; funktionieren nicht bei anisotropem Rauschen
* [Inhalt] Beschädigte &quot;Shape&quot;-Instanz in einigen Schmutz Maps
* [3D-Ansicht] UV-Skalierung wird nicht angewendet, wenn die Height-Skala 0 ist
* [3D-Ansicht] Reflexion mit Shader Blinn funktioniert nicht mehr
* [2D-Ansicht] Das Informationsfenster weist ein fehlerhaftes Layout auf.
* [Graph]-Problem beim Steuern der Ausgabegröße mit einer Funktion für eine verknüpfte Bitmap, die in einem Diagramm instanziiert wird
* [Funktion] Diagramm nicht ungültig, wenn ein Link gelöscht wird
* [Bibliothek] Favoriten funktionieren nicht
* [PSD-Export] Der Inhalt der PSD-Datei ändert sich jedes Mal, wenn ein Export abgeschlossen ist
* [Verlauf] Absturz beim Bearbeiten von Tasten im Verlaufseditor
* [Vorlagen] Positionszuordnung für Substance Painter-Vorlagen ist falsch
* [AxF] Falsches physisches Height
* [MDL] UVW-Skalierung von Physische Größe ist in MDL SBS-Knoten invertiert
* [Bäcker] $custom funktioniert nicht mehr
* [Voreinstellungen] Absturz beim Start auf Mac

### 7.2.1 (2017.2.1)

*(Freigegeben: 20. Oktober 2017)*

**Fest:**

* [Engine] Absturz beim Rendern von Text mit GPU-Engine
* [Inhalt] Kachel Sampler: Zeilen-/Spalten-ID funktioniert nicht ordnungsgemäß mit nicht quadratischen Elementen
* [Inhalt] Kachel Sampler Color: Die Farbparametrisierung ist falsch
* [Inhalt] Kachel Sampler: falscher Standardwert für den Betrag des X-/Y-Musters
* [Export] Exportierte PSD enthalten keine Metadaten

### 7.2.0 (2017.2.0)

*(Freigegeben: 19. Oktober 2017)*

**Hinzugefügt:**

* [Inhalt] Fügen Sie Flutfüllungen und zugehörige Filter hinzu (konvertieren Sie eine Schwarzweißmaske in Farbverläufe, zufällige Farben usw.).
* [Inhalt] Fügen Sie neue Geräusche, Schmutz Maps und Mustergeneratoren hinzu, die nicht quadratische Formate unterstützen (alte Versionen werden als &quot;Legacy&quot; markiert).
* [Inhalt] Neues Splatter Circular mit viel mehr Funktionen hinzugefügt
* [Inhalt] Neuen Scratches-Generator hinzufügen
* [Inhalt] Filter &quot;Wirbel hinzufügen&quot;
* [Inhalt] Histogramm hinzufügen - Auswahl
* [Inhalt] Sternmuster hinzufügen
* [Inhalt] Formenzuordnungsfilter hinzufügen
* [Inhalt] Hinzufügen des Vektormorphen-Filters
* [Inhalt] Verlauf linear 3 hinzufügen
* [Inhalt] Kachel zufällig/Tile Generator: Symmetrie-Modus hinzufügen (h+v, h, v)
* Tile Generator [Inhalt]: Hinzufügen mehrerer Bildeingaben
* [Inhalt] Benennen Sie &quot;RGB-A Merge&quot; in &quot;Alpha Merge&quot; um.
* [2D-Ansicht] Switch-Node-Ausgabeanzeige mit Taste C
* [2D-Ansicht] Optimieren des Histogramm-/Info-Layouts je nach Anzeigeverhältnis
* [2D-Ansicht] Hinzufügen einer Schaltfläche zum Aktivieren/Deaktivieren der Kachelanzeige
* [3DView] Optimieren der Rechengeschwindigkeit von Kugelharmonikas
* [3D-Ansicht] Aktualisieren Sie PBR-Shader, um Fibonacci-Sampling anstelle von Hammersley zu verwenden
* [3D-Ansicht] Fügen Sie eine Option hinzu, um den aktuellen Szenenstatus als Standard zu speichern
* [3D-Ansicht]&#x200B;[Bäcker] Serialisieren von Daten in einem vom Menschen lesbaren Format
* [Bäcker] Hinzufügen von Vorgaben - Export/Import (JSON)
* [Publish] Erstellen Sie das Subsar-Archiv als nicht fest
* [Publish] Speichern Sie das Diagrammbild/die Miniaturansicht in der Unterleiste
* [Publish] Anzeigen einer Fortschrittsleiste, wenn ein Paket veröffentlicht wird
* [Abhängigkeiten] Zeigen Sie die SBS-Datei an, die eine Abhängigkeit im Fenster &quot;Fehlende Abhängigkeit&quot; anfordert.
* [Abhängigkeiten] Berichtsfenster: grünes Symbol angezeigt, wenn das Problem behoben wurde
* [Abhängigkeiten] Fügen Sie eine Option hinzu, um die benutzerdefinierten Abhängigkeiten des Pakets im Paket-Explorer zu öffnen.
* [Voreinstellungen] Fügen Sie eine Option hinzu, um den Standardszenenstatus in den Projekteinstellungen festzulegen
* [Voreinstellungen] Fügen Sie eine Option hinzu, um den Pfad für die Bibliothek zu aktivieren/deaktivieren
* [Diagramm] Fügen Sie eine Option hinzu, um einen Screenshot (im Maßstab 1:1) des Diagramms zu erstellen
* [Graph] Entfernen der QuickInfo vom Hintergrund von Compositing-Graphen
* [Scripting] Hinzufügen von onBeforeFileLoaded- und onAfterFileLoaded-Rückrufen
* [Engine] Hinzufügen eines Basisparameters, um den Pixelverhältnismodus anzupassen
* [Console] Verbessern der Konsolenleistung
* [Parameter] Widget &quot;Neue Position (XY)&quot;
* [Iray] Upgrade auf IRay SDK 2017.1
* [PSD] Speichern Sie den Status des PSD-Widgets als Text statt als Binärdatei
* [Bibliothek] Verwenden Sie Miniaturansichten von &quot;sbsar&quot;, wenn sie vorhanden sind
* [Explorer] Benennen Sie &quot;Abhängigkeiten&quot; um. Eintrag in &quot;Abhängigkeitsverwaltung&quot;
* Import von AXF-Dateien

**Fest:**

* [MDL] MDL-Modul kann nicht exportiert werden, wenn die Textur mit einem angezeigten Parameter verbunden ist
* [MDL] Versuchen Sie, die Abhängigkeit für MDL-Zeichenfolgenvariablen (konstanter Knoten) zu registrieren.
* [MDL] Absturz nach dem Schließen des Pakets
* [MDL] Absturz beim Verbinden eines Float 3 mit einem Farbknoten
* [MDL] kann die Knotenbibliothek nicht öffnen, wenn ein Verknüpfungsknoten in einem Frame freigegeben wird
* [MDL] Absturz bei Verwendung einer Dateistruktur
* [MDL] Abhängigkeitsverhalten registriert zu viele Operanden
* [Graph] Connector-Namen werden nach FX-Map-Bearbeitung deaktiviert
* [Graph] Absturz beim Rückgängigmachen
* [Graph] Seltsames Verhalten mit Verknüpfungen zwischen Knoten
* [Graph] Ausgeblendete Knoten - Streuung und Lösen, wenn rückgängig gemacht wird
* [Graph] Funktionsinstanzen werden nicht aktualisiert, wenn die Referenz geändert wird
* [Versionskontrolle] Paket wird neu geladen, wenn eine benutzerdefinierte Versionskontrollaktion ausgelöst wird
* [Versionskontrolle] Deaktivierte Arbeitsbereiche für die Versionskontrolle sind weiterhin im Kontextmenü eines Pakets verfügbar.
* [Versionskontrolle] Benutzerdefinierte Aktion entfernen entfernt diese nicht aus dem Kontextmenü eines Pakets
* [Eigenschaften] Die Parametervorschau wird bei Verwendung des Gizmos nicht aktualisiert
* [Iray] Problem mit der maximalen Zeitanzeige
* [Iray] Problem mit der Option zum Anhalten
* [Bäcker] Absturz beim Backen konvertieren UV in SVG mit koreanischer/japanischer Übersetzung
* [Bäcker] Das Ändern des Pfads nach dem ersten Backen funktioniert nicht
* [PSD Exporter] Problem rückgängig machen
* [PSD] Ordner und Ebenen sind in Photoshop CS5 gesperrt
* [UI]-Farbcursor ist immer auf Weiß eingestellt, wenn ein einheitlicher Farbknoten erstellt wird
* [UI] Beim Öffnen einer vorhandenen Registerkarte sollte diese angezeigt werden, anstatt sie zu duplizieren.
* [Vorgaben] stürzt ab, wenn der in einer Vorgabe verwendete Parametertyp geändert wird
* [3D-Ansicht] Sampler mit derselben Verwendung werden zusammengeführt
* [2D-Ansicht] Pixelinformationen funktionieren nicht für Bilder, deren Auflösung nicht eine Potenz von 2 ist
* [Library] Problem beim Umbenennen von Filtern
* [Daten] Verschiedene Tippfehler in SBS-Dateien beheben
* [Parameter] Level Node - Problem mit automatischer Präzision
* [Voreinstellungen] Die Schaltflächen für Vorlagenverzeichnisse sollten für &quot;Standardprojekt&quot; deaktiviert sein.

### 7.1.4 (2017.1.4)

*(Freigegeben: 2. Oktober 2017)*

**Hinzugefügt:**

* [Bäcker] Krümmung aus Gitterrücken hinzufügen
* [Neue Versionsprüfung] Fügen Sie eine Befehlszeilenoption hinzu, um die Prüfung auf eine neue Version zu deaktivieren (—news hide\_changelog:true).
* [Skripterstellung] Qprocess-Zeitüberschreitung deaktivieren

**Fest:**

* [Bäcker] können die Materialfarbe in UV nicht in SVG ändern
* [UI] kann die Diagrammansicht nicht mit einem Radklick schließen
* [Inhalt] Einige Geräusche sind in 8 Bit anstelle von 16 Bit vorhanden.
* [Inhalt] Kurvenglättung führt zu falschem Ergebnis, wenn Kachelung deaktiviert ist
* [Text] Absturz beim Ändern der Größe bestimmter Schriftarten

### 7.1.3 (2017.1.3)

*(Freigegeben: 31. August 2017)*

**Fest:**

* [3D View] Absturz beim Versuch, 3D View-Optionen unter Mac 10.10.5 anzuzeigen
* [3D-Ansicht] Textinformationen werden in der 3D-Ansicht nicht angezeigt, wenn der Bildschirm &quot;Hohe Auflösung&quot; verwendet wird
* [3D-Ansicht] Die globale Voreinstellung für OpenGL/DirectX wird beim Zurücksetzen des Materials nicht berücksichtigt
* [Inhalt] Height normal: Normal wird bei Verwendung von Sobel-Sampling umgekehrt
* [Inhalt] Die umgebende Verdeckung (hbao\_2) verhält sich nicht korrekt, wenn sie auf nicht quadratisch festgelegt ist
* [Inhalt] Eingaben der Maskengeneratoren befinden sich nicht in derselben Reihenfolge wie der Kombinator &quot;Gitterdaten&quot;.
* [2D-Ansicht] Histogramm: Auswahlinformationen werden bei einer Bildänderung nicht aktualisiert
* [2D-Ansicht] Histogramm: Informationen zum verwendeten Bereich werden für Graustufenbilder nicht angezeigt
* [Vorgaben] stürzt beim Umbenennen einer Vorgabe eines Graphen ab, der in einem anderen Graphen verwendet wird
* [Diagramm] X und Y werden auf der Symbolleiste &quot;Übergeordnete Größe&quot; invertiert

### 7.1.2 (2017.1.2)

*(Freigegeben: 03. August 2017)*

**Fest:**

* [Content] Filterproblem in den Filtern &quot;Smart Auto Tile&quot; und &quot;Crop Grayscale&quot;
* [Inhalt] Bibliotheksfilter berücksichtigen die OpenGL/DirectX-Voreinstellung nicht
* [Inhalt] SBSAR kann mit nicht\_square\_transform nicht gekocht werden
* [Inhalt] Panoramaform: Hotspot wird im RGB-Kanal gespiegelt
* [Inhalt] Kachel Sampler: Die Parametrisierung der Positionsfarbe ist nicht normalisiert.
* [Inhalt] Kachel Sampler: Muster sind unsichtbar, wenn die Unterteilung deaktiviert ist
* [Diagramm] Der Schalter $normal\_map\_format funktioniert nicht, wenn das Menü &quot;Bibliothek/Leertaste&quot; verwendet wird
* [Graph] Falsches Format im Bitmap-Knoten beim Ziehen und Ablegen einer RGBxxF-Ressource
* [Bäcker] Farbe aus Gitter mit Materialfarbe ist defekt
* [3D-Ansicht] jede Änderung in der 3D-Ansicht generiert Aktionen im Rückgängig-Stapel
* [Abhängigkeiten] stürzt ab, wenn in einem Diagramm Ressourcen in der benutzerdefinierten Bibliothek fehlen.
* [Iray] Absturz beim Start unter OSX Version ist älter als 10.11

### 7.1.1 (2017.1.1)

*(Freigegeben: 18. Juli 2017)*

**Hinzugefügt:**

* [Bäcker] Hinzufügen einer Aktion &quot;Zurücksetzen&quot; für Ressourcenfelder
* [Bäcker] Verwenden Sie schwarze Farbe, wenn keine Scheitelpunktfarbe gefunden wird
* [Vorgaben] Ausblenden des Vorgabe-Widgets in Instanzen, wenn keine Vorgaben verfügbar sind
* [Voreinstellungen] Entfernen Sie die Option &quot;Binormal durch Fragment berechnen&quot; in den Projekteinstellungen (jetzt wird diese Option im Tangentenrahmen-Plug-in behandelt).
* sbsupater.exe Anpassungen

**Fest:**

* [Bäcker] Das Fehlersystem funktioniert nicht mehr
* [Bäcker] Optionen Serialisierung: alte Schlüssel bleiben erhalten
* [Bäcker] stürzt beim Ändern des Namens eines Bäckerers ab
* [Bäcker] Benutzeroberflächenfehler
* [Inhalt] Farbabstimmungsfilter - Unterschied zwischen CPU/GPU
* [Inhalt] Einige GrungeMaps geben 8-Bit-Bilder statt 16 Bit aus.
* [Graph] Absturz bei Verwendung von X &quot;switch links&quot; auf fx-map node
* [3D-Ansicht] Zufälliger Absturz beim Öffnen der 3D-Ansicht
* [3D-Ansicht] Binormal werden immer durch Fragment berechnet, unabhängig vom Tangentenraum-Plugin
* [Updater] XML-Fehler bei Verwendung einer bestimmten Schriftart
* [Cooker] modulo auf negative Zahl gibt nicht das gleiche Ergebnis zurück wie die Engine
* Problem mit der Benutzeroberfläche von [UI] bei Verwendung des Auswahlverlaufs auf einem Bildschirm mit hoher DPI
* [MDL] Farbknoten behält seinen Wert nicht bei
* [Verpacken] Mikkt Unreal Tangentenraum-Plugin fehlt

### 7.1.0 (2017.1.0)

*(Freigegeben: 29. Juni 2017)*

**Hinzugefügt:**

* [Bäcker] Neue Benutzeroberfläche
* [Bäcker] Speichern Sie einen Cache mit hohem Def-Mesh, bis das Bäckerfenster geschlossen ist
* [Bäcker] Fügen Sie eine Option hinzu, um die Verzerrung mithilfe einer Graustufenmaske zu korrigieren.
* [Bäcker] Unterstützen Sie die Verwendung von Hochpoly-als-Niedrigpoly-in-Bäcker aus Gitter
* [Bäcker] Das Fenster &quot;Bäcker&quot; nicht modal machen
* [Bäcker] Speichern Sie den Status in einer .sbs-Datei im vom Menschen lesbaren Format
* [Parameter] Kopieren/Einfügen von Parametern von einem Diagramm in ein anderes
* [Parameter] Fügen Sie eine Option hinzu, um einen einzelnen Eingabeparameter zu kopieren (und anschließend einzufügen).
* [Parameter] Entfernen Sie die Funktionsschaltfläche für den Parameter &quot;Farbmodus&quot;.
* [Parameter] Bearbeiten/Speichern/Anzeigen eingebetteter Parametervorgaben
* [Parameter] Erlaubt dem Benutzer, Parameterattribute zu kopieren, wenn ein Paket gesperrt ist.
* [3D-Ansicht] Speichern Sie die 3D-Ansichtseinstellungen der letzten Sitzung nicht mehr in der Registrierung.
* [3D-Ansicht] Neue 3D-Ressource aus aktueller Szene erstellen
* [3D-Ansicht] Speichern Sie den 3D-Ansichtsstatus nicht mehr von einer Sitzung zu einer anderen in der Registrierung.
* [3D-Ansicht] Zusammenführen der Menüs &quot;Szene&quot; und &quot;Geometrie&quot;
* [3D-Ansicht] Separate sRGB-Konvertierung vom Fragment-Shader (Sie müssen Ihre benutzerdefinierten Shader aktualisieren!)
* [3D-Ansicht] Fügen Sie eine Option hinzu, um eine neue 3D-Ressource aus dem aktuellen Status zu erstellen.
* [3D-Ansicht] Verbessern der Fehlermeldung, die generiert wird, wenn #include in einen Shader-Code ausfallen
* [3D-Ansicht]&#x200B;[Explorer] Erstellen einer 3D-Szene aus Grundformen
* [3D-Ansicht] Richtige Zeilennummer anzeigen, wenn die Kompilierung des GLSL-Shaders fehlgeschlagen ist und Code #include Direktiven enthält
* [Diagramm] Die Größe eines Rahmens kann von allen Ecken/Rändern aus geändert werden.
* [Graph] Informationen zur übergeordneten Größe in der Diagrammressource statt in der lokalen Registrierung speichern
* [Graph] Optimierung der Generierungsgeschwindigkeit von Knoten-Miniaturansichten
* [Graph] Stellen Sie das Speichercachebudget in den Voreinstellungen bereit.
* [Graph] Hinzufügen einer Option &quot;Zurücksetzen und in 3D-Ansicht anzeigen&quot; auf Knoten
* [Inhalt] PBR-Konverter: Neue Arnold 4/5-, Corona 1.6- und Renderman-Vorgaben hinzufügen
* [Inhalt] AutoLevel-Knoten optimieren und HDR-Eingabe unterstützen
* [Inhalt] HBAO-Filter optimieren, wenn GPU-Optimierung deaktiviert ist, 16 Samples hinzufügen
* [Cooker] Ausgabe der nicht unterstützten SVG-Funktion in das Protokoll
* [Cooker] Verwerfen Sie nicht alle SVG-Ressourcen, wenn nur eine Funktion nicht unterstützt wird
* [UI] Größe des Beschreibungsblocks erhöhen
* [UI] Hinzufügen von Dateipfadinformationen zu Diagramminstanzen
* [Funktionen] Hinzufügen von &quot;Open Reference&quot; zu Funktionsinstanzen
* [Funktionen] Zeigt die Liste der Funktionsdiagramme an, wenn .sbs per Drag &amp; Drop in ein Funktionsdiagramm gezogen wird.
* [Explorer] Neue 3D-Ressource aus primitiven Elementen erstellen
* [Engine] Variable $tiling hinzufügen
* [Kurve] Hinzufügen von Optionen zum horizontalen/vertikalen Spiegeln der Kurve
* [Farbmanagement] ICC-Profil auf Bitmaps lesen
* [Exportieren] Fügen Sie &quot;Label&quot;, &quot;Group&quot; und &quot;User Data&quot; in der Makro-Liste Muster hinzu.
* [Voreinstellungen] Fügen Sie die Möglichkeit hinzu, den Pfad für Temp-Dateien zu ändern
* [Dok] Hinzufügen des MDL-Diagrammformats zur Dokumentation zum SBS-Format

**Fest:**

* [Graph] Cache-Problem: Ansicht der Ausgaben in der 3D-Ansicht funktioniert nicht mehr
* [Graph] Cache leeren
* [Diagramm] Generierungsanforderungen für Knoten-Miniaturansichten werden nicht abgebrochen, wenn das Diagramm ungültig wird.
* [Graph] Lösungsprobleme nach Verwendung von F5
* [Diagramm] Diagrammansicht fehlt beim Start
* [Graph] Das Ändern eines Parameters erzeugt einen mehrfachen Renderaufruf
* [Graph] Absturz bei Verwendung einer benutzerdefinierten Vorlage, die durch Baking erzeugte Map enthält
* [Graph] Absturz bei verknüpften Knoten in einer Diagrammfunktion
* [3D-Ansicht] Paralleles Laden mit ProgressManager
* [3D-Ansicht] Rendern mit Bild mit benutzerdefinierter Auflösung ist nicht Vollbild
* [3D-Ansicht]&#x200B;[Iran] Materialdefinition wird nicht beibehalten.
* [2D-Ansicht] Histogramm ist auf LDR-Bildern leer
* [2D-Ansicht] Anzeigeproblem bei aktiviertem Anordnungsmodus
* [MDL] Parameter nicht verfügbar gemacht
* [MDL]-Absturz beim Verschieben einer MDL von einem Paket in ein anderes während des Renderns
* [MDL] Fragen Sie nicht, wo die MDL zugewiesen werden soll, wenn Sie auf ein Diagramm doppelklicken.
* [Baker] Absturz beim Backen einer bestimmten .obj-Datei
* [Bäcker] Übertragene Textur aus Mesh / Normal führt zu einem falschen Ergebnis
* [Transformation 2D] Der Offset im 2D-Transformationsknoten kann nicht mit den Pfeiltasten geändert werden
* [Transformation 2D] Artefaktproblem mit niedriger Auflösung
* [Updater] Aktualisierungsbericht wird nicht angezeigt, wenn Strg+o/open verwendet wird
* [Eigenschaften]&#x200B;[Format] Einige Zeichen werden in UserTags zweimal mit Escapezeichen versehen
* [Bitmap-Knoten] Strg Z funktioniert nicht in der 2D-Ansicht
* [Voreinstellung] Nicht verwendeter leerer Bereich auf der Registerkarte &quot;Aliase&quot;
* [Installationsprogramm] Die Installation einer früheren Version funktioniert nicht beim ersten Mal
* Dropdownliste [Parameter]: Wenn einige Leerzeichen auf den letzten Wert gesetzt werden, friert SD unendlich ein
* [UI]&#x200B;[MAC] &quot;Info zum Substance&quot; zeigt Iray-Informationen an.
* [SVG] Absturz beim Importieren einer bestimmten SVG
* [Inhalt] HBAO-Filter: Der Parameter &quot;Radius&quot; verhält sich in Abhängigkeit von der Auflösung anders (ein neuer hbao\_2.sbs wurde hinzugefügt, der alte hbao.sbs ist jetzt veraltet).

## Version 6

### 6.0.4

*(Freigegeben: 21. Juni 2017)*

**Fest:**

* [Graph] Absturz mit X-Verknüpfung
* [Graph] stürzt nach dem Löschen einer Verknüpfung zwischen Knoten ab
* [Graph] Löschen eines Teilungspunkts führt zum Absturz von SD
* [Inhalt] Typo in mg\_surface\_brush
* [Inhalt] Geringere Qualität auf HBAO als 6.0.2
* [Library] Die Symbole benutzerdefinierter Filter werden nicht gespeichert.
* [Explorer] Absturz beim Öffnen einer 3D-Ressource, die auf eine fehlende Datei verweist
* [Bäcker] Die Option &quot;Textur aus Mesh übertragen&quot; wird gespiegelt, wenn die Option &quot;Normal&quot; aktiviert ist

### 6.0.3

*(Freigegeben: 1. Juni 2017)*

**Hinzugefügt:**

* [Exportieren] Speichern Sie die Physische Größe als dpi in exportierten Texturen
* [2D-Ansicht] Anzeigen der Matrixparameterbeschriftung im Menü &quot;Transformation&quot;

**Fest:**

* [Inhalt] Kachel Sampler: Die Parametrisierung der Positionsfarbe ist nicht normalisiert.
* [Inhalt] Freistellen: Geisterdiagramm im Pixelprozessor
* [Inhalt] Panoramaform: Hotspot wird im RGB-Kanal gespiegelt
* [Inhalt] HBAO-Filter kann eine negative Auflösung generieren
* [Inhalt] Farbabgleich-Filter wird in einigen Situationen falsch gerendert
* [Inhalt] &quot;Vormultipliziert in gerade&quot; entfernt den Alphakanal
* [Inhalt] Tippfehler in verschiedenen Beschriftungen
* [Graph] Bittiefe-Informationen werden beschnitten, wenn die DPI-Skalierung auf 125,1520 oder 175 % eingestellt ist
* [Diagramm] Wenn eine Auswahl, die einen Rahmen enthält, eingefügt wird, wird der nicht ausgewählte Rahmen
* [Diagramm] Wenn eine Auswahl einen Kommentar enthält, werden die eingefügten Elemente im Diagramm verschoben
* [Graph] Problem mit Teilungspunkten
* [Graph] Einige Stiftverbindungen rasten nicht ein, wenn der Mauszeiger bewegt wird
* [Diagramm] Diagrammansicht fehlt beim Start
* [Export] Fehlende Bitmaps nach Export
* [Exportieren] Exportiert die Abhängigkeiten nicht in der Dampfversion.
* [Bäcker] Absturz mit Gitter, das zu viele UV-Sätze hat
* [Bäcker] UV Map Baker-Absturz beim Backen von Netzen ohne UV-Sets
* [Engine] Sampler-Fehler mit Fxmap+HDR
* [Engine] Absturz mit hochauflösenden JPEG-Bildern
* [2D-Ansicht] Transformieren-Widget fehlt in 2D-Ansicht, wenn der Vorschaumodus &quot;Kacheln&quot; aktiviert ist
* [3D-Ansicht] Die Diagramminstanz mit benutzerdefinierter Verwendung wird nicht korrekt an die 3D-Ansicht gesendet
* [Voreinstellungen] Falscher Pfad für mikktspace.dll
* [Explorer] Durch Verschieben einer Bitmapressource in ein Paket wird das Menü &quot;link/embed&quot; geöffnet.
* [Parameter] Absturz bei Verwendung von &quot;Tiling&quot; als Parametername
* [MDL] keine farbigen Verknüpfungen zwischen Knoten
* [Linker] Pixelprozessor: Falsche Generierung von GLSL-Shadern
* Problem mit der Bittiefe von [Cooker]

### 6.0.2

*(Freigegeben: 17. März 2017)*

**Hinzugefügt:**

* [Engine] Integration der neuesten Engine mit JPEG-Dekomprimierungsoptimierung

**Fest:**

* [Inhalt] Clone-Patch funktioniert nicht mehr
* [Inhalt] Die Materialausgabe ist nicht Teil der Materialgruppe in Vorlagen.
* [MDL] Absturz beim Löschen einer Diagramminstanz
* [MDL] Keine Warnung zwischen in Konflikt stehenden Knoten
* [MDL] Benutzerlose Warnmeldungen beim Exportieren
* [Kurve] Adressierungsparameterexponierung sollte nicht verfügbar gemacht werden können.
* [Engine] Absturz beim Importieren eines SBSAR, der eine HDR-Bitmap enthält
* [Textknoten] Die Schriftspezifikation generiert eine ungültige XML-Datei.
* [Verlaufseditor] Werte werden nicht korrekt eingespannt
* [3D-Ansicht] Absturz bei Verwendung einer benutzerdefinierten (hochauflösenden) HDRi als Umgebung

### 6.0.1

*(Freigegeben: 03. März 2017)*

**Hinzugefügt:**

* [Bäcker] Verbessern des Fortschrittsaufgaben-Managements
* [Bäcker] Ändern der Fehler-QuickInfo, wenn kein Gitter ausgewählt ist
* [Eigenschaften] 3DView Post Effect-Parameter sollten deaktiviert sein, wenn &quot;Post Process&quot; in den Voreinstellungen deaktiviert ist
* [Lizenz] Geben Sie einen benutzerdefinierten Pfad für die Lizenz für Substance Designer 6 an.
* [Verlauf] Deaktivieren Sie den Regler &quot;Präzision&quot;, wenn kein Verlauf ausgewählt wurde.
* [Cooker] Fehlende Ressource in der Bildeingabe ignorieren, um Fehler beim Kochen zu verhindern
* [3D-Ansicht] Ändern der Handhabung von Specular-Reflektionslecks
* [Graph] Fügen Sie weitere Parameter für die Kompatibilität der Engine V6 hinzu.

**Fest:**

* [Bäcker] Normalmap aus Gitter (Weltraum) wird auf Y-Achse gespiegelt
* [Bäcker] Beim Backen eines Gitters ohne UV kann kein Fehler gemeldet werden.
* [Bäcker] Durchschnittliche Normalität funktioniert nicht
* [Bäcker] SD stürzt beim Backen von AO mit einem bestimmten Gitter ab
* [Bäcker] Das Ausgabeformat wird nicht richtig wiederhergestellt
* [Text] Benutzerdefinierte Schrift funktioniert nicht im Player
* [Text] Warnung zu ungültiger Schrift beim erneuten Öffnen eines Pakets mit Schrift in Ressourcen
* [Text] Texteingabe funktioniert nicht im Vorschaumodus
* [Text] Schriftartparameter kann angezeigt werden.
* [Text] Einfrieren/Absturz beim Erstellen einer Funktion im Textparameter
* [Text] Absturz beim Anzeigen der Schriftgröße
* [2D-Ansicht] Der Zoomfaktor wird bei Verwendung der Taste &quot;F&quot; nicht korrekt angezeigt
* [2D-Ansicht] Bild wird verschoben, wenn die Größe geändert wird
* [2D-Ansicht] Diskontinuität bei der Anzeige der Unterteilung
* [2D-Ansicht] Transformations-Guizmo ist im Vorschaumodus nicht sichtbar/bearbeitbar
* [3D-Ansicht] Physische Größe wird von PBR Parralax Shader nicht berücksichtigt
* [3D-Ansicht] Die Einstellung der Aktualisierungsrate wird von einer Sitzung in eine andere nicht korrekt wiederhergestellt
* [Diagramm] multiangle\_to\_normal verhindert Veröffentlichung
* [Graph] Die Ausgabegröße des Pow-Filters ist gesperrt
* [Graph] .sbsar-Dateien können nicht instanziiert werden.
* [Kurve] Benutzeroberfläche beschnitten
* [Kurve] Die Zahlenanzeige wird leicht beschnitten.
* [Kurve] Widget verschwindet, wenn die Größe der Symbolleiste geändert wird
* [Inhalt] Der Glühknoten ist defekt.
* [Inhalt] Kachel Sampler: Muster sind unsichtbar, wenn die Unterteilung deaktiviert ist
* [Inhalt] MG Mask Builder - Kontrastparameter für invertierte Krümmung
* Color Equalizer [Inhalt]: benutzerdefinierte\_farbe\_variationsgruppenparameter nicht verbunden
* [Inhalt] Klonpatch: Ausbesserungsbereich nicht sichtbar, wenn er in Ecken positioniert wird
* [Explorer] Das erneute Laden eines Pakets, während seine Abhängigkeit geöffnet ist, unterbricht das Abhängigkeitspaket.
* [Explorer] Eine 32-Bit-PSD-Ressource kann nicht importiert werden.
* [Publish] Fehler beim Kochen (ERR:No-Vererbung (absolut))
* [Verlauf] Der Verlauf sollte als Linear angezeigt werden, wenn sRGB deaktiviert ist
* [Transformation2D] Offset-Eindruck beim Verschieben eines Guizmo mit Achseneinschränkung
* [Parameter] Mausfokus wird durch Dropdown gestohlen
* [Engine] Keine Kachelung hat keine Auswirkungen auf den Distanzknoten auf der GPU-Engine
* [Export] Absturz beim Exportieren von Ausgaben als TGA
* [MDL] Exportvorgabe funktioniert nicht

### 6.0.0

*(Freigegeben: 14. Februar 2017)*

<b>Hinzugefügt:</b>

* [Engine] Neuer Kurvenknoten
* [Engine] Neuer Textknoten
* [Engine] 16f/32f Bittiefe Compositing
* [Engine] Instanziieren für GPU FX-Maps
* [Engine] Funktion &quot;log2 hinzufügen&quot;
* [Bäcker] 8k Kartenbacken
* [Bäcker] Backen nach Material / &quot;Textur Set&quot;
* [Bäcker] Anzeige einer Lademeldung, wenn die Bitmapausgabe codiert/auf die Festplatte geschrieben wird
* [Bäcker] Hinzufügen einer Abbruchoption während des Backens
* [Verlaufsknoten] Hinzufügen globaler Anpassungen für mehrere ausgewählte Tasten
* [Verlaufsknoten] Optionen der Option &quot;Verlaufsauswahl vereinfachen&quot;
* [Diagramm] Fügen Sie eine Option hinzu, um die übergeordnete Standardgröße zu ändern.
* [Graph] Anzeige der Pixel-Tiefe des Bilds unter dem Knoten
* [Voreinstellungen] Globale Voreinstellungen für DirectX/OpenGL
* [Voreinstellungen] Verwenden von Registerkarten in den Voreinstellungen/in der Projekt-Benutzeroberfläche
* [Voreinstellungen] Parameter MaxTextureSize in den &quot;3DView&quot;-Voreinstellungen entfernen
* [Voreinstellungen] Kurze Hilfe zum automatischen Speichern anzeigen
* [Voreinstellungen] Optionen für das Bildformat verfügbar machen
* [Voreinstellungen] Fügen Sie eine Option hinzu, um die Umgebungskarte standardmäßig in der 3D-Ansicht auszublenden.
* [Voreinstellungen] Hinzufügen einer Option für die Standardalphanoption des normalen Map-Filters
* [2D-Ansicht] Fügen Sie die Möglichkeit hinzu, von den Texturgrenzen weg zu schwenken
* [2D-Ansicht] Interpretieren des X/Y-Verhältnisses der Physische Größe
* [3D-Ansicht] Verbesserung des Texturmanagements
* [3D-Ansicht] Deaktivieren Sie Post Effects standardmäßig (um Abstürze bei geringer GPU zu verhindern)
* [MDL-Diagramm] Verwalten des ausgeblendeten Flags für den IRay-Parameter
* [MDL-Graph] Erlauben Sie, den Konstruktor &quot;material()&quot; als Stammknoten festzulegen.
* [MDL Graph] SBS Graph-Instanzknotenvorschau erstellen
* [Inhalt] Neue Filter für die Scanverarbeitung hinzufügen
* [Inhalt] Hinzufügen neuer Einstellungsfilter (Klemmen, POW, HDR-Bereichsanzeige)
* [Inhalt] Blaues Rauschen hinzufügen (schnelle Annäherung)
* [Inhalt] Hinzufügen neuer Formeffekte (Leuchten, Schlagschatten, Kontur)
* [Publish] Fügen Sie die Aktion &quot;Als vorherigen exportieren&quot; hinzu, um das zuletzt ausgewählte Paket erneut zu veröffentlichen.
* [Publish] Verbessern der SBSAR-Generierung bei Verwendung von Bitmaps mit hoher Auflösung
* [Publish] Warnen Sie den Benutzer vor der Einstellung &quot;relativ zum übergeordneten x1-Diagramm&quot;, wenn er die Grafik veröffentlicht oder auf Share hochgeladen hat
* [Eigenschaften] Hinzufügen des Attributs &quot;Physische Größe&quot; in SBS-Diagrammen
* [Parameter] Entfernen von Funktionsaktionen für PKG-Ressourcenpfade
* [Parameter] Popup-Fenster &quot;Vorschauwerte geändert&quot; entfernen

<b>Fest:</b>

* [Diagramm] Die Speichernutzung wächst regelmäßig, wenn das Kontextmenü geöffnet wird
* [Graph] [In SSE2] Die Knoten des Polygons zeigen keine Formen an, wenn der Parameter &quot;Skalierung&quot; negativ ist
* [Graph] Absturz beim Wechsel von &quot;Integer&quot; zu &quot;Float&quot; bei einem angezeigten Parameter
* [Diagramm] Wenn Sie Knoten verschieben, während ein Teilungspunkt ausgewählt ist, werden die Knoten neu berechnet.
* [Diagramm] &quot;Rückgängig&quot; wird von &quot;Teilungspunkten&quot; nicht unterstützt.
* [Diagramm] leere QuickInfo, die angezeigt wird, wenn die Diagrammbeschreibung nicht druckbare Zeichen enthält
* [MDL Graph] Absturz, wenn der aktuelle, in der Eigenschaftenansicht angezeigte Knoten gelöscht wird
* [MDL-Diagramm] MDL-Diagramm, das die material()-Konstruktorfunktion als Stamm verwendet, wird in der 3D-Ansicht nicht korrekt gerendert
* [MDL] MDL-Modul kann nicht exportiert werden, wenn ein bedingter Operator mit einem einheitlichen booleschen Exposé-Parameter verwendet wird
* [MDL] Absturz beim zweimaligen Laden einer MDL-Diagrammvorlage
* [MDL-Archiv] Materialien, die eine Textur verwenden, werden nicht ordnungsgemäß verwaltet
* [3D-Ansicht] IRay-Material wird nicht geändert, wenn sich der Stammknoten des MDLGraph ändert
* [3D-Ansicht] willkürlicher Absturz beim Schließen der 3D-Ansicht, während ein Gitter geladen wird
* [3D-Ansicht] Yebis wird nach dem Speichern des Renderings nicht wieder aktiviert
* [3D-Ansicht] Beim Speichern des Renderergebnisses einer Bildszene wurde eine ungültige PSD-Datei generiert.
* [3D-Ansicht] Punktlicht 1 leuchtet nicht
* [UI] Der Erkennungsbereich der Kontrollkästchen ist in den Parametern &quot;Bäcker aus Gitter&quot; zu breit.
* [UI] Ästhetisches Problem in &quot;Bäcker aus Mesh&quot; Parametern
* [Mac] Das Öffnen von SD durch Doppelklick auf einen SBS sendet keine Ausgabe an die 3D-Ansicht
* [Mac] [Iran] Fotoreales Cluster-Rendering funktioniert nicht auf MacOS
* [Engine] Atan2(0, 0) führt zum Absturz des Motors
* [Engine] Kritisches Synchronisierungsproblem
* [Bäcker] Automatische Normalisierung für Height-Bäcker kann nicht deaktiviert werden
* [Parameter] beim Konvertieren von Graustufen in RGBA sollte Alpha 255 sein
* [Funktionen] Es ist möglich, eine Funktion als Ausgabeknoten festzulegen, auch wenn sie nicht kompatibel ist.
* [Export] Ungültige Abhängigkeiten nach dem Exportieren eines Pakets mit PSD-Ressourcen
* [Konsole] Das Löschen der Konsole führt zum Absturz von SD

## Version 5

### 5.6.2

*(Freigegeben: 08. Februar 2017)*

**Fest:**

* [Voreinstellungen] Standard-Shader wird nicht berücksichtigt
* [3D-Ansicht] Absturz, wenn der Standardshader zur Laufzeit geändert wird
* [Engine] Problem mit $size erhalten

### 5.6.1

*(Freigegeben: 17. Januar 2017)*

**Hinzugefügt:**

* [3D-Ansicht] Legen Sie die Größe der Grundelemente auf 100 cm fest.
* [Inhalt] Hinzufügen von &quot;Bildeingangsfilterung&quot; zu &quot;Platterkreis&quot; und &quot;Platter&quot;
* [Bäcker] &quot;Krümmung aus Mesh&quot; Konsolenwarnungen unter Kanal &quot;Mesh Sanity Check&quot; hinzufügen

**Fest:**

* [3D-Ansicht] Verschwinden, wenn sie abgedockt ist
* [Graph] Die Parameter &quot;Noise&quot; und &quot;Precision&quot; der Verlaufsumsetzung funktionieren nicht mehr
* [3D-Ansicht] ALT+R funktioniert nach dem Speichern des Renderings nicht
* [Bäcker] &quot;Curvature From Mesh&quot;-Absturz mit einigen ZBrush-Netzen

### 5.6.0

*(Freigegeben: 15. Dezember 2016)*

**Hinzugefügt:**

* [Inhalt] Neuer Filter &quot;AO (Horizon Base Ambient Verdeckung)&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Height-Überblendung&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Height zu Normal (Welteinheiten)&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Material Height Blend&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Snow Cover&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Wasserstand&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Farbabgleich&quot; hinzugefügt
* [Inhalt] Neuer Filter &quot;Histogramm-Scan (ungleichmäßig)&quot; hinzugefügt
* [Voreinstellungen] [UI] Fügen Sie in den Voreinstellungen eine Option hinzu, um die High-DPI-Erkennung zu deaktivieren
* [3d View] Option &quot;Kameraposition zurücksetzen&quot; hinzufügen
* [Iray] Integrieren von IRay SDK 2016.2 für Pascal-Architekturunterstützung
* [Graph] Option &quot;Knoteninformationen in die Zwischenablage kopieren&quot; im Kontextmenü hinzufügen

**Fest:**

* [MDL] Algenmaterialwurzel wird in der exportierten Voreinstellung nicht entfernt
* [MDL-Diagramm] Links für fehlende Ressource werden im MDL-Diagramm nicht gelöscht.
* [Library] Erstellen eines neuen Filters erstellt zwei Grundbedingungen
* [Library] Ordner filtert den Inhalt der Bibliothek nicht mehr
* [Bäcker] Fortschrittsleiste kommt und geht
* [Bäcker] Nicht vorhandene Käfigressource verhindert das Backen
* [Content] Verschiedene Fehler in &quot;Functions.sbs&quot;
* [Exportieren] Dateiformat wird immer auf png zurückgesetzt
* [UI] Problem mit der Skalierung der Substance Designer-Benutzeroberfläche
* [Graph] Absturz beim Verschieben des Originalpakets einer Graph-Instanz
* [Voreinstellungen] Wenn das Standardprogramm für Shader/Tangente-Plugin/... nicht gefunden wird, verwenden Sie die im Standardprojekt definierten
* [Parameter] Schieberegler sind in Mac zu präzise
* [Explorer] Das Verschieben von 3D-Gittern aus einem Ordner in einen anderen beschädigt diese Ressource.
* Das Schließen des Fensters beendet den SD-Prozess nicht
* Das Dialogfeld zum Öffnen von Dateien zeigt keine Dateien mit dem Filter &quot;Alle Formate&quot; an

### 5.5.3

*(Freigegeben: 28. Oktober 2016)*

**Fest:**

* [Shelf] Absturz beim Erstellen des Ordners
* [Bäcker] World\_Space\_Direction funktioniert nicht mehr

### 5.5.2

*(Freigegeben: 18. Oktober 2016)*

**Hinzugefügt:**

* [MDL Graph] Übergeben von SBS Graph-Standardwerten an die SBS Graph Node-Instanz in MDL Graph
* [MDL] Unterstützung von Drag &amp; Drop des SBSAR-Diagramms
* [IRay] Upgrade auf SDK 2016.1.6 (261500.16187)
* [sbsrender] Optimieren Sie die Speicherverwaltung von sbsrender, um die Player-Leistung anzupassen
* [3D-Ansicht] Erlaubt, dass die Widget-Größe kleiner als die obere Menüleiste ist
* [Konsole] Kopieren einiger Zeilen in die Zwischenablage zulassen

**Fest:**

* [Player] Absturz bei der Wiedergabe eines Pakets direkt in Designer durch die &quot;Wiedergabe-Schaltfläche&quot;
* Popup-Fenster [Startup] zeigt fehlende Datei nvcuvid.dll an
* [Environment init] Das Doppelklicken auf eine .sbs-Datei lädt sie nicht in SD
* [Export] Export mit Abhängigkeiten stürzt ab
* [MDL] Synchronisierungsproblem zwischen einem Diagramm und seiner Instanz
* [MDL] sbsar-Instanzknoten geben texture\_return anstelle von Werten aus
* [IRay 3D View] In Iray Renderer wird der &quot;Height Channel&quot; nicht korrekt aktualisiert, wenn Sie die Height Map ändern
* [IRay 3D View Undocked] &quot;Kamera > Render speichern&quot; funktioniert nicht, nachdem die App in der Windows-Taskleiste ausgeblendet wurde
* [Mac IRay] NVIDIA GPU wird von IRay nicht mehr erkannt
* [Bäcker] Transferierte Textur aus Mesh Crash beim Backen von Nicht-POT-Texturen
* [Absturz] Absturz beim Exportieren eines Diagramms auf dem Substance share
* [Graph] Absturz beim Auswählen einer Ghost-Instanz
* [3D-Ansicht] Die orthogonale Kamera kann im Iray-Modus nicht verschoben werden (Einzoomen oder Auszoomen)
* [UI] Der Farbwähler verwaltet die Anzeige mit hohem DPI-Wert nicht
* [Graph] (MacOS 10.11.06) Unendliche Berechnung mit Multimaterial-Mischknoten
* [Graph] Kopieren/Einfügen Graph&#39;s content ==> paste in the content and also a reference to that graph
* [Graph] Mehrere Material-Überblendungen in der Szene, es automatisch die falschen Ausgaben auswählen
* [Graph] Metal-Edge Wear blockiert PC
* [Bibliothek] In den SBSAR-Dateien wird &quot;S&quot;-Logo anstelle von Miniaturen angezeigt.
* [Bibliothek] Ordner in .sbsar werden in der Bibliothek angezeigt

### 5.5.1

*(Freigegeben: 08. September 2016)*

**Hinzugefügt:**

* [Iray] Hinzufügen des &quot;IQ&quot;-Modus zum Cloud-Rendering
* [Iray] Aktualisierung auf Iray SDK 2016.1.5

**Fest:**

* [MDL] Die Ansicht in der 3D-Ansicht funktioniert zum ersten Mal nicht ordnungsgemäß.
* [MDL] Farbverlauf\_Interpolation\_linear wird nicht mit dem vollständigen Pfad exportiert
* [MDL] neu erstellter Rahmen unten rechts ist genau mit dem zugehörigen Knoten ausgerichtet
* [MDL] Die Miniaturansicht des Stammmaterials wird in einigen Fällen nicht aktualisiert
* [MDL] Absturz beim Löschen aller Knoten und Wiederholen
* [MDL] Langsame Bewegungen in der Graphanzeige im Vergleich zum Substance-Grafen
* [MDL] MDL-Modul kann aufgrund des IOR-Parameters nicht exportiert werden
* [MDL] Angezeigte Parameter entsprechen nicht dem ausgewählten Knoten
* [3D-Ansicht] MDL-Material, das aus einem MDL-Diagramm stammt, wird nicht zurückgesetzt, wenn der Stammknoten gelöscht wird
* [3D-Ansicht] Standard-Kamerarahmen gehen nach dem Laden des Gitters von fbx verloren
* [3D-Ansicht] Texturzuweisung wird beim Wechsel zu Iray nicht beibehalten
* [Iray] Warnmeldung von IRay beim Bewegen der Kamera
* [Iray] Absturz beim Wechsel zu Iray
* [Iray] VCA-Kennwort wird nicht gespeichert
* [Graph] Absturz beim Löschen von Knoten
* [Diagramm] Das Drücken von STRG zum Kopieren des Links funktioniert nicht mit dem Materialmodus
* [Graph] Absturz beim Löschen des Ausgabeknotens in einem Instanzknotenmaterial
* [Bäcker]&#x200B;[3D-Ansicht] High-Definition-Mesh kann nicht geladen werden
* [Mac]&#x200B;[3D View] Absturz beim Versuch, getrennte Fenster auf dem sekundären Monitor wiederherzustellen
* [Parameter] Ein Wert kann in einem Spinbox-Edit nicht bearbeitet werden, ohne das Suffix zu entfernen
* [UI] Verwenden Sie &quot;Abbrechen&quot; beim Schließen von SD sollte Nachrichtenfeld stoppen
* Absturz beim Öffnen von zwei 3D-Ansichten
* Absturz in Alg::Scripting::Engine, wenn viele VisibleIf-Bedingungen verwendet werden
* Dateien werden durch automatisches Speichern gelöscht, wenn eine .algautosave-Datei vorhanden ist

### 5.5.0

*(Freigegeben: 25. August 2016)*

<b>Hinzugefügt:</b>

* Substance Designer ist jetzt unter Linux verfügbar
* Neuer MDL-Editor (Material Definition Language)
* [Bäcker] Neue Krümmung von Mesh-Bäcker
* [Library] Verwenden Sie SVG-Symbole anstelle von Bitmapdateien
* [Library] Fügen Sie eine Option hinzu, um das Ergebnis nach MDL, Compositing, Funktion und Fxmap zu filtern.
* [Graph] Erweitern Sie den &quot;Anzeige neu erstellten Knoten&quot; zu kopieren / eingefügt / dupliziert Knoten
* [Neues Dokument] Erstellen eines Vorlagenauswahl-Widgets beim Erstellen eines neuen MDL-Diagramms
* [3D-Ansicht]&#x200B;[Iris] Anzeige des Rendermodus + VCA-Knoten neben Iterationen/Zeit
* [3D-Ansicht] Verbessern der Menüleistung &quot;Material&quot; beim Öffnen
* [3DView]&#x200B;[Bäcker] Update auf FBX SDK 2017
* [3D-Ansicht] Sie können Rendering-Informationen (Auflösung, Iterationen usw.) ein- bzw. ausblenden. im Anzeigemenü der 3D-Ansicht
* [Iray] Stellen Sie die Tesselierungsparameter wieder der Szenenbearbeitung zur Verfügung.
* [Project] Automatisch generierte Alias für das Projektdateiverzeichnis hinzufügen
* [Projekt] Geben Sie die Standardumgebungstextur in den Projekteinstellungen an.
* [Inhalt] Neues Studio HDRi hinzugefügt
* [Inhalt] Hinzufügen eines nicht quadratischen Transformationsknotens zur Bibliothek
* SD mit einer bestimmten .sbscfg-Datei starten

<b>Fest:</b>

* [Diagramm] Eingaben werden nicht automatisch mit Ausgaben derselben Verwendung verbunden.
* [Graph] Eingaben eingefügter Knoten werden nicht korrekt eingesteckt
* [Graph] Die Deaktivierung sollte auch einen Knoten unter der Maus auswählen
* [Graph] Knoteneinfügung wird nicht mit allen Verknüpfungen verbunden
* [Bäcker] Falsche Diffusion im Krümmungsbäcker
* [Bäcker] &quot;Transferred texture from mesh&quot; stürzt ab, wenn das HD-Mesh keine UVs hat
* [UI] Funktionssymbol für Parameter wird nicht geändert, wenn eine Funktion definiert ist
* [UI] QuickInfos für Parameter werden ausgeschnitten
* [3D-Ansicht] mehr als 1000 Lichter werden in der Szene angezeigt
* [3D-Ansicht] GLSL Lambert-Shader verwaltet die srgb-Textur nicht korrekt
* [3D-Ansicht] Kachelparameter fehlen beim Verbinden von Stoffen in Irak
* [Iray] Voreingestellter Export von mdl funktioniert nicht, wenn Leerzeichen im Namen
* [Iray] Untergliederungsparameter werden nicht berücksichtigt.
* [Parameter] Die Parameterkennung wird nicht mehr angezeigt.
* [Parameter] Absturz beim Ändern der Ressourcen-URL von der &quot;Von Ressource...&quot; Aktion
* [Parameter] Falsche Konvertierung von und Zeichen
* [Explorer] Wenn Sie auf ein &quot;großes&quot; Diagramm doppelklicken, können Sie es häufig nicht in der Diagrammansicht öffnen
* [Explorer] Eingebettete SVG werden im Explorer als fehlend angezeigt
* [Explorer] Absturz beim Umbenennen eines Elements mit dem Zeichen &quot;&amp;&quot;
* [Inhalt] Die Kachelung von Farbverlauf 1 ist falsch, wenn eine 90/180°-Drehung verwendet wird
* [Perforce] Die Integration funktioniert anscheinend nicht, wenn sich der Arbeitsbereich im Stammverzeichnis der Festplatte befindet
* [Daten] Für Knoten generierte UID sind nicht eindeutig.
* [Voreinstellungen] Das Hinzufügen eines Alias für HDD-Root führt zu Pfadfehlern in sbsprj
* [MEMORY LEAK] Einige QDialoge werden nicht zerstört, wenn sie geschlossen werden

### 5.4.0

*(Freigegeben: 29. April 2016)*

**Hinzugefügt:**

* Link zum Substance Store hinzufügen
* [UI] Unterstützung für hohe DPI-Auflösungen
* [UI] Neuanordnung von Registerkarten zulassen
* [3D-Ansicht] Exportieren des Renderings in die ArtStation zulassen
* [3D-Ansicht] Hinzufügen des Standard-Shaders in der Shader-Liste
* [Graph] Zeigt den Ressourcennamen über dem Bitmapknoten an.
* [Graph] Verbessern der Auflistungsreihenfolge des Leertaste-Suchmenüs
* [Bäcker] Neuer Bäcker &quot;Position from Mesh&quot;
* [Bäcker] Neue Einstellung &quot;Normalmap&quot; für Texturtransferbaker
* [Bäcker] Neue Einstellung &quot;Tangent&quot; &amp; &quot;Binormal&quot; für World Space Normal Bäcker
* [Skripterstellung] Erlaubt die Ausführung von Skripten während der Aktionen &quot;Speichern&quot;, &quot;Exportieren&quot; und &quot;Publish&quot;
* [Abhängigkeiten] Fügen Sie je nach Auswahl eine Option zum Reduzieren/Erweitern hinzu.
* Es wurde eine Warnung zu Konflikten mit Shellerweiterungen hinzugefügt.

**Fest:**

* Absturz beim Beenden
* Substance Designer-Prozess kann nach dem Beenden noch ausgeführt werden
* [Iray] Ausgaben werden beim Wechseln des Renderers nicht an mdl-Materialien gesendet
* [Inhalt] Mustergenerator: Musterrotation zufällig sollte die Form nicht drehen

### 5.3.5

*(Freigegeben: 06. April 2016)*

**Fest:**

* [2D-Ansicht] Die Menüoption &quot;Transformation 2D Rechtsklick&quot; ist für jeden Knoten verfügbar.
* [2D-Ansicht] Transformation 2D-Gizmo nach dem Löschen des Transformationsknotens noch bearbeitbar
* [3D-Ansicht] Der Umgebungspfad sollte nicht in den Umgebungsparametern angezeigt werden.
* [3D-Ansicht] Post-Effekt-Parameter werden nicht in 3D-Ressourcen gespeichert
* [3D-Ansicht] Das Symbolleistenmenü verhält sich nicht wie ein normales Menü
* [Voreinstellungen] Der &quot;Engine-Cache-Grenzwert&quot; kann nicht höher als 4095 eingestellt werden
* [Voreinstellungen] Das Festlegen eines Standard-Shaders wird nicht berücksichtigt
* [Iray] Farbparameter werden nicht korrekt abgerufen.
* [Iray] MDL-Materialfarben werden zurückgesetzt.
* [Iray] Bitmaps werden nicht zusammen mit der MDL-Vorgabe exportiert
* [IRay/Mac] Das Ändern der Größe der 3D-Ansicht führt zum Absturz der Mac Workstation
* [Graph] PSD-Dokument kann nicht exportiert werden
* [Graph] Falsche angezeigte Knotengröße
* [Funktionsdiagramm] Ein Beispielknoteneingabebild kann nicht bearbeitet werden, wenn nur ein Bild angeschlossen ist
* [Engine] Absturz beim Berechnen des Fxmap-Diagramms
* [Engine OGL] Fehler bei der Pixelprozessorgenerierung
* [Farbverlauf] Die Farbverlaufsauswahl funktioniert nicht auf Mac
* [PSD] 8-Bit-Bild wurde nicht korrekt in 16-Bit konvertiert
* [Parameter] Histogramm-Widget auf Ebene hat nicht dasselbe Height in Farbe und Graustufen
* [Konsole] Durch Klicken auf eine Zelle wird die Ansicht horizontal gescrollt.
* [Explorer] Umgesiedelte 3D-Ressourcen werden in der 3D-Ansicht nicht korrekt geöffnet

### 5.3.4

*(Freigegeben: 16. Januar 2016)*

**Fest:**

* [Iray] Tangente/binormal werden nicht korrekt berücksichtigt
* [Explorer] Das Paket ist als unmittelbar nach dem Öffnen zu speichernd markiert.
* [3D-Ansicht] IBL Diffuse Reflexion ist zu stark
* [3D-Ansicht] Absturz beim Ziehen und Ablegen eines 8-Bit-Bildes aus dem Explorer in die 3D-Ansicht
* Applikation stürzt seit dem 1. Januar 2016 ab

### 5.3.3

*(Freigegeben: 10. November 2015)*

**Hinzugefügt:**

* [Inhalt] Hinzufügen von &quot;White Noise Fast&quot; (basierend auf Pixelprozessor)
* [Inhalt] Hinzufügen von &quot;Offset global horizontal/vertikal&quot; auf Musterelementen

**Fest:**

* Absturz beim Erstellen einer neuen Substance in einigen Situationen
* [Bäcker] Absturz, wenn durch Baking erzeugte Map den Graph aktualisieren
* [Bäcker] OBJ aus zbrush sollte Dateiname für &quot;Mit Namen abgleichen&quot; verwenden
* [Parameter] Absturz beim Rückgängigmachen/Wiederholen/Rückgängigmachen im Funktionsdiagramm
* [Diagramm] Teilungspunkte werden nicht an der richtigen Position eingefügt

### 5.3.2

*(Freigegeben: 30. Oktober 2015)*

**Hinzugefügt:**

* [Inhalt] Hinzufügen einer Filtersteuerung für die Mustereingabe auf Tile Generatoren

**Fest:**

* [3D-Ansicht] Fokuspunkt nicht korrekt initialisiert
* [3D-Ansicht] Falsche ferne Clipebene beim mehrmaligen Umschalten von 3D-Gitterressourcen
* [3D-Ansicht] Kurzes Rendering-Artefakt beim Laden eines Gitters
* [3D-Ansicht] Die Umgebungszuordnung ist schwarz, wenn die Datei nicht gefunden werden kann -> Fallback auf die Standardumgebung
* [3D-Ansicht] Absturz nach Verwendung eines benutzerdefinierten Breiten-/Längengradbilds
* [3D-Ansicht] Absturz beim Laden einer bestimmten OBJ-Datei
* [3D-Ansicht] Mesh-Autoreload funktioniert nicht richtig
* [Iray] Textur kann nicht auf externem MDL zugewiesen werden
* [Iray] Nach dem Zurücksetzen des Materials können dem Anisotropie-Kanal keine Texturen zugewiesen werden
* [UI] Windows Popup-Menü wird angezeigt, wenn die rechte Maustaste nach dem Verschieben in 3DView losgelassen wird
* [2D-Ansicht] Das Info-Tool gibt den Farbwert des Pixels unter dem Cursor nicht zurück
* [Bäcker] Graustufenbilder werden als indiziert im Tag-Format gespeichert
* [Diagramm] Anzeigeausgaben in der 3D-Ansicht sollten die Kanäle zurücksetzen, bevor die Ausgaben an die 3D-Ansicht gesendet werden
* [Parameter] Der Name der Parametereingabe ist leer, wenn er von &quot;Knotenparameter verfügbar machen&quot; angezeigt wird
* [Leistung] Legen Sie den onSubstanceCallbackProfileEvent-Rückruf NUR für die Engine fest, wenn Zeitangaben aktiviert sind.

### 5.3.1

*(Freigegeben: 21. Oktober 2015)*

**Hinzugefügt:**

* [3D-Ansicht] Zeigen Sie den Gitternamen in der Szene/Bearbeitung anstelle von &quot;Entität&quot; an.
* [3D-Ansicht] Auf Standardfarbe zurücksetzen, wenn eine neue 3D-Ansicht geöffnet wird
* [3D-Ansicht] Fokuskamera beim Wechsel von der Szene zur Grundform
* [3D-Ansicht] Zeigt die Render-Viewport-Auflösung an, wenn eine benutzerdefinierte Auflösung verwendet wird
* [Iray] Anpassen der Darstellung der Unterteilungsparameter
* [Iray] Ausgabe der IRay-Protokollinformationen an das SD-Protokoll
* [Bäcker] Lesen Sie OBJ-Dateien richtig, um die Übereinstimmung nach Namen kompatibel zu machen

**Fest:**

* [3D-Ansicht] Falsche Anzeige von Gittern mit einer anderen Skala als 1,0
* [3D-Ansicht] Automatische Near-Clip-Berechnung funktioniert bei großen Objekten nicht gut
* [3D-Ansicht] Drahtgitter-Modus zeigt zu dicke Verdrahtungen an
* [3D-Ansicht] Fenster zum Speichern des Renderings wird nicht angezeigt, wenn Post-Effekte deaktiviert sind
* [3D-Ansicht] Absturz beim Wechseln der Geometrie
* [3D-Ansicht] &quot;QOpenGLWidget: Die Meldung &quot;Nicht initialisiertes Widget aktuell&quot; im Protokoll kann nicht erstellt werden.
* [3D-Ansicht] Die Beleuchtung wird nicht berechnet, wenn die Umgebungszuordnung geändert wird, während Irak ausgeführt wird
* [3D-Ansicht] Absturz beim Anzeigen von 3D-Gittern
* [3D-Ansicht] Sehr schlechte OpenGL-Leistungen nach Verwendung von Iray
* [3D-Ansicht] Clipebenen werden nicht korrekt berechnet
* [3D-Ansicht] Wenn Sie die Umgebungszuordnung ändern, wird die 3D-Ansicht nicht aktualisiert
* [3D-Ansicht] Texturen werden beim Diagrammwechsel nicht aktualisiert
* [3D-Ansicht] Ausgeblendete GLSLFX-Sampler werden weiterhin im Auswahlmenü angezeigt
* [3D-Ansicht] Material wird beim Öffnen der Gitterressource nicht ordnungsgemäß wiederhergestellt
* [3D-Ansicht] RAM/VRAM-Speicherverlust beim Öffnen verschiedener Gitter und Zuweisen mehrerer Diagramme
* [3D-Ansicht] Der Fokus berücksichtigt nicht die Brennweite
* [Iray] nvcuvid.dll fehlt (Deinstallieren Sie die vorherige Version, um die Meldung zu entfernen)
* [Iray] Dialogfeld &quot;Export der Vorgabe&quot;... nicht das Dialogfeld öffnen
* [Iran] Refraktion/Streuung funktioniert nicht korrekt im physischen\_diffuse\_Specular
* [Iray] Standard-mdl kann nicht gefunden werden (Magentafarbe)
* [Iray] Schließen Sie Standardtexturen nicht an MDL-Material an, um den Wertmodus in &quot;Material bearbeiten&quot; zu aktivieren.
* [Iray] Die Deskalierung wird nicht ausgelöst, wenn eine Textur aktualisiert wird
* [Bäcker] Normalbäcker im Weltraum rendern ein schwarzes Bild
* [Bäcker] Absturz beim Backen der normalen Karte mit abgedockter 3D-Ansicht
* [Bäcker] Backen mit der Methode &quot;Eingebettet&quot;, während ein ungültiger Pfad für &quot;link&quot; festgelegt ist, verhindert das Speichern der Ressource
* [Bakers] Backen mit &quot;Embedded&quot;-Methode und Ändern des Dateiformats ändert die Erweiterung auf der Festplatte nicht
* [Bäcker] Zufällige Namen für eingebettete Ressourcen haben alle einen XXX... Namen
* [Bäcker] Mehrere Objekte in .obj werden nicht korrekt importiert
* [Inhalt] Materialüberblendung: Grundfarbausgabe wird nicht ausgeblendet, wenn Kanal deaktiviert ist
* [Inhalt] Weiß\_Rauschen und abgeleitete Rauschen werden bei 8k nicht korrekt gerendert
* [Graph] Langsame Bewegungen im Graph
* [Diagramm] Absturz beim Ziehen und Ablegen des Funktionselements aus der Bibliothek in das Funktionsdiagramm
* [Graph] &quot;View ausgaben in 3D view&quot; sollte nur die sichtbare Ausgabe des Knotens in der 3D View senden
* [Voreinstellungen] Standardbenutzer\_Projekt hat leeres &quot;Namenssuffix&quot; für die Funktion &quot;Nach Name abgleichen&quot;.
* [Engine] Color -> Graustufen-Konvertierung führt zu Präzisionsverlusten
* [Konsole] Konsole/Protokoll wird durch viele Meldungen verschmutzt
* [Freigeben] Absturz beim Freigeben eines Pakets
* [UI] QuickInfo bleibt über dem Menü &quot;Zuletzt verwendete Dateien&quot; hängen
* Absturz beim Beenden

### 5.3.0

*(Freigegeben: 1. Oktober 2015)*

<b>Hinzugefügt:</b>

* [3D-Ansicht] Nvidia Iray-Renderer hinzufügen
* [3D-Ansicht] Drehen der Umgebung mit STRG+Umschalt+RMB
* [3D-Ansicht] Rendern des 3D-Ansichtsports mit einer benutzerdefinierten Auflösung (Ogl / Iray)
* [3D-Ansicht] Asynchrones Laden der Szene
* [3D-Ansicht] Anzeigen der globalen Szene in der Szene Browser
* [3D-Ansicht] Deaktivieren des Rasters standardmäßig
* [3D-Ansicht] Hinzufügen einer umgekehrten quadratischen Distanzdämpfung für Punktlichter
* [3D-Ansicht] Anzeigefarbparameter in RGB anstelle von RGBA
* [3D-Ansicht] Separate Licht-/Kamera-/Umgebungseinstellungen
* [Freigeben] Verbesserungen für das Substance share-Upload-Fenster

<b>Fest:</b>

* [3D-Ansicht] Fehler bei der Normalisierung von PBR-Shadern
* [3D-Ansicht] Absturz beim Rechtsklick auf den Stamm im Szenenbrowser
* [3D-Ansicht] PBR-Shader : diffuse vs. spec Energieeinsparung und Punktlichter
* [3D-Ansicht] Setzen Sie mit &quot;Material/Zurücksetzen&quot; auch die Kanäle auf die Standardfarbe zurück.
* [Bäcker] Position mit Bsphere-Normalisierung nicht zentriert
* [UI] Gleitender Windows-Status wird beim Schließen der Anwendung nicht gespeichert
* [Cooker] Kann nicht veröffentlicht werden, wenn sich das SBS in einem Pfad befindet, der ein Sonderzeichen enthält
* [Veröffentlichen] Wenn Sie nach der Veröffentlichung &quot;Enter&quot; in das Namensfeld drücken, wird das Dialogfeld abgebrochen.
* [Freigeben] Export sbs behält den Alias sbs:// nicht bei.

### 5.2.5

*(Freigegeben: 15. September 2015)*

**Hinzugefügt:**

* [Freigeben] Publish-Paket für Substance share
* [UI] Substance share-Link im Hilfemenü hinzufügen

**Fest:**

* [Cooker] &quot;Größe außerhalb des gültigen Bereichs&quot; ist ein Fehler anstelle einer Warnung.
* [Cooker] &quot;Untergraph-Ausgabe kann nicht gefunden werden&quot; ist ein Fehler anstelle einer Warnung.
* [3D-Ansicht] PBR diffuse/spec bevorzugt Grundfarbe anstelle von diffuse
* [3D-Ansicht] Kachelung funktioniert nicht ordnungsgemäß mit Tesselierungsschattierungen
* [Engine] Absturz beim Instanziieren einer bestimmten SBSAR-Datei
* [Engine] Sizelog2-/pow2-Funktionen funktionieren nicht ordnungsgemäß.
* [Engine] &quot;set&quot; in der Ausgabegröße funktioniert nicht
* [Motor] Mipmap-Stufe ist für negative Werte nicht eingeklemmt.
* [Inhalt] Ein Diagramm mit einem dreidimensionalen Filter kann nicht veröffentlicht werden.

### 5.2.1

*(Freigegeben: 27. August 2015)*

**Fest:**

* [Graph] Absturz beim Berechnen eines bestimmten SBSAR
* [Graph] Absturz beim Instanziieren von fxmap mit mehreren Bildeingaben
* [Engine] Absturz mit sizelog2
* [Engine] Der Standardwert des exponierten Parameters wird bei der DX10-Engine ignoriert.
* [Library] Die Berechnung der Miniaturansichten ist fehlerhaft, wenn das Projekt einen ungültigen Alias enthält
* [Kochen] Stellen Sie &quot;unbekannt\_parameter&quot; und &quot;duplizierter Parameter&quot; als Warnung statt als Fehler ein.
* [Voreinstellungen] Engine-Cache-Grenze ist bei 4095 MB blockiert
* [Funktion] Eingabeparameterbeschriftung wird als Kennzeichnung interpretiert

### 5.2.0

*(Freigegeben: 18. August 2015)*

**Hinzugefügt:**

* [Library] Fügen Sie in den Voreinstellungen eine Option hinzu, um PSD-Ebenen auszublenden/anzuzeigen
* [Parameter] Benutzerdaten dürfen in mehreren Zeilen vorliegen.
* [Diagramm] Fügen Sie eine Voreinstellungsoption hinzu, um Kommentare in konstanter Größe zu rendern
* [Graph] Fügen Sie eine Voreinstellungsoption hinzu, um die Anzeige neuer Knoten in der 2D-Ansicht zu deaktivieren.
* [Leistung] Leistungssteigerung bei Pixelprozessoren bei der DX10-Engine
* [3D-Ansicht] Hinzufügen von Tesselierung zu PBR-Shadern
* [3D-Ansicht] Hinzufügen einfacher Deckkraft zu PBR-Shadern (keine Gesichtersortierung)
* [Content] Vray/Corona/Redshift/Arnold-Ziele zum PBR-Konverterfilter hinzufügen (um Maps für diese Renderer zu konvertieren)
* [Inhalt] Fügen Sie dem normalen Kombinationsfilter die Technik &quot;Detailorientiert&quot; hinzu

**Fest:**

* Absturz beim Öffnen von SBS mit leerer Abhängigkeit
* Verknüpfung zu PSD-Ebenen wird nach dem erneuten Laden des Pakets unterbrochen
* [Funktionen] Verschachtelte Funktionen brechen die Typsicherheit
* [Funktionen] Beschriftungen und Gruppen und Beschreibungen werden nicht angezeigt.
* [Funktionen] Absturz beim Kopieren/Einfügen von einer gelöschten Funktion
* [Diagramm] Materielle Verknüpfung mit Balkendiagrammen unterbrochen
* [Graph] Wenn mehrere Bitmap-Knoten aus Ressourcen erstellt werden, werden die Knoten übereinander gestapelt.
* [Graph] Kommentarelement wird nicht an der richtigen Position erstellt, wenn es einem Knoten untergeordnet ist
* [Diagramm] Auswahl des Blockbereichs &quot;Lange Kommentare&quot;
* [Bäcker] Tangent Space Normales Kartenschwarz auf Mac
* [Parameter] Visible If funktioniert nicht, wenn der Eingabename &quot;-&quot; enthält
* [Parameter] Der Schrittwert in &quot;Eingabeparameter&quot; wird ignoriert, wenn er unter 0,01 liegt.
* [Library] Tag &quot;Sichtbar in Bibliothek&quot; wird für sbsar nicht berücksichtigt

### 5.1.1

*(Freigegeben: 4. Juni 2015)*

**Hinzugefügt:**

* [Graph] Verringern des Abstands zwischen zwei Knoten bei Verwendung von AutoConnect
* [Graph] Deaktivieren der automatischen Verbindung bei Verwendung von Drag &amp; Drop im Diagramm
* [Diagramm] Richten Sie den Rahmen am Raster aus
* [Diagramm] Knoteneinfügung über/auf ausgewähltem Link für Materialverknüpfung deaktivieren
* [Voreinstellungen] Festlegen des Höchstwerts für die maximale Texturgröße auf 8192
* [Inhalt] Hinzufügen von Symmetrie-Optionen zum Knoten &quot;Sicheres Transformieren&quot;

**Fest:**

* [Graph] Neuer Knoten wird nicht am Raster ausgerichtet
* [Graph] Das Austauschen von Verknüpfungen kann zu Schleifen/Abstürzen führen
* [Diagramm] Anzeigefehler, wenn Knotengröße/Timings deaktiviert sind
* [Bäcker] Absturz beim Backen einer Ressource, die denselben Namen wie die Szene verwendet
* [Bäcker] Der Standardressourcenname wird nicht aus der richtigen Projektdatei übernommen.
* [Engine] Problem mit der Pow2/log-Funktion
* [Engine] Fehler bei der Funktionsauswertung
* [Fxmaps] Absturz, wenn Parameter auf Standard zurückgesetzt wird
* [FxMaps] Bewertung einer fehlerhaften Funktion
* [Voreinstellungen] Beim Klicken auf die Projektregisterkarte stürzt SD ab
* [3D-Ansicht] Benutzerdefinierte Verwendung wird in Kleinbuchstaben konvertiert
* [Parameter] Elemente in Dropdown-Listen können nicht neu angeordnet werden
* [Explorer] Absturz beim Verschieben eines Funktionsdiagramms im Explorer

### 5.1.0

*(Freigegeben: 28. Mai 2015)*

**Hinzugefügt:**

* [Diagramm] Suchen/Anzeigen von Inhalten aus der Bibliothek über das Leertaste-Menü
* [Graph] Neuen Knoten anzeigen/öffnen
* [Graph] Link-Umleitung (Alt+Umschalttaste)
* [Diagramm] Knotenübergeordnete auswählen
* [Diagramm] 2 Verknüpfungen austauschen (X)
* [Graph] Fügen Sie einen Knoten über eine Verknüpfung per Drag &amp; Drop ein.
* [Graph] Diagramm aus einer Knotenauswahl erstellen
* [Graph] Link löschen, wenn Alt + LMB auf einem Knoten-Pin verwendet wird
* [Diagramm] Neuen Knoten nicht mit der Umschalttaste mit dem vorherigen verbinden
* [Graph] Hinzufügen einer Symbolleiste für Basisfilter
* [Graph] Verbessern des Rasters (Ausrichten und Auflösung)
* [Diagramm] Verschieben des Menüs &quot;Kommentar/Frame/Pin&quot; nach rechts
* [Graph] Knoten über einem ausgewählten Link erstellen
* [Graph] Hinzufügen von Symbolen zu Funktionselementen
* [Graph] Ändern der Pin-Farben im Funktionsdiagramm
* [Graph] Verwenden Sie die Umschalttaste, um die automatische Knotenverbindung zu deaktivieren
* [Diagramm] Die ausgewählte Verknüpfung wird über die anderen Verknüpfungen gezogen.
* [Graph] Hinzufügen von Symbolen zu Fxmap-Knoten
* [Diagramm] Hinzufügen eines Schalters zum Zeichnen gekrümmter oder rechteckiger Verknüpfungen
* [Funktion] Unterscheiden Sie den verschiedenen Vektortyp im Funktionsdiagramm (Pin-/Link-Farben)
* [Funktionen] Hinzufügen von Symbolen auf Knoten und Anzeigen von Werten für Konstante / Satz / Abruf
* [Funktionen] Hinzufügen von Farben zum Knotentitel
* [Funktion] Verbessern der Leistung für die Funktionsauswertung (SSE-generierten Code verwenden)
* [Funktion] Warnung anzeigen, wenn der Knoten &quot;Set/Get&quot; leer ist
* [Bäcker]&#x200B;[Graph] Dither-Bitmap bei Konvertierung in 8bpc
* [Bäcker] Durchschnittliche Scheitelpunktnormalen in OBJ-Datei, wenn das Gitter keine enthält
* [Bäcker] Übereinstimmung nach Name: Suffix als Trennzeichen verwenden
* [Parameter] Hinzufügen einer Option, um auf dem Farb-Widget zwischen RGB und HSV zu wechseln
* [Parameter] Schaltfläche &quot;Pipette hinzufügen&quot; im Farb-Widget
* [Library] Fügen Sie eine Kategorie für Basisinhalte hinzu (Kompositionsknoten, fxmap, Funktion...)
* [2D-Ansicht] Info: Anzeige im Bereich [0, 1] und HSV hinzufügen
* [3D-Ansicht] Hinzufügen von Mipmap-Unterstützung für die Umgebung
* [Abhängigkeiten] Nicht verwendete Abhängigkeiten mit dem Updater bereinigen
* [Updater] Speichern Sie Pakete nicht automatisch

**Fest:**

* [Absturz] beim Schließen des Pakets
* [Absturz] beim Öffnen des Abhängigkeitsmanagers in einem nicht gespeicherten Paket
* [Absturz] Beispiel-Farbfehler
* [Engine] Deadlock für FxMap-Kachelbereich
* [Engine] Genauigkeitsproblem mit SSE-Engine mit Weichzeichner- und/oder Mischknoten
* [Engine] Die Berechnung wird nicht angehalten, wenn sie durch 0 dividiert wird
* [Explorer] Absturz beim Exportieren von Paketen mit Abhängigkeiten, wenn Abhängigkeitszyklen enthalten sind
* [Explorer] Ziehen und Ablegen von Ressourcen funktioniert oft nicht
* [Bäcker] Gebackene Normalität wird schwarz gerendert, wenn sie höher als 256\*256 ist
* [Bäcker] Wenn Sie ein Paket am selben Speicherort wie den Exportpfad speichern, wird der Pfad unterbrochen
* [Bäcker] Falscher Standardzielpfad, wenn das Paket noch nicht gespeichert wurde
* [Engine] Fehlerhaftes Pixelgrößenergebnis, wenn von übergeordneter Funktion geerbt
* [Abhängigkeiten] Nicht verwendete Abhängigkeit wird nicht entfernt.
* [Abhängigkeiten] Absturz beim Öffnen des Abhängigkeitsfensters des Pakets, das Paketzyklen enthält
* [Diagramm] Die Auswahl des Auswahlrechtecks wird in Funktion des Zooms neu skaliert
* [Graph]-Link &quot;rastet&quot; nicht am nächsten Ein-/Ausgang ein
* [Graph] Falscher Rückgängigstapel (kann Abstürze verursachen)
* [Graph] Mehrfachverbindung mit Strg funktioniert nicht, wenn der Pin bereits angeschlossen ist
* [3D-Ansicht] Die Rasterfarbe wird von der Hintergrundfarbe beeinflusst
* [3D-Ansicht]&#x200B;[Graph]-Ausgabeknoten, der mehrere Anwendungen enthält, wird nicht korrekt an die 3D-Ansicht gesendet
* [3D-Ansicht] Tesselations-Shader : Kompilierungsfehler auf AMD-GPUs
* [2D-Ansicht] Pin-Systemproblem
* [Functions] Fehler bei der Funktionskompilierung (falls vorhanden)
* [Voreinstellungen] Suffix &quot;niedrig/hoch&quot; wird nicht korrekt aus sbsprj gelesen
* [Library] Wenn Sie einen Ordner per Drag &amp; Drop über einen anderen Ordner ziehen, wird er entfernt
* [Windows] Es können mehrere SD-Sitzungen ausgeführt werden.
* [Lizenz] Alte Lizenz wird nicht beibehalten.
* [Inhalt] Kantenerkennungs-Filterproblem

### 5.0.3

*(Freigegeben: 1. April 2015)*

**Hinzugefügt:**

* [Voreinstellungen]&#x200B;[Bäcker] Fügen Sie eine Option hinzu, um tbn nach Scheitelpunkt oder Pixel zu berechnen, um UE4 zu entsprechen
* [Bibliothek] Bilineare Filter für Miniaturansichten verwenden
* [Bäcker] Lassen Sie das Fenster auf weniger als 800 px Height herunterskalieren
* [3DView] Ausgleichen der Umgebungszuordnungsbelichtung/Normalisierung der Drehung, um konsistente Blitze zu erhalten
* Benennen einer Anwendungsverknüpfung mit der Hauptversion

**Fest:**

* [Graph] Absturz beim Löschen einiger Ghost-Knoten
* [Graph] angedockter Knoten bleibt angedockt, wenn Knoten dupliziert wird
* [Graph] Absturz beim Löschen von Knoten
* [Diagramm] Exportausgabeeinstellungen werden nicht pro Diagramm gespeichert
* [Graph] Ungültiger Knotenandockingstatus beim Löschen des Knotens
* [Bäcker] Fehler werden nicht mehr in einem Dialogfeld angezeigt
* [Bäcker] Fehlende Ressource wird im Backfenster nicht als fehlend angezeigt
* [Veröffentlichen] fehlgeschlagenes Fenster sollte nicht bearbeitbar sein
* [Veröffentlichen] SBSAR Falsches Ergebnis
* [3D-Ansicht] Mehrere Materialien aus aktualisierten FBX-Netzen werden nicht ordnungsgemäß neu geladen.
* [3D-Ansicht] Diffuses SH kann in einigen Fällen in PBR-Shadern negative Werte erzeugen
* [2D-Ansicht] Die angezeigte Bittiefe für Ressourcenbilder beträgt immer 8 Bit pro Kanal.
* [Parameter] Parameter werden nicht immer in den Diagrammeigenschaften angezeigt
* [Menü] &quot;Protokolldatei exportieren&quot;. action kann die log.txt-Datei nicht finden
* [BatchTools] Subsmutator-Fehler
* [Explorer] Das Laden von Paketen behält die Markierung bei
* [Eigenschaften] Absturz beim Löschen einer Funktion für einen enum-Parameter
* [Voreinstellungen] Mikkt-Tangentenraum-Plug-in ist in user\_project nicht auf Standard festgelegt
* [Evaluierung/Aktivierung] Online kann unter Windows nicht ausgewertet/aktiviert werden
* Computing-Statusleiste verschiebt die Schnittstelle beim Aktualisieren
* Mehrere SD gleichzeitig starten
* Player-URL aktualisieren, wenn .exe nicht gefunden wird
* Dateiänderung auf Datenträger nicht richtig erkannt

### 5.0.2

*(Freigegeben: 17. März 2015)*

**Hinzugefügt:**

* [Bibliothek] Normales Steuerelement im Material hinzufügen\_adjustment\_blend
* [Library] Fülloption für normales Material hinzufügen\_color\_blend
* Upgrade auf Qt 5.4.1

**Fest:**

* [Absturz] OSX 10.9 und 10.10 in FreeImage
* [Absturz] Beim Öffnen einer FBX-Datei, die Elemente ohne Scheitelpunkte enthält
* [Graph] Drag-and-Drop-Probleme
* [Graph] Cache-Verknüpfung wurde unterbrochen
* [Graph] TGA erscheint schwarz/transparent in SD
* [Library] Triplanare Graustufen-Normaleingabe falsch
* [Library] Der Edge Detect Node funktioniert mit der CPU-Engine nicht ordnungsgemäß.
* [Parameter] Schiebereglerbereich für float2/3/4 falsch
* [Parameter] Wenn Sie &quot;Parameter freigeben&quot; zweimal ausführen, stürzt Designer ab
* [Konsole] Die Größe wird nicht korrekt geändert.
* [Console] Duplizierung in der Kanalliste: View3D und 3DView
* [3DView] Die in glslfx definierte Parameterreihenfolge wird in der GUI nicht beibehalten.
* [Explorer] Absturz beim Aktualisieren fehlender Texturen auf der Festplatte
* [Funktion] Wert ändern und bearbeiten führt zum Absturz
* [Baker] Absturz beim Öffnen des Backfensters auf einer fehlenden 3D-Ressource
* [PSD] Psdparse-Absturz (MSVCR120.dll fehlt)
* [Info-Fenster] Fehlender Zeilenumbruch bei Steam-Version
* [SBS] Nicht verwendete neue Engine-Funktionen in SBS
* [Sbsar] Neue Funktionen werden in SD nicht unterstützt
* [Ui] Die Fortschrittsleiste wird nach Abschluss eines Exports mit Abhängigkeiten nicht gelöscht
* vcomp100.dll nicht gefunden beim Starten von SD auf einem neu installierten Windows 7

**Bekannte Probleme:**

* [Windows 8] Drag &amp; Drop funktioniert beim ersten Start nicht. Starten Sie SD neu, um es zu beheben.

### 5.0.1

*(Freigegeben: 05. März 2015)*

**Fest:**

* Fehler beim Exportieren von Bitmaps unter Windows behoben.

### 5.0.0

*(Freigegeben: 04. März 2015)*

**Hinzugefügt:**

* [Exportieren] Alpha-Kanal für TGA und BMP verwerfen, wenn er vollständig undurchsichtig ist
* [3d View] PBR-Shader standardmäßig einstellen
* [2D-Ansicht] Wechseln Sie zur Bildanzeige als Alpha vormultipliziert
* Größe: Hinzufügen einer Breiten-/Height-Sperre/Anzeigen von Werten in Dropdown-Listen
* [Abhängigkeiten] Neuer Abhängigkeitsmanager
* [Abhängigkeiten] zeigt die Knoteninstanz an, die einer Abhängigkeit entspricht.
* [Abhängigkeit] Öffnen Sie ein Abhängigkeitspaket im Paket-Explorer
* [Motor] Angleichen: Unterstützung des Parameters &quot;Deckkraft&quot; bei Verwendung einer Maske
* [Motor] Angleichen: Hinzufügen neuer Füllmethoden (Overlay, Screen, Softlight, Divide)
* [Motor] Angleichen: Alpha-Füllmethode unterstützen
* [Engine] Neuer Knoten &quot;Dynamischer Verlauf&quot;
* [Engine] Neuer Distanzknoten
* [Engine] Neuer Pixelprozessorknoten
* [Engine] FXMAP: Unterstützung dynamischer Funktionen für Eingabebilder
* [Engine], Funktion Sampler: bilineares Sampling unterstützen
* [Engine] FXMAP: Unterstützung der bilinearen/nächsten Filterung für Eingabebilder
* [Engine] FXMAP: Unterstützung für Alpha-Bild des geraden/vormultiplizierten Eingabebilds
* [Bäcker] Fügen Sie eine Option hinzu, um die Geometrie nach Netznamen zwischen tiefe und hohe Def-Gitter anzupassen
* [Vorlagen] Erstellen einer Vorlagensubstanz für Substance Painter
* [Bäcker] Neue Texturkarte vom Mesh-Bäcker
* [Graph] Fügen Sie eine &quot;Kompatibilitätsprüfung&quot; hinzu, um Knoten hervorzuheben, die nicht mit der vorherigen Engine kompatibel sind.
* [UI] Anpassungen des Hilfemenüs
* [Voreinstellungen] Stellen Sie das Mikkt-Tangentenraum-Plugin auf den Standardwert ein (setzen Sie es in den Voreinstellungen auf Standard, wenn SD4 installiert ist).
* [Library] Neue HDR-Maps hinzufügen
* Neue Substance aus Vorlage
* Zu Qt5 wechseln
* Aktualisieren des Lizenzsystems auf SD5

**Fest:**

* [Nur Mac] Farbwählerproblem mit Retina-Display
* [Nur Mac] Ziehen Sie das Drag &amp; Drop-Symbol in der 3D-Ansicht unter Mac OS, um die Ansicht ebenfalls zu drehen
* [Bäcker] Backen einer Karte ohne Ausgabeordner erzeugt eine leere Textur
* [Graph] Verankerte Knoten im Rahmen bewegen sich auf seltsame Weise
* [Parameter] Benutzerdefinierte Bibliothekspfade werden nicht aus sbsprj-Dateien geladen
* [3D-Ansicht] STRG + R , um alle Shader neu zu laden, lösen auch das Zurücksetzen der 3D-Ansicht aus.
* [3D-Ansicht] Umschlag Uniform-Wechsel des Mipmap-Heights auf Standard beim Laden des Shaders
* [3D-Ansicht] PBR-Shader : Diffuse vs. baseColor typo
* [Library] Nicht rekursiver Bibliothekspfad beschädigt verknüpfte Texturen in Paketen
* [Library] Umgebungszuordnungen zeigen keine .hdr-Datei an.
* [Explorer] &quot;Kopieren/Einfügen&quot; für die Substanz sollte nicht möglich sein.
* [Explorer] Rechtsklick auf die Option &quot;Einfügen&quot;, die noch in einem Diagramm verfügbar ist
* [Funktion] QuickInfo des Samplers ist falsch
* [Diagramm] Im Kompaktmodus zeigen Instanzen nicht alle Verknüpfungsnamen an, wenn sie automatisch erweitert werden, um einen Graustufen-Konverter hinzuzufügen

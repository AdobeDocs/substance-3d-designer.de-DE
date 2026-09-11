---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/release-notes/version-11-3.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 11.3 , um mehr über neue Funktionen, Verbesserungen und Fehlerbehebungen zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 11.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 1%

---


# Version 11.3

**Substance 3D Designer**

Freigabedatum: *24. November 2021*

## Hauptmerkmal

### Neue Modelldiagramm-Funktionen

![](../../assets/banner-model.jpg)

Dem Modelldiagramm wurden viele Verbesserungen hinzugefügt, um die Modellierungsmöglichkeiten zu erweitern:

* <b>Workflow für neue Partikeln</b>\
  Mit dem neuen Geometriemodellierungs-Workflow können Sie Punktwolken erstellen, um Partikeln zu bearbeiten. Sie können verwendet werden, um viele neue komplexe und/oder sich wiederholende Formen zu erstellen, wie z. B. die Dachziegel auf dem Bild oben.\
  Weitere Informationen zum neuen Arbeitsablauf für die Partikel finden Sie auf den folgenden Dokumentationsseiten:

  * Elementtypen in einer Szene
  * Partikel
  * Partikelbeschneidung
  * Partikel aus Instanzen

  ![](../../assets/particle-pruning.gif)

* <b>Neue Modellierungs- und Deformationsknoten</b>\
  Es wurden weitere neue Knoten hinzugefügt, um komplexere Formen zu erstellen. Klicken Sie auf die einzelnen Knoten, um mehr über sie zu erfahren:
  * Generatives Transformieren
  * Organisches Muster
  * Drehbank
  * Kurve zuschneiden

* <b>Allgemeine Verbesserungen\
  </b>Der Workflow für den Modellierungs-Graf wurde verbessert durch:
  * Neue QuickInfos zu Knoten-Parametern, die das Lernen erleichtern.
  * Die 3D-Modellhierarchie bleibt jetzt beim Exportieren in FBX erhalten
  * Die Zuweisung von Materialien kann mit den Dateiformaten OBJ und FBX exportiert werden.
  * Vorschau der Zwischenknoten im Viewport im Überlagerungsmodus

### Verbesserte Interoperabilität

![](../../assets/banner-sendto.jpg)

Die Sende-an-Aktionen wurden um zwei neue Möglichkeiten erweitert:

* **SBSM (Substance Model File) an Stager senden**\
  Prozedurale 3D-Modelle können jetzt an Stager gesendet und von dort mit den freigelegten Parametern bearbeitet werden.

* **SBS/SBSAR von Sampler empfangen**\
  Es ist jetzt möglich, von Sampler generierte Substance-Dateien direkt in Designer zu empfangen.

### Sonstiges

![](../../assets/banner-misc-3.jpg)

Es wurden verschiedene Verbesserungen der Lebensqualität vorgenommen:

* **Eingaben relativ zu Eingaben**\
  Graf-Eingaben, die unter &quot;Relativ zu Eingaben&quot; festgelegt sind, erben jetzt die Größe des verbundenen Grafen anstelle der Standardgröße des übergeordneten Knotens. Dadurch wird die Verwaltung unterschiedlicher Auflösungen über Eingaben unterschiedlicher Größe deutlich vereinfacht.

  ![](../../assets/relative-to-inputs.jpg){width="400px"}

* **Neues Graf-Fenster**\
  Das neue Graf-Fenster wurde überarbeitet und ermöglicht es nun, die Details einer bestimmten Vorlage besser zu sehen und neuen Graf direkt in einem bestehenden Paket zu erstellen.

  ![](../../assets/new-graph.png){width="400px"}

* **Alle Pakete schließen**\
  Eine kleine Aktion, die die Verwaltung vieler Pakete im Explorer weniger mühsam macht. Verwenden Sie **Datei** > **Alle schließen**, um alle derzeit geöffneten Pakete zu schließen.

  ![](../../assets/close-all-packages.png)

* **Aktuelle Ansicht maximieren**\
  Verwenden Sie die neue Titelleiste **Symbol** oder den Tastaturbefehl **UMSCHALT+Leertaste**, um ein Fenster auf den Vollbildmodus zu erweitern. Dies kann auch auf schwebenden Fenstern verwendet werden.

* **Verbesserungen der 3D-Ansicht**\
  Die 3D-Ansicht verfügt über neue Anzeigeeinstellungen, mit denen Sie die Anzeige der hinteren Flächen eines 3D-Modells sowie die Anzeige von Scheitelpunkten, Tangenten und Bitangenten ein- bzw. ausschalten können.

### Inhalt

![](../../assets/render-content.jpg)

In dieser Version wurden neue Diffusion-Nodes und Verbesserungen für den PBR-Rendering-Node hinzugefügt:

* <b>Diffusion </b>\
  Die neuen Knoten &quot;Diffusion&quot;, &quot;Diffusion&quot;, &quot;Graustufen&quot; und &quot;Diffusion UV&quot; ermöglichen die Erzeugung von weichen Blutungsunschärfen auf Basis einer Eingabemaske.

  ![](../../assets/diffusion-normal.jpg){width="230px"}

  ![](../../assets/diffusion-grayscale.jpg) ![](../../assets/diffusion-uv.jpg)

* **Verbesserter PBR-Rendering-Knoten**\
  Für diesen Knoten wurden die folgenden Änderungen vorgenommen:
  * Neuer kubischer UV-Modus für die Form &quot;Kugel&quot;.
  * Neue Unterstützung für Volumenstreuung.
  * Anisotropie folgt jetzt dem Adobe Strand Material (5ASM).
  * Die bildbasierte Beleuchtung wurde mithilfe von Sample-Verfahren verbessert.
  * Die Beleuchtung von emissive wurde mithilfe wichtiger Stichproben verbessert.

## Versionshinweise

### 11.3.0

*(veröffentlicht am 24. November 2021)*

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
* [Materials] Eingaben relativ zu Eingängen
* [Inhalt] Option &quot;Kachelung&quot; auf 3D-Perlin-Rauschen hinzufügen
* [Inhalt] Neuer Prozessknoten für Diffusionen
* [Inhalt] Neue PBR-Rendering-Knotenversion
* [Interoperabilität] Empfangen von SBS und SBSAR von Sampler
* [Interoperabilität] SBSM an Stager senden
* [3D-Ansicht] Fügen Sie eine Option hinzu, um Rückseiten-Ausblendung zu deaktivieren.
* [3D-Ansicht] Fügen Sie eine Option hinzu, um den Tangente-Speicherplatz des Scheitelpunkts anzuzeigen
* [Explorer] Markieren Sie Graf im Explorer, wenn Sie auf den Hintergrund der Graphansicht doppelklicken
* [Explorer] Entfernen Sie die Option &quot;Durchsuchen&quot; in Kontextmenüs.
* [Baker] Veraltete Baker ausblenden
* [Farbmanagement] Unterstützung für OCIO v2-Konfigurationsdateiregeln hinzufügen
* [Library] Umbenennen von Kategorien nach Grafen
* [Voreinstellungen] Automatische Deaktivierung der CPU in den Voreinstellungen für die Iray-Hardware, wenn unterstützte CUDA-GPU erkannt wird

**Fest:**

* [Substance-Modelle] Absturz auf Mac bei Verwendung der Option &quot;as sudb&quot; auf .fbx
* [Substance-Modelle] Absturz beim Exportieren nach SBSM in einem bestimmten Fall
* [Substance-Modelle] Exportfehler beim Exportieren von freigelegten Parametern, die nie erstellt wurden
* [Substance-Modelle] Zufälliger Absturz beim Öffnen eines Grafen, der sich auf mehrere .fbx-Dateien bezieht
* [Substance-Modelle] Bereiche werden in den Widgets der freigelegte Parameter nicht dynamisch angewendet
* [Substance-Modelle] Option &quot;Mesh neu laden&quot; funktioniert nicht für Ressourcen, die im Graf &quot;Substance-Modelle&quot; verwendet werden
* [Substance-Modelle] Szenen werden in einem bestimmten Fall nicht in einer verfügbaren 3D-Ansicht angezeigt
* [UI] Der Bereich &quot;Deaktivieren&quot; ist in den Material-Optionen zu groß
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

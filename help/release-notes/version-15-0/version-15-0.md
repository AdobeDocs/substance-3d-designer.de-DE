---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-0.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 15.0, um mehr über den neuen 3D-Renderer und die native Unterstützung in USD zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 15.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1894'
ht-degree: 0%

---


# Version 15.0

Dieses Update enthält einen brandneuen 3D-Renderer mit Raster- und Pathtracer-Modi sowie eine native Unterstützung von [USD](https://openusd.org/release/index.html), mit der Sie Szenen ohne Datenverlust bearbeiten und exportieren können.

*Freigabedatum: 15. Juli 2025*

![Banner](../../assets/banner-47.png "Version 15.0 Banner")

## Neuer 3D-Renderer

### Neuer Raster- und Pathtracer

Diese neue Version bietet Ihnen Zugriff auf einen erweiterten [3D-Renderer](../../interface/3d-view/3d-renderers/3d-renderers.md) mit einem Rastermodus (für eine Echtzeitvorschau während der Arbeit an Ihrem Material) und einem Pfadverfolgungsmodus (ein Raytracing-Modus, um ein perfektes und genaues Rendering zu erhalten). Dieser neue Renderer verbessert die Funktionalität mit Funktionen wie Schatten im Rastermodus, verbessert die Qualität und Leistung und wurde zur Unterstützung zukünftiger Technologien wie [MaterialX](https://materialx.org/) entwickelt. Es ergänzt die bestehenden OpenGL- und Iray-Renderer in Designer und stimmt mit den in Substance 3D Viewer und Substance 3D Sampler verfügbaren Renderern überein, um ein einheitliches Erlebnis im gesamten Ökosystem zu gewährleisten.

![Schatten und Lichtdurchlässigkeit im Rastern](../../assets/feature_1b.png)

Die [3d-Ansichtssymbolleiste](../../interface/3d-view/3d-view.md) wurde aktualisiert, um einen schnellen Zugriff auf einige der neuen Funktionen zu ermöglichen, die in diesem Renderer verfügbar sind:

* <b>Auswahlwerkzeug:</b>, um ein Teilnetz in der Szene auszuwählen. Sobald ein Teilgitter ausgewählt ist, können Sie sich darauf konzentrieren (F) oder auf seine Materialeigenschaften zugreifen (Rechtsklick).
* <b>Aktivieren Sie den Pathtracer:</b>, um schnell zwischen dem Pathtracer- und dem Rastermodus zu wechseln.
* <b>Aktivieren Sie Schatten:</b>, um Schatten in der Szene zu aktivieren. Dies ist hilfreich, um zu sehen, wie sich Ihre Materialien gemäß dem Licht verhalten.
* <b>Aktivieren Sie die Grundebene:</b>, um die Grundebene in der Szene zu aktivieren oder nicht.

Darüber hinaus wurde der Hotkey zum Drehen der Umgebungsbeleuchtung entsprechend den anderen Substance-Apps geändert, sodass jetzt *<b>Rechtsklick bei gedrückter Umschalttaste</b>* statt *<b>Rechtsklick bei gedrückter Strg-Umschalttaste</b>* verwendet wird.

### Post-Effekte

[Post-Effekte sind zurück](../../interface/3d-view/camera/post-effects/post-effects.md)! Sie sind jetzt über das Menü &quot;Kamera&quot; verfügbar und werden jetzt intern entwickelt.

* <b>Blüte:</b> simulieren Blendeffekte um helle Flecken wie Lichter und Reflexionen, sodass emittierende Oberflächen besser sichtbar sind.
* <b>Farbtonzuordnung: </b>den Farbbereich mit Profilen, um einen HDR-Effekt (High Dynamic Range) zu erhalten.
* <b>Die Tiefe des Halbbildes:</b> simuliert die Fokuseigenschaften eines Kameraobjektivs (nur Rasterobjektiv).

![Post FX in Designer 15.0](../../assets/postfx.gif)

## Asset-Edition im Kontext.

Wenn Sie an Ihren Materialien arbeiten, können Sie eine [Vorschau im Kontext einer bestimmten 3D-Szene anzeigen](../../working-with-3d-scenes/working-with-3d-scenes.md). Aus diesem Grund haben wir die Möglichkeit hinzugefügt, eine vollständige Szene mit all ihren Texturen, Kameras und Lichtern zu importieren und zu rendern. Und Kirsche oben, wenn diese Szene MaterialX-Shader referenziert, werden sie korrekt mit dem Rasterprogramm gerendert!

![USD-Szene geladen und in Designer gerendert](../../assets/feature_2.png)

Nach dem Import können Sie an Ihrer Szene arbeiten, indem Sie ein Gitter auswählen (mit einem Klick bei gedrückter UMSCHALTTASTE oder dank des Szenenbrowsers) und [alle Materialien überschreiben](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md). Sie können dann:

* Erstelle oder lade ein Diagramm, und wende es auf ein Szenenmaterial an.
* Nehmen Sie Anpassungen an einem vorhandenen Material vor, indem Sie [seine Texturen &#x200B;](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) in ein neues Diagramm extrahieren.

Nachdem Sie Ihre 3D-Szene bearbeitet haben, können Sie [die Szene &#x200B;](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) als neue Datei oder als neue Ebene der Originaldatei exportieren, um Datenverluste zu vermeiden (nur bei USD-Format).

Nicht zuletzt werden jetzt weitere 3D-Formate sowohl für den Import als auch den Export unterstützt: USD (+ usda, usdc, usdz), STL, PLY und GLTF, zusätzlich zu den bereits verfügbaren Formaten FBX und OBJ.

## Formatierte QuickInfos

Es wurden umfangreiche QuickInfos eingeführt, um den Zweck jedes Knotens besser zu demonstrieren. Diese QuickInfos, die derzeit nur für [atomare Knoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) verfügbar sind, enthalten Visuals, um die Wirkung des Knotens zu demonstrieren und einen direkten Link zur Dokumentation mit detaillierten Informationen bereitzustellen, einschließlich der Liste der Parameter, Tipps und Tricks.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Blend-Knoten](../../assets/blend.gif)

</td>
<td style="border: 0;" valign="top">

![Weichzeichnungsknoten](../../assets/blur.gif)

</td>
<td style="border: 0;" valign="top">

![Distanzknoten](../../assets/distance.gif)

</td>
</tr>
</table>

## Verbessern der nicht quadratischen Unterstützung

Wenn du mit nicht quadratischen Texturen arbeiten musst, ist diese neue Option ideal für dich. In den [Materialeigenschaften](../../interface/3d-view/material-properties/material-properties.md) in der 3D-Ansicht können Sie in den UVs-Optionen zum Steuern der Kachelung jetzt einen anderen Wert für beide Achsen festlegen.

![unterschiedliche U V-Skalierung](../../assets/nonsquare.png){zoomable="yes"}

## Baker

Während die Backing-Oberfläche nur geringfügige Aktualisierungen erlebt hat (weitere Informationen finden Sie in der detaillierten Liste unten), wurde die Baker-Bibliothek vollständig neu erstellt, um GPU-basierte Backups zu verwenden, was zu einer viel besseren Leistung führte. Zusammen mit den oben genannten neuen unterstützten Dateiformaten stellt dieses Update eine wesentliche Verbesserung für Benutzer dar, die Backing-Workflows verwenden.

Hinweis: Wenn Sie sbsbaker.exe zur Automatisierung Ihres Prozesses verwendet haben, wurde das Tool in substance3d\_baker.exe umbenannt (verwenden Sie substance3d-baker —help, um weitere Informationen zu erhalten).

## Aktualisierungen der VFX-Plattformanforderungen

Die [VFX Reference Platform](https://vfxplatform.com/) veröffentlicht jedes Jahr eine Liste von Tools und Bibliotheksversionen, die in jeder Software für die VFX-Branche verwendet werden können, um Inkompatibilitäten zwischen der Software zu minimieren. Wie gewöhnlich *aktualisieren wir alle unsere Abhängigkeiten*, um alle diese Empfehlungen zu respektieren.

## Video

[![Substance 3D Designer-Update: Neuer Renderer, POST-FX und Kontextbearbeitung | Adobe Substance 3D](../../assets/video_15.png)](https://www.youtube.com/watch?v=6EkXxu-0Q_E)

## Versionshinweise

### 15.0.0

*(veröffentlicht am 15. Juli 2025)*

### Hinzugefügt

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

### Fehlerbehebungen

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

### BEKANNTE FRAGEN

* [Baker] Abstürze beim Backen mit einigen bestimmten NVidia-Treibern
* [3D-Ansicht] OpenGL: Einige importierte Szenen werden möglicherweise nicht gerendert.
* [3D-Ansicht] Rastereffekt: Schattenartefakte bei Verwendung von Versatz in einer flachen Szene
* [3D-Ansicht] Pathtracer: langsame Bewegungen beim Aktualisieren von Texturen mit aktivierter Tesselierung/Versatz
* [3D-Ansicht] Einige Farbmaterialeigenschaften werden beim Überschreiben nicht korrekt farbverwaltet
* [3D-Ansicht] Szenen mit animierten Grundelementen werden nicht ordnungsgemäß unterstützt.
* [3D-Ansicht] Gitter mit mehreren UDims werden noch nicht unterstützt.
* [3D-Ansicht] Gitter mit mehreren UVs werden nicht ja unterstützt und können zu ungültiger Materialdarstellung führen
* [3D-Ansicht] Pathtracer wird auf AMD-Grafikkarten nicht unterstützt

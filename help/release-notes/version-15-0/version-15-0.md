---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-0.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 15.0, um mehr über den neuen 3D-Renderer und die Unterstützung für native USD zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 15.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
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

Diese neue Version bietet Ihnen Zugriff auf einen erweiterten [3D-Renderer](../../interface/3d-view/3d-renderers/3d-renderers.md), der einen Rastermodus (für eine Echtzeitvorschau während der Arbeit an Ihrem Material) und einen Pfadverfolgungsmodus (einen Raytracing-Modus, um ein perfektes und präzises Rendering zu erhalten) aufweist. Dieser neue Renderer verbessert die Funktionalität mit Funktionen wie Schatten im Rastermodus, verbessert die Qualität und Leistung und wurde zur Unterstützung zukünftiger Technologien wie [MaterialX](https://materialx.org/) entwickelt. Es ergänzt die bestehenden OpenGL- und Iray-Renderer in Designer und stimmt mit den in Substance 3D Viewer und Substance 3D Sampler verfügbaren Renderern überein, um ein einheitliches Erlebnis im gesamten Ökosystem zu gewährleisten.

![Schatten und translucency im Rasterprogramm](../../assets/feature_1b.png)

Die [3d-Ansichtssymbolleiste](../../interface/3d-view/3d-view.md) wurde aktualisiert, um einen schnellen Zugriff auf einige der neuen Funktionen zu ermöglichen, die in diesem Renderer verfügbar sind:

* <b>Auswahlwerkzeug:</b> zum Auswählen eines Teilnetzes in der Szene. Sobald ein Teilgitter ausgewählt ist, können Sie sich darauf konzentrieren (F) oder auf seine Material-Eigenschaften zugreifen (Rechtsklick).
* <b>Aktivieren Sie den Pathtracer:</b>, um schnell zwischen dem Pathtracer- und dem Rastermodus zu wechseln.
* <b>Aktivieren Sie Shadows:</b>, um Shadows in der Szene zu aktivieren. Dies ist hilfreich, um zu sehen, wie sich Ihre Materialien entsprechend der Lichtverhältnisse verhalten.
* <b>Aktivieren Sie die Boden-Ebene:</b>, um die Boden-Ebene in der Szene zu aktivieren oder nicht.

Darüber hinaus wurde der Hotkey zum Drehen des Umgebungslichts entsprechend den anderen Substance-Apps geändert. Daher lautet er jetzt *<b>Umschalt+Rechtsklick</b>* anstelle von *<b>Strg-Umschalt+Rechtsklick</b>*.

### Post-Effekte

[Post-Effekte sind zurück](../../interface/3d-view/camera/post-effects/post-effects.md)! Sie sind jetzt über das Menü &quot;Kamera&quot; verfügbar und werden jetzt intern entwickelt.

* <b>Blüte:</b> simulieren Blendeffekt um helle Flecken wie Lichter und Reflexionen, sodass emissive-Oberflächen besser sichtbar sind.
* <b>Farbtonzuordnung: </b>den Farbbereich mit Profilen, um einen Effekt mit hohem Dynamikbereich (HDR.) zu erhalten.
* <b>Die Tiefe des Halbbildes:</b> simuliert die Fokuseigenschaften einer Kamera-Linse (nur Rastereffekt).

![Post FX in Designer 15.0](../../assets/postfx.gif)

## Asset-Edition im Kontext.

Wenn Sie an Ihren Materialien arbeiten, möchten Sie möglicherweise eine [Vorschau im Kontext einer bestimmten 3D-Szene anzeigen](../../working-with-3d-scenes/working-with-3d-scenes.md). Deshalb haben wir die Möglichkeit hinzugefügt, eine vollständige Szene mit all ihren Texturen, Kameras und Lichtern zu importieren und zu rendern. Und Kirsche oben, wenn diese Szene MaterialX-Shader referenziert, werden sie korrekt mit dem Rasterprogramm gerendert!

![USD Szene geladen und in Designer gerendert](../../assets/feature_2.png)

Nach dem Import können Sie an Ihrer Szene arbeiten, indem Sie einen Mesh auswählen (mit einem Klick bei gedrückter UMSCHALTTASTE oder dank des Szene-Browsers) und [alle Material überschreiben](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md). Sie können dann:

* Erstellen oder laden Sie einen Graf und wenden Sie ihn auf ein Szene-Material an.
* Nehmen Sie Anpassungen an einem bestehenden Material vor, indem [die Texturen ](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) in einen neuen Graf extrahiert werden.

Nachdem Sie Ihre 3D-Szene bearbeitet haben, können Sie [die Datei ](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) als neue Datei oder als neue Ebene der Originaldatei exportieren, um Datenverluste (nur bei USD) zu vermeiden.

Nicht zuletzt werden jetzt weitere 3D-Formate sowohl für den Import als auch den Export unterstützt: USD (+ usda, usdc, usdz), STL, PLY und GLTF, zusätzlich zu den bereits verfügbaren Formaten FBX und OBJ.

## Formatierte QuickInfos

Es wurden umfangreiche QuickInfos eingeführt, um den Zweck jedes Knotens besser zu demonstrieren. Diese QuickInfos, die derzeit nur für [elementare Knoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) verfügbar sind, enthalten Visuals, um die Wirkung des Knotens zu veranschaulichen, und stellen einen Direktlink zur Dokumentation bereit, in der detaillierte Informationen, einschließlich der Liste der Parameter, Tipps und Tricks, enthalten sind.

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

Wenn Sie mit nicht quadratischen Texturen arbeiten müssen, ist diese neue Option ideal für Sie. In den [Material-Eigenschaften](../../interface/3d-view/material-properties/material-properties.md) in der 3D-Ansicht können Sie in den UVs-Optionen zum Steuern der Kachelung jetzt einen anderen Wert für beide Achsen festlegen.

![unterschiedliche U V-Skalierung](../../assets/nonsquare.png){zoomable="yes"}

## Baker

Während für die Benutzeroberfläche des Bakings nur geringfügige Aktualisierungen vorgenommen wurden (weitere Informationen finden Sie in der detaillierten Liste unten), wurde die Leistungsbibliothek für die Verwendung von GPU-basierten Bakern vollständig neu erstellt, was zu einer deutlich besseren Baker-Leistung führte. Zusammen mit den oben genannten neuen unterstützten Dateiformaten stellt dieses Update eine wesentliche Verbesserung für Benutzer dar, die sich mit dem Baking von Arbeitsabläufen beschäftigen.

Hinweis: Wenn Sie sbsbaker.exe zur Automatisierung Ihres Prozesses verwendet haben, wurde das Tool in substance3d\_Baker.exe umbenannt (verwenden Sie substance3d-Baker —help, um weitere Informationen zu erhalten).

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
* [3D-Ansicht] Neue Option &quot;Szene mit Ebenen exportieren...&quot; hinzufügen im Menü &quot;Szene&quot;
* [3D-Ansicht] Hinzufügen neuer Symbolleistenschaltflächen
* [3D-Ansicht] Fügen Sie die Möglichkeit hinzu, zwischen mehreren Kameras in einer USD Szene zu wechseln.
* [3D-Ansicht] Fokussierung auf das ausgewählte Objekt zulassen, wenn F im Viewport gedrückt wird
* [3D-Ansicht] Generieren eines Substance-Compositing-Grafen aus einem bestehenden Material zulassen
* [3D-Ansicht] Erlaubt das Senden eines SBS Comp-Grafen in der 3D-Ansicht und weist seine eindeutige Ausgabe der Umgebung/Panorama-Nutzung zu.
* [3D-Ansicht] Löschen der aktuellen Auswahl durch Drücken der Escape-Taste
* [3D-Ansicht] Anzeigen importierter 3D-Szenen mit Texturen
* [3D-Ansicht] X- und Y-Texturen-Wiederholungssteuerungen unterscheiden
* [3D-Ansicht] Aktivieren/Deaktivieren von Schatten
* [3D-Ansicht] Boden-Ebene aktivieren/deaktivieren
* [3D-Ansichten] Fügen Sie im Menü &quot;Materials&quot; die Option &quot;Entfernen&quot; nur für die Materials hinzu, die manuell hinzugefügt wurden und nicht verwendet werden.
* [3D-Ansicht] Entfernen Sie im Menü &quot;Materialien&quot; die Aktion &quot;Alle entfernen&quot;.
* [3D-Ansicht] Macht exportierte USDZ-Dateien eigenständig
* [3D-Ansicht] Die Renderereigenschaften dauerhaft festlegen, wenn der Renderermodus gewechselt wird.
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
* [Baker] 2D-Ansichten-Maps-Listenreihenfolge mit Bakern-Renderlistenreihenfolge abgleichen
* [Baker] Das Baking führend Fenster modal gestalten
* [Baker] Verwalten von Tonzuordnungsparametern
* [Baker] Tangentialraum-Plug-in-Auswahl entfernen
* [Baker] Speicherstatus &quot;aktiviert&quot; oder &quot;deaktiviert&quot; für Baker beim Speichern einer Vorgabe
* [Baker] Material standardmäßig im Widget &quot;Auswählen&quot; auswählen
* [Baker] Legen Sie die Standardausrichtung der Textur &quot;Normale Ausgabe&quot; relativ zur Voreinstellung fest.
* [Baker] Stellen Sie die UV-Kacheln standardmäßig auf Alle ein.
* [Baker] WordSpaceDirection add option FromTexture/FromValue
* [Baker] Welt in Tangente: die Standardeingabe auf &quot;von Textur&quot; setzen
* [SBSBaker] Erstellen einer Option zur Steuerung der Backend-Reihenfolge
* [SBSBaker] Verbessern der Verwendung des StringList-Arguments
* [SBSBaker] Umbenennen von &quot;match\_source\_instance&quot; in &quot;match\_Mesh\_name&quot;
* [SBSBaker] Umbenennen von &quot;Submesh&quot; in &quot;GeomSubset&quot;
* [SBSBaker] Umbenennen in substance3d\_Baker
* [Inhalt] Hinzufügen der Form &quot;Hemisphere&quot; zu Generatorknoten, die Quadrantenformen legt
* [Interop] Unterstützung des GLTF-Dateiformats
* [Interop] Unterstützung des PLY-Dateiformats
* [Interop] Unterstützung des STL-Dateiformats
* [Library] Vereinheitlichte QuickInfos für elementare Knoten
* [Mac] Unterstützung für MacIntel-Plattform beenden
* [Nodes] Hinzufügen von Richtungs-Tooltips für elementare Knoten
* [Parameter] Schließen Sie den Abschnitt &quot;Attribute&quot; standardmäßig.
* [Parameter] Der Benutzer kann Standardwerte für Basisparameter für neue Instanzen angeben.
* [Voreinstellungen] Baker: Fügen Sie eine boolesche Option hinzu, um den Tangente-Speicherplatz pro Fragment zu berechnen.
* [Voreinstellungen] Entfernen Sie die Plug-ins für den Tangente-Speicherplatz
* [Voreinstellungen] Speichern Sie die Voreinstellungen pro Nebenversion von SD (XX.X).
* [VFX] Update Boost auf 1.85.0
* [VFX] Aktualisieren der MacOS-Mindestversion auf 12.0
* [VFX] Update OpenColorIO auf 2.4.2
* [VFX] Update OpenColorIO auf 2.4.x
* [VFX] Update OpenExr auf 3.3.x
* [VFX] Update Qt auf 6.5.8

### Fehlerbehebungen

* [3D-Ansicht] Texturen in exportierten USD Szenen werden nicht korrekt angewendet
* [3D-Ansicht] [UDIM] UDIM-Graphausgaben können nicht in 3D-Ansicht angezeigt werden, wenn die automatische Anzeige beim Öffnen des Grafen in den Graf-Einstellungen deaktiviert ist
* [Baker] &#39;Glätten.&#39; und &quot;Durchschn. Die Zellen von Normalen für nicht zutreffende Baker sind leer und bearbeitbar.
* [Baker] Die Aktion &quot;Aktualisieren&quot; verwendet ein Raytracing-Backend, wenn sie in den Einstellungen deaktiviert ist
* [Baker] Baker wurden nach einem Fehler während des Vorgangs &quot;Alle durch Baking erzeugte Map aktualisieren&quot; als ausgelastet blockiert.
* [Baker] Absturz bei mehr als 180 UDIM beim Baking der OpenGL-Positionszuordnung auf einem bestimmten Mesh
* [Baker] Absturz beim mehrmaligen Öffnen des Dialogfelds &quot;Baking-Modellinformationen&quot; in einer Zeile (nur macOS)
* [Baker] Beim Export von JSON-Vorgaben wird der Wert &quot;udim&quot; durch &quot;1001&quot; ersetzt, wenn er auf &quot;Alle&quot; festgelegt wurde
* [Baker] Speicher wird unter Linux nicht korrekt erkannt
* [Baker] Fehlende Zuordnungseingabeabhängigkeit löst keine Warnung und/oder Blockrendering aus
* [Baker] Keine Fehlerbezeichnung, wenn der Ausgabename leer ist
* [Baker] Der Wechsel von der High-Poly-Mesh-Datei hat keine Auswirkungen
* [Baker] Ziel-Baker ist standardmäßig nicht ausgewählt, wenn die Aktion &quot;Rebake&quot; verwendet wird
* [Engine] Entfernung: sichtbarer &quot;Schnitt&quot; in einigen Situationen
* [Engine] Fx-Map: Negative Farben werden nicht unterstützt, wenn die Bittiefe 8 Bit beträgt (nur GPU-Engine)
* [Lokalisierung] Die Zeicheneingabe wechselt im Knotenmenü von Japanisch zu Lateinisch zurück
* [Sicherheit] Sicherheitslücke, die beim Analysieren von USDC-Dateien außerhalb des gültigen Bereichs auftritt
* [Sicherheit] Out-of-Bound WRITE Vulnerability II, beim Analysieren von NEF-Dateien
* [Sicherheit] Sicherheitslücke beim Lesen außerhalb des gültigen Bereichs III beim Analysieren von DNG-Dateien
* [Voreinstellungen] UX-Probleme in den Projekteinstellungen für schreibgeschützte Projekte
* [Ressourcen] Beim Öffnen von FBX werden nicht mehrere UV-Satz angezeigt
* [UI] Überlappende Beschriftungen in der Statuszeile
* [UI] QuickInfos zum Dropdown-Menü &quot;Link-Erstellungsmodus&quot; werden nicht angezeigt.

### BEKANNTE FRAGEN

* [Baker] Absturz beim Baking mit bestimmten NVidia-Treibern
* [3D-Ansicht] OpenGL: Einige importierte Szenen werden möglicherweise nicht gerendert.
* [3D-Ansicht] Rasterizer: Schattenartefakte bei Verwendung von Versatz auf einer flachen Szene
* [3D-Ansicht] Pathtracer: langsame Leistung beim Aktualisieren von Texturen mit aktivierter Tesselierung/aktiviertem Versatz
* [3D-Ansicht] Einige Color-Material-Eigenschaften werden beim Überschreiben nicht ordnungsgemäß farbverwaltet.
* [3D-Ansicht] Szenen mit animierten Grundformen werden nicht ordnungsgemäß unterstützt.
* [3D-Ansicht] Mesh mit mehreren UDims werden noch nicht unterstützt.
* [3D-Ansicht] Mesh mit mehreren UVs wird nicht ja unterstützt und kann zu ungültigem Material-Rendering führen
* [3D-Ansicht] Pathtracer wird auf AMD-Grafikkarten nicht unterstützt

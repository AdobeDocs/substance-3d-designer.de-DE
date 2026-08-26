---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-4.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 12.4, um mehr über neue Funktionen, Verbesserungen und Fehlerbehebungen zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 12.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---


# Version 12.4

**Substance 3D Designer 12.4** bietet verschiedene Verbesserungen der Lebensqualität (ein Tool zum Bereinigen eines Diagramms, das einfache Formeln zum Festlegen von Parametern verwendet, eine Schaltfläche zum Generieren von Zufallswerten, eine Sperre für die Größe usw.) und Unterstützung von Substance-Modellgrafiken in der Python-API. Weitere Informationen zu diesen Änderungen finden Sie unten.

Freigabedatum: *31. Januar 2023*

## Verbesserungen der Lebensqualität

### „Graph bereinigen“-Werkzeug

Wenn du dein Diagramm bearbeitest, musst du manchmal mehrere Möglichkeiten ausprobieren und verschiedene Knoten an- oder abstecken, bis du das gewünschte Ergebnis erzielt hast. Dann haben Sie am Ende einige Knoten in Ihrem Diagramm, die nicht mit einer Ausgabe verbunden sind, also keine Auswirkungen auf das Endergebnis haben. Mit diesem neuen Tool können Sie diese Knoten automatisch erkennen und löschen, um Ihre Diagramme zu bereinigen, bevor Sie sie abschließen. Das Bereinigungswerkzeug sucht optional auch nach Parameterfunktionen und kann über die entsprechende Schaltfläche in der Symbolleiste der Diagrammansicht oder über eine Auswahl von Diagrammen in der Explorer-Ansicht auf dem aktuellen Diagramm gestartet werden.

![](../../assets/final-clean.gif){width="640px"}

### Eingeben von Formeln in Parameterfelder

Es ist nicht mehr nötig, einen Rechner zu benutzen oder im Kopf zu rechnen, wenn man bestimmte Parameterwerte eingeben will. Sie können jetzt direkt grundlegende Formeln wie Additionen, Divisionen, Multiplikationen oder Subtraktionen eingeben, wenn Sie einen numerischen Wert für einen Parameter in den Eigenschaften und an anderen Stellen in der Anwendung festlegen.

![](../../assets/final-formula.gif){width="640px"}

### Schaltflächen für den Schnellzugriff in der 3D-Ansicht

Wir haben in der [3D-Ansicht](../../interface/3d-view/3d-view.md) eine zusätzliche Symbolleiste hinzugefügt, die allen im Menü [Anzeige](../../interface/3d-view/3d-view.md) verfügbaren Optionen entspricht, damit Sie schnell auf alle diese Optionen zugreifen können (z. B. Drahtgitter, Raster, Begrenzungsrahmen usw.). wie Schaltflächen umgeschaltet werden. Wir haben auch einen Schalter hinzugefügt, um die Umgebungskarte ein-/auszublenden.

![](../../assets/final-3dview.gif){width="640px"}

### Schaltfläche zum Generieren einer Zufallsverteilung

Sie können jetzt schnell verschiedene Varianten erstellen, indem Sie einen neuen Button verwenden, um die zufällige Geschwindigkeit für Ihr Diagramm zu generieren, anstatt einen Schieberegler zu verschieben.

![](../../assets/final-seed.gif){width="640px"}

### Sperre für das Widget &quot;Ausgabegröße&quot;

Sie können nun die Breite und das Height der Ausgabegröße sperren, um sicherzustellen, dass die Größe quadratisch bleibt und die beiden Werte nicht jedes Mal geändert werden, wenn Sie sie aktualisieren möchten.

![](../../assets/final-lock.gif){width="640px"}

### Transformieren der Bildeingabe in Farbe/Graustufen

Wechseln Sie über das Kontextmenü des Knotens schnell zwischen einer [Eingabefarbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) und einer [Graustufen-Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md).

![](../../assets/final-switch.gif){width="640px"}

### Auswählen des angeklickten Pins bei der Anzeige des Verlaufseditors

Wenn Sie im Eigenschaftenfenster auf einen Pin klicken, um einen Verlauf zu bearbeiten, wählen Sie jetzt automatisch den entsprechenden Pin im angezeigten [Verlaufseditor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) aus.

![](../../assets/final-gradient.gif){width="640px"}

### Nachgelagerte Knoten auswählen

Neuer Eintrag im [Knoten-Kontextmenü](../../interface/the-graph-view/the-graph-view.md), um alle Knoten auszuwählen, die direkt oder indirekt mit der Ausgabe der ausgewählten Knoten verbunden sind. Sie wählen also alle Knoten aus, die von Ihrem Knoten betroffen sind. Nützlich, um einen Teil Ihres Diagramms zu löschen oder das Diagrammlayout neu zu bearbeiten.

![](../../assets/final-downstream.gif){width="640px"}

## Python-API-Updates

Diese Version 12.4 bietet auch die vollständige Unterstützung von Substance-Modellgrafiken über die Python-API. Das bedeutet, dass Sie jetzt über alle erforderlichen Tools verfügen, um Substance-Modellgrafiken zu erstellen, zu bearbeiten oder zu bewerten. Ausführliche Informationen finden Sie in der Dokumentation, die Sie über das Hilfemenü der Software finden.

## Versionshinweise

### 12.4.0

*(veröffentlicht am 24. Januar 2023)*

<b>Hinzugefügt:</b>

* [3D-Ansicht] Fügen Sie Schaltflächen für den Schnellzugriff hinzu, um Anzeigeoptionen (Drahtgitter, Umgebungskarte, Szenenstatistiken usw.) festzulegen.
* [Farbmanagement] Verbessern der Qualität von gebackenen 3D-LUTs im ACE-Modus
* [Dokumentation] Beispielprojekte für Substance-Graphen
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
* [UI] Markieren Sie in der 3D-Ansicht das derzeit im Szenenbrowser ausgewählte Element.
* [UX] Zurücksetzen von Schiebereglerbereichen, wenn ihr Wert zurückgesetzt wird
* [API] Hinzufügen von Aktionen zu Symbolleisten der Diagrammansicht zulassen
* [API] Erstellen, Bearbeiten und Bewerten eines Substance-Modelldiagramms über die API zulassen

<b>Fest:</b>

* [3D-Ansicht] Der Eigenschaftswert &quot;DirectX Normal&quot; wird nicht für alle Renderer freigegeben
* [3D-Ansicht] Die Anzeige der Szenenstatistik wird erweitert, wenn der Viewport klein ist
* [3D-Ansicht] Drahtgitter-Anzeigeeigenschaft wird nicht gespeichert
* [Inhalt] Die Parameter für die radiale Weichzeichnungsfarbe haben keine Auswirkungen auf den Alphakanal
* [Lokalisierung] Zusätzliche Schieberegler und Schaltflächen werden in den OpenGL-Eigenschaften der Umgebung angezeigt.
* [MDL][Substance-Modell] Absturz beim Löschen exponierter Knoten
* [Voreinstellungen] Die Datei Default\_config wird nie neu erstellt, wenn sie gelöscht wird
* [Substance-Modell] Parameter für die Neuanordnung von Abstürzen, der nicht auf Instanzebene angezeigt wird
* [API] SDProperty.getDefaultValue() gibt fast immer None zurück.

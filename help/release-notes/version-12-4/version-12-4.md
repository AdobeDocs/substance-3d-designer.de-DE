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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---


# Version 12.4

**Substance 3D Designer 12.4** bietet verschiedene Verbesserungen der Lebensqualität (ein Tool zum Bereinigen eines Grafen, Verwenden von Grundformeln zum Festlegen von Parametern, eine Schaltfläche zum Generieren zufälliger Startwerte, eine Sperre für die Größe usw.) und Unterstützung von Substance-Modelldiagrammen in der Python-API. Weitere Informationen zu diesen Änderungen finden Sie unten.

Freigabedatum: *31. Januar 2023*

## Verbesserungen der Lebensqualität

### „Graph bereinigen“-Werkzeug

Wenn du deinen Graf bearbeitest, musst du manchmal verschiedene Möglichkeiten ausprobieren und verschiedene Knoten an- bzw. abschließen, bis du das gewünschte Ergebnis erzielt hast. Dann haben Sie am Ende einige Knoten im Graf, die nicht mit einer Ausgabe verbunden sind, also keine Auswirkungen auf das Endergebnis. Mit diesem neuen Tool können Sie diese Knoten automatisch erkennen und löschen, um die Graf zu bereinigen, bevor Sie sie abschließen. Das Reinigungswerkzeug sucht optional auch nach Parameterfunktionen und kann auf dem aktuellen Graf über die spezielle Schaltfläche in der Graphansicht-Symbolleiste oder auf einer Auswahl von Grafen aus der Explorer-Ansicht gestartet werden.

![](../../assets/final-clean.gif){width="640px"}

### Eingeben von Formeln in Parameterfelder

Es ist nicht mehr nötig, einen Rechner zu benutzen oder im Kopf zu rechnen, wenn man bestimmte Parameterwerte eingeben will. Sie können jetzt direkt grundlegende Formeln wie Additionen, Divisionen, Multiplikationen oder Subtraktionen eingeben, wenn Sie einen numerischen Wert für einen Parameter in den Eigenschaften und an anderen Stellen in der Anwendung festlegen.

![](../../assets/final-formula.gif){width="640px"}

### Schaltflächen für den Schnellzugriff in den 3D-Ansichten

Wir haben in der [3D-Ansicht](../../interface/3d-view/3d-view.md) eine zusätzliche Symbolleiste hinzugefügt, die allen im Menü [Anzeige](../../interface/3d-view/3d-view.md) verfügbaren Optionen entspricht, damit Sie schnell auf alle diese Optionen zugreifen können (z. B. Drahtgitter, Raster, Begrenzungsrahmen usw.). wie Schaltflächen umgeschaltet werden. Wir haben auch einen Ein-/Ausblenden-Schalter für den Umgebungs-Map hinzugefügt.

![](../../assets/final-3dview.gif){width="640px"}

### Schaltfläche zum Generieren einer Zufallsverteilung

Sie können jetzt schnell verschiedene Varianten erstellen, indem Sie eine neue Schaltfläche verwenden, um die zufällige Geschwindigkeit für Ihren Graf zu generieren, anstatt einen Schieberegler zu verschieben.

![](../../assets/final-seed.gif){width="640px"}

### Sperre für das Widget &quot;Ausgabegröße&quot;

Sie können nun die Breite und das Height der Ausgabegröße sperren, um sicherzustellen, dass die Größe quadratisch bleibt und die beiden Werte nicht jedes Mal geändert werden, wenn Sie sie aktualisieren möchten.

![](../../assets/final-lock.gif){width="640px"}

### Transformieren der Bildeingabe in Farbe/Graustufen

Wechseln Sie über das Kontextmenü des Knotens schnell zwischen einer [Eingabefarbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) und einer [Graustufen-Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md).

![](../../assets/final-switch.gif){width="640px"}

### Bei Anzeige des Verlaufseditors angeklickte Nadel auswählen

Wenn Sie im Eigenschaftenfenster auf eine Nadel klicken, um einen Verlauf zu bearbeiten, wählen Sie jetzt automatisch die entsprechende Nadel im angezeigten [Verlaufseditor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) aus.

![](../../assets/final-gradient.gif){width="640px"}

### Nachgelagerte Knoten auswählen

Neuer Eintrag im [Knoten-Kontextmenü](../../interface/the-graph-view/the-graph-view.md), um alle Knoten auszuwählen, die direkt oder indirekt mit der Ausgabe der ausgewählten Knoten verbunden sind. Sie wählen also alle Knoten aus, die von Ihrem Knoten betroffen sind. Nützlich, um einen Teil Ihres Grafen zu löschen oder das Graf-Layout zu überarbeiten.

![](../../assets/final-downstream.gif){width="640px"}

## Python-API-Updates

Diese Version 12.4 bietet auch die volle Unterstützung von Substance-Modellgrafiken über die Python-API. Das bedeutet, dass Sie jetzt über alle erforderlichen Werkzeuge verfügen, um Substance-Modellgrafiken zu erstellen, zu bearbeiten oder zu bewerten. Ausführliche Informationen finden Sie in der Dokumentation, die Sie über das Hilfemenü der Software finden.

## Versionshinweise

### 12.4.0

*(veröffentlicht am 24. Januar 2023)*

<b>Hinzugefügt:</b>

* [3D-Ansichten] Fügen Sie Schaltflächen für den Schnellzugriff hinzu, um Anzeigeoptionen festzulegen (Drahtgitter, Umgebungs-Map, Szene usw.)
* [Farbmanagement] Verbessern der Qualität Baking geführt 3D-LUTs im ACE
* [Dokumentation] Beispielprojekte für Substance-Graf
* [Dokumentation] Beispielprojekt für Funktions-Graf
* [Explorer] Verschieben von Graf und Ressourcen von einem übergeordneten Element zu einem anderen zulassen, ohne Widgets zu schließen oder zu ungültig zu machen
* [Verlaufseditor] Wählen Sie die angeklickte Nadel aus, wenn Sie den Verlaufseditor anzeigen
* [Graf] Option zum Hinzufügen einer Option zum Auswählen aller untergeordneten Knoten im Kontextmenü eines Knotens
* [Graf] Bereinigen Sie das Graf-Tool, um nicht verwendete Graf in allen Knotentypen und Eigenschaften-Grafen zu erkennen und zu entfernen
* [Graf] Transformieren der Bildeingabe in Farb-/Graustufendarstellung
* [Parameter] Sperre für Ganzzahl2-Widgets hinzufügen
* [Parameter] Einfache Formeln können als Parameter eingegeben werden
* [Substance-Modell] Umschalten zwischen Werten und Symbolen für Wertknoten
* Schaltfläche [UI] zum Generieren eines zufälligen Werts, wenn ein zufälliger Seed erforderlich ist
* [UI] Markieren Sie in der 3D-Ansicht das derzeit im Szenen-Browser ausgewählte Element.
* [UX] Zurücksetzen von Schiebereglerbereichen, wenn ihr Wert zurückgesetzt wird
* [API] Hinzufügen von Aktionen zu Graphansicht-Symbolleisten zulassen
* [API] Erstellen, Bearbeiten und Bewerten eines Substance-Modelldiagramms über die API zulassen

<b>Fest:</b>

* [3D-Ansicht] Der Eigenschaftswert &quot;DirectX Normal&quot; wird nicht für alle Renderer freigegeben
* [3D-Ansicht] Die Anzeige der Szenenstatistik wird erweitert, wenn der Viewport klein ist
* [3D-Ansicht] Drahtgitter-Anzeigeeigenschaft wird nicht gespeichert
* [Inhalt] Die Parameter für die radiale Weichzeichnungsfarbe haben keine Auswirkungen auf den Alphakanal
* [Lokalisierung] Zusätzliche Schieberegler und Schaltflächen werden in den OpenGL-Eigenschaften der Umgebung angezeigt.
* [MDL]&#x200B;[Substance-Modell] Absturz beim Löschen exponierter Knoten
* [Voreinstellungen] Die Datei Default\_config wird nie neu erstellt, wenn sie gelöscht wird
* [Substance-Modell] Parameter für die Neuanordnung von Abstürzen, der nicht auf Instanzebene angezeigt wird
* [API] SDProperty.getDefaultValue() gibt fast immer None zurück.

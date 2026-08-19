---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/release-notes/version-14-1.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 14.1, um mehr über die Knotenanordnungstools und die neuen Spline- und Path-Knoten zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 14.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 1%

---


# Version 14.1

Dieses Update enthält neue Funktionen, mit denen Sie die tägliche Nutzung von Substance 3D Designer verbessern können: Knotenanordnungs-Tools zum schnellen Verbessern des Diagrammlayouts, zum Kopieren/Einfügen von Parametern, um einen Satz von Parametern auf einen anderen Knoten anzuwenden, und zum Verfolgen eines bestimmten Pixels beim Debuggen des Diagramms in der 2D-Ansicht ein Pixelpin. Außerdem werden neue Inhalte hinzugefügt, um insbesondere die Knotensätze Spline und Path zu vervollständigen.

*Freigabedatum: 14. Januar 2025*

![Streuung-Splines auf Splines](../../assets/fond.png)

## Splines- und Pfade-Updates

Splines und Pfadknoten wurden in Version 13.0 eingeführt, und dank Ihres Feedbacks haben wir erste Verbesserungen vorgenommen. Zuerst haben wir den Knoten [Streuung-Splines auf Splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-splines-splines/scatter-splines-on-splines.md) hinzugefügt, der Splines entlang eines übergeordneten Splines verteilt und Optionen anbietet, die denen eines regulären Streuung-Knotens ähneln. Darüber hinaus wurde der Knoten [In Pfade maskieren](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) verbessert, um mehr Kontrolle über die Position des ersten Scheitelpunkts auf dem Pfad zu erteilen. Wir haben es auch ermöglicht, Zufälligkeit in den Knoten [Spline Bridge List](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) einzufügen.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Streuung Spline auf Spline-Animation 1](../../assets/spline1.gif){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines 2](../../assets/spline2.gif){zoomable="yes"}

</td>
</tr>
</table>

## Werkzeuge zur Knotenausrichtung

Wenn Sie ein sauberes und lesbares Diagramm erstellen möchten, sind die [Knoten-Ausrichtungswerkzeuge](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md) für Sie erstellt und wurden vollständig überarbeitet! Es ist jetzt möglich, die Knoten gleichmäßig (horizontal oder vertikal) zu verteilen, und durch das Ausrichten der Knoten werden Überlappungen durch das saubere Stapeln vermieden. Kirschrot oben: beide Features berücksichtigen die tatsächliche Größe der Knoten!

![Knoten ausrichten](../../assets/alignment.gif){zoomable="yes"}

## Kopieren und Einfügen von Parametern

Es ist jetzt möglich, [die Parameter eines Knotens zu kopieren und in einen anderen Knoten einzufügen](../../compositing-graphs/manage-parameters/manage-parameters.md), sodass alle übereinstimmenden Parameter im Zielknoten auf die Werte des Quellknotens aktualisiert werden. Dies ist sehr nützlich, wenn Sie beispielsweise die Parameter eines Farbknotens auf die Graustufenversion übertragen möchten oder umgekehrt. (z. B. der Knoten Sampler anordnen )

## Anheften eines Pixels in der 2D-Ansicht

Mit dem neuen [Color Sampler-Tool](../../interface/2d-view/color-sampler/color-sampler.md) in der 2D-Ansicht können Sie den Wert eines ausgewählten Pixels verfolgen, indem Sie einen Pin darauf ablegen. Dies ist sehr nützlich, um sicherzustellen, dass Sie immer die Informationen desselben Pixels über mehrere Knoten in einem Diagramm anzeigen. Öffnen Sie das Bedienfeld &quot;Informationen&quot;, um auf das Tool zuzugreifen und es auszuprobieren!

![Farbaufnehmer: mit dem Tool](../../assets/color-sampler-demo.gif "Farbaufnehmer: Verwenden des Tools "){width="640px" zoomable="yes"}

## Verbesserte Suchfunktion

Das [Knotenfinder](../../interface/the-graph-view/node-finder/node-finder.md)-Tool wurde leicht verbessert:

* Sie können jetzt einen rekursiven Modus für eine tiefere Suche aktivieren.
* Der Fuzzy-Modus kann deaktiviert werden, wenn Sie nach einem genauen Begriff suchen möchten.
* Der Fokus wird automatisch auf das Suchfeld gesetzt, wenn das Knotensuchwerkzeug aktiviert wird;
* Das Layout der Symbolleiste wurde überdacht, um Platz zu sparen.

![Suchsymbolleiste](../../assets/search-53.png){width="640px"}

## Videos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![Video-Streuung-Splines auf Splines](../../assets/video_spline.png)](https://www.youtube.com/watch?v=aUUWV1dYQdI)

</td>
<td style="border: 0;" valign="top">

[![Funktionen für Videobenutzererlebnisse](../../assets/video_ux.png)](https://www.youtube.com/watch?v=LwexybAEjaI)

</td>
</tr>
</table>

## Versionshinweise

### 14.1.0

*(veröffentlicht am 14. Januar 2025)*

### Hinzugefügt

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

### Fehlerbehebungen

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

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-3.html"
breadcrumb-title: ''
description: Lesen Sie die Versionshinweise für Substance 3D Designer 12.3, um mehr über neue Funktionen, Verbesserungen und Fehlerbehebungen zu erfahren.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 12.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---


# Version 12.3

<b>Substance 3D Designer 12.3</b> hebt die Substance-Modelldiagramme mit der <b>Unterstützung von Untergraphen</b> (oder Diagramminstanzen) sowie der <b> auf ein neues Level. &#39;Sichtbar, wenn&#39; </b>Steuerung für exponierte Parameter und einige <b> neue Knoten</b>, die der Kurven-Edition zugeordnet sind. In dieser Version werden auch zwei neue Bedienfelder (<b>Willkommen </b> und <b>Neue Funktionen</b>) eingeführt, um das Onboarding von Benutzern zu verbessern, sowie einige andere kleinere Funktionen oder Fehlerbehebungen, die unten beschrieben werden.

Freigabedatum: *6. Oktober 2022*

![](../../assets/largef.png){width="1111px"}

## Wichtigste Funktionen

### Unterstützung von Diagramminstanzen in Substance-Modelldiagrammen

Wenn Sie es gewohnt sind, Graphen zu erstellen, möchten Sie in der Lage sein, Untergraph (oder Graphinstanzen) zu erstellen, um Ihre Arbeit wiederzuverwenden, Graphen weniger überladen und effizienter zu gestalten.\
Dies ist jetzt auch für Substance-Modellgrafiken möglich: Ziehe den Untergraph einfach aus dem Explorer in das Hauptdiagramm, um ihn als Instanzknoten zu verwenden.

![](../../assets/subgraph.gif){width="600px"}

Wir haben auch das Konzept der Ausgabeknoten für Substance-Modellgrafiken eingeführt, wie z. B. Ausgabeszene. Sie haben jetzt die Möglichkeit, einen oder mehrere Ausgänge in Ihrem Diagramm zu haben.\
Jede Ausgabe entspricht einem Ausgabepin, wenn Ihr Diagramm in einem anderen Diagramm instanziiert wird.

![](../../assets/image2022-10-4-15-31-27.png){width="600px"}

Wenn Sie mit der rechten Maustaste auf einen Instanzknoten klicken, können Sie natürlich auf den zugehörigen referenzierten Untergraph zugreifen, um diesen anzuzeigen oder zu bearbeiten.

![](../../assets/image2022-10-4-16-28-36.png){width="600px"}

Mithilfe von Untergraphen und angezeigten Parametern können Sie komplexe Elemente erstellen und unendliche Variationen anwenden, wie in der Abbildung unten gezeigt.

![](../../assets/seasons.gif){width="600px"}

### Weitere Verbesserungen für Substance-Modellgrafiken

* <b>Sichtbar, wenn für verfügbar gemachte Parameter</b>\
  Beim Anzeigen von Parametern können Sie die Parameter basierend auf dem Status anderer Parameter ein- oder ausblenden. Ein Schieberegler wird beispielsweise nur angezeigt, wenn eine Schaltfläche aktiviert ist.\
  Mit <b>Visible If</b> können Sie Bedingungen zur Parametersichtbarkeit hinzufügen, wobei eine klare und funktionale Benutzeroberfläche erhalten bleibt. Dieser Mechanismus, der bereits für Substance-Graphen verfügbar ist, wird nun auf Substance-Modellgraphen erweitert, wobei natürlich die gleiche Syntax verwendet wird. <b>\
  </b>

  ![](../../assets/visibleif.gif){width="600px"}

* <b>Neue Knoten für die Kurven-Edition\
  </b>Diese Version enthält einige neue Knoten für die Kurven-Edition: <b>Kurve umkehren</b> tauscht die beiden Enden einer Kurve aus, <b>Kurve unterteilen</b> fügt weitere Scheitelpunkte auf Segmenten nach zwei Methoden hinzu, <b>Kurve glätten </b> alle Winkel auf einer 2D-Kurve glättet und <b>Kurve verschieben</b> bläst eine 2D-Kurve auf oder entleert sie, wie unten dargestellt.<b>

  </b>

  ![](../../assets/curve-offset-4.gif){width="600px"}
* <b>Neues Diagrammfenster </b>\
  Das Fenster &quot;<b>Neues Substance-Modelldiagramm</b>&quot; ist jetzt auch für Substance-Modelldiagramme verfügbar. Sie können Ihre eigenen Vorlagen hinzufügen oder eine Standardvorlage auswählen, dann geben Sie direkt den Namen Ihres Diagramms ein und wählen das Paket aus, dem das Diagramm hinzugefügt werden soll.

  ![](../../assets/image2022-10-5-15-25-42.png){width="600px"}

### Bedienfelder &quot;Willkommen&quot; und &quot;Neue Funktionen&quot;

Wir haben zwei neue Bedienfelder eingeführt, die Ihnen den Einstieg in Designer erleichtern:

Zunächst bietet das Bedienfeld <b>Willkommen </b> - das beim ersten Start von *Designer* angezeigt wird - einen globalen Überblick über die Software und ihre Rolle im Substance 3D-Ökosystem. Das Bedienfeld <b>Neuerungen </b> - wird angezeigt, wenn Sie zum ersten Mal eine *neue Version* von Designer ausführen - zeigt schnell die Hauptfunktionen, die in dieser Version eingeführt wurden.

Diese beiden Bereiche sind auch über das Menü &quot;Hilfe&quot; zugänglich.

![](../../assets/image2022-10-3-15-47-28.png)

![](../../assets/image2022-10-3-15-47-55.png)

### Sonstiges

* <b>Zwei Schaltflächen-Widget für verfügbar gemachte boolesche Parameter</b>\
  Sie haben jetzt eine neue Möglichkeit, boolesche Parameter in einem Substance-Diagramm darzustellen. Zusätzlich zur Schaltfläche &quot;Wechseln&quot; können Sie <b>Schaltflächen nebeneinander</b> mit benutzerdefinierten Texten verwenden, um die beiden verschiedenen Modi, die durch den booleschen Parameter gesteuert werden, besser sichtbar zu machen.
* <b>Skalierungsprobleme für HD-Bildschirme lösen </b>\
  In früheren Versionen konnte Designer den im Betriebssystem festgelegten Skalierungsfaktor nicht korrekt verarbeiten. Wie Sie in der Abbildung unten sehen können, ist alles perfekt verwaltet auf einem 4K-Display mit 125 % Skalierung mit allen Schriften und Tasten in einer kohärenten Größe angezeigt.\
  Beachten Sie, dass die Option &quot;High DPI deaktivieren&quot; in den Voreinstellungen in dieser neuen Version auf *False* zurückgesetzt wurde, da diese Option nicht mehr erforderlich ist, um über eine verwendbare Schnittstelle zu verfügen.

  ![](../../assets/highdpi-fix.gif){width="600px"}

* **Native Unterstützung für Apple Silicon (M1/M2) für Steam-Version**\
  Die 12.2-Version von Designer war die erste, die die volle Unterstützung für neue Apple-Rechner auf der Basis von M1- oder M2-Chips mitbrachte, aber diese Unterstützung fehlte in der Steam-Edition. Ab jetzt können alle Designer-Benutzer von einer schnelleren und effizienteren Benutzererfahrung auf diesen Computern profitieren.

## Versionshinweise

### 12.3.0

*(veröffentlicht am 06. Oktober 2022)*

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

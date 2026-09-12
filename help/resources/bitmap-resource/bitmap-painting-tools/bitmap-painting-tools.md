---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource/bitmap-painting-tools.html"
breadcrumb-title: ''
description: Mit den Bitmap-Malwerkzeugen in Substance 3D Designer können Sie direkt auf Bitmap-Ressourcen malen, um Strukturen zu bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource > Bitmap painting tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap-Malwerkzeuge
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9b772dfaab124991f6c6420f451179304d2731cd
workflow-type: tm+mt
source-wordcount: '1964'
ht-degree: 0%

---


# Bitmap-Malwerkzeuge

Auf dieser Seite werden die Malwerkzeuge beschrieben, die im Bereich [2D View](../../../interface/2d-view/2d-view.md) für kompatible Bitmaps verfügbar sind.

![Bitmap-Malwerkzeuge in der 2D-Ansicht](bitmap-painting-tools.resources/2dview-paintingtools-main_1.png "Bitmap-Malwerkzeuge in der 2D-Ansicht"){width="512px"}

## Überblick

Das Bedienfeld [2D View](../../../interface/2d-view/2d-view.md) bietet grundlegende Bitmapmalwerkzeuge, mit denen Sie Bilder *manuell* direkt in der Anwendung erstellen oder bearbeiten können. Diese Tools sind besonders nützlich, um beispielsweise *Masken* schnell zu malen.

Die Tools unterstützen die Stifteingabe, einschließlich *Stiftdruck*. Um die Vorteile von Stiftanzeigen zu nutzen, können Sie das Bedienfeld [2D-Ansicht](../../../interface/2d-view/2d-view.md) [abdocken](../../../interface/customizing-your-wor/customizing-your-workspace.md) und es dann in eine beliebige Konfiguration platzieren und skalieren, die für das Malen angenehmer ist.

Bearbeitungen können *einzeln rückgängig gemacht werden*, und alle anderen Funktionen des Bedienfelds &quot;2D-Ansicht&quot; sind weiterhin *verfügbar*, während Sie das Bild bearbeiten, z. B. das Bedienfeld [Histogramm](../../../interface/2d-view/2d-view.md), die [Musteranzeige](../../../interface/2d-view/2d-view.md) und das [Hintergrundbild](../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Sie können *nur* auf *8-Bit* [Bitmapressourcen](../../../resources/bitmap-resource/bitmap-resource.md) malen, die [neu oder importiert](../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) sind.

>[!WARNING]
>
> **Nur Windows**
> 
> Tablet-Benutzer sollten die auf der folgenden Seite beschriebenen Einstellungen anwenden, um ein möglichst zuverlässiges Erlebnis zu erzielen: [Konfigurieren von Stiften und Tablets](https://docs.substance3d.com/display/SPDOC/Configuring+Pens+and+Tablets)

![Neues Bitmapdialogfeld](bitmap-painting-tools.resources/2dview-paintingtools-new-bitmap.png "Neues Bitmapdialogfeld"){width="512px"}

## Aktivieren der Malwerkzeuge

Die Malwerkzeuge werden automatisch im Bedienfeld [2D-Ansicht](../../../interface/2d-view/2d-view.md) aktiviert, wenn die folgenden Kriterien für eine Bitmap erfüllt sind:

* Die Bitmap ist eine [neue oder importierte &#x200B;](../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)-Ressource.
* Die Bitmap weist die Präzision *8-Bit* auf.
* Die Bitmap wird im Bereich [2D-Ansicht](../../../interface/2d-view/2d-view.md) angezeigt.

*Neue* Bitmaps können auf folgende Weise erstellt werden:

* Klicken Sie im Bereich [Explorer](../../../interface/the-explorer-window/the-explorer-window.md) auf RMB in einem *SBS-Paket* oder einem *Ordner* in einem Paket, um das Kontextmenü zu öffnen. Öffnen Sie dann das Untermenü <b>Neu</b> und wählen Sie die Option <b>Bitmap</b> aus.
* Erstellen Sie in einem [Diagramm](../../../interface/the-graph-view/the-graph-view.md) einen [Bitmapknoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), und wählen Sie die <b>Von neuer Ressource...Option </b> im Kontextmenü

Das Fenster <b>Neue Bitmap</b> wird geöffnet, in dem Sie die *Namen*, *Auflösung* und *Hintergrundfarbe* der neuen Bitmapressource festlegen können.

>[!NOTE]
>
> *Neue* Bitmapressourcen *immer* haben *RGBA* Farben und *8-Bit* Genauigkeit.

>[!WARNING]
>
> Für die beste Leistung mit den Malwerkzeugen empfehlen wir die Verwendung von Bitmaps mit Auflösungen, die *Potenzen von zwei* sind - z. B. 128, 256, 512, 1024, ...

## Symbolleisten

Die Malwerkzeuge und -optionen sind in *Symbolleisten* im Bedienfeld [2D-Ansicht](../../../interface/2d-view/2d-view.md) angeordnet. Diese Symbolleisten können auf *eine beliebige Seite* des Bedienfelds oder als *schwebende Symbolleiste* verschoben werden, indem Sie auf ihrem *Handle* auf <b>LMB</b> klicken und diese gedrückt halten - angezeigt als dreifache Linie - und dann <b>LMB</b> an der gewünschten Position freigeben.

Zwei Werkzeugleisten werden angezeigt, wenn die Malwerkzeuge aktiviert sind: die [Werkzeugauswahlsymbolleiste](#bitmappaintingtools-toolselectiontoolbar) und die Werkzeugoptionssymbolleiste, die unten beschrieben werden.

## Werkzeugleiste für Werkzeugauswahl

Die Malwerkzeuge befinden sich in der Symbolleiste **Werkzeugauswahl**, die standardmäßig auf der *linken Seite* des Bedienfelds [2D-Ansicht](../../../interface/2d-view/2d-view.md) platziert ist. Tastaturbefehle ermöglichen einen schnellen Zugriff auf diese Werkzeuge und sind unten in Klammern nach dem Werkzeug-/Funktionsnamen gekennzeichnet:

![](bitmap-painting-tools.resources/2dview-paintingtools-icon-colors-primary.png)![](bitmap-painting-tools.resources/2dview-paintingtools-icon-colors-secondary.png) <b>Farbauswahl</b> <b>Miniaturansichten:</b> Ermöglicht Ihnen das Definieren einer *primären* und *sekundären* Farbe. Klicken Sie auf eine dieser Miniaturansichten, um das Fenster &quot;<b>Color Editor</b>&quot; anzuzeigen und eine Farbe zu definieren. Tools verwenden die Farbe *primär*. Die primären und sekundären Farben können jederzeit *ausgetauscht* (<b>X</b>) werden.

![](bitmap-painting-tools.resources/2dview-paintingtools-icon-brush.png) <b>Pinselwerkzeug (B):</b> Wendet die *primäre* Farbe an der Cursorposition an, wenn die Stiftspitze oder die <b>LMB</b>-Schaltfläche gedrückt wird, wobei die in der Werkzeugoptionsleiste definierten Optionen verwendet werden

![](bitmap-painting-tools.resources/2dview-paintingtools-icon-clone.png) <b>Stempelwerkzeug (T):</b> Ermöglicht das Stempeln eines Teils des Bildes auf ein anderes. Sie können die *Quelle* definieren, die gestempelt werden soll, indem Sie die <b>Alt</b>-Taste gedrückt halten und auf <b>LMB</b> klicken. Dieser Bereich des Bildes wird dann auf den Bereich *target* des Bildes an der Cursorposition gestempelt, wenn die Stiftspitze oder die Schaltfläche <b>LMB</b> gedrückt wird, wobei die in der Werkzeugoptionsleiste definierten Optionen verwendet werden. Beachten Sie, dass die Quelle *die Bewegungen des Ziels* verfolgt und dass die Größe des Bereichs *Quelle* *mit* der Größe des *Pinsels* übereinstimmt.

![](bitmap-painting-tools.resources/2dview-paintingtools-clone-alignment.png) <b>Ausrichtung aktivieren (Stempelwerkzeug-Option):</b> Hiermit können Sie definieren, ob die Quelle *an Ort und Stelle bleiben soll*, wenn ein neuer Stempel beginnt, oder ob *sie relativ zur neuen Stempelstelle verschieben soll*

<b>![](bitmap-painting-tools.resources/2dview-paintingtools-icon-eraser.png) Radiergummi (E):</b> Ersetzt die aktuelle Farbe des Bildes durch den Wert (0, 0, 0, 0) an der Cursorposition, wenn die Stiftspitze oder die Schaltfläche <b>LMB</b> gedrückt wird, und verwendet dabei die in der Werkzeugoptionsleiste definierten Optionen. Stellen Sie sicher, dass die [Transparenzanzeige](../../../interface/2d-view/2d-view.md) aktiviert ist, um die Auswirkungen dieses Tools auf den Kanal <b>Alpha</b> verfolgen zu können.

## Werkzeugoptionsleiste

Die Optionen für die in der Werkzeugleiste [Werkzeugauswahl](#bitmappaintingtools-toolselectiontoolbar) verfügbaren Werkzeuge finden Sie in der Werkzeugleiste für Werkzeugoptionen, die standardmäßig auf der *oberen Seite* des Bedienfelds [2D-Ansicht](../../../interface/2d-view/2d-view.md) platziert ist.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### PINSELAUSWAHL

Mit der ![](bitmap-painting-tools.resources/2dview-paintingtools-brush-thumb.png) <b>Pinselauswahl</b> können Sie einen *vorkonfigurierten* Pinsel aus dem verfügbaren Pinsel *Vorgaben* auswählen, seine <b>Größe</b> und <b>Härte</b> *(* siehe Abschnitt <b>Form</b> des Pinseleditors) festlegen und eine *Vorschau* eines Pinselstrichs anzeigen.

Pinselvorgaben können im Pinseleditor erstellt und bearbeitet und in *Bibliotheken* angeordnet werden. Die Pinselvorgaben, die in diesem Bereich angezeigt werden, sind die *Summe* aller geladenen Pinselvoreinstellungsbibliotheken. Diese Bibliotheken können über das Menü ![](bitmap-painting-tools.resources/2dview-paintingtools-brushpresets-library.png) <b>Pinselbibliothek</b> verwaltet werden (siehe Abschnitt <b>Vorgaben</b> des Pinsel-Editors).

Mit der Schaltfläche ![](bitmap-painting-tools.resources/2dview-paintingtools-brushpresets-previewbkgd.png) <b>Hintergrundfarbe auswählen</b> können Sie die Hintergrundfarbe der *Pinselstrichvorschau* ändern.

</td>
<td style="border: 0;" valign="top">

![Pinselauswahlfenster](bitmap-painting-tools.resources/2dview-paintingtools-brushes.png "Pinselauswahlfenster")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### PINSELEDITOR

Der ![](bitmap-painting-tools.resources/2dview-paintingtools-icon-brush-options.png) <b>Pinsel-Editor</b> bietet Zugriff auf granulare Optionen zum Definieren des Verhaltens des Pinsels:

<b>Vorgaben</b>

Pinsel können angepasst und dann als <b>Pinselvorgabe</b> gespeichert werden, die dann in der Liste ![](bitmap-painting-tools.resources/2dview-paintingtools-editor-currentpreset.png) <b>Pinselvorgaben</b> und im Bereich ![](bitmap-painting-tools.resources/2dview-paintingtools-brush-thumb.png) <b>Pinselauswahl</b> verfügbar ist.

Um eine Vorgabe zu erstellen, legen Sie die folgenden Eigenschaften nach Ihren Wünschen fest. Klicken Sie dann auf die Schaltfläche ![](bitmap-painting-tools.resources/2dview-paintingtools-editor-addpreset.png) <b>Pinselvorgabe hinzufügen </b> und legen Sie im Fenster <b>Vorgabenname</b> einen Pinselnamen fest. Die neue Vorgabe wird jetzt automatisch in der Liste <b>Pinselvorgaben</b> ausgewählt, und Sie können sie jederzeit ![](bitmap-painting-tools.resources/2dview-paintingtools-editor-updatepreset.png) <b>aktualisieren</b> mit den neuen aktuellen Einstellungen oder ![](bitmap-painting-tools.resources/2dview-paintingtools-editor-deletepreset.png) <b>löschen</b>.

Vorgaben werden in *Bibliotheken* organisiert und gespeichert, die im Menü ![](bitmap-painting-tools.resources/2dview-paintingtools-editor-presetlibrary.png) <b>Pinselbibliothek</b> verwaltet werden können:

<b>Bibliothek exportieren:</b> *Speichern* der aktuellen Vorgaben und aller zugehörigen Einstellungen in einer Bibliotheksdatei

<b>Bibliothek importieren:</b> *Vorgaben laden* aus einer vorhandenen Bibliotheksdatei, und *sie der aktuellen Liste hinzufügen* - Vorgaben mit *demselben Namen werden ersetzt* durch die Vorgaben aus der Bibliotheksdatei

<b>Bibliothek zurücksetzen:</b> setzt die aktuellen Vorgaben durch die Standardbibliothek zurück.

<b>Bibliothek ersetzen:</b> *Vorgaben aus einer vorhandenen Bibliotheksdatei laden* und *die aktuelle Liste schließen*

</td>
<td style="border: 0;" valign="top">

![Pinsel-Editor](bitmap-painting-tools.resources/2dview-paintingtools-brusheditor.png "Pinsel-Editor")

</td>
</tr>
</table>

#### Pinseleinstellungen

Die Einstellungen eines Pinsels sind in die folgenden Abschnitte unterteilt:

+++Form
Der Parameter <b>Shape type</b> steuert die Grundform des Pinsels. Verfügbare Formen sind:

* *Ellipse*: eine runde Form, die standardmäßig als *Kreis* festgelegt ist

* *Rechteck*: eine gerade Form, die standardmäßig als *Quadrat* festgelegt ist

* *Polygon*: eine gerade Form mit einer *anpassbaren* Anzahl von Kanten und Winkeln

<b>Anzahl der Kanten </b>(*Nur Polygon*-Form): können Sie die Anzahl von *Gesichtern* des Polygons auswählen

<b>Innerer Radius </b>(*Nur Polygon*-Form): ermöglicht die Kontrolle über den Abstand zwischen einem Gesicht *Mittelpunkt* und dem Mittelpunkt der Form, wodurch effektiv ein Muster *Stern* erstellt wird

<b>Härte</b>: definiert *Überblendungsradius* der Form

+++

+++Transformieren
Wenn Sie einen Pinselstrich auf das Bild anwenden, handelt es sich bei dem Strich im Grunde um ein wiederholtes Stanzen des Pinselmusters, entsprechend dem Verhalten, das durch die Steuerelemente in diesem Abschnitt definiert wird.

<b>Größe</b>: legt den *Durchmesser* der Pinselform in Pixel fest

<b>Größe Jitter</b>: lässt Sie *randomisieren* die Pinselgröße pro Stempel, wird als *Prozentsatz* des <b>Größe</b>-Werts ausgedrückt und steuert den *Bereich* der zufälligen Werte von <b>0</b> bis zum <b>Größe</b>-Wert.

<b>Größensteuerung</b>: Wenn Sie eine Stifteingabe mit Unterstützung für den *Stiftdruck* verwenden, können Sie mit diesem Parameter die Pinselgröße steuern

<b>Abstand</b>: steuert den Abstand *zwischen jedem einzelnen Stempel* entlang eines Pinselstrichs. Dadurch können Sie die Formmuster besser trennen und deutlicher definieren

<b>Rundheit</b>: Standardmäßig weist der im Abschnitt <b>Shape</b> ausgewählte <b>Shape-Typ</b> ein Height-zu-Breite-Verhältnis von *1:1* auf. Mit diesem Parameter können Sie dieses Verhältnis ändern, indem Sie die Breite *als Prozentwert des Heights um* verringern.

<b>Rundheitsjitter</b>: lässt Sie *die Rundheit pro Stempel zufällig* zuordnen, wird als *Prozentsatz* des <b>Rundheitswerts</b> ausgedrückt und steuert den *Bereich* der zufälligen Werte von <b>0</b> bis zum <b>Rundheitswert</b>

<b>Winkel</b>: steuert die *Drehung* des Pinselmusters in *Grad*

<b>Angle Jitter</b>: lässt Sie die Drehung pro Stempel *zufällig* zuordnen, wird als *Prozentsatz* des <b>Winkels</b>-Werts ausgedrückt und steuert den *Bereich* zufälliger Werte von <b>0</b> bis <b>360 </b>Grad

+++

+++Streuung
Standardmäßig ist das Formmuster entlang der Kontur streng gestempelt. Sie können den Effekt umkehren, indem Sie einen Versatz auf das Formmuster anwenden, damit sie um den Strich herum gestreut werden können, um einen organischeren oder chaotischeren Effekt zu erzielen.

<b>Streuung</b>: die maximale *Entfernung*, um die jeder einzelne Stempel von der Kontur versetzt werden soll, ausgedrückt als Prozentsatz der *Pinselgröße*. Beachten Sie, dass dieser Abstand standardmäßig *randomisiert* ist, von <b>0</b> bis zum *festgelegten Prozentsatz* der Pinselgröße, und dass die *Richtung* des Versatzes ebenfalls zufällig ist.

<b>Anzahl</b>: die Anzahl der verstreuten Exemplare der Einzelmarke;

+++

+++Color
Die vom Pinsel angewendete Farbe wird durch die *ausgewählte Primärfarbe* definiert - und die <b>Pinselstruktur</b>, sofern diese aktuell angewendet wird. Diese Farbe kann mithilfe der Steuerelemente in diesem Abschnitt dynamisch geändert werden.

<b>Flussjitter</b>: lässt Sie *zufällig* den Textfluss pro Stempel zuordnen, wird als *Prozentsatz* des maximalen Textflusses ausgedrückt

<b>Flusssteuerung</b>: Wenn Sie eine Stifteingabe mit Unterstützung für *Stiftdruck* verwenden, können Sie diesen Parameter verwenden, um den Fluss zu steuern

<b>Farbton-Jitter</b>: lässt Sie *randomisieren* der Farbton *offset* pro Stempel wird als *Prozentsatz* des gesamten Farbtonbereichs ausgedrückt.

<b>Sättigungsjitter</b>: lässt Sie *randomisieren* die Farbsättigung *offset* pro Stempel, ausgedrückt als *Prozentsatz* des gesamten Sättigungsbereichs

<b>Helligkeitsjitter</b>: lässt Sie *randomisieren* die Farbhelligkeit *offset* pro Stempel, ausgedrückt als *Prozentsatz* der gesamten Helligkeitsspanne

+++

+++Textur
Sie können eine *Bitmapdatei* auf den Pinsel anwenden und diese Bitmapdatei anstelle einer einfachen Farbe für *Stempel* verwenden. Die Pinsel-Textur verhält sich wie folgt:

<b> Textur: </b> definiert den *Pfad* der Bitmap, der als Pinsel-Textur verwendet werden soll. Sie können die Bitmap über den Dateibrowser Ihres Systems auswählen, indem Sie die Schaltfläche ![](bitmap-painting-tools.resources/2dview-paintingtools-brusheditor-selecttexture.png) neben dem Eingabefeld verwenden

Die Textur *only* ersetzt die einfache Flächenfarbe des Pinsels, d. h. *alle oben aufgeführten Pinseleigenschaften können weiterhin verwendet werden* und funktionieren wie beschrieben.

Die Farben der Textur sind *farblich verschoben* in Richtung der *festgelegten Primärfarbe*, was bedeutet, dass die Farben der Textur unverändert verwendet werden können, wenn die festgelegte Primärfarbe Weiß ist. Je gesättigter die eingestellte Primärfarbe ist, desto stärker werden die Farbtonfarben zu der Textur hin verschoben

+++

### DECKKRAFT/DURCHFLUSS

Die Pinsel-, Stempel- und Radiergummi-Werkzeuge bieten Steuerelemente für die <b>Deckkraft</b> und <b>Fluss</b>:

<b>Deckkraft</b> steuert die *maximale Deckkraft* des Stempels. Es ist *additiv auf separaten Strichen*, was bedeutet, dass die Deckkraft eines Bereichs auf den maximalen Wert von 100 % zurückgesetzt werden kann, indem mehrere *separate* Striche in diesem Bereich ausgeführt werden.

<b>Flow</b> steuert den *Betrag des Effekts des Tools*, der zu einem beliebigen Zeitpunkt angewendet wird. Es ist *additiv auf derselben Kontur*, was bedeutet, dass die Deckkraft eines Bereichs auf den maximalen Wert von 100 % zurückgesetzt werden kann, indem mehrere Durchgänge der *gleichen Kontur* in diesem Bereich oder mehrere separate Konturen ausgeführt werden.

![Deckkraft- und Flusssteuerelemente](bitmap-painting-tools.resources/2dview-paintingtools-opacityflow.png "Deckkraft- und Flusssteuerelemente")

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### KACHELUNGSMODUS

Mit den Pinsel-, Stempel- und Radiergummi-Werkzeugen können Sie auch die ![](bitmap-painting-tools.resources/2dview-paintingtools-icon-tiling.png) <b>Kachelung-Modi</b> einstellen, die festlegen, dass *eine Schleifenwiedergabe um* erfolgen kann, wenn ein Strich auf einen Bereich außerhalb der Bildgrenzen wirkt:

<b>Kachelung X und Y</b>: Pinselstrichkachel *sowohl horizontal als auch vertikal*

<b>Kachelung X</b>: Pinselstrichkachel *nur horizontal*

<b>Kachelung Y</b>: Pinselstrichkachel *nur vertikal*

<b>Keine Kachelung</b>: Pinselstriche *nicht kacheln*

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Kachelung-Modus](bitmap-painting-tools.resources/2dview-paintingtools-tiling.png "Kachelung-Modus")

</td>
</tr>
</table>

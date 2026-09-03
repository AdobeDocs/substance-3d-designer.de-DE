---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/frame.html"
breadcrumb-title: ''
description: Verwenden Sie Rahmen in der Substance 3D Designer-Graphansicht, um Knoten für mehr Übersichtlichkeit zu organisieren und zu gruppieren.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Frame
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rahmen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 1%

---


# Rahmen

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Rahmen-Symbol](frame.resources/frame-01.png "Rahmen-Symbol")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ein Rahmen erleichtert die Lesbarkeit und das Layout von Grafen, indem er Objekte in diesem Graf visuell gruppiert und all diese Objekte einfach zusammenführt.

So können beispielsweise Rahmen benannt und eingefärbt werden, sodass die Struktur des Grafen bei der Übersicht deutlich hervortritt, was mit zunehmender Komplexität eines Grafen sehr hilfreich ist.

Sie können auch mit Anmerkungen versehen werden und dienen somit als Dokumentationswerkzeug, um zu erklären, warum einige Knoten auf eine bestimmte Weise eingerichtet wurden.

</td>
</tr>
</table>

## Erscheinungsbild

Abhängig von der Position des Mauszeigers oder davon, ob er Teil einer Auswahl ist, präsentiert sich ein Rahmen in verschiedenen visuellen Stilen, sodass Sie wissen, ob und wie Sie damit interagieren können.

+++Standard
Standardmäßig ist der Rahmen ein Rechteck mit abgerundeten Ecken, das mit der in der Eigenschaft <b>Rahmen Color</b> ausgewählten Farbe gefüllt ist. Eine dunklere Schattierung dieser Farbe wird auf die Umrisslinie des Rahmens angewendet.

Der in der <b>Title</b>-Eigenschaft festgelegte Titel wird in Grau auf der linken oberen Ecke des Rahmens angezeigt.

![Rahmen (Standardstatus)](frame.resources/frame-02.png "Rahmen (Standardstatus)")



+++

+++Header Hover
Wenn Sie den Mauszeiger über den Rahmen führen, wird eine Kopfzeile angezeigt.

Ziehen Sie die Kopfzeile bzw. den Rahmen.

![Rahmen (Hover-Zustand)](frame.resources/frame-03.png "Rahmen (Hover-Zustand)")



+++

+++Ausgewählt
Nach der Auswahl werden Titel und Umriss des Rahmens weiß hervorgehoben. Die Kontur wird dicker.

![Rahmen (ausgewählter Status)](frame.resources/frame-04.png "Rahmen (ausgewählter Status)")



+++

## Erstellen von Rahmen

Rahmen können in einem beliebigen Graf-Typ auf eine der folgenden Arten hinzugefügt werden:

+++Knotenmenü
Drücken Sie die <b>Leertaste</b> in der Graphansicht, um das <b>Knotenmenü</b> zu öffnen, und wählen Sie das Element &quot;Rahmen&quot; in der Liste aus.

Geben Sie &#39;Rahmen&#39; in das Suchfeld ein, um das Element anzuzeigen und es schneller zu finden.

+++

+++Tastaturbefehl
Wenn ein Tastaturbefehl der Tastatur dem Element &quot;Rahmen&quot; in den [Voreinstellungen](../../../../interface/preferences-window/preferences-window.md) zugeordnet ist, drücken Sie diesen Tastaturbefehl, wenn die Graphansicht den Fokus hat.

+++

+++Kontextmenü
Drücken Sie in der Graphansicht <b>RMB</b> für ein beliebiges Objekt oder in einem leeren Bereich und wählen Sie die Option <b>Rahmen hinzufügen</b> aus.

+++

+++Diagrammsymbolleiste
Klicken Sie in der Symbolleiste der Diagrammansicht auf die Schaltfläche &quot;Frame&quot; in der <b>Node-Palette</b>.

+++

+++Bibliothek
Wählen Sie in der Bibliothek die Kategorie <b>Graf-Elemente</b> aus, ziehen Sie dann das Element &#39;Rahmen&#39; in die Graphansicht und legen Sie es ab.

+++

### Auswahlrahmen

Wenn beim Erstellen eines Frames eine Auswahl in einem Diagramm aktiv ist, wird dieser Frame automatisch angepasst, damit die ausgewählten Objekte vollständig einbezogen werden.

Vor diesem Hintergrund ist es beim Erstellen von Rahmen mit einem Tastaturbefehl noch schneller, den Inhalt eines Diagramms zu rahmen.

![Frames: Erstellungsmethoden](frame.resources/frame-05.gif "Frames: Erstellungsmethoden"){width="480px"}

>[!TIP]
>
> Wenn ein Frame erstellt wird, erhält seine Eigenschaft &quot;Titel&quot; automatisch den Fokus, sodass Sie den Titel des Frames sofort bearbeiten können.

## Bearbeiten von Frames

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Rahmen können <b>verschoben</b> werden, indem der Titel oder die Kopfzeile gezogen wird, und <b>ihre Größe geändert</b>, indem die Ränder oder Ecken gezogen werden.

In der Abbildung werden die Interaktionsbereiche zum Schwenken (blau) und Skalieren (gelb) hervorgehoben.

</td>
<td style="border: 0;" valign="top">

![Frames: Interaktionszonen](frame.resources/frame-06.png "Frames: Interaktionszonen")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Rasterausrichtung

Standardmäßig wird ein Rahmen beim Verschieben oder Ändern der Größe am mittleren Raster ausgerichtet.

Halten Sie die Taste <b>Strg</b> (Windows) bzw. <b>Cmd</b> (macOS) gedrückt, um diese Ausrichtung auf das kleine Raster zu verschieben, um feinere Anpassungen vorzunehmen.

</td>
<td style="border: 0;" valign="top">

![Frames: Rasterausrichtung](frame.resources/frame-07.gif "Frames: Rasterausrichtung ")

</td>
</tr>
</table>

## Eigenschaften

Wenn ein Frame ausgewählt ist, sind die folgenden Eigenschaften im Dock [Eigenschaften](../../../../interface/properties/properties.md) verfügbar:

+++Titel
Der <b>Titel</b>, der oben links auf dem Rahmen liegt. Die Sichtbarkeit des Titels kann mithilfe der <b>Title Visible</b>-Eigenschaft aktiviert oder deaktiviert werden.

Die Größe des Titels kann bei einer minimalen Bildschirmgröße gesperrt werden, sodass der Titel beim Auszoomen aus dem Diagramm lesbar bleibt. Sie können dies tun, indem Sie die Option &quot;Bildtitel&quot; im Dropdown-Menü <b>Informationen</b> in der Symbolleiste [Diagrammansicht](../../../../interface/the-graph-view/the-graph-view.md) aktivieren.

![Frames: Titel](frame.resources/frame-08.gif "Bilder: Titel"){width="640px"}



+++

+++Beschreibung
Die <b>Beschreibung</b> ist ein optionaler zusätzlicher Textausschnitt, der zum Kommentieren des Inhalts des Rahmens verwendet werden kann.

Der Text kann mit HTML-Tags formatiert werden. Diese Formatierung wird durch Klicken auf die Schaltfläche ![](frame.resources/frame-09.png) <b>HTML-Markup</b> umgeschaltet.

Weitere Informationen finden Sie im Abschnitt &quot;Beschreibung&quot; weiter unten.

![Frames: Beschreibung](frame.resources/frame-10.gif "Rahmen: Beschreibung"){width="640px"}



+++

+++Color
Die <b>Rahmen-Farbe</b> wird verwendet, um den Rahmen in der Graphansicht zu füllen. Wählen Sie mit dem Farbwähler eine beliebige Farbe aus.

Der Alphakanal der Farbe steuert die *Deckkraft* des Rahmens, wobei ein Wert von 0 bedeutet, dass der Rahmen vollständig transparent ist.

![Frames: Color](frame.resources/frame-11.gif "Rahmen: Farbe "){width="640px"}



+++

## Beschreibung

Ein Rahmen kann mit einem Text versehen werden, der innerhalb des Rahmens platziert wird. Der Text wird links ausgerichtet und beginnt in der linken oberen Ecke des Rahmens. Verwenden Sie die [Description](#properties)-Eigenschaft des Rahmens, um diesen Text zu bearbeiten.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Standard

Der <b>Titel</b> wird in einer fetten Schrift angezeigt, die sich oben links im Rahmen befindet. Die Sichtbarkeit des Titels kann ein- oder ausgeschaltet werden.

Sein Format kann bei einer minimalen Bildschirmgröße gesperrt werden, sodass es beim Verkleinern des Grafen lesbar bleibt. Sie können dies tun, indem Sie die Option &quot;Bildtitel&quot; im Dropdown-Menü <b>Informationen</b> in der Symbolleiste [Diagrammansicht](../../../../interface/the-graph-view/the-graph-view.md) aktivieren.

</td>
<td style="border: 0;" valign="top">

![Rahmen (Standardbeschreibung)](frame.resources/frame-12.png "Rahmen (Standardbeschreibung)"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### HTML-Formatierung

Der Text kann mithilfe von HTML-Tags in der <b>Description</b>-Eigenschaft des Rahmens formatiert werden. Die Formatierung muss aktiviert werden, indem die Schaltfläche ![](frame.resources/frame-09.png) <b>HTML-Markup</b> in derselben Eigenschaft verwendet wird.

</td>
<td style="border: 0;" valign="top">

![Rahmen (HTML-formatierte Beschreibung)](frame.resources/frame-13.png "Rahmen (HTML-formatierte Beschreibung)"){zoomable="yes"}

</td>
</tr>
</table>

Sie können dieses Beispiel kopieren und in die Description-Eigenschaft des Rahmens einfügen, um diese Funktion selbst zu testen:

```
<h2>HTML formatting</h2>

<p>This is a description formatted using <b>HTML markup</b>.</p>

<p>Formattig text makes it more <i>pleasant</i>, <font color="#CC8822">impactful</font> and <code>clearly structured</code> for users.</p>

<p><img src="image_filepath">  Images are also supported! <sup>How nice!</sup></p>
```


Im Folgenden finden Sie eine Liste hilfreicher Tags zum Formatieren von Text:

+++HTML von Formatierungstags

|  |  |
| --- | --- |
| Fett | &lt;b>...&lt;/b> |
| Kursiv | &lt;i>...&lt;/i> |
| Color | &lt;font color=&quot;#4A567C&quot;>...&lt;/font> |
| Absatz | &lt;p>...&lt;/p> |
| Zeilenumbruch | &lt;br> |
| Überschriften | &lt;h1>...&lt;/h1>, &lt;h2>...&lt;/h2> usw. |
| Bild | &lt;img src=&quot;{path\_to\_image}&quot;> |
| Hochstellen | &lt;sub>...1&lt;/sub> |
| Ungeordnete Liste (Aufzählungszeichen) | &lt;ul> &lt;li>...&quot;&lt;/li> &quot;&lt;li>...&lt;/li> &lt;/ul> |
| Geordnete Liste (Zahlen) | &lt;ol> &lt;li>...&quot;&lt;/li> &quot;&lt;li>...&lt;/li> &lt;/ol> |
| Code | &lt;code>...&lt;/code> |


+++

## Integrationsregeln

Ein Objekt gilt als in einen Rahmen eingeschlossen, wenn es seine Einschlussregel erfüllt. Diese Regeln variieren je nach Objekt und Sonderfall. Sie sind unten aufgeführt.

Das gelbe Symbol in jeder Abbildung stellt den Punkt oder Bereich dar, der vollständig innerhalb der Grenzen eines Rahmens liegen muss, damit ein Objekt in diesen Rahmen aufgenommen werden kann.

+++Knoten
Der <b>Mittelpunkt</b> wird verwendet.

Abzeichen, Verbindungen und Informationen, die unter dem Knoten angezeigt werden, werden alle ignoriert.

Die Knoten können je nach Anzahl der Ein- oder Ausgangsanschlüsse unterschiedliche Height aufweisen.

Wenn Connectors angezeigt oder ausgeblendet, hinzugefügt oder entfernt werden, wird das Height des Knotens vom *Center* aus angepasst.

Daher sollte sich die Position des Mittelpunkts eines Knotens erst ändern, wenn er *absichtlich verschoben wurde*.

![Frame-Einbindung: hohe Knoten](frame.resources/frame-14.png "Frame-Einbindung: hohe Knoten")



Der <b>c</b><b>Einstiegspunkt</b> des *Host*-Knotens wird verwendet.

Der Hostknoten ist der Knoten, an den ein Knoten angedockt ist.

Wenn mehrere Knoten in einer Kette angedockt sind, wird der Hostknoten des letzten angedockten Knotens für die gesamte Kette verwendet.

Abzeichen, Verbindungen und Informationen, die unter dem Knoten angezeigt werden, werden alle ignoriert.

![Frame-Einbindung: angedockte Knoten](frame.resources/frame-15.png "Frame-Einbindung: angedockte Knoten")



![Frame-Einbindung: node](frame.resources/frame-16.png "Frame-Einbindung: nodes")



+++

+++Punktknoten
Der <b>Mittelpunkt</b> des Punkts wird verwendet.

Connectors, Portalsymbole und Namen werden ignoriert.

![Frame-Einbindung: Punktknoten](frame.resources/frame-17.png "Frame-Einbindung: Punktknoten")



+++

+++Kommentare
Der <b>Mittelpunkt</b> des *Begrenzungsrahmens* des Kommentars (gelbe Kontur) wird verwendet.

Übergeordnete Kommentare folgen nicht den Einschlussregeln für Kommentare.

Stattdessen wird der <b>Mittelpunkt</b> des *übergeordneten*-Knotens verwendet.

Abzeichen, Verbindungen und Informationen, die unter dem Knoten angezeigt werden, werden alle ignoriert.



![Frame-Einbindung: übergeordnete Kommentare](frame.resources/frame-18.png "Frame-Einbindung: übergeordnete Kommentare")



![Frame-Einbindung: comments](frame.resources/frame-19.png "Frame-Einbindung: Kommentare")



+++

+++Pins
Der <b>Tipp</b> des Pin-Symbols wird verwendet.

![Frame-Einbindung: Navigationsstifte](frame.resources/frame-20.png "Rahmeneinbindung: Navigationsstifte")



+++

+++Rahmen
Der <b>Begrenzungsrahmen</b> des verschachtelten Rahmens wird verwendet.

Das bedeutet, dass ein verschachtelter Frame vollständig innerhalb der Grenzen eines anderen Frames liegen muss, um in diesen Frame aufgenommen zu werden.

Der Titel wird ignoriert.

![Frame-Einbindung: geschachtelte Frames](frame.resources/frame-21.png "Frame-Einbindung: geschachtelte Frames")



+++

## Größe an Inhalt anpassen

![Frames: Größe an Inhalt anpassen](frame.resources/frame-22.png "Bilder: Größe an Inhalt anpassen")

Wenn du in deinem Diagramm Anpassungen vornimmst, wird ein Frame möglicherweise nicht mehr elegant an seinen Inhalt angepasst. In diesem Fall ist es möglich, die Position und die Größe des Rahmens automatisch so anzupassen, dass er sich an die Spanne seines Inhalts anpasst, mit einer Auffüllung von einer Zelle mit mittlerem Raster.

Klicken Sie dazu auf <b>RMB</b> in der Titel- oder Kopfzeile des Rahmens - siehe [Darstellung](#appearance) - und wählen Sie im Kontextmenü die Option <b>Größe an Inhalt anpassen</b>.

>[!NOTE]
>
> Die Option ist verfügbar, wenn mindestens *ein* Graf-Objekt die [Einschlussregeln](../../../../interface/the-graph-view/graph-items/frame/frame.md) des Rahmens erfüllt.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Einpassen des Beschreibungstextes

Wenn der Rahmen eine Beschreibung hat, wird die zugehörige Spalte so angepasst, dass nach Möglichkeit ein leerer Bereich neben der Beschreibung verwendet wird.

Wenn kein eingeschlossenes Objekt in diesen Bereich passt, wird das Height des Rahmens entsprechend angepasst.

</td>
<td style="border: 0;" valign="top">

![Frames: Größe an Inhalt anpassen (mit Beschreibung)](frame.resources/frame-23.png "Rahmen: Größe an Inhalt anpassen (mit Beschreibung)")

</td>
</tr>
</table>

+++Beispiel
![Frames: Größe an Inhalt anpassen (GIF)](frame.resources/frame-24.gif "Rahmen: Größe an Inhalt anpassen (GIF)"){width="640px"}



+++

## Automatisch erweitern

![Frames: Automatisch erweitern](frame.resources/frame-25.png "Rahmen: Automatische Erweiterung")

Wenn das Diagramm wächst, muss der Inhalt der Rahmen möglicherweise neu angeordnet werden. Die Knoten können sich verschieben, um Platz für Ergänzungen zu schaffen, oder die Inhalte müssen möglicherweise weiter voneinander entfernt werden, um die Lesbarkeit zu verbessern.

Um diese Anpassungen zu erleichtern, ist es möglich, einen Rahmen automatisch zu erweitern, wenn [eingeschlossene Objekte](#inclusion-rules) verschoben werden: Halten Sie <b>Umschalt</b> an einem beliebigen Punkt gedrückt, während Sie ein Objekt verschieben, damit die Begrenzungen des Rahmens automatisch angepasst werden, damit das Objekt innerhalb seiner Begrenzungen bleibt.

Dies gilt auch für Auswahlen, die mehrere Objekte enthalten können. In diesem Fall wird der Host-Rahmen jedes Objekts gleichzeitig angepasst.

Wenn ein Objekt nicht vollständig von den Begrenzungen des Rahmens umschlossen ist, aber trotzdem seine [Einschlussregel](#inclusion-rules) erfüllt, wird der Rahmen so angepasst, dass er es vollständig mit einer zusätzlichen Auffüllung von einer Mediumzelle umschließt, sobald die <b>Umschalttaste</b> gedrückt wird, sobald der Raster die --Taste gedrückt hat.

>[!NOTE]
>
> Während die Taste <b>Umschalt</b> während des Verschiebens gedrückt oder losgelassen werden kann, um die automatische Korrektur des Rahmens auszulösen oder abzubrechen, muss sie *gedrückt werden*, wenn der Vorgang abgeschlossen ist, um die Korrektur effektiv anzuwenden.

+++Beispiel
![Frames: Automatisch erweitern (GIF)](frame.resources/frame-26.gif "Rahmen: Automatisch erweitern (GIF)"){width="640px"}



+++

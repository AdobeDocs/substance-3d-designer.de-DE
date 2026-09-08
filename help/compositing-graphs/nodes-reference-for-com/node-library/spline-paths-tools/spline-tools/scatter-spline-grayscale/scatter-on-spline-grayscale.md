---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie die Streuung des Knotens "Spline Grayscale", um Graustufenelemente für prozedurale Muster entlang von Spline-Pfaden zu verteilen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Streuung in Spline Grayscale
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '2853'
ht-degree: 0%

---


# Streuung in Spline Grayscale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/scatter-on-spline-grayscale-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet die angegebenen Muster entlang der Eingabe-Splines über dem Eingabehintergrund.

</td>
</tr>
</table>

Der Knoten bietet umfassende Anpassungsoptionen für die Steuerung der Streuung von Mustern.

Einige Aspekte der Streuung können mithilfe von Bildern von anderen Knoten im Diagramm gesteuert werden, um den dynamischen Aspekt des Ergebnisses zu fördern.

>[!NOTE]
>
> Siehe auch [Streuung für Spline-Farbe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrund</b> <i>Graustufen</i> (primär) | Das Graustufenbild, über das Splines gezeichnet werden sollen. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |
| <b>Mustereingabe #</b> <i>Graustufen</i> | Die Muster, die entlang der Splines gestreut werden sollen. |
| <b>Zuordnungsskalierung</b> <i>Graustufen</i> | Die Karte, die den Maßstab der gestreuten Muster steuert. Der Effekt dieser Karte wird durch den Parameter &#39;Scale Map Input Multiplier&#39; gesteuert und mit den anderen Parametern in der Gruppe &#39;Size&#39; kombiniert. |
| <b>Height-Map</b> <i>Graustufen</i> | Die Karte, die das Height der Streumuster steuert. Die Wirkung dieser Map wird durch den Parameter &#39;Height Input Multiplier&#39; gesteuert und mit den anderen &#39;Color&#39; Parametern in der Gruppe &#39;Color&#39; kombiniert. |
| <b>Maskenzuordnung</b> <i>Graustufen</i> | Die Karte, die die Maskierung der verstreuten Muster steuert. Der Effekt dieser Karte wird durch den Parameter &quot;Schwellenwert der Maskenzuordnung&quot; gesteuert und mit den anderen Parametern &quot;Maske&quot; in der Gruppe &quot;Farbe&quot; kombiniert. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Bild, das die Muster darstellt, die entlang der Eingabe-Spline(s) über dem Eingabehintergrund gestreut sind. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Spline-Eingabe</b> <i>Integer</i> | Die Methode zur Auswahl der Splines, die für Streuungsmuster verwendet werden sollen:<br><br>- <i>Alle Splines</i>: Alle Splines in der Eingabeliste verwenden;<br>- <i>Einzelne Spline</i>: Verwenden Sie nur den angegebenen Spline aus der Eingabeliste;<br>- <i>Spline Range</i>: Verwenden Sie nur die Splines im angegebenen Bereich aus der Eingabeliste. |
| <b>Spline-Index</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Spline-Eingabe&quot; auf &quot;Einzelne Spline&quot; festgelegt ist) | Der Listenindex des Splines, der für Streuungsmuster verwendet werden soll. |
| <b>Spline-Bereich</b> <i>Ganzzahl2</i> (verfügbar, wenn &quot;Spline-Eingabe&quot; auf &quot;Spline-Bereich&quot; festgelegt ist) | Der Bereich der Listenindizes, einschließlich der Splines, die für Streuungsmuster verwendet werden sollen. |
| <b>Streuung-Modus</b> <i>Integer</i> | Die Methode zum Streuen der Muster entlang der Splines, die sich auf die Anzahl der Muster auf jedem Spline auswirkt:<br><br>- Shape Amount: Die angegebene Anzahl von gleichmäßig verteilten Mustern ist gestreut;<br>- Shape-Abstand: Die Anzahl der Muster wird automatisch an den angegebenen gleichmäßigen Abstand angepasst.<br><br>In beiden Fällen fallen das erste und das letzte Muster genau auf den Anfang bzw. das Ende jedes Splines. |
| <b>Betrag der Form</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Streuung-Modus&quot; auf &quot;Shape-Stärke&quot; festgelegt ist) | Die Anzahl der gleichmäßig beabstandeten Muster, die entlang jeder Spline verstreut sind. |
| <b>Formverteilung entlang Spline</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Streuung-Modus&quot; auf &quot;Shape-Stärke&quot; festgelegt ist) | Die Methode zum Verteilen der Muster entlang eines Splines: <br><br>- <i>Von Quelle</i>: Der Abstand der Muster wird durch die Tangenten des Spline-Punkts beeinflusst, bei denen Formen weiter auseinander liegen in der Nähe von Punkten mit langen Tangenten;<br>- <i>Uniform</i>: Die Muster werden entlang der Spline gleichmäßig verteilt, unabhängig von ihren Tangenten und ihrer Flugbahn. |
| <b>Formabstand</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Streuung-Modus&quot; auf &quot;Shape-Abstand&quot; festgelegt ist) | Der minimale Abstand entlang einer Spline, um den Muster beabstandet sein sollten, während das erste und das letzte Muster noch am Anfang bzw. Ende jeder Spline landen. |
| <b>Start</b> <i>Gleitend</i> | <span id="_Hlk135680521"></span>Verschiebt den Punkt vom Anfang eines Splines an dem die Streuung beginnt. Der Wert ist die normalisierte Länge jedes Splines. |
| <b>Ende</b> <i>Gleitend</i> | Versetzt den Punkt vom Anfang eines Spline-Effekts an den Punkt, an dem die Streuung endet. Der Wert ist die normalisierte Länge jedes Splines. |
| <b>Form-Pivot</b> <i>Float2</i> | Verschiebt den Drehpunkt des Musters X und Y in der Tangente der Spline.<br>Wenn man bedenkt, dass der Drehpunkt auf dem Spline platziert ist, verschiebt dies die Muster effektiv entlang oder senkrecht zum Spline.<br>Hinweis: Die Positionen der Drehpunkte wirken sich auf die Auswirkungen der Parameter &quot;Skalierung&quot; und &quot;Drehung (Pivot)&quot; aus. |
| <b>Muster</b> |  |
| <b>Muster</b> <i>Integer</i> | Das Muster, das entlang der Splines gestreut werden soll:<br><br>- <i>Mustereingabe</i>: Verwenden Sie die Muster, die an die Eingaben von &quot;Pattern Input #&quot; übergeben werden;<br>- Square;<br>- Disk;<br>- Paraboloid;<br>- Bell;<br>- Gaussian;<br>- Dorn;<br>- Pyramide;<br>- Ziegel;<br>- Abstufung;<br>- Waves;<br>- Halbglocke;<br>- Rändelglocke;<br>- Mondsichel;<br>- Kapsel;<br> - Kegel;<br>- Abstufung w. offset;<br>- Hemisphäre. |
| <b>Mustereingabenummer</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Pattern&quot; auf &quot;Pattern-Eingabe&quot; festgelegt ist) | Wählt den Index des Eingabemusters aus, der gestreut werden soll. |
| <b>Mustereingabeverteilung</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Pattern&quot; auf &quot;Pattern-Eingabe&quot; festgelegt ist) | Die Methode, mit der ausgewählt wird, welches der Eingabemuster auf einem angegebenen Spline gestreut werden soll:<br><br>- <i>Zufällig</i>: Ein Muster wird zufällig ausgewählt;<br>- <i>Entlang Spline</i>: Der Musterindex nimmt entlang des Splines allmählich zu;<br>- <i>Musterindex</i>: Schleifen über den Index der Eingabemuster entlang jedem Spline;<br>- <i>Spline-Index</i>: Der Index der Eingabemuster wird in der Liste der Eingabesplines von einem Spline zum nächsten durchlaufen. |
| <b>Verteilungs-Jittering</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Pattern Input Distribution&quot; auf &quot;Along Spline&quot; festgelegt ist) | Erhöht oder verringert den ausgewählten Index von Mustern auf dem Spline nach dem Zufallsprinzip. |
| <b>Erstes Muster überschreiben</b> <i>Boolescher Wert</i> | Wählen Sie manuell den Index des Musters aus, das am Anfang jedes Splines platziert werden soll. |
| <b>Erster Mustereingabeindex</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Erstes Muster überschreiben&quot; auf &quot;Wahr&quot; festgelegt ist) | Der Index des Musters, das am Anfang jedes Splines platziert werden soll. |
| <b>Letztes Muster überschreiben</b> <i>Boolescher Wert</i> | Wählen Sie manuell den Index des Musters aus, das am Ende jedes Splines platziert werden soll. |
| <b>Letzter Mustereingabeindex</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Letztes Muster überschreiben&quot; auf &quot;Wahr&quot; festgelegt ist) | Der Index des Musters, das am Ende jedes Splines platziert werden soll. |
| <b>Duplikate</b> |  |
| <b>Verteilungsmodus</b> <i>Integer</i> | Die zum Platzieren der duplizierten Muster verwendete Methode:<br><br>- <i>Linear</i>: Duplikate werden entlang der Spline-Normalen gleichmäßig von der ursprünglichen Position des Musters beabstandet;<br>- <i>Circular</i>: dupliziert werden, werden entlang eines virtuellen Kreises angeordnet, der auf der Spline an der ursprünglichen Position des Musters zentriert ist. |
| <b>Anzahl der Duplikate</b> <i>Integer</i> | Die Anzahl der duplizierten Muster. |
| <b>Offset</b> <i>Fließkommazahl2</i> (verfügbar, wenn der Verteilungsmodus auf &quot;Linear&quot; festgelegt ist) | Wendet einen Versatz auf die Duplikatpositionen entlang der Spline-Tangente (parallel) und der Senkrechten (senkrecht) an.<br>Duplikate auf gegenüberliegenden Spline-Seiten werden in entgegengesetzte Richtungen verschoben. |
| <b>Offset-Center</b> <i>Fließkommazahl2</i> (verfügbar, wenn der Verteilungsmodus auf &quot;Linear&quot; festgelegt ist) | Wendet einen Versatz auf die Duplikate entlang der Spline auf X (parallel) und Y (senkrecht) an. |
| <b>Spread Angle</b> <i>Fließkommazahl</i> (verfügbar, wenn der Verteilungsmodus auf &quot;Zirkular&quot; festgelegt ist) | Der Bogen des virtuellen Kreises, entlang dem Duplikate verteilt sind, wie der Winkel dieses Bogens, wobei 1 der volle Kreis ist. |
| <b>Offset-Abstand</b> <i>Fließkommazahl</i> (verfügbar, wenn der Verteilungsmodus auf &quot;Zirkular&quot; festgelegt ist) | Der Radius des virtuellen Kreises, entlang dem Duplikate verteilt werden. |
| <b>Drehung</b> <i>Gleitend</i> | Dreht den virtuellen Kreis, entlang dem Duplikate verteilt werden. |
| <b>Startdämpfung/Enddämpfung versetzen</b> <i>Float2</i> | Klammert den Abstand zwischen dem Mittelpunkt des Spline-Effekts und seinen Anfangs- und Endpunkten aus, wenn Versätze auf Duplikate angewendet werden.<br>Dies bedeutet, dass die Abstände für Duplikate verringert werden, die sich näher an den Enden eines Splines befinden. |
| <b>Versatzdämpfung durch Thickness</b> <i>Gleitend</i> | Faktoren in der Thickness des Splines, wenn Versätze auf Duplikate angewendet werden.<br>Dies bedeutet, dass die Abstände für Duplikate auf einem Abschnitt eines Splines mit einer niedrigeren Thickness verringert werden. |
| <b>Größe</b> |  |
| <b>Größenmodus</b> <i>Integer</i> | Die Methode zum Festlegen der Größe der gestreuten Muster:<br><br>- <i>Normal</i>: Die Größe wird mithilfe des globalen Parameters &quot;Skalierung&quot; einheitlich gesteuert;<br>- <i>Thickness aus Spline verwenden</i>: Die Größe hängt von der Thickness des Splines ab. |
| <b>Auswirkungen der Thickness</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Größenmodus&quot; auf &quot;Thickness aus Spline verwenden&quot; festgelegt ist) | Gibt an, welche Achse der Skalierung eines Musters von der Spline-Thickness gesteuert werden soll: <br><br>- X &amp; Y: Die Thickness wird mit der Größe in der X- und Y-Achse multipliziert;<br>- <span id="_Hlk135741125"></span>X: Die Thickness wird nur mit der Größe auf der X-Achse multipliziert;<br>- Y: Die Thickness wird nur mit der Größe der Y-Achse multipliziert.<br><br>Wenn sie nicht multipliziert wird, ist die Originalskala des Musters die gesamte Bildspanne.<br>Dies bedeutet, dass im X-Modus die Größe in der Y-Achse die gesamte Bildspanne ist und mit dem Parameter &quot;Größe&quot; angepasst werden muss. Dasselbe gilt für die Größe in der X-Achse, wenn der Y-Modus verwendet wird. |
| <b>Größe</b> <i>Float2</i> | Die ursprüngliche Größe von Mustern in X und Y, bevor andere Anpassungen durch andere Parameter vorgenommen werden. |
| <b>Größe zufällig</b> <i>Float2</i> | Wendet einen Zufallsmultiplikator bis zum angegebenen Wert an, um die Größe der Muster in X und Y zu verringern. |
| <b>Skalierung der Thickness</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Größenmodus&quot; auf &quot;Thickness aus Spline verwenden&quot; festgelegt ist) | Ein zusätzlicher Multiplikator für die Skalierung der Muster, wenn sie durch die Thickness des Splines gesteuert wird. |
| <b>Skalierung</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Größenmodus&quot; auf &quot;Normal&quot; festgelegt ist) | Eine globale Steuerung für die Größe aller Muster, wobei 1 die gesamte Bildspanne ist.<br>Die Skalierung wird relativ zum Pivot eines Musters angewendet. Die Pivot-Position kann mit dem Parameter &#39;Shape Pivot&#39; versetzt werden. |
| <b>Zufällige Skalierung</b> <i>Gleitend</i> | Wendet einen Zufallsmultiplikator bis zum angegebenen Wert an, um die Größe der Muster zu verringern. |
| <b>Zuordnungseingabemultiplikator skalieren</b> <i>Gleitend</i> | Steuert die Intensität des Scale Map-Eingangs. Diese Karte dient als Multiplikator für die aktuelle Größe der Muster.<br>Der Effekt dieser Karte wird mit den anderen Parametern in der Gruppe &quot;Größe&quot; kombiniert. |
| <b>Sampling-Eingabemodus für Skalierung</b> <i>Textur-Speicherplatz</i> | Die Methode zum Zuordnen der Werte in der Skalierungszuordnung zu den Splines:<br><br>- <i>Texturen-Leerzeichen</i>: Die Werte werden auf die Splines angewendet, wo sie sich befinden würden, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;in place&quot;;<br>- <i>Horizontal entlang Spline</i> angewendet: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird;<br>- <i>Hor. entlang der Spline (Rand). Versatz X)</i>: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Coords);<br>- <i>Hor. entlang der Spline (Rand). Offset Y)</i>: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird. |
| <b>Dämpfung starten/beenden</b> <i>Float2</i> | Klammert beim Skalieren der Muster den Abstand zwischen dem Mittelpunkt des Spline-Effekts und seinem Anfang und Ende aus.<br>Dies bedeutet, dass die Größe für Muster, die sich den Extremitäten eines Splines nähern, verringert wird. |
| <b>Position</b> |  |
| <b>Lokaler Offset</b> <i>Float2</i> | Wendet einen Versatz auf die Positionen der Muster entlang der Tangente des Splines (parallel) und der Normale (senkrecht) an. |
| <b>Lokaler Versatz zufällig</b> <i>Float2</i> | Wendet einen zusätzlichen zufälligen Versatz auf die Positionen der Muster entlang der Spline-Tangente (parallel) und -Normale (senkrecht) an. |
| <b>Lokaler Versatz zufälliger Mittelpunkt</b> <i>Float2</i> | Verschiebt den Mittelpunkt des zufälligen Versatzes, der durch den Parameter Lokaler Versatz zufällig entlang der Tangente (parallel) und Normal (senkrecht) des Splines angewendet wird. |
| <b>Dämpfung für lokalen Versatz Start/Ende</b> <i>Float2</i> | Klammert den Abstand zwischen dem Mittelpunkt des Spline-Effekts und seinem Anfang und Ende aus, wenn Positionsoffsets auf die Muster angewendet werden.<br>Dies bedeutet, dass die Abstände bei Mustern, die sich näher an den Enden eines Splines befinden, verringert werden. |
| <b>Dämpfung des lokalen Offsets durch Thickness</b> <i>Gleitend</i> | Faktoren in der Thickness des Splines, wenn Versätze auf Muster angewendet werden.<br>Dies bedeutet, dass die Abstände für Duplikate auf einem Abschnitt eines Splines mit einer niedrigeren Thickness verringert werden. |
| <b>Offset auf Spline</b> <i>Gleitend</i> | Wendet einen Positionsversatz auf die Muster entlang der Splines an. |
| <b>Zufälliger Versatz auf Spline</b> <i>Gleitend</i> | Wendet einen zusätzlichen Positionsversatz auf die Muster entlang der Splines an. |
| <b>Drehung</b> |  |
| <b>An Tangente ausrichten</b> <i>Boolescher Wert</i> | Dreht die Muster entsprechend der Richtung des Spline-Effekts an ihrer Position. |
| <b>Drehung (Pivot)</b> <i>Gleitend</i> | Dreht die Muster um ihren Drehpunkt.<br>Die Pivot-Position kann mit dem Parameter &#39;Shape Pivot&#39; versetzt werden. |
| <b>Drehung zufällig (Pivot)</b> <i>Gleitend</i> | Wendet eine zusätzliche zufällige Drehung auf die Muster um ihre Drehpunkte an.<br>Die Pivot-Position kann mit dem Parameter &#39;Shape Pivot&#39; versetzt werden. |
| <b>Drehungszufallszentrum (Pivot)</b> <i>Gleitend</i> | Dreht sich um die Achse des Musters und schwenkt den Mittelpunkt der zufälligen Drehungen, die durch den Parameter &quot;Drehung zufällig&quot; angewendet werden. |
| <b>Drehung (Mitte)</b> <i>Gleitend</i> | Dreht die Muster um ihren Mittelpunkt. |
| <b>Drehung zufällig (Mitte)</b> <i>Gleitend</i> | Wendet eine zusätzliche zufällige Drehung auf die Muster um ihren Mittelpunkt an. |
| <b>Drehungszufallszentrum (Mitte)</b> <i>Gleitend</i> | Dreht sich um die Mitte des Musters und um den Mittelpunkt der zufälligen Drehungen, die mit dem Parameter &quot;Drehung zufällig&quot; angewendet werden. |
| <b>Farbe</b> |  |
| <b>Füllmethode</b> <i>Integer</i> | Die Methode zum Mischen der Farben von Mustern mit dem Hintergrund und anderen überlappenden Mustern: <br><br>- <i>Max</i>: Die hellste Farbe verwenden;<br>- <i>Hinzufügen</i>: Füge die Farben zusammen. |
| <b>Form-Grundfarbe</b> <i>Gleitend</i> | Die Grundfarbe der Muster. |
| <b>Farbmultiplikator der Grundform</b> <i>Gleitend</i> | Die Intensität der Shape-Grundfarbe der Muster.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Spline-Thickness-Multiplikator</b> <i>Gleitend</i> | Die Intensität, mit der die Farbe jedes Musters mit der Thickness des Splines an seiner Position multipliziert wird.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Formindexmultiplikator</b> <i>Gleitend</i> | Die Intensität, mit der die Farbe jedes Musters mit seinem normalisierten Index multipliziert wird.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Hemisphere Height-Modus</b> <i>Ganzzahl</i> (verfügbar, wenn &quot;Pattern&quot; auf &quot;Hemisphere&quot; festgelegt ist) | Die Auswirkung des Spline-Heights auf ein darauf verstreutes Hemisphärenmuster:<br><br>- <i>Offset</i>: Das Spline-Height wird dem Height der Hemisphäre hinzugefügt;<br>- <i>Skalierung</i>: das Spline-Height wird mit dem Height der Hemisphäre multipliziert. |
| <b>Spline-Height-Multiplikator</b> <i>Gleitend</i> | Die Intensität, mit der die Farbe jedes Musters mit dem Height des Splines an seiner Position multipliziert wird.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Formskalierungsmultiplikator</b> <i>Gleitend</i> | Die Intensität, mit der die Farbe jedes Musters mit der Skala multipliziert wird.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Zufällige Luminanz</b> <i>Gleitend</i> | Wendet einen zufälligen Multiplikator bis zum angegebenen Wert an, um die Luminanz der Muster zu verringern.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Height-Eingangsmultiplikator</b> <i>Gleitend</i> | Steuert die Intensität des Höhen-Map-Eingangs. Diese Karte dient als Multiplikator für die aktuelle Luminanz der Muster.<br>Der Effekt dieser Karte wird mit den anderen Parametern in der Gruppe &quot;Farbe&quot; kombiniert.<br>Hinweis: Die Ausgangsfarbe ist das gewichtete Ergebnis aller Farbmultiplikatoren. |
| <b>Sampling-Modus für Height-Zuordnungseingabe</b> <i>Integer</i> | Die Methode zum Zuordnen der Werte auf der Höhen-Map zu den Splines:<br><br>- <i>Texturen-Leerzeichen</i>: Die Werte werden auf die Splines angewendet, wo sie sich befinden würden, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;in place&quot;;<br>- <i>Horizontal entlang Spline</i> angewendet: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird;<br>- <i>Hor. entlang der Spline (Rand). Versatz X)</i>: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Coords);<br>- <i>Hor. entlang der Spline (Rand). Offset Y)</i>: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird. |
| <b>Zufällige Maske</b> <i>Gleitend</i> | Passt den Bereich der zufälligen Maskierung von Mustern an, wobei 0 bedeutet, dass keine Muster maskiert werden und 1 bedeutet, dass alle Muster maskiert werden. |
| <b>Schwellenwert für Maskenzuordnung</b> <i>Gleitend</i> | Werte in der Maskenübersicht unterhalb dieses Schwellenwerts werden schwarz verarbeitet, Werte oberhalb des Schwellenwerts werden weiß verarbeitet.<br>Dies bedeutet, dass alle Muster in Bereichen der Maskenkarte unter diesem Wert maskiert werden. |
| <b>Maskenzuordnungs-Eingabeaufnahmemodus</b> <i>Integer</i> | Die Methode zum Zuordnen der Werte in der Maskenzuordnung zu den Splines:<br><br>- <i>Texturen-Leerzeichen</i>: Die Werte werden auf die Splines angewendet, wo sie sich befinden würden, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;in place&quot;;<br>- <i>Horizontal entlang Spline</i> angewendet: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird;<br>- <i>Hor. entlang der Spline (Rand). Versatz X)</i>: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Coords);<br>- <i>Hor. entlang der Spline (Rand). Offset Y)</i>: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird. |
| <b>Maskenzuordnung umkehren</b> <i>Boolescher Wert</i> | Kehrt die Werte der Maskenzuordnung mit einem Vorgang von &quot;Eins minus&quot; um (1 - x). |
| <b>Maske umkehren</b> <i>Boolescher Wert</i> | Kehrt die Maskierung der Muster um. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Positionen der Punkte an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGrayscale-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-After.jpg" alt="ScatterOnSplineGrayscale-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGrayscale-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-After.jpg" alt="ScatterOnSplineGrayscale-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo.gif "Knotenbeispiel 2")

</td>
<td style="border: 0;" valign="top">

![Knotendemo 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo2.gif "Knotendemo 2")

</td>
</tr>
</table>

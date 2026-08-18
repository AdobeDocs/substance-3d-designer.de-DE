---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-splines-on-splines.html"
breadcrumb-title: ''
description: Verteilen Sie untergeordnete Splines entlang übergeordneter Spline-Pfade mithilfe des Knotens Splines in Streuungen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter Splines on Splines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Streuung Splines on Splines
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '2840'
ht-degree: 0%

---


# Streuung Splines on Splines

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Streuung-Splines auf Splines: Symbol ](../../../../../../assets/scatter-splines-on-splines-icon.png "Streuung-Splines auf Splines: Symbol ")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Platziert Splines entlang der übergeordneten Splines für die Eingabe.

Der Node bietet umfassende Anpassungsoptionen, mit denen Sie die Streuung von Splines steuern und einfache, gerade Splines oder eigene benutzerdefinierte Splines in der Streuung verwenden können.

Mithilfe des Knotens können Sie komplexe Strukturen für das Zuordnen von Farben und Bildern mithilfe der Knoten [Spline Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md) oder als Skelett für das Platzieren von Formen mithilfe der Streuung [auf den Knoten Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md) erstellen.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Tutorial

Klicken Sie auf das Bild auf der rechten Seite, um auf unser <b>Tutorial </b> zuzugreifen. Dort erhalten Sie eine Einführung in die Funktionen des Knotens und seine Verwendung im Rahmen eines Spline-basierten Workflows.

</td>
<td style="border: 0;" valign="top">

[![Video-Spline-Knoten](../../../../../../assets/video_spline.png)](https://youtu.be/aUUWV1dYQdI)

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Vorschau</b> *Graustufen* | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> *Farbe* | Die Koordinaten der Punkte der übergeordneten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - X-Position <b>G</b> - Y-Position <b>B</b> - Height <b>A</b> - Packed data:          - Signieren: Spline ist geschlossen (negativ) oder offen (positiv) - Absoluter Wert: THICKNESS + 1 |
| <b>Spline-Daten</b> *Farbe* | Zusätzliche Daten der übergeordneten Splines, die in den RGBA-Kanälen eines Farbbilds codiert sind:  <b>R</b> - Tangenten X <b>G</b> - Tangenten Y <b>B</b> - Tangenten Z <b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> *Integer* | Die Anzahl der übergeordneten Splines. |
| <b>Benutzerdefinierte Spline-Codes</b> *Farbe* | Die Koordinaten der Punkte der benutzerdefinierten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - X-Position <b>G</b> - Y-Position <b>B</b> - Height <b>A</b> - Packed data:          - Signieren: Spline ist geschlossen (negativ) oder offen (positiv) - Absoluter Wert: THICKNESS + 1 |
| <b>Benutzerdefinierte Spline-Daten</b> *Farbe* | Zusätzliche Daten zu den benutzerdefinierten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - Tangenten X <b>G</b> - Tangenten Y <b>B</b> - Tangenten Z <b>A</b> - Nicht verwendet |
| <b>Benutzerdefinierter Spline-Betrag</b> *Integer* | Die Anzahl der benutzerdefinierten Splines. |
| <b>Zuordnungsskalierung</b> *Graustufen* | Die Graustufen-Map, die die Skalierung der gestreuten Splines steuert.  Der Effekt dieser Karte wird durch den <b>Scale Map Input Multiplier</b>-Parameter gesteuert und mit den anderen Parametern in der <b>Size</b>-Gruppe kombiniert. |
| <b>Rotation Map</b> *Graustufen* | Die Graustufenkarte, die die Drehung der gestreuten Splines steuert.  Die Wirkung dieser Map wird durch den <b>Rotation Map-Eingabemultiplikator</b>-Parameter gesteuert und mit den anderen Parametern in der <b>Drehung</b>-Gruppe kombiniert. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Vorschau</b> *Graustufen* | Die Vorschau der verstreuten Splines als Graustufenbild. |
| <b>Spline-Kabel</b> *Farbe* | Die Koordinaten der Punkte der gestreuten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - X-Position <b>G</b> - Y-Position <b>B</b> - Height <b>A</b> - Packed data:          - Signieren: Spline ist geschlossen (negativ) oder offen (positiv) - Absoluter Wert: THICKNESS + 1 |
| <b>Spline-Daten</b> *Farbe* | Zusätzliche Daten zu den gestreuten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - Tangenten X <b>G</b> - Tangenten Y <b>B</b> - Nicht verwendet <b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> *Integer* | Die Anzahl der verstreuten Splines. |

## Parameter

|  |  |
| --- | --- |
| <b>Seite</b> *Integer* | Steuert, auf welcher Seite(n) der übergeordneten Splines die Splines gestreut werden sollen, da &quot;vorwärts&quot; die Richtung der *übergeordneten* Splines ist:   Links Platzieren Sie die Splines auf der linken Seite.   Rechts Platzieren Sie die Splines auf der rechten Seite.   Links + Rechts Platzieren Sie die Splines auf beiden Seiten.   Links/Rechts - Alternativer Spline-Verlauf links und dann rechts alternativ (z. B. jede andere Seite).   Links/Rechts - Zufällig Wählen Sie die Seite zufällig für jeden Spline aus. |
| <b>Betragsmodus</b> *Integer* | Die Methode zum Streuen der Splines entlang der übergeordneten Splines, die sich auf die Anzahl der gestreuten Splines auf jedem übergeordneten Spline auswirkt:   Feste Menge pro Spline Die angegebene Menge an gleichmäßig beabstandeten Splines wird gestreut.   Abstand Die Stärke der Splines wird automatisch an den angegebenen gleichmäßigen Abstand angepasst.   In beiden Fällen liegen der erste und der letzte gestreute Spline genau am Anfang bzw. Ende jedes übergeordneten Splines. |
| <b>Spline-Betrag pro Spline</b> *Integer* | Die Anzahl der gleichmäßig beabstandeten Splines, die entlang jeder übergeordneten Spline verstreut sind. |
| <b>Spline-Abstand</b> *Gleitend* | Der Mindestabstand entlang übergeordneter Splines, um den Splines ein Abstand zueinander gesetzt werden sollen, während der erste und der letzte Spline noch am Anfang bzw. Ende jedes übergeordneten Splines landen. |
| <b>Spline-Typ</b> *Integer* | Legt fest, welcher Spline-Typ auf den übergeordneten Splines gestreut werden soll:   Gerade Eine einfache, gerade Spline.   Benutzerdefinierter Spline Der Spline bzw. die Splines, die für die <b>Benutzerdefinierter Spline</b>-Eingaben bereitgestellt wurden. Mehrere Splines werden unterstützt, wenn sie zusammen an eine Liste angehängt werden. |
| <b>Benutzerdefinierte Spline-Auswahl</b> *Integer* | Wenn Sie mehrere benutzerdefinierte Splines verwenden, die an eine Liste angehängt sind, können Sie mit diesem Parameter auswählen, wie diese Splines in der Streuung verteilt werden sollen.   Gesamte Liste Alle Splines werden als Gruppe verstreut.   Sequenziell Jeder einzelne Spline wird in der Reihenfolge gestreut und in einer Schleife um die Liste herum angeordnet.   Zufällig Ein zufälliger Spline wird für jeden Spline, der verstreut ist, aus der Liste ausgewählt. |
| <b>Start</b> *Gleitend* | Versetzt den Punkt vom Anfang der übergeordneten Splines an die Stelle, an der die Streuung beginnt.  Der Wert ist die normalisierte Länge jedes übergeordneten Splines. |
| <b>Ende</b> *Gleitend* | Verschiebt den Punkt vom Anfang der übergeordneten Splines an der Stelle, an der die Streuung endet.  Der Wert ist die normalisierte Länge jedes übergeordneten Splines. |
| <b>Richtung spiegeln</b> *Boolescher Wert* | Kehrt die Richtung der gestreuten Splines um. |
| <b>Symmetriemodus links/rechts</b> *Integer* | Die Symmetriemethode, die auf die Splines angewendet wird, die auf jeder Seite der übergeordneten Splines gestreut sind.   Deaktiviert Es wird keine Symmetrie angewendet, die Splines werden auf jeder Seite durch eine einfache Drehung platziert.   Linkssymmetrie Der Spline auf der linken Seite ist symmetrisch zum Spline auf der rechten Seite relativ zum Elternspline.   Rechtssymmetrie Der Spline auf der rechten Seite ist symmetrisch zum Spline auf der linken Seite relativ zum Elternspline. |
| <b>Links/Rechts zufälliger Link</b> *Boolescher Wert* | Steuert, ob die Splines auf jeder Seite des übergeordneten Splines die gleichen Werte verwenden sollen, wenn zufällige Drehung, zufällige Skalierung usw. verwendet werden. Mit anderen Worten:   *- Falsch:* Jeder Spline verwendet separate zufällige Werte *- Wahr:* Beide Splines verwenden dieselben zufälligen Werte. |
| <b>Spline-Pivot-Modus</b> *Integer* | Legt die Methode zum Platzieren des Drehpunkts für gestreute Splines fest, der sich auf die Drehung und Skalierung auswirkt.   Beachten Sie, dass der Pivot immer auf dem übergeordneten Spline *platziert ist und seine Steuerelemente sich auf den gestreuten Spline auswirken.* Mit anderen Worten: Der Drehpunkt bewegt sich nicht, es ist der gestreute Spline, der sich relativ zu ihm bewegt und skaliert.   Positionieren entlang der Spline Bewegen Sie den Drehpunkt entlang der gestreuten Spline.   Absolute Position Legen Sie eine beliebige Position für den Drehpunkt fest. |
| <b>Pivot-Position entlang Spline</b> *Gleitend* | Die normierte Position des Drehzapfens entlang der gestreuten Spline, wobei 0 sein Anfang und 1 sein Ende ist.   Beachten Sie, dass der Drehpunkt der *Richtung* des gestreuten Splines folgt und sich die Ausrichtung des Splines ändern kann, um die Position und Drehung des Drehpunkts relativ zum übergeordneten Spline beizubehalten. |
| <b>Absolute Pivot-Position</b> *Float2* | Die Position des Drehpunkts im UV-Raum. |
| <b>Nicht-quadratische Korrektur</b> *Boolescher Wert* | Passen Sie die Splines-Positionen und die Thickness an, um die Form in nicht quadratischen Auflösungen beizubehalten.   *Hinweis:* Bei Verwendung von benutzerdefinierten Splines sollte der benutzerdefinierte Spline das *gleiche Bildverhältnis* wie die <b>Splines der Streuung </b> auf Splines verwenden. |

+++Größe

|  |  |
| --- | --- |
| <b>Spline-Skalierung</b> *Gleitend* | Ein globales Steuerelement für die Größe aller Splines, wobei 1 ihre volle Originalgröße ist.   Die Skalierung wird relativ zum Drehpunkt eines Splines angewendet. Die Pivot-Position kann mit dem Parameter <b>Spline Pivot</b> versetzt werden. |
| <b>Spline-Skalierung zufällig</b> *Gleitend* | Wendet einen zufälligen Multiplikator bis zum angegebenen Wert an, um die Größe der Splines zu verringern. |
| <b>Zuordnungseingabemultiplikator skalieren</b> *Gleitend* | Steuert die Intensität der <b>Skalierungszuordnung</b>-Eingabe. Diese Karte dient als Multiplikator für die aktuelle Größe der Muster.   Der Effekt dieser Karte wird mit den anderen Parametern in der Gruppe <b>Größe</b> kombiniert. |
| <b>Sampling-Modus für Zuordnungseingabe skalieren</b> *Integer* | Die Methode zum Zuordnen der Werte in der <b>Skalierungszuordnung</b> zu den Splines:   Texturraum Die Werte werden auf die Splines angewendet, wo sie sich befinden würden, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;an Ort und Stelle&quot; Horizontal entlang Spline angewendet. Die Werte werden direkt auf die codierten Splines-Koordinaten angewendet (siehe <b>Spline Coords</b> -Eingabe), wobei jede Zeile auf einen anderen Spline angewendet wird, von oben nach unten Hor. entlang der Spline (Rand). offset X) Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe <b>Spline Coords</b> Eingabe), mit einem zufälligen horizontalen Versatz in der <b>Skalierungszuordnung</b> für jeden Spline (d. h. jede Zeile in <b>Spline Coords</b>) Hor. entlang der Spline (Rand). offset Y) Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe <b>Spline Coords</b> Eingabe), mit einem zufälligen vertikalen Versatz in der <b>Skalierungszuordnung</b> für jeden Spline (d. h. jede Zeile in <b>Spline Coords</b>) |
| <b>Dämpfung starten/beenden</b> *Float2* | Klammert bei der Skalierung der Splines den Abstand zwischen dem Mittelpunkt des Splines und seinen Werten <b>Anfang</b> und <b>Ende</b> ein.   Dies bedeutet, dass die Größe von Splines, die sich näher an den Extremitäten eines Splines befinden, verringert wird. |


+++

+++Position

|  |  |
| --- | --- |
| <b>Lokaler Offset</b> *Float2* | Wendet einen Versatz auf die Positionen der Splines entlang der Tangente (parallel) und Normalen (senkrecht) des übergeordneten Splines an. |
| <b>Offset auf Spline-Bereich</b> *Integer* | Legt den Bereich des Versatzes fest, der auf die gestreuten Splines entlang der übergeordneten Splines angewendet wird.   Intervall Der Bereich erstreckt sich über das Intervall *zwischen* jedem gestreuten Spline.   Übergeordneter Spline Der Bereich erstreckt sich über die *volle Länge* des übergeordneten Splines. |
| <b>Offset auf Spline</b> *Gleitend* | Wendet einen Positionsversatz auf die Splines entlang der übergeordneten Splines an. |
| <b>Bereich für zufällige Verschiebung</b> *Integer* | Legt den Bereich des zufälligen Versatzes fest, der auf die gestreuten Splines entlang der übergeordneten Splines angewendet wird.   Intervall Der Bereich erstreckt sich über das Intervall *zwischen* jedem gestreuten Spline.   Übergeordneter Spline Der Bereich erstreckt sich über die *volle Länge* des übergeordneten Splines. |
| <b>Zufälliger Versatz auf Spline</b> *Gleitend* | Wendet einen zusätzlichen Positionsversatz auf die Splines entlang der übergeordneten Splines an. |
| <b>Offset durch Thickness</b> *Gleitend* | Wendet einen Versatz auf die gestreuten Splines entlang der Normalen der übergeordneten Splines bis zur Thickness der übergeordneten Splines an.   Mit einem Wert von 1 können Sie die gestreuten Splines auf der *Fläche* der Hüllkurve der übergeordneten Splines platzieren. |


+++

+++Rotation

|  |  |
| --- | --- |
| <b>Benutzerdefinierte Spline-Ausrichtung</b> *Integer* | Steuert die anfängliche Ausrichtung der benutzerdefinierten Spline(s) auf den übergeordneten Splines.   Erster Punkt Tangente Die Splines werden entsprechend der Tangente ihres ersten Punktes ausgerichtet. Mit anderen Worten, sie gehen von den übergeordneten Splines in die Richtung, die durch ihren ersten Punkt festgelegt wird.   Bildraum Die Splines werden so platziert, wie sie ursprünglich erscheinen, ohne dass ihre Position oder Ausrichtung zusätzlich angepasst wird, als ob das Bild, das sie darstellt, auf dem übergeordneten Spline läge. |
| <b>Rotationsmodus</b> *Integer* | Legt die ursprüngliche Ausrichtung der gestreuten Splines fest.   Aus Spline Die Splines sind so ausgerichtet, dass sie der *Normalen* der übergeordneten Splines an ihrer Position entsprechen.   Absolut Die Splines sind alle *gleich ausgerichtet*, unabhängig von der Richtung der übergeordneten Splines. |
| <b>Drehung</b> *Gleitend* | Dreht die Splines um ihre Drehpunkte in verschiedenen Drehungen. Die Pivot-Position kann mit dem Parameter <b>Spline Pivot</b> versetzt werden. |
| <b>Drehung zufällig</b> *Gleitend* | Wendet eine zusätzliche zufällige Drehung auf die Splines um ihre Drehpunkte an, in der Anzahl der Windungen. Die Pivot-Position kann mit dem Parameter <b>Spline Pivot</b> versetzt werden. |
| <b>Linker/Rechter Winkel</b> *Gleitend* | Steuert den Winkel der symmetrischen Drehung, die auf die Splines auf jeder Seite der übergeordneten Splines angewendet wird, in der Anzahl der Windungen. |
| <b>Linker/Rechter Winkel zufällig</b> *Gleitend* | Fügt den Splines auf jeder Seite der übergeordneten Splines eine zufällige symmetrische Drehung in der Anzahl der Windungen hinzu. |
| <b>Rotation Map-Eingangsmultiplikator</b> *Gleitend* | Steuert die Intensität der <b>Rotation Map</b>-Eingabe. Diese Karte dient als Multiplikator für die aktuelle Drehung der Muster.   Der Effekt dieser Karte wird mit den anderen Parametern in der Gruppe <b>Drehung</b> kombiniert. |
| <b>Rotation Map-Eingabeaufnahmemodus</b> *Integer* | Die Methode zum Zuordnen der Werte in <b>Rotation Map</b> zu den Splines:   Texturraum Die Werte werden auf die Splines angewendet, wo sie sich befinden würden, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;an Ort&quot;, &quot;Horizontal&quot; entlang Spline angewendet. Die Werte werden direkt auf die codierten Splines-Koordinaten angewendet (siehe <b>Spline Coords</b> input), wobei jede Zeile auf einen anderen Spline von oben nach unten, Hor, angewendet wird. entlang der Spline (Rand). offset X) Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe <b>Spline Coords</b> Eingabe), mit einem zufälligen horizontalen Versatz in der <b>Rotation Map</b> für jeden Spline (d. h. jede Zeile in <b>Spline Coords</b>).   Ehre. entlang der Spline (Rand). offset Y) Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe <b>Spline Coords</b> Eingabe), mit einem zufälligen vertikalen Versatz in der <b>Rotation Map</b> für jeden Spline (d. h. jede Zeile in <b>Spline Coords</b>)<b>.</b> |
| <b>Auswirkungen auf Rotation Map-Eingabe</b> *Integer* | Wählt den Rotationsparameter aus, der von der <b>Rotation Map</b> betroffen ist:   Spline-Drehung Die Karte beeinflusst die globale Drehung der Splines im Uhrzeigersinn.   Links/Rechts-Winkel Die Karte wirkt sich auf die symmetrische Drehung der <b>Links/Rechts</b>-Splines aus. |


+++

+++Höhe

|  |  |
| --- | --- |
| <b>Height-Modus starten</b> *Integer* | Verfahren zur Berechnung des Anfangs-Heights der gestreuten Splines.   Manuell Stellen Sie den gleichen absoluten Wert für alle gestreuten Splines ein.   Aus übergeordnetem Spline (+ benutzerdefiniertem Spline) Verwenden Sie das Height des übergeordneten Splines, und fügen Sie dann das Height des benutzerdefinierten Splines mit dem Height für den benutzerdefinierten Spline-Start <b> hinzu.</b>-Parameter.   Von benutzerdefiniertem Spline Verwenden Sie das Height des benutzerdefinierten Splines so, wie es ist.   *Hinweis:* Legen Sie den <b>Spline-Typ</b> auf &quot;Benutzerdefinierter Spline&quot; fest und verbinden Sie die <b>Benutzerdefinierter Spline</b>-Eingaben, um das Height benutzerdefinierter Splines zu verwenden. |
| <b>Benutzerdefiniertes Spline-Start-Height Mult.</b> *Gleitend* | Steuert den Beitrag des eigenen Anfangs-Heights des benutzerdefinierten Splines zum Anfangs-Height der gestreuten Splines, wobei 1 bedeutet, dass das vollständige Height des benutzerdefinierten Splines verwendet wird.   Das Height des benutzerdefinierten Splines wird entsprechend dem ausgewählten <b>Startmodus des Heights</b> anders verwendet:  *- Vom übergeordneten Spline (+ benutzerdefinierter Spline):* Das Height wird dem übergeordneten Spline hinzugefügt *- Vom benutzerdefinierten Spline:* Das Height wird direkt verwendet |
| <b>Height-Offset starten</b> *Gleitend* | Wendet einen absoluten Versatz auf das Anfangs-Height des gestreuten Splines an. |
| <b>Height starten</b> *Gleitend* | Legt einen absoluten Wert für das Anfangs-Height des gestreuten Splines fest. |
| <b>Height beenden</b> *Integer* | Verfahren zur Berechnung des End-Heights der gestreuten Splines.   Manuell Stellen Sie den gleichen absoluten Wert für alle gestreuten Splines ein.   Aus übergeordnetem Spline (+ benutzerdefiniertem Spline) Verwenden Sie das Height des übergeordneten Spline, und fügen Sie dann das Height des benutzerdefinierten Spline mit dem Height-Mult für das benutzerdefinierte Spline-Ende <b>hinzu.</b>-Parameter.   Von benutzerdefiniertem Spline Verwenden Sie das Height des benutzerdefinierten Splines so, wie es ist.     *Hinweis:* Legen Sie den <b>Spline-Typ</b> auf &quot;Benutzerdefinierte Spline&quot; fest und verbinden Sie die <b>Benutzerdefinierte Spline</b>-Eingaben, um das Height der benutzerdefinierten Splines zu verwenden. |
| <b>Benutzerdefiniertes Spline-End-Height.</b> *Gleitend* | Steuert den Beitrag des eigenen End-Heights des benutzerdefinierten Splines zum End-Height der verstreuten Splines, wobei 1 bedeutet, dass das vollständige Height des benutzerdefinierten Splines verwendet wird.   Das Height des benutzerdefinierten Splines wird entsprechend dem ausgewählten <b>Height beenden</b> anders verwendet:  *- Vom übergeordneten Spline (+ benutzerdefinierter Spline):* Das Height wird dem übergeordneten Spline hinzugefügt *- Vom benutzerdefinierten Spline:* Das Height wird direkt verwendet |
| <b>Height-Versatz beenden</b> *Gleitend* | Wendet einen absoluten Versatz auf das Height des gestreuten Splines an. |
| <b>Height beenden</b> *Gleitend* | Legt einen absoluten Wert für das Height des gestreuten Splines fest. |


+++

+++Stärke

|  |  |
| --- | --- |
| <b>Thickness starten</b> *Integer* | Verfahren zur Berechnung der Anfangs-Thickness der gestreuten Splines.   Manuell Stellen Sie den gleichen absoluten Wert für alle gestreuten Splines ein.   Aus übergeordnetem Spline Verwenden Sie die Thickness des übergeordneten Splines.   Von benutzerdefiniertem Spline Verwenden Sie die Thickness des benutzerdefinierten Splines.   *Hinweis:* Legen Sie den <b>Spline-Typ</b> auf &quot;Benutzerdefinierte Spline&quot; fest und verbinden Sie die <b>Benutzerdefinierte Spline</b>-Eingaben, um die Thickness von benutzerdefinierten Splines zu verwenden. |
| <b>Multiplikator der Thickness starten</b> *Gleitend* | Skaliert die Anfangs-Thickness der gestreuten Splines, wobei 1 die volle Thickness ist. |
| <b>Offset der Thickness starten</b> *Gleitend* | Wendet einen absoluten Versatz auf die Anfangs-Thickness des gestreuten Splines an. |
| <b>Thickness starten</b> *Gleitend* | Legt einen absoluten Wert für die Anfangs-Thickness des gestreuten Splines fest. |
| <b>Thickness beenden</b> *Integer* | Das Verfahren zum Berechnen der End-Thickness der gestreuten Splines.   Manuell Stellen Sie den gleichen absoluten Wert für alle gestreuten Splines ein.   Aus übergeordnetem Spline Verwenden Sie die Thickness des übergeordneten Splines.   Von benutzerdefiniertem Spline Verwenden Sie die Thickness des benutzerdefinierten Splines.   *Hinweis:* Legen Sie den <b>Spline-Typ</b> auf &quot;Benutzerdefinierte Spline&quot; fest und verbinden Sie die <b>Benutzerdefinierte Spline</b>-Eingaben, um die Thickness von benutzerdefinierten Splines zu verwenden. |
| <b>Multiplikator der Thickness beenden</b> *Gleitend* | Skaliert die Anfangs-Thickness der gestreuten Splines, wobei 1 die volle Thickness ist. |
| <b>Offset der Thickness beenden</b> *Gleitend* | Wendet einen absoluten Versatz auf die Thickness des gestreuten Splines an. |
| <b>Thickness beenden</b> *Gleitend* | Legt einen absoluten Wert für die Thickness des gestreuten Splines fest. |


+++

+++Vorschau

|  |  |
| --- | --- |
| <b>Richtungshelfer anzeigen</b> *Boolescher Wert* | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze am Ende in der <b>Vorschau</b>-Ausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> *Boolescher Wert* | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Thickness (px)</b> *Gleitend* | Passt die Thickness der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe in Pixel an. |
| <b>Segmentierungsbetrag</b> *Integer* | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe verwendet werden. Je höher der Wert, desto glatter die Linie. |
| <b>Hintergrundintensität</b> *Gleitend* | Die Intensität der <b>Vorschau</b>-Eingabe in der <b>Vorschau</b>-Ausgabenvisualisierung. |


+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: Beispiel 1](../../../../../../assets/scatter-splines-on-splines-example-1.png "Streuung-Splines auf Splines: Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: Beispiel 1](../../../../../../assets/scatter-splines-on-splines-example-2.png "Streuung-Splines auf Splines: Beispiel 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: Beispiel 3](../../../../../../assets/scatter-splines-on-splines-example-4.png "Streuung-Splines auf Splines: Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: Beispiel 4](../../../../../../assets/scatter-splines-on-splines-example-3.png "Streuung-Splines auf Splines: Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

## Renderings

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: 1](../../../../../../assets/scatter-splines-on-splines-demo-1.png "Streuung-Splines auf Splines rendern: 1"){zoomable="yes"} rendern

</td>
<td style="border: 0;" valign="top">

![Streuung-Splines auf Splines: 2](../../../../../../assets/scatter-splines-on-splines-demo-3.png "Streuung-Splines auf Splines rendern: 2"){zoomable="yes"} rendern

</td>
</tr>
</table>

![Streuung-Splines auf Splines: 3](../../../../../../assets/scatter-splines-on-splines-demo-2.png "Streuung-Splines auf Splines rendern: 3"){zoomable="yes"} rendern

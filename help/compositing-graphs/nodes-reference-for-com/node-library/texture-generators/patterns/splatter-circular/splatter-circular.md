---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kreisförmige Sprenkelung", um kreisförmige Formen über Texturen hinweg Streuung, um organische und zufällige Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kreisförmige Farbspritzer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Kreisförmige Farbspritzer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

## Kreisförmig (Farbe) plattieren

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

&quot;Splatter Circular&quot; generiert ein ringbasiertes Muster mit verschiedenen Steuerelementen. Es kann vordefinierte Formen oder benutzerdefinierte Eingaben verwenden. Es ist ähnlich wie [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), jedoch mit einer kreisförmigen Platzierung anstelle eines Rasters.

Dies ist nützlich, wenn Sie Formen mit verschiedenen Zufallsgenerierungsoptionen kreisförmig platzieren möchten.

## Parameter

### Eingaben

Beide Eingänge sind optional.

* **Musterbildeingabe 1-6**: *Graustufeneingabe (Farbeingabe)*\
  Nur kreisförmige Farbspritzer: Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist.
* **Hintergrund**: *Graustufeneingabe (Farbeingabe)*

### Parameter

* **Mustermenge**: *1 - 64*\
  Anzahl der Musterelemente, die auf einem Ring platziert werden sollen.
* **Zufälliger Musterbetrag**: *0.0 - 1.0*\
  Randomisierung der Anzahl der zu platzierenden Muster. Am besten verwendet mit einem Ring Betrag höher als 1.
* **Zufällige Anzahl an Mustern**: *1 - 10* Legt die minimale Anzahl von Mustern für die Randomisierung fest.
* **Rufbetrag**: *1 - 10*\
  Legt die Anzahl der zu füllenden Ringe fest. Die Ringe sind immer innerhalb des äußeren platziert und gleichmäßig verteilt.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.
* **Muster**
  * **Muster**: *Bildeingabe, Quadrat, Disc, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Gradation, Wellen, Halbglockenton, Ganghütte, Halbmond, Kapsel, Kegel*\
    Wählt die zu verwendende Musterform aus.
  * **Mustereingabenummer**: *1 - 6* Legt die Anzahl der zu verwendenden unterschiedlichen Bildeingaben fest. Nur verfügbar, wenn oben &quot;*Image Input*&quot; ausgewählt wurde.
  * **Mustereingabeverteilung**: *Zufällig, Nach Musternummer, Nach Rufnummer* Legt fest, wie mehrere Mustereingaben ausgewählt werden. Zufällig bedeutet, dass ein zufälliger Ring ausgewählt wird, Pattern Number bedeutet, dass er nur in einer Schleifensequenz platziert wird. Mit Ring-Nummern wird angegeben, dass jeder Ring einen anderen Ring in der Reihenfolge hat.
  * **Bildeingabefilter**: *Bilinear + Mipmaps, Bilinear, Nächste*
  * **Musterspezifisch**: *0.0 - 1.0*\
    Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab.
  * **Symmetrie zufällig**: *0.0 - 1.0*\
    Legt die Anzahl der Kacheln fest, die nach dem Zufallsprinzip gemäß dem folgenden Verhalten gespiegelt/gespiegelt werden sollen.
  * **Zufallssymmetriemodus**: *Horizontal + Vertikal, Horizontal, Vertikal* Bestimmt das Verhalten der Symmetriespiegelung.
* **Position**
  * **Radius**: *0.0 - 1.0*\
    Legt den Radius ab der Mitte fest, in der die Muster platziert werden.
  * **Radius Random**: *0.0 - 1.0* Der Radius für jede Musterkachel wird zufällig festgelegt.
  * **Ring Radius Multiplier**: *0.0 - 1.0*\
    Wirkt sich auf den Abstand mehrerer Ringe aus.
  * **Winkel zufällig**: *0.0 - 1.0* Randomisiert den Winkel jedes Musters. Höhere Beträge bedeuten mehr Rotation.
  * **Spiralfaktor**: *0.0 - 1.0*\
    Wandelt die Ringe in Spiralen um, wo jede Kachel mit einem leicht steigenden Radius platziert wird.
  * **Druckbogen**: *0.0 - 2.0* Legt die Anzahl der Umdrehungen fest, die ein Ring ausführt. Dies kann über seine Grenzen hinaus erhöht werden.
  * **Versatz entlang der Richtung**: *0.0 - 1.0*\
    Verschiebt jedes Muster entlang seines Winkels aus der Mitte heraus. Der Effekt hängt stark vom Wert &quot;Winkel, zufällig&quot; ab oder ähnelt einem Multiplikator für den Radius.
  * **Globaler Offset**: *0.0 - 1.0*\
    Übersetzt die gesamte Form.
* **Größe**
  * **Verbindungsmuster**: *Falsch/Wahr* Die Länge der Musterelemente hängt vom Radius ab, d. h., jede Form sollte die vorherige und die nächste berühren.
  * **Größe (verbunden)**: *0.0 - 1.0*\
    Ändert die Größe jedes Musters global. Wenn sie verbunden sind, ist sie relativ zum Gesamtradius.
  * **Größe zufällig**: *0.0 - 1.0*\
    Die Größe der einzelnen Muster wird zufällig festgelegt.
  * **Skalierung**: *0.0 - 2.0*\
    Skaliert jedes Muster gleichmäßig.
  * **Zufällige Skalierung**: *0.0 - 1.0*\
    Zufällige gleichmäßige Skalierung.
  * **Skalierung nach Musternummer**: *0.0 - 1.0* Macht die Musterskalierung von der Position entlang des Rings abhängig.
  * **Musternummer umkehren**: *False/True*\
    Wird mit der vorherigen Option verwendet, kann dies die Skalierung von klein auf groß umkehren und umgekehrt.
  * **Skalierung nach Rufnummer**: *0.0 - 1.0* Macht die Skalierung von der Rufnummer abhängig.
  * **Rufnummer umkehren**: *Falsch/Wahr* Wird mit der vorherigen Option verwendet, kann die Skalierung von klein auf groß umgekehrt werden und umgekehrt.
* **Drehung**
  * **Musterrotation**: *0.0 - 1.0* Dreht jedes Muster gleichmäßig.
  * **Zufällige Musterdrehung**: *0.0 - 1.0*\
    Zufällige Musterrotation.
  * **Drehpunkt für Muster**: *Center, Min X, Max X, Min Y, Max Y*\
    Legt die Schwenkpunktposition fest, um die jedes Muster einzeln gedreht werden soll.
  * **Zentrierausrichtung**: *False/True*\
    Dreht jedes Muster so, dass es zur Mitte des Rings zeigt. Wenn Sie ihn auf drehen, haben alle die gleiche Ausrichtung - dies kann zu unerwünschten Effekten mit dem Versatz entlang der Richtung führen.
  * **Ringdrehung**: *0.0 - 1.0* Dreht den gesamten Ring um die Mitte.
  * **Ringdrehung zufällig**: *0.0 - 1.0* Rotation pro Ring (zufällig).
  * **Ring-Rotationsversatz**: *0.0 - 1.0*\
    Verschiebt die Drehung pro Ring.
* **Farbe**
  * **Farbe**: *(Graustufenwert)*Farbe, die mit dem ausgewählten Muster multipliziert wird.
  * **Luminanzzufall**: *0.0 - 1.0* Zufallswerte für Farbe oder Luminanz für jede Musterkachel.
  * **Luminanz nach Skalierung**: *0.0 - 1.0* Macht die Luminanz von der einzelnen Musterskala abhängig.
  * **Luminanz nach Musternummer**: *0.0 - 1.0* Luminanz abhängig von der Mustersequenz. Kann beispielsweise mit Spiralen verwendet werden.
  * **Musternummer umkehren**: *Falsch/Wahr* Kehrt die vorherige Option um.
  * **Luminanz nach Rufnummer**: *0.0 - 1.0* Macht die Luminanz von der Ringsequenz abhängig.
  * **Rufnummer umkehren**: *Falsch/Wahr* Kehrt die vorherige Option um.
  * **Zufallsmaske**: *0.0 - 1.0* Blendet Muster zufällig aus.
  * **Hintergrundfarbe**: *(Graustufenwert)*Ändert die Volltonhintergrundfarbe.
  * **Füllmethode**: *Hinzufügen, Max, Sub hinzufügen* Legt fest, wie überlappende Muster überblendet werden.
  * **Globale Deckkraft**: *0.0 - 1.0* Legt die globale Deckkraft des gesamten Ergebnisses fest.

## Beispielbilder

![](../../../../../../assets/circularsplatter-ex.png)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kreisförmige Sprenkel", um kreisförmige Formen über Texturen hinweg Streuung, um organische und zufällige Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kreisförmige Farbspritzer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 8%

---


# Kreisförmige Farbspritzer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

<b>In:</b> Texturen > Muster generieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

&quot;Splatter Circular&quot; generiert ein ringbasiertes Muster mit verschiedenen Steuerelementen. Es kann vordefinierte Formen oder benutzerdefinierte Eingaben verwenden. Es ist ähnlich wie [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), jedoch mit einer kreisförmigen Platzierung anstelle eines Rasters.

Dies ist nützlich, wenn Sie Formen mit verschiedenen Zufallsgenerierungsoptionen kreisförmig platzieren möchten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

Beide Eingänge sind optional.

|  |  |
|:---|:---|
| <b>Musterbildeingabe 1-6</b> <i>Graustufeneingabe (Farbeingabe)</i> | Nur kreisförmige Farbspritzer: Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist. |
| <b>Hintergrund</b> <i>Graustufeneingabe (Farbeingabe)</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Mustermenge</b> <i>1 - 64</i> | Anzahl der Musterelemente, die auf einem Ring platziert werden sollen. |
| <b>Zufälliger Musterbetrag</b> <i>0.0 - 1.0</i> | Randomisierung der Anzahl der zu platzierenden Muster. Am besten verwendet mit einem Ring Betrag höher als 1. |
| <b>Zufällige Anzahl an Mustern</b> <i>1 - 10</i> | Legt die minimale Anzahl von Mustern für die Randomisierung fest. |
| <b>Rufbetrag</b> <i>1 - 10</i> | Legt die Anzahl der zu füllenden Ringe fest. Die Ringe sind immer innerhalb des äußeren platziert und gleichmäßig verteilt. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |
| <b>Muster</b> |  |
| <b>Muster</b> <i>Bildeingabe, Quadrat, Datenträger, Paraboloid, Glockensymbol, Gaußsch, Dorn, Pyramide, Ziegel, Abstufung, Wellen, Halbglocke, Rändelglocke, Mondsichel, Kapsel, Kegel</i> | Wählt die zu verwendende Musterform aus. |
| <b>Mustereingabenummer</b> <i>1 - 6</i> | Legt die Anzahl der zu verwendenden Bildeingaben fest. Nur verfügbar, wenn oben &quot;<i>Image Input</i>&quot; ausgewählt wurde. |
| <b>Mustereingabeverteilung</b> <i>Zufällig, nach Musternummer, nach Rufnummer</i> | Legt fest, wie mehrere Mustereingänge ausgewählt werden. Zufällig bedeutet, dass ein zufälliger Ring ausgewählt wird, Pattern Number bedeutet, dass er nur in einer Schleifensequenz platziert wird. Mit Ring-Nummern wird angegeben, dass jeder Ring einen anderen Ring in der Reihenfolge hat. |
| <b>Filterung der Bildeingabe</b> <i>Bilinear + Mipmaps, Bilinear, Nächste</i> |  |
| <b>Musterspezifisch</b> <i>0.0 - 1.0</i> | Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab. |
| <b>Symmetrie zufällig</b> <i>0.0 - 1.0</i> | Legt die Anzahl der Kacheln fest, die nach dem Zufallsprinzip gemäß dem folgenden Verhalten gespiegelt/gespiegelt werden sollen. |
| <b>Zufallsmodus der Symmetrie</b> <i>Horizontal + Vertikal, Horizontal, Vertikal</i> | Bestimmt das Verhalten der Symmetrie-Spiegelung. |
| <b>Position</b> |  |
| <b>Radius</b> <i>0.0 - 1.0</i> | Legt den Radius ab der Mitte fest, in der die Muster platziert werden. |
| <b>Radius Random</b> <i>0.0 - 1.0</i> | Der Radius für jede Musterkachel wird zufällig festgelegt. |
| <b>Ring-Radius-Multiplikator</b> <i>0.0 - 1.0</i> | Wirkt sich auf den Abstand mehrerer Ringe aus. |
| <b>Winkel zufällig</b> <i>0.0 - 1.0</i> | Zufallswert für den Winkel jedes Musters. Höhere Beträge bedeuten mehr Rotation. |
| <b>Spiralfaktor</b> <i>0.0 - 1.0</i> | Wandelt die Ringe in Spiralen um, wo jede Kachel mit einem leicht steigenden Radius platziert wird. |
| <b>Druckbogen</b> <i>0.0 - 2.0</i> | Legt die Anzahl der Umdrehungen eines Rings fest. Dies kann über seine Grenzen hinaus erhöht werden. |
| <b>Versatz entlang Richtung</b> <i>0.0 - 1.0</i> | Verschiebt jedes Muster entlang seines Winkels aus der Mitte heraus. Der Effekt hängt stark vom Wert &quot;Winkel, zufällig&quot; ab oder ähnelt einem Multiplikator für den Radius. |
| <b>Globaler Offset</b> <i>0.0 - 1.0</i> | Kamera bewegt die gesamte Form bei. |
| <b>Größe</b> |  |
| <b>Verbindungsmuster</b> <i>False/True</i> | Macht die Länge der Musterelemente vom Radius abhängig, d. h., jede Form sollte die vorherige und die nächste berühren. |
| <b>Größe (verbunden)</b> <i>0.0 - 1.0</i> | Ändert die Größe jedes Musters global. Wenn sie verbunden sind, ist sie relativ zum Gesamtradius. |
| <b>Größe zufällig</b> <i>0.0 - 1.0</i> | Die Größe der einzelnen Muster wird zufällig festgelegt. |
| <b>Skalierung</b> <i>0.0 - 2.0</i> | Skaliert jedes Muster gleichmäßig. |
| <b>Zufällige Skalierung</b> <i>0.0 - 1.0</i> | Zufällige gleichmäßige Skalierung. |
| <b>Skalierung nach Musternummer</b> <i>0.0 - 1.0</i> | Macht das Muster von der Position entlang des Rings abhängig. |
| <b>Musternummer umkehren</b> <i>False/True</i> | Wird mit der vorherigen Option verwendet, kann dies die Skalierung von klein auf groß umkehren und umgekehrt. |
| <b>Skalierung nach Rufnummer</b> <i>0.0 - 1.0</i> | Macht die Skalierung von der Rufnummer abhängig. |
| <b>Rufnummer umkehren</b> <i>False/True</i> | Bei Verwendung der vorherigen Option kann die Skalierung von klein auf groß umgekehrt werden und umgekehrt. |
| <b>Drehung</b> |  |
| <b>Musterrotation</b> <i>0.0 - 1.0</i> | Dreht jedes Muster gleichmäßig. |
| <b>Musterrotation zufällig</b> <i>0.0 - 1.0</i> | Zufällige Musterrotation. |
| <b>Drehpunkt für Muster</b> <i>Center, Min X, Max X, Min Y, Max Y</i> | Legt die Schwenkpunktposition fest, um die jedes Muster einzeln gedreht werden soll. |
| <b>Zentrierausrichtung</b> <i>False/True</i> | Dreht jedes Muster so, dass es zur Ringmitte hin Fläche wird. Wenn Sie ihn auf drehen, haben alle die gleiche Ausrichtung - dies kann zu unerwünschten Effekten mit dem Versatz entlang der Richtung führen. |
| <b>Ringdrehung</b> <i>0.0 - 1.0</i> | Dreht den gesamten Ring um die Mitte. |
| <b>Ringdrehung zufällig</b> <i>0.0 - 1.0</i> | Zufällige Drehung pro Ring. |
| <b>Ring-Rotationsversatz</b> <i>0.0 - 1.0</i> | Verschiebt die Drehung pro Ring. |
| <b>Farbe</b> |  |
| <b>Farbe</b> <i>(Graustufenwert)</i> | Mit ausgewähltem Muster zu multiplizierende Farbe. |
| <b>Luminanz zufällig</b> <i>0.0 - 1.0</i> | Weist jeder Musterkachel eine beliebige Farbe oder Luminanz zu. |
| <b>Luminanz nach Skalierung</b> <i>0.0 - 1.0</i> | Macht die Luminanz von der individuellen Musterskala abhängig. |
| <b>Luminanz nach Musternummer</b> <i>0.0 - 1.0</i> | Macht die Luminanz von der Mustersequenz abhängig. Kann beispielsweise mit Spiralen verwendet werden. |
| <b>Musternummer umkehren</b> <i>False/True</i> | Kehrt die vorherige Option um. |
| <b>Luminanz durch Rufnummer </b> <i>0.0 - 1.0</i> | Macht die Luminanz von der Ringsequenz abhängig. |
| <b>Rufnummer umkehren</b> <i>False/True</i> | Kehrt die vorherige Option um. |
| <b>Zufallsmaske</b> <i>0.0 - 1.0</i> | Blendet Muster zufällig aus. |
| <b>Hintergrundfarbe</b> <i>(Graustufenwert)</i> | Ändert die Volltonhintergrundfarbe. |
| <b>Füllmethode</b> <i>Hinzufügen, Max, Sub hinzufügen</i> | Legt fest, wie überlappende Muster angeglichen werden. |
| <b>Globale Deckkraft</b> <i>0.0 - 1.0</i> | Legt die globale Deckkraft des gesamten Ergebnisses fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/circularsplatter-ex.png" />
        </td>
    </tr>
</table>

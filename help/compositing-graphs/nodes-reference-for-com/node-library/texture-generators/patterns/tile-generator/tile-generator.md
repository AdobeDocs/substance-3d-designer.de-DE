---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Tile Generator", um prozedurale Kachelmuster mit anpassbaren Steuerelementen für Größe, Offset und Variation zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kachelgenerator
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Kachelgenerator

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

## Tile Generator (Farbe)

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Tile Generator ist einer der am weitesten fortgeschrittenen Knoten in der Bibliothek. Wenn du lernst, es zu beherrschen, kannst du jede Art von Muster erstellen (innerhalb einiger Einschränkungen). Seit Version 2017 2.1 wurden einige große Updates veröffentlicht, die diesen Knoten mehr in Einklang mit den Möglichkeiten von [Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) bringen.

Dieser Knoten ist für eine Vielzahl von Szenarien sehr nützlich. Beachten Sie jedoch, dass Sie beim Lesen von Parametern nicht vollständig lernen können, wie Sie sie verwenden. Wir empfehlen Ihnen, auch zu experimentieren!

Für 99% aller Fälle wird die Farbversion NICHT benötigt!

Einige allgemeine Tipps zur Verwendung:

* Sie können mit einer Grundform beginnen, aber wenn Sie über eine benutzerdefinierte Eingabe verfügen (legen Sie **Mustertyp** auf *Bildeingabe* fest), erstellen Sie diese zuerst! Es bestimmt einen großen Teil des Aussehens.
* Beginnen Sie mit der korrekten Einstellung der X- und Y-Werte.
* Finden Sie den richtigen **Size**-Modus: Relative Modi wie **Interstice** verhalten sich ganz anders als **Absolute** Modi.
* Globale **Skalierung** und nicht einheitliche **Größe** als Nächstes anpassen.
* Passen Sie schließlich jeden **-Parameter &quot;Variation&quot;** an, bis er Ihren Anforderungen entspricht. Subtilität ist der Schlüssel zur Variation!

## Parameter

### Eingaben

* **Mustereingabe 1-6**: *Graustufen-Eingabe*\
  Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist.
* **Hintergrund**:*Graustufeneingabe* Der zu verwendende Hintergrund anstelle der Volltonfarbe.

### Parameter

* **X Betrag**: *1 - 64*\
  Anzahl der X-Wiederholungen des Musters.
* **Y Betrag**: *1 - 64*\
  Anzahl der Y-Wiederholungen des Musters.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.
* **Muster**
  * **Muster**: *Bildeingabe, Quadrat, Disc, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Gradation, Wellen, Halbglockenton, Ganghütte, Halbmond, Kapsel, Kegel*\
    Wählt die zu verwendende Musterform aus.
  * **Mustereingabenummer**: *1 - 6* Anzahl der zu verwendenden verschiedenen Bildeingaben. Nur verfügbar, wenn oben &quot;*Image Input*&quot; ausgewählt wurde.
  * **Mustereingabeverteilung**: *Zufällig, nach Musternummer* So wählen Sie zwischen den verschiedenen Bildeingaben aus, wenn mehr als 1 ausgewählt ist.
  * **Musterspezifisch**: *0.0 - 1.0*\
    Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab.
  * **Bildeingabefilter (nur Engine >v4)**: *Bilinear + Mipmaps, Bilinear, Nächste*
  * **Drehung**: *0, 90, 180, 270* Dreht alle Kacheln global um einen bestimmten Winkel in Schritten von 90 Grad.
  * **Drehung zufällig**: *0.0 - 1.0* Zufällig dreht eine Kachel um einen von vier 90-Grad-Schritten.
  * **Quincunx Flip**: *Falsch/Wahr* Dreht jede zweite Kachel um 90 Grad.
  * **Symmetrie zufällig**: *0.0 - 1.0* Spiegelt zufällig bestimmte Muster nach dem ausgewählten Zufallsmodus der Symmetrie. Je höher dieser Wert, desto mehr Muster werden gespiegelt.
  * **Zufallssymmetriemodus**: *Horizontal + Vertikal, Horizontal, Vertikal* Bestimmt das Spiegelungsverhalten, wenn die zufällige Symmetrie größer als 0 ist.
* **Größe**
  * **** Größenmodus **:***Normal - Interstice, Normal - Size, Keep Ratio, Absolute, Pixel*Legt das allgemeine Verhalten der Mustergröße fest.\
    Normal : Mit der Option &quot;Abstand&quot; können Sie den Abstand zwischen den Musterelementen definieren. Er wird durch den X- und Y-Wert beeinflusst.\
    Normal : Mit dieser Option können Sie die Größe der Musterelemente definieren, unabhängig vom Abstand. Er wird durch den X- und Y-Wert beeinflusst.\
    Mit &quot;Verhältnis beibehalten&quot; können Sie eine Größe festlegen, die von einem x- und einem y-Wert beeinflusst wird, aber das x- und y-Verhältnis zwischen den beiden bleiben intakt.\
    Mit &quot;Absolut&quot; können Sie eine absolute Größe festlegen, die nicht durch den X- und Y-Wert beeinflusst wird.\
    Mit Pixel können Sie eine absolute Größe in Pixeln festlegen, die von der X- und Y-Größe nicht beeinflusst wird. Eine Änderung der Auflösung wirkt sich auf die Größe der Elemente aus.
  * **Mittlere Größe**: *0.0 - 1.0*&#x200B;Ändert die Größe auf abwechselnder Spalten- und Zeilenbasis.
  * **Interstice X/Y**: *0.0 - 1.0* Nur im Modus &quot;Normal - Schnittstellengröße&quot; verfügbar. Ändert die Lücke in der Lücke. Wirkt sich auf die Naht zwischen Formen aus und ermöglicht eine ungleichmäßige Steuerung im Gegensatz zu **Skalierung**.
  * **Größe (Absolut/Pixel)**: *0.0 - 1.0*\
    Nur außerhalb von &quot;Normal&quot; verfügbar - Schnittstellengrößenmodus. Legt im Gegensatz zu **Skalierung** eine nicht einheitliche Größe fest.
  * **Skalierung**: *0.0 - 2.0* Legt die globale Skalierung fest.
  * **Zufällige Skalierung**: *0.0 - 1.0* Legt die globale Skalierungsvariation pro Kachel fest.
  * **Zufallsverteilung skalieren**: *0 - 1000* Verschiebt den Samen der Skalierungsvariante.
* **Position**
  * **Offset**: *0.0 - 1.0* Verschiebt das gesamte Muster schrittweise über jede aufeinander folgende Zeile oder Spalte hinweg (das Verhalten hängt vom Parameter &quot;Vertikaler Versatz&quot; ab).
  * **Offset zufällig**: *0.0 - 1.0* Randomisiert den Zeilenversatz.
  * **Offset Zufallsverteilung**: *0 - 1000*&#x200B;Ändert die relative Geschwindigkeit für den zufälligen Versatzeffekt.
  * **Vertikaler Versatz**: *Falsch/Wahr* Legt fest, ob der Versatzeffekt auf Zeilen oder Zeilen angewendet wird; Horizontal oder Vertikal.
  * **Position zufällig**: *0.0 - 1.0* Die Position wird auf eine ungleichmäßige Weise mit separater Steuerung für X und Y randomisiert.
  * **Globaler Offset**: *0.0 - 1.0* Verschiebt das gesamte Ergebnis über X- und Y-Achsen.
* **Drehung**
  * **Drehung**: *0.0 - 1.0* Führt eine gleichmäßige freie Drehung aller Musterelemente durch.
  * **Drehung zufällig**: *0.0 - 1.0* Randomisiert die freie Drehung aller Kacheln. Je höher dieser Wert ist, desto mehr Kacheln können gedreht werden.
* **Farbe**
  * **Farbe**: *(Graustufenwert)*Legt die Farbfläche der Kachel fest.
  * **Luminanz/Farbzufall**: *0.0 - 1.0* Führt Farb- oder Luminanzvariationen pro Kachel ein.
  * **Luminanz nach Zahl**: *Falsch/Wahr* Verblasst die Luminanz über das gesamte Muster.
  * **Luminanz nach Skalierung**: *Falsch/Wahr* Macht die Luminanzvariation von der Kachelskala abhängig.
  * **Prüfmaske**: *Falsch/Wahr* Blendet jede andere Kachel aus.
  * **Horizontale Maske**: *Falsch/Wahr* Blendet jede zweite Spalte aus.
  * **Vertikale Maske**: *Falsch/Wahr* Blendet jede zweite Zeile aus.
  * **Zufallsmaske**: *0.0 - 1.0* Blendet Kacheln zufällig aus. Je höher dieser Wert ist, desto mehr Kacheln werden ausgeblendet.
  * **Maske umkehren**: *Falsch/Wahr* Kehrt das Ergebnis aller Maskierungseffekte aus diesem Abschnitt um.
  * **Füllmethode**: *Hinzufügen, Max, Sub hinzufügen* Legt den zu verwendenden Mischmodus fest.
  * **Hintergrundfarbe**: *(Graustufenwert)*Legt die einfarbige Hintergrundfarbe fest.
  * **Globale Deckkraft**: *0.0 - 1.0* Legt die Deckkraft globaler Kacheln fest.
  * **Renderreihenfolge umkehren**: *Falsch/Wahr* Die Kacheln werden nach vorne gerendert oder umgekehrt.

## Beispielbilder

![](../../../../../../assets/tilesampler-ex.png)

![](../../../../../../assets/image2020-9-17-14-50-18.png)

![](../../../../../../assets/image2020-9-17-14-52-4.png)

![](../../../../../../assets/image2020-9-17-14-53-47.png)

</td>
</tr>
</table>

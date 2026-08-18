---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Verwenden Sie den Sampler-Kachelknoten zum Aufnehmen und Anordnen von Kacheln aus Eingabetexturen, um Kachelmuster in Substance 3D Designer zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sampler anordnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# Sampler anordnen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## Sampler anordnen (Farbe)

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Tile Sampler ist der ultimative Kachelmuster-Erzeugungsknoten. Es handelt sich um eine weiterentwickelte, komplexere Version von [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Ab 2017 2.1 sind die Unterschiede zwischen Tile Sampler und [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) viel geringer. Die Hauptunterschiede bestehen nun nur noch in den sieben verschiedenen Kartensteckplätzen, die für Skalierung, Position, Drehung, Größe, Farbe und Maskierung zur Verfügung stehen. Ihr Effekt kann separat eingemischt werden.

Kachel-Sampler ist hilfreich beim Erstellen künstlicher prozeduraler Muster, mit zusätzlicher Kontrolle über bestimmte Parameter, die von externen Eingabemaps gesteuert werden.

Vergewissern Sie sich, dass Sie mit [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) vertraut sind, bevor Sie mit Tile Sampler fortfahren. In den meisten Fällen reichen [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) aus und Sie benötigen nicht die zusätzliche Komplexität von Tile Sampler.

## Parameter

### Eingaben

* **Mustereingabe 1-6**: *Graustufen-Eingabe/Farbeingabe*\
  Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist.\
  Die Menge der verfügbaren Eingaben wird durch den Parameter **Mustereingabenummer** bestimmt.
* **Zuordnungseingabe skalieren**: *Graustufeneingabe* Graustufenzuordnung zum Steuern der Kachelskalierung.
* **Versatz-Zuordnungseingabe**: *Graustufeneingabe* Graustufenzuordnung zum Steuern des Kachel-Versatzes.
* **Rotation Map-Eingabe**: *Graustufen-Eingabe*\
  Graustufen-Map, um die Drehung der Kacheln zu steuern.
* **Vektorzuordnungseingabe**: *Farbeingabe*\
  Farbvektorkarte zur ungleichmäßigen Skalierung.
* **Farbzuordnungseingabe**: *Graustufen-Eingabe/Farbeingabe* Karte zum Steuern der Farbtönung pro Kachel.
* **Maskenzuordnungseingabe**: *Graustufen-Eingabe*\
  Maskenschlitz zum Ausblenden bestimmter Kacheln.
* **Musterverteilungszuordnungseingabe**: *Graustufen-Eingabe*\
  Maskenschlitz, der zum Steuern mehrerer benutzerdefinierter Mustereingaben verwendet wird.
* **Hintergrundeingabe**: *Graustufen-Eingabe/Farbeingabe* Optionales Hintergrundbild.

### Parameter

* **X Betrag**: *0 - 64*\
  Anzahl der X-Wiederholungen des Musters.
* **Y Betrag**: *0 - 64*\
  Anzahl der Y-Wiederholungen des Musters.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.
* **Muster**
  * **Muster**: *Mustereingabe, Quadrat, Disc, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Abstufung, Wellen, halbe Glocke, Gekrätzte Glocke, Halbmond, Kapsel, Kegel*\
    Wählt die zu verwendende Musterform aus.
  * **Mustereingabenummer**: *1 - 6* Anzahl benutzerdefinierter Muster, aus denen zufällig ausgewählt werden kann.
  * **Mustereingabeverteilung**: *Zufällig, Musternummer, Verteilungszuordnung* Legt fest, wie mehrere Mustereingaben ausgewählt werden. &quot;Zufällig&quot; bedeutet, dass ein zufälliger Wert ausgewählt wird. &quot;Musternummer&quot; bedeutet, dass er nur in eine Schleifensequenz eingefügt wird. Die Verteilungszuordnung verwendet eine Graustufenzuordnungseingabe, um die Platzierung zu steuern.
  * **Mustereingabefilter (Engine > v4)**: *Bilinear + Mipmaps, Bilinear, Nächste*
  * **Musterspezifisch**: *0.0 - 1.0*\
    Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab.
  * **Musterspezifische Zufallszahl**: *0.0 - 1.0* Der Randomisierungseffekt hängt vom ausgewählten Muster ab.
  * **Drehung**: *0, 90, 180, 270* Drehung schrittweise (90 Grad).
  * **Drehung zufällig**: *0.0 - 1.0* Zufällige freie Drehung pro Kachel.
  * **Symmetrie zufällig**: *0.0 - 1.0* Legt die Anzahl der Kacheln fest, die gemäß dem Verhalten unten zufällig gespiegelt/gespiegelt werden sollen.
  * **Zufallssymmetriemodus**: *Horizontal + Vertikal, Horizontal, Vertikal* Bestimmt das Verhalten der Symmetriespiegelung.
* **Größe**
  * **Größenmodus**: *Normal, Verhältnis beibehalten, Absolut, Pixel* Legt das allgemeine Verhalten der Mustergröße fest.\
    Mit Normal können Sie die Größe der Musterelemente definieren. Er wird durch den X- und Y-Wert beeinflusst.\
    Mit &quot;Verhältnis beibehalten&quot; können Sie eine Größe festlegen, die von einem x- und einem y-Wert beeinflusst wird, aber das x- und y-Verhältnis zwischen den beiden bleiben intakt.\
    Mit &quot;Absolut&quot; können Sie eine absolute Größe festlegen, die nicht durch den X- und Y-Wert beeinflusst wird.\
    Mit Pixel können Sie eine absolute Größe in Pixeln festlegen, die von der X- und Y-Größe nicht beeinflusst wird. Eine Änderung der Auflösung wirkt sich auf die Größe der Elemente aus.
  * **Größe (Absolut/Pixel)**: *0.0 - 1.0*&#x200B;Ändert ungleichmäßige Proportionen für Kacheln. Das genaue Verhalten hängt vom Größenmodus ab.
  * **Größe zufällig**: *0.0 - 1.0* Randomisiert die Proportionen pro Kachel.
  * **Skalierung**: *0.0 - 10.0* Legt die globale Kachelskala fest.
  * **Zufällige Skalierung**: *0.0 - 1.0* Zufällige Skalierung pro Kachel
  * **Zuordnungsmultiplikator skalieren**: *0.0 - 1.0*&#x200B;Überblendungen im Effekt der Skalierungszuordnung.
  * **Vektorzuordnungsvervielfacher skalieren**: *0.0 - 1.0*&#x200B;Überblendungen im Effekt der Skalierungsvektorkarte, um eine ungleichmäßige Skalierung zu steuern.
  * **Effekt der Skalierungsparameter**: *X und Y, X, Y* Legt fest, welche Achsen von der Skalierungsparameter betroffen sind. Kann verwendet werden, um zu erreichen, dass die Skalierungszuordnung nur das X oder Y von Elementen beeinflusst.
* **Position**
  * **Position zufällig**: *0.0 - 10.0* Randomisiert die Kachelposition auf beiden Achsen.
  * **Offset**: *0.0 - 1.0*\
    Verschiebt die Kacheln je nach Versatztyp.
  * **Offsettyp**: *Horizontaler Quincux, Vertikaler Quincux, Horizontaler Globaler, Vertikaler Globaler*&#x200B;Ändert, in welche Richtung der Offset arbeitet.
  * **Globaler Offset**: *0.0 - 1.0* Verschiebt alle Kacheln auf der X- oder Y-Achse global.
  * **Intensität der Versatz-Map**: *0.0 - 1.0*&#x200B;Überblendungen in der Stärke der Versatz-Map im Offset.
  * **Versatz-Winkel**: *0.0 - 1.0* Legt den Winkel fest, unter dem die Verschiebung erfolgen soll.
  * **Versatz für Vektorzuordnung**: *0.0 - 1.0* Verwendet die Vektorzuordnung zum Steuern von Versatz und Winkel.
* **Drehung**
  * **Drehung**: *0.0 - 1.0* Dreht alle Kacheln global.
  * **Drehung zufällig**: *0.0 - 1.0* Rotiert willkürlich pro Kachel.
  * **Rotation Map-Multiplikator**: *0.0 - 1.0*&#x200B;Überblendungen im Effekt des Rotation Map bei der Drehung pro Kachel.
  * **Vektorkartenmultiplikator**: *0.0 - 1.0* Verwendet die Vektorzuordnung, um die Drehung pro Kachel zu steuern.
* **Farbe**
  * **Schwellenwert für Maskenzuordnung**: *0.0 - 1.0* Schwellenwert für Maskenzuordnung, wann mit dem Ausblenden von Kacheln begonnen werden soll.
  * **Umkehren der Maskenzuordnung**: *Falsch/Wahr* Kehrt den Maskenzuordnungseffekt um.
  * **Maskenzuordnungs-Sampling-Technik**: *Mustermitte, Musterbegrenzungsrahmen (langsamer)*Ob das Verbergen durch einen einzelnen Punkt oder einen Begrenzungsrahmen bestimmt werden soll. Vermeidet unregelmäßige Pixel, die seltsame Effekte verursachen.
  * **Zufällige Maske**: *0.0 - 1.0* Zufällige Maskierung, funktioniert parallel zur Maskenzuordnung.
  * **Maske umkehren**: *Falsch/Wahr* Kehrt die zufällige Maskierung um.
  * **Füllmethode**: *Add/Sub, Max (Tile Sampler) /* Add/Sub, Alpha Blend* (Tile Sampler Color)*Mischmodus für Kacheln auf Hintergrund und untereinander.
  * **Farbe**: *(Graustufenwert) / (Farbwert)*Volltonfarbe, globale Kachelfarbe.
  * **Zufällige Farbe/Luminanz**: *0.0 - 1.0* Randomisierung der Farbe pro Kachel.
  * **Farbparametrisierungsmodus**: *Farbeingabe, Skalierung, Zeilenindex, Zeilenindex, Musterindex (Kachel-Sampler)*\
    */ *Farbkarte, Skalierung, Zeilenindex, Zeilenindex, Musterindex, Mustermittenposition, Mustermittenposition, Mustermittenposition (RG) Bsphere Size (B) (Tile Sampler Color)**Legt fest, wie genau die Farbrandomisierung parametriert wird.
  * **Farbparametrisierungsvervielfacher**: *0.0 - 1.0*&#x200B;Überblendungen im obigen Parametrisierungseffekt.
  * **Effekt &quot;Farbparametrisierung&quot; (nur Farbe):** **RGB+Alpha, nur RGB, nur Alpha** Legt fest, wie sich die Parametrisierung auf die Farbe auswirkt.
  * **Globale Deckkraft (nur Graustufen)**: *0.0 - 1.0* Legt die globale Kacheldeckkraft fest.
  * **Hintergrundfarbe**: *(Graustufenwert) / (Farbwert)*Legt die Volltonhintergrundfarbe fest.
  * **Renderreihenfolge umkehren**: *Falsch/Wahr* Kehrt die Renderreihenfolge um und wechselt von hinten nach vorne.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*Beispiel zeigt, wie Parameter durch Eingabemaps gesteuert werden (Musterverteilung, Skalierung, Drehung).*

</td>
</tr>
</table>

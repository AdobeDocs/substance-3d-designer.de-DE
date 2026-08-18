---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knotenpunkt "Form-Spritzer", um Formen in Streuungen über Texturen hinweg anzuordnen, um prozedurale Muster und Details zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Formaufteilung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# Formaufteilung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## Formaufteilung

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein sehr komplexer Knoten, der für die Verwendung mit den zugehörigen Knoten [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) und [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md) entwickelt wurde. Wird verwendet, um Formen ähnlich wie [Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) oder [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) zu spritzen, jedoch mit einem dynamischen, nicht-destruktiven Prozess, der die Kontrolle über jeden Schritt über ein mehrstufiges System ermöglicht, das dem [Flood Fill ähnelt.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Während der Flood Fill eine Basiseingabekarte aus einer externen Quelle verwendet, generiert Shape Splatter die Zuordnung und die darauf folgenden Daten in einem einzigen Schritt als eine Art erweiterte Version von [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Der Hauptzweck besteht darin, die Platzierung von Formen auf und gesteuert durch eine Height-Map zu ermöglichen und dann verschiedene Maps aus den Splatter-Daten zu generieren. Zum Beispiel das Platzieren von Felsen, Zweigen und Blättern auf einer Landschaft, orientiert und angetrieben von verschiedenen Karten. Verschiedene Maps können dann für Height, Normal, Grundfarbe, Raueit und jeden anderen Kanal verwendet werden, während alle immer noch auf den gleichen gemeinsamen Splatter-Daten basieren.

## Parameter

### Eingaben

* **Hintergrund-Height**: *Graustufen-Eingabe* Hintergrund-Height, um Kacheln auf verschiedenen Effekten zu platzieren und diese zu steuern.
* **Muster 1-8**: *Eingabe-/Optionales***
* **Musterverteilung**: *Graustufen-Eingabe* Graustufen-Zuordnung zu
* **Formskalierung**: *Graustufeneingabe* Graustufenzuordnung zum Steuern der Kachelskalierung.
* **Formdrehung**: *Graustufeneingabe* Graustufenzuordnung zum Drehen der Kachel.
* **Height-Offset**: *Graustufen-Eingabe* Graustufen-Map zur Verwendung als Offset für Kachel-Height.
* **Height-Skalierung**: *Graustufen-Eingabe* Graustufen-Map zur Verwendung als Offset für Kachel-Height.
* **Zufällige Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Vektorzuordnung**: *Farbeingabe* Farbvektorzuordnung zum Steuern der Kachelpositionierung und -drehung.

### Parameter

* **X Betrag**: *1 - 64*\
  Anzahl der X Wiederholungen des Musters.
* **Y Betrag**: *1 - 64*\
  Anzahl der Y-Wiederholungen des Musters.
* **Muster**
  * **Mustereingabenummer**: *1 - 8* Legen Sie die Anzahl der zu verwendenden unterschiedlichen Muster fest. Entsperrt neue Steckplätze für Mustereingabe.
  * **Musterverteilungsmodus**: *Zufällig, Musterindex, Zeilenindex, Spaltenindex* Legen Sie fest, wie das zu verwendende Muster bestimmt wird. Zufällig oder nach Muster, Zeile oder Spalte.
  * **Zuordnungsmultiplikator für Musterverteilung**: *0.0 - 1.0* Legen Sie den Einfluss der optionalen Verteilungszuordnung auf die Platzierung von Mustern fest.
  * **Musterrotation**: *0, 90, 180, 270* Vorgabe festlegen, Drehung der Muster um 90 Grad.
  * **Zufällige Musterdrehung**: *0.0 - 1.0* Legen Sie die Stärke der zufälligen 90-Grad-Schrittrotation für Muster fest.
* **Größe**
  * **Skalierung**: *0.0 - 5.0*\
    Legen Sie die einheitliche Skalierung für jede Kachel fest.
  * **Zufällige Skalierung**: *0.0 - 1.0* Einheitliche Skalierung für jede Kachel zufällig anpassen.
  * **Keine Überlappung skalieren**: *0.0 - 1.0* Zufällige Skalierung gleichmäßig, aber nur nach unten, um überlappende Kacheln zu vermeiden. Sollte nicht in Verbindung mit den beiden vorherigen Parametern verwendet werden.
  * **Zuordnungsmultiplikator skalieren**: *0.0 - 1.0* Einfluss der Skalierungskarte festlegen.
  * **Größe**: *0.0 - 1.0* Ermöglicht eine ungleichmäßige Skalierung von Kacheln.
  * **Größenverhältnis von Bg-Steigung**: *0.0 - 1.0* Verwendet die Steigung der Hintergrundzuordnung (berechnet als &quot;Normal&quot;), um Kacheln ungleichmäßig zu skalieren. Simuliert perspektivisches Verkrümmen.
  * **Größe nach X/Y-Verhältnis**: *0.0 - 1.0* Ungleichmäßige Skalierung zum Ausgleich eines unterschiedlichen Verhältnisses in X- und Y-Beträgen.
* **Position**
  * **Position zufällig**: *0.0 - 2.0* Position für zufälligen Versatz für jede Kachel.
  * **Zufallsverteilung**: *Gaußsch, Gleichmäßig* Legt die Berechnung fest, die für den vorherigen Parameter verwendet werden soll. Macht keinen großen Unterschied, auffälliger mit hohen Zahlen. Gaußsche Proportionen neigen dazu, eine gleichmäßigere Verteilung zu geben.
  * **Vektorkartenmultiplikator**: *0.0 - 1.0* Einfluss der Vektoreingabekarte auf Offsets.
  * **Horizontaler Versatz**: *-2.0 - 2.0* Globaler horizontaler Offset.
  * **Vertikaler Versatz**: *-2.0 - 2.0* Globaler vertikaler Offset.
  * **Out-of-Bounds-Option**: *Form skalieren, Position beschränken* Aktion, die ausgeführt wird, wenn eine Kachel außerhalb des gültigen Bereichs angezeigt wird.
* **Drehung**
  * **Drehung**: *0.0 - 1.0* Dreht alle Kacheln global.
  * **Drehung zufällig**: *0.0 - 1.0* Rotiert willkürlich pro Kachel.
  * **Drehung aus Bg-Steigung**: *0.0 - 1.0* Verwendet die Steigung der Hintergrundzuordnung (berechnet als &quot;Normal&quot;) zum Drehen von Kacheln. Kann verwendet werden, um Formen auf Steigungen nach oben oder unten zeigen zu lassen.
  * **Rotation Map-Multiplikator**: *0.0 - 1.0*&#x200B;Überblendungen im Effekt des Rotation Map bei der Drehung pro Kachel.
  * **Vektorkartenmultiplikator**: *0.0 - 1.0*&#x200B;Überblendungen im Effekt des Rotation Map bei der Drehung pro Kachel.
* **Height**
  * **Automatische Anpassung der Height-Skalierung**: *Falsch/Wahr* Passen Sie den Bereich des Heights automatisch relativ zum Hintergrund an, anstatt einen absoluten Bereich zu definieren. Ermöglicht weniger oder mehr Kontrolle.
  * **Height-Offset**: *-1.0 - 1.0* Modifizierer zum gleichmäßigen Versetzen/Verschieben aller Kacheln durch den Bereich des Heights.
  * **Height-Offset zufällig**: *0.0 - 1.0*&#x200B;Ändert den Height-Offset zufällig pro Kachel.
  * **Height-Versatzzuordnungs-Multiplikator**: *0.0 - 1.0* Modifizierer zum Festlegen des Einflusses der Offset-Map.
  * **Height-Skalierung**: *0.0 - 1.0* Modifizierer zum gleichmäßigen Skalieren/Erweitern aller Kacheln über den Bereich des Heights. Im Gegensatz zum Offset werden dabei Werte wie der Kontrast weiter auseinander getrieben.
  * **Zufällige Skalierung des Heights**: *0.0 - 1.0*&#x200B;Ändert zufällig die Skalierung des Heights pro Kachel.
  * **Height-Skalierungszuordnungsvervielfacher**: *0.0 - 1.0* Modifizierer zum Festlegen des Einflusses der Skalierungszuordnung.
  * **Mit Hintergrund konform**: *0.0 - 1.0* Wirkt sich auf das Mischen von Kacheln mit Hintergrund aus. Keine konformen Mittel Höhenkarten bleiben starr, konforme Mittel folgen der Hintergrundform. Gut für Blätter oder Stöcke zum Beispiel.
  * **Glätten konformer Hintergrund**: *0.0 - 2.0* Glättungswert für den vorherigen Effekt, um falsche oder extreme Variationen zu vermeiden.
  * **Neigung von Bg-Steigung**: *0.0 - 1.0* Passen Sie das Height der Kachel für die Steigung an, das von der Steigung des Hintergrunds gesteuert wird (berechnet als Normal).
  * **Smoothness der Hintergrund-Steigung**: *0.0 - 2.0* Glättungswert für den vorherigen Effekt, um falsche oder extreme Variationen zu vermeiden.
  * **Schwarze Pixel ausschneiden**: *Falsch/Wahr* Schalten Sie um, um schwarze (0) Pixel von Kachelgrundformen zu ignorieren.
  * **Reduzierte Musterbasis**: *Falsch/Wahr* Passt das Kachelmischverhalten mit dem Hintergrund an: -Kacheln schneiden sich entweder mit dem Hintergrund (False) oder überschreiben den Hintergrund, wenn sie niedriger sind.
* **Maskieren**
  * **Zufällige Maske**: *0.0 - 1.0* Blendet Kacheln zufällig aus. Je höher dieser Wert ist, desto mehr Kacheln werden ausgeblendet.
  * **Zufällige Maskenzuordnungsvervielfacher**: *0.0 - 1.0* Schwellenwert für Maskenzuordnung, wenn mit dem Ausblenden von Kacheln begonnen werden soll.
  * **Maske aus Bg-Steigung**: *-1.0 - 1.0* Verwendet die Steigung der Hintergrundzuordnung (berechnet als &quot;Normal&quot;), um Kacheln auszublenden.

## Beispielbilder

</td>
</tr>
</table>

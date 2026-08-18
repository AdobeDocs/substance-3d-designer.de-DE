---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Mit dem Knoten "Dreidimensional planar" können Sie Texturen aus drei orthogonalen Ebenen projizieren, um eine nahtlose Texturzuordnung auf komplexe Geometrie zu ermöglichen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tri Planar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Tri Planar

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## Tri Planar (Graustufen)

**In:** *Mesh-basierte Generatoren**/Dienstprogramme*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser erweiterte Knoten führt eine dreiplanare Projektionszuordnung in 2D durch, basierend auf den Daten &quot;Backed Position&quot; und &quot;World Space Normal&quot;. Das bedeutet, dass UV-Koordinaten im Wesentlichen vollständig in eine (meist) nahtlose Abbildung auf Basis des Gitters selbst konvertiert werden.

Dies ist eine gute Möglichkeit, Nähte zu vermeiden, ohne jedes Mal nachbacken zu müssen (es ist möglich, etwas Ähnliches mit dem Bäcker zu erreichen). Der Nachteil ist, dass dieser Knoten ziemlich schwer und damit nicht schnell ist.

Denken Sie daran, dass Ihre Backen sehr präzise sein sollten: 8-Bit-Backen führen nicht zu sehr schönen Ergebnissen.

## Parameter

### Eingaben

* **Position**: *Farbeingabe*\
  Backed-Positions-Map. Idealerweise 16-Bit oder höher.
* **Normaler Weltraum**: *Farbeingabe*\
  Baked World Space Normal Karte, Idealerweise 16-Bit oder höhere Präzision.
* **Eingabe X**: *Farbeingabe (Graustufeneingabe)*Eingabemap zur Neuzuordnung von UV zum Weltraum über Triplanar-Projektion. Wird für alle Achsen verwendet, wenn &quot;Bildeingaben&quot; auf 1 gesetzt ist, für die X-Achse, wenn auf 3 gesetzt.
* **Eingabe Y**: *Farbeingabe (Graustufeneingabe)*Nur wenn &quot;Bildeingabe&quot; auf 3 eingestellt ist. Eingabe-Map, um von UV zum Weltraum auf der Y-Achse neu zuzuordnen.
* **Eingabe Z**: *Farbeingabe (Graustufeneingabe)*Nur wenn &quot;Bildeingabe&quot; auf 3 eingestellt ist. Eingabe-Map, um von UV zum Weltraum auf der Z-Achse neu zuzuordnen.

### Parameter

* **Projektion**: *Alle Achsen, nur X, nur Y, nur Z* Legt fest, welche Achsen angeglichen werden sollen.
* **Image-Eingaben**: *1 Eingabe, 3 Eingaben*\
  Legen Sie fest, ob eine Karte für alle Achsen oder eine bestimmte Karte pro Achse verwendet werden soll.
* **Füllmethode**: *linear, erweitert* Erhöht Genauigkeit und Präzision.
* **Füllmethode**: *0.001 - 1.0*&#x200B;Übergangskontrast, Übergang zwischen glatten oder harten Übergängen.
* **Normalisierungsfaktor**: *0.0 - 1.0*\
  Verbessert die Projektionsüberblendung, indem der Kontrastverlust im Überblendungsbereich wiederhergestellt wird.
* **Texturkachelung**: *0.0 - 10.0* Anzahl der Kacheln der Eingabetexturen.
* **Globale Drehung**: *0.0 - 1.0*\
  Globale Drehung für alle Achsen.
* **Gespiegelte Projektion korrigieren**: *Falsch/Wahr* Legen Sie fest, wie gespiegelte Projektionen behandelt werden.
* **Drehung X**: *0.0 - 1.0* Einzelne Drehung über die X-Achse der Projektion.
* **Drehung Y**: *0.0 - 1.0* Einzelne Drehung über die Y-Achse der Projektion.
* **Drehung Z**: *0.0 - 1.0* Einzelne Drehung um die Z-Achse der Projektion.
* **Versatz X**: *0.0 - 1.0* Versatz über die X-Achse der Projektion.
* **Zufälliger Versatz X**: *0.0 - 1.0*\
  Zulassen, dass der Versatz der X-Achse zufällig gewählt wird.
* **Versatz Y**: *0.0 - 1.0* Versatz über Y-Achse der Projektion.
* **Zufallsversatz Y**: *0.0 - 1.0*\
  Zulassen, dass der Y-Achsenversatz randomisiert wird.
* **Versatz Z**: *0.0 - 1.0* Versatz über Z-Achse der Projektion.
* **Zufallsversatz Z**: *0.0 - 1.0*\
  Zulassen, dass der Versatz der Z-Achse randomisiert wird.

## Beispielbilder

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Knotenzuordnung", um Werte über verbundene Regionen mithilfe von Flutfüllungsalgorithmen für die Texturverarbeitung zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# Flood Fill Mapper

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## Flood Fill Mapper (Graustufen)

**In:** *Filter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Flood Fill Mapper ermöglicht die Neuzuordnung eines bestehenden Musters oder einer bestehenden Textur auf jede einzelne Zelle eines [Flood Fills](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Sie unterscheidet sich von anderen Farbkonvertierungen wie [Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) oder [Gradient](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) insofern, als sie keine Volltonfarben oder -werte generiert, sondern Ihnen die Verwendung eigener Eingabemaps ermöglicht. Es kann als eine Art Kombination aus [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) und [Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) oder [Formenzuordnung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md) angesehen werden, da es einige ähnliche Steuerelemente und Schnittstellen bietet.

Die Farbversion verfügt über zusätzliche Steuerelemente für die Arbeit mit Normalzuordnungen, wobei sie [die Normapdrehungen des Tangentenraums kompensieren kann](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

## Parameter

### Eingaben

* **Flood Fill-Box**: *Farbeingabe* Standardfarbeingabe, Flood Fill erforderlich.
* **Mustereingabe 1-8**: *Graustufen-/Farbeingabe*\
  Benutzerdefinierte Musterbildeingabe.
* **Musterverteilungszuordnung**: *Graustufen-Eingabe* ID-Karte, um zu bestimmen, welches Muster zu welcher Zelle führt. Kann von anderen Indexzuordnungen stammen, z. B. vom Flood Fill zum Flood Fill.
* **Skalierungszuordnung**: *Graustufeneingabe* Karte, um die Skalierung pro Zelle zu bestimmen.
* **Rotation Map**: *Graustufeneingabe* Karte zur Bestimmung der Drehung pro Zelle.
* **Luminanzversatzkarte**: *Graustufeneingabe* Karte zum Festlegen der Luminanz pro Zelle

### Parameter

* **Kachelmodus**: *Kein Kacheln, H+V* Legen Sie fest, ob Kacheln verwendet werden soll oder nicht. Nur sichtbar, wenn Größe oder Skalierung unter 1 eingestellt sind.
* **Muster**
  * **Mustereingabenummer**: *1 - 8* Menge der zu verwendenden benutzerdefinierten Mustereingaben festlegen.
  * **Musterverteilungsmodus**: *Zufällig, Formgröße, Verteilungszuordnungs-Eingabe* Legen Sie die Methode fest, um zu bestimmen, welches Muster in einer Zelle angezeigt wird.
  * **Musterverteilung-Jittering**: *0.0 - 1.0* Ermöglicht eine geringfügige Änderung oder einen Versatz in der Musterverteilung, ohne alles durch die Zufallsverteilung zu ändern.
* **Größe**
  * **Größenmodus**: *Relativ zur Textur, Relativ zur Form BSphere, Relativ zur größten Form, Relativ zur kleinsten Form, Formfeld anpassen* Legen Sie fest, wie die Größe des Musters in jeder Zelle bestimmt wird.
  * **Größe**: *0.0 - 1.0* Ermöglicht eine ungleichmäßige Skalierung des Musters.
  * **Skalierung**: *0.0 - 1.0*\
    Legen Sie die globale (einheitliche) Skalierung für den Effekt fest.
  * **Zuordnungsmultiplikator für Skalierung**: *0.0 - 1.0* Legen Sie den Einfluss der optionalen Skalierungszuordnung fest.
  * **Zufällige Skalierung**: *-1.0 - 1.0* Legen Sie die Stärke der zufälligen Variation innerhalb der Musterskala fest.
* **Drehung**
  * **Drehung**: *0.0 - 1.0* Legen Sie die globale, einheitliche Drehung für jede Zelle fest.
  * **Rotation Map-Multiplikator**: *0.0 - 1.0* Legen Sie den Einfluss der optionalen Rotation Map fest.
  * **Drehung zufällig**: *0.0 - 1.0* Legen Sie den Grad der zufälligen Drehung für jede Zelle fest.
  * **Automatische Drehungsskalierung**: *Falsch/Wahr* Legen Sie fest, ob ein Muster seine Skalierung anpassen soll, damit es beim Drehen in eine Zelle passt.
* **Position**
  * **Positionsversatz**: *0.0 - 1.0* Legen Sie den globalen Positionsoffset für jede Zelle fest.
  * **Ausrichtung des Positionsversatzes**: *Textur, Muster* Legen Sie fest, dass der Versatz 0 Punkt entweder an der Zelle &quot;Pattern&quot; oder an der Textur ausgerichtet wird.
  * **Positionsversatz zufällig**: *0.0 - 1.0* Legen Sie den Umfang der Offset-Randomisierung für die Position pro Zelle fest.
* **Color** (Nur für Graustufenversion)
  * **Luminanzbereich**: *0.0 - 1.0* Legt den globalen Kontrast für die Textur fest, wobei 0 zu Mittelgrau wird.
  * **Luminanzbereich zufällig**: *0.0 - 1.0* Legt den Grad der Randomisierung für den Luminanzbereich fest.
  * **Luminanzversatz**: *-1.0 - 1.0* Legt den Offset für die Luminanz fest, die als Helligkeitssteuerung fungiert.
  * **Luminanzversatz zufällig**: *0.0 - 1.0* Legt den Grad der Randomisierung für den Luminanzversatz fest.
  * **Luminanzversatzzuordnungs-Multiplikator**: *0.0 - 1.0* Legt den Einfluss der optionalen Luminanzversatzkarte fest.
  * **Hintergrundfarbe**: *(Graustufenwert)*Legt die Hintergrundfarbe fest, mit der die Texturen vermischt werden.
* **Color** (Nur für Farbversion)
  * **ist normale Karte**: *Falsch/Wahr* Legt fest, dass die Mustereingabe als normale Karte interpretiert wird. Ausgleich und Korrektur der normalen Tangenten-Raumdrehung.
  * **Normales Format**: *DirectX, OpenGL*\
    Wechseln zwischen verschiedenen Normalen-Map-Format (invertiert den grünen Kanal). Nur aktiv, wenn &quot;Ist Normalmap&quot; auf &quot;True&quot; gesetzt ist.
  * **HSL-Anpassung**: *-1.0 - 1.0* Passen Sie HSL global an.
  * **HSL Random**: *-1.0 - 1.0* Legen Sie die HSL-Randomisierung pro Zelle fest.
  * **Alpha-Korrektur**: *-1.0 - 1.0* Legen Sie die globale Alpha-Anpassung fest, um den Alpha-Kontrast zu reduzieren.
  * **Alpha zufällig**: *-1.0 - 1.0* Zufällige Anpassung der Alphas pro Zelle festlegen.
  * **Hintergrundfarbe**: *(Farbwert)*Legt die Hintergrundfarbe fest, mit der Strukturen vermischt werden.

.

## Beispielbilder

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>

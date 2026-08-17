---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Spritzen", um Formen über Texturen hinweg Streuung, um zufällige Muster und organische Texturdetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spritzer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Spritzer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## Farbspritzer (Farbe)

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Splatter ist ein Mustergenerator, der für die zufällige Platzierung eines Karteneingangs vorgesehen ist. Es verfügt über viele Steuerelemente für die geometrisch gemusterte Platzierung und ist einfacher in der Verwendung als [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Letzteres kann ähnliche Ergebnisse erzielen, ist aber viel komplexer.

Spritzer eignen sich gut, um schnell einige Formen zu stempeln, ohne dass zu viele Anpassungen erforderlich sind.

Beachten Sie, dass die standardmäßigen Splatter-Parameter überhaupt nicht zufällig aussehen: Sie müssen einige von ihnen anpassen, um randomisiert zu werden (hauptsächlich die Parameter der Störung). Beachten Sie auch, dass Splatter eine Map-Eingabe erfordert, um zu arbeiten.

## Parameter

* **Breite der Mustergröße**: *0.0 - 1000.0* Anzahl der Muster, die auf der X-Achse verwendet werden sollen.
* **Height der Mustergröße**: *0.0 - 1000.0* Anzahl der Muster, die auf der Y-Achse verwendet werden sollen.
* **Drehung**: *-360.0 - 360.0* Dreht jedes Muster um einen bestimmten Betrag.
* **Drehungsvariation**: *0.0 - 360.0* Führt eine zufällige Drehung für jede einzelne Form ein.
* **Zoom**: *100.0 - 10000.0* Skaliert das Endergebnis. Denken Sie daran, dass dies Kacheln bricht!
* **Verstärkung**: *0.0 - 10.0* Passt die Mischverstärkung jedes Musters an. Sie heben sich besser ab.
* **Schwenken X**: *-100.0 - 100.0* Schwenken des gesamten Ergebnisses auf der X-Achse.
* **Pan Y**: *-100.0 - 100.0* Schwenken des gesamten Ergebnisses auf der Y-Achse.
* **Störung**: *0.0 - 100.0*\
  Verschiebt Formen zufällig.
* **Rasternummer**: *0 - 8* Wechselt durch verschiedene Rastergrößen, um die Ergebnisskala anzupassen. Beibehält die Unterteilung bei.
* **Störungswinkel**: *0.0 - 360.0* Steuert den Winkel der Verschiebung der Störung.
* **Zufallsstörung**: *Falsch/Wahr* Zufallswerte für den Störungswinkel, was zu noch mehr Chaos führt.
* **Mustergröße**: *5 - 12*
* **Größenänderung**: *0.0 - 100.0* Führt eine zufällige Skalierung für jede Form ein.
* **Image Input Filtering (nur Engine > v4)**: *Bilinear + Mipmaps, Bilinear, Nächste* Welche Filter auf das Eingabebild angewendet werden sollen.
* **Min. für Ausgangspegel**: *0.0 - 1.0* Einstellung der Mindeststufe ist nicht verfügbar.
* **Max. Ausgangspegel**: *0.0 - 1.0* Maximale Pegelanpassung überschritten.
* **Hintergrundfarbe**: *(Graustufenwert)*Legt die einfarbige Hintergrundfarbe fest.
* **Luminanzvariation**: *0.0 - 1.0 (nur Graustufenversion)*Führt Luminanzvariation ein.
* **Farbvariation**: *0.0 - 1.0 (Nur Farbversion)*Führt Farbvariationen ein.

## Beispielbilder

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>

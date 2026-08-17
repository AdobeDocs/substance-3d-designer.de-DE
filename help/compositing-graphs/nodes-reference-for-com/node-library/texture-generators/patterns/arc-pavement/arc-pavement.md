---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Pflaster, um bogenförmige Pflastermuster zum Erstellen gekrümmter Straßen- und Pfadstrukturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bogenpflaster
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Bogenpflaster

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## Bogenpflaster

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert ein Pariser Bogen-Straßenmuster. Dieser Effekt kann nicht mit dem Standardknoten &quot;[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)&quot; oder &quot;[Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)&quot; erzielt werden, daher dieser dedizierte Knoten.

## Parameter

* **Skalierung**: *1 - 8* Legt die globale Skalierung/Unterteilung fest.
* **Mustermenge**: *1 -* 32\
  Legt die Anzahl der in jedem Bogen verwendeten Steine fest.
* **Zufälliger Musterbetrag**: *0.0 - 1.0*\
  Zufallswerte für die Anzahl der Steine in jedem Bogen. Hat den zusätzlichen Effekt, dass Ziegelsteine verschiedene Schuppen.
* **Mindestgröße des Musters**: *1 - 10*\
  Steuert die Mindestmenge an Steinen, wenn Bögen randomisiert werden.
* **Bogenbetrag**: *0 - 20*\
  Legt die Stärke der vertikal gestapelten Bögen fest. Ändert das Height der Steine.
* **Muster**: *Eingabebild, Quadrat, Disc, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Abstufungen, Wellen, Halbglocke, Gekrächelte Glocke, Halbmond, Kapsel, Kegel*\
  Wählt die zu verwendende Musterform aus.
* **Eingangsbildfilter**: *Bilinear + Mipmaps, Bilinear, Nächste*
* **Musterskalierung**: *0.0 - 1.0* Legt die Skalierung für jede Kachel fest.
* **Musterbreite**: *0.0 - 1.0*\
  Legt die Breite für jedes Teil fest.
* **Pattern-Height**: *0.0 - 1.0*\
  Legt das Height für jede Kachel fest.
* **Zufällige Musterbreite**: *0.0 - 1.0*\
  Weist der Kachelbreite Zufallswerte zu.
* **Muster-Height zufällig**: *0.0 - 1.0*\
  Randomisiert Kachel-Height.
* **Globale Musterbreite zufällig**: *0.0 - 1.0* Randomisiert die Kachelbreite, ohne größere Lücken zwischen den Kacheln zu erstellen.
* **Pattern Height Verringern**: *0.0 - 1.0* Steuert das Quetschen des Heights an den Enden jedes Bogens.
* **Farbzufall**: *0.0 - 1.0*\
  Randomisiert Kachelfarben.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.

## Beispielbilder

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>

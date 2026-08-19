---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Verwenden Sie den Shape -Knoten, um grundlegende geometrische Formen zum Erstellen von Mustern und Texturen in Substance 3D Designer zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Form
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Form

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## Form

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Vielzahl von prozeduralen Formen mit Optionen zum Ändern von Grundformen. Die Formen sind immer perfekt interpoliert und präzise.

Trotz seiner Einfachheit ist dies ein sehr nützlicher Knoten: Es ist der Baustein der meisten prozeduralen Heightmap-Generierung! Durch das Kombinieren einfacher Formen mit Transformationsknoten können Sie eine vollständig prozedurale Höhenkarte erstellen, die viel präziser ist als jede Bitmap.

## Parameter

* **Anordnen**: *1 - 16*\
  Legt fest, wie oft das Ergebnis gekachelt werden soll.
* **Muster**: *Quadrat, Disc, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Gradation, Wellen, Halbglocke, Glockenrippe, Kreskant, Kapsel, Kegel*, Hemisphäre**\
  Wählt die zu verwendende Musterform aus.
* **Musterspezifisch**: *0.0 - 1.0*\
  Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab.
* **Skalierung**: *0.0 - 1.0* Skaliert die gesamte Form.
* **Größe**: *0.0 - 1.0* Ermöglicht eine ungleichmäßige Skalierung über die X- oder Y-Achse.
* **Winkel**: *0.0 - 1.0* Dreht die gesamte Form.
* **Drehung 45°**: *Falsch/Wahr* Dreht sich um voreingestellte 45 Grad.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.
* **Kachelung (nicht quadratisch)**&#x200B;**:** *Falsch/Wahr*Wenn die Quadratische Ausbreitung aktiviert ist, wird die Form ohne Unterdrücken kachelbar.

## Beispielbilder

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>

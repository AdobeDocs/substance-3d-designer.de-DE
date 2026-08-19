---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D-Knoten "Planare Projektion", um Texturen mithilfe planarer Projektionen für die Texturzuordnung auf Gitteroberflächen zu projizieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Projektion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 3D-Projektion

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## 3D-Projektion (Farbe)

**In:** *Mesh-basierte Generatoren**/Dienstprogramme*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt eine planare Projektion auf der Grundlage von Gitterdaten aus (Position und Normal-Weltkarte). Ermöglicht es Ihnen, Aufkleber über Nähte zu projizieren und zu platzieren, unabhängig von der ursprünglichen UV-Zuordnung.

## Parameter

### Eingaben

* **Positionszuordnung**: *Farbeingabe* Karte der gebackenen Position
* **Normaler Weltraum**: *Farbeingabe* Normalmap für gebackenen Weltraum
* **Projizierte Textur**: *Farbeingabe* Geben Sie Textur in das Projekt auf das Ziel ein.

### Parameter

* **Positionierung**
  * **Projekteingabe**: *UV-Position, Weltraumposition* Wählen Sie aus, ob die Projektionsposition in 2D/UV oder 3D/Weltraum festgelegt wird.
  * **UV-Zielposition**:\
    Nur mit UV-Positionseingabe, am besten verwendet, um einen Punkt in der 2D-Ansicht auf der Positionskarte auszuwählen.
  * **Zielposition**: *(Farbwert)*Nur mit der Weltraum-Positionseingabe können Sie eine exakte 3D-Koordinate definieren.
  * **Ziel Normal**: *(Farbwert)*
  * **Drehung**: *0.0 - 1.0\
    Dreht die projizierte Textur entlang ihrer normalen Achse.*
  * **Skalierung**: *0.0 - 1.0*\
    Lege die globale Skalierung für die projizierte Struktur fest.
  * **Größe**: *0.0 - 2.0* Führen Sie eine ungleichmäßige Skalierung der projizierten Textur durch.
* **Maskieren**
  * **Maximale Tiefe**: *0.0 - 1.0* Steuert, wie tief die projizierte Textur erscheint, wenn sie abgeschnitten wird.
  * **Tiefe Fade**: *0.0 - 1.0* Stellen Sie die Überblendung für die abgeschnittene Tiefe als abrupt oder verblasst ein.
  * **Normaler Schwellenwert**: *-1.0 - 1.0* Legen Sie den Schwellenwert für Flächen fest, die nicht genau mit der Projektionsnormalen ausgerichtet sind.
  * **Normale Überblendung**: *0.0 - 1.0* Stellen Sie den Übergang für Flächen ein, die nicht auf plötzliche Überblendungen ausgerichtet sind.

## Beispielbilder

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Scratches-Generator, um prozedurale Kratzmuster zum Hinzufügen von Verschleiß und Beschädigung von Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scratches Generator
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Scratches Generator

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Scratches-Generator (Normal)

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies setzt zufällige Kratzer mit vielen Anpassungsoptionen, zum Beispiel, die es Ihnen ermöglichen, die Richtung, den Abstand und die Verzerrung festzulegen.

Es gibt eine Sonderversion von Scratches Generator, Scratches Generator Normal, die Normalmaps generiert, die auf der Tiefe dieser Kratzer basieren. Die meisten Optionen sind identisch, aber es gibt einige zusätzliche Parameter, die für die normalen Einstellungen deutlich gekennzeichnet sind (siehe unten).

## Parameter

* **Spline-Nummer**: *1 - 512* Anzahl der zu platzierenden Kratzer (Splines).
* **Max. Segmente pro Spline**: *2 - 256* Anzahl der Segmente/Unterteilungen über die Länge eines Kratzers. Ermöglicht glattere Kurven und Verzerrungen. Dieser Effekt ist bei höheren Verzerrungen deutlicher zu erkennen.
* **Spline-Drehung**: *0.0 - 1.0* Gleichmäßige Drehung aller Splines, um sie in einer Richtung auszurichten.
* **Spline-Drehung zufällig**: *0.0 - 1.0* Winkelvariationen, die jeden Spline zufällig drehen.
* **Spline-Skalierung**: *0.0 - 1.0* Skaliert alle Splines gleichmäßig.
* **Spline-Skalierung zufällig**: *0.0 - 1.0* Skaliert jeden Spline zufällig einzeln.
* **Spline-Verzerrung**: *0.0 - 1.0* Einheitliche Verzerrung über alle Splines hinweg.
* **Spline-Verzerrung zufällig**: *0.0 - 1.0* Die Verzerrung jedes Splines wird einzeln zufällig festgelegt.
* **Häufigkeit der Spline-Verzerrung**: *0.0 - 1.0* Legt die Häufigkeit der Verzerrung fest und steuert die Detailskalierung der Verzerrung.
* **Spline Width**: *0.0 - 2.0* Legt die Breite aller Splines gleichmäßig fest.
* **Spline Width Random**: *0.0 - 1.0* Die Spline-Breite jedes Splines wird einzeln zufällig festgelegt.
* **Spline-Position zufällig**: *0.0 - 1.0* Die Position jedes Splines wird einzeln randomisiert. Je niedriger dieser Wert ist, desto mehr Splines werden zur Mitte der Arbeitsfläche gruppiert. Kann verwendet werden, um Flecken von Kratzern zu erstellen.
* **Spline-Breite in px** festlegen: *Falsch/Wahr* Bestimmt die Einheiten, die für Spline-Breiteneinstellungen verwendet werden.
* **Luminanzzufall (nur Graustufenversion)**: *0.0 - 1.0* Die Luminanz jedes Splines wird einzeln zufällig angepasst.
* **Normalintensität (nur normale Version)**: *0.0 - 1.0* Legt die Stärke des Effekts &quot;Normal&quot; für jeden Spline global fest.
* ** Zufällige ** bei normaler Intensität (nur normale Version)****: *0.0 - 1.0*Randomisiert die normale Stärke für jeden Spline einzeln.
* ** Normales Format **(nur normale Version)****: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
* **Überblendmodus**: *Ohne, Anfang, Ende, Anfang + Ende* Legt fest, ob und in welche Richtung die Splines verblassen.
* **Überblendungslänge**: *0.0 - 1.0* Legt die Länge des Überblendungseffekts fest, sofern oben aktiviert.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>

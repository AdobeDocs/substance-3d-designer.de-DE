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
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# Tri Planar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/triplanar-1.png){width="128px"}

![](tri-planar.resources/triplanar-grayscale.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser erweiterte Knoten führt eine dreiplanare Projektionszuordnung in 2D durch, basierend auf den Daten &quot;Backed Position&quot; und &quot;World Space Normal&quot;. Das bedeutet, dass UV-Koordinaten im Wesentlichen vollständig in eine (meist) nahtlose Abbildung auf Basis des Gitters selbst konvertiert werden.

Dies ist eine gute Möglichkeit, Nähte zu vermeiden, ohne jedes Mal nachbacken zu müssen (es ist möglich, etwas Ähnliches mit dem Bäcker zu erreichen). Der Nachteil ist, dass dieser Knoten ziemlich schwer und damit nicht schnell ist.

Denken Sie daran, dass Ihre Backen sehr präzise sein sollten: 8-Bit-Backen führen nicht zu sehr schönen Ergebnissen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Position</b> <i>Farbeingabe</i> | Backed-Positions-Map. Idealerweise 16-Bit oder höher. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> | Baked World Space Normal Karte, Idealerweise 16-Bit oder höhere Präzision. |
| <b>Eingabe X</b> <i>Farbeingabe (Graustufeneingabe)</i> | Eingabe-Map für die Neuzuordnung von UV zu Welt-Raum per Triplanare Projektion. Wird für alle Achsen verwendet, wenn &quot;Bildeingaben&quot; auf 1 gesetzt ist, für die X-Achse, wenn auf 3 gesetzt. |
| <b>Eingabe Y</b> <i>Farbeingabe (Graustufeneingabe)</i> | Nur, wenn &quot;Bildeingaben&quot; auf 3 eingestellt ist. Eingabe-Map, um von UV zum Weltraum auf der Y-Achse neu zuzuordnen. |
| <b>Eingabe Z</b> <i>Farbeingabe (Graustufeneingabe)</i> | Nur, wenn &quot;Bildeingaben&quot; auf 3 eingestellt ist. Eingabe-Map, um von UV zum Weltraum auf der Z-Achse neu zuzuordnen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Projektion</b> <i>Alle Achsen, nur X, nur Y, nur Z</i> | Legt fest, mit welchen Achsen gemischt werden soll. |
| <b>Image-Eingaben</b> <i>1 Eingabe, 3 Eingaben</i> | Legen Sie fest, ob eine Karte für alle Achsen oder eine bestimmte Karte pro Achse verwendet werden soll. |
| <b>Füllmethode</b> <i>linear, erweitert</i> | Höhere Präzision und Genauigkeit. |
| <b>Füllkontrast</b> <i>0.001 - 1.0</i> | Überblendungskontrast, Überblendung zwischen glatten oder harten Übergängen. |
| <b>Normalisierungsfaktor</b> <i>0.0 - 1.0</i> | Verbessert die Projektionsüberblendung, indem der Kontrastverlust im Überblendungsbereich wiederhergestellt wird. |
| <b>Textur Kachelung</b> <i>0.0 - 10.0</i> | Anzahl der Male, die die Eingabe-Texturen kacheln sollen. |
| <b>Globale Drehung</b> <i>0.0 - 1.0</i> | Globale Drehung für alle Achsen. |
| <b>Gespiegelte Projektion korrigieren</b> <i>False/True</i> | Legen Sie fest, wie gespiegelte Projektionen behandelt werden. |
| <b>Drehung X</b> <i>0.0 - 1.0</i> | Einzelne Drehung über Projektion X-Achse. |
| <b>Drehung Y</b> <i>0.0 - 1.0</i> | Einzelne Drehung um die Y-Achse der Projektion. |
| <b>Drehung Z</b> <i>0.0 - 1.0</i> | Einzelne Drehung um die Z-Achse der Projektion. |
| <b>Versatz X</b> <i>0.0 - 1.0</i> | Versatz über Projektion X-Achse. |
| <b>Zufälliger Versatz X</b> <i>0.0 - 1.0</i> | Zulassen, dass der Versatz der X-Achse zufällig gewählt wird. |
| <b>Versatz Y</b> <i>0.0 - 1.0</i> | Versatz über die Y-Achse der Projektion. |
| <b>Zufallsversatz Y</b> <i>0.0 - 1.0</i> | Zulassen, dass der Y-Achsenversatz randomisiert wird. |
| <b>Versatz Z</b> <i>0.0 - 1.0</i> | Versatz über die Z-Achse der Projektion. |
| <b>Zufallsversatz Z</b> <i>0.0 - 1.0</i> | Zulassen, dass der Versatz der Z-Achse randomisiert wird. |

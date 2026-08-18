---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Form-Extrudieren", um Formen zu extrudieren und 3D-ähnliche Tiefe-Effekte in Substance 3D Designer-Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Form > Extrudieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# Form > Extrudieren

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## Form > Extrudieren

**In:** *Texturgeneratoren**/Muster*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein erweiterter Knoten, mit dem 2D-, binäre &quot;Shape&quot;-Eingaben in 3D-gedrehte Höhenkarten gerendert werden können. Funktioniert ähnlich wie beim Extrudieren in einem 3D-Paket, bei dem eine Form entlang ihrer Achse extrudiert wird, um ein Volumen zu erstellen. In Kombination mit der Profilverlaufsmaske können auch Körper vom Typ Revolution/Drehmaschine erzeugt werden. Sehr nützlich zum Erstellen komplexer künstlicher Formen für Höhenkarten.

## Parameter

### Eingaben

* **Shape-Eingabe extrudieren**: *Graustufen-Eingabe* Wenn die Option &quot;Form extrudieren&quot; auf &quot;Benutzerdefiniert&quot; eingestellt ist, schließen Sie hier Ihre eigene (vorzugsweise) binäre Formmaske an.
* **Profilverlauf**: *Graustufen-Eingabe\
  Wenn der Profiltyp auf &quot;Vertikaler Verlauf&quot; festgelegt ist, kann er verwendet werden, um die Skalierung der Form entlang der Achse für Revolutionskörper zu definieren.*
* **Profilmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Ausblenden oder Anzeigen der extrudierten Form entlang ihrer Achse. Kann verwendet werden, um die Kontinuität der Form entlang ihrer Achse zu unterbrechen. Nur als binär interpretiert: Graustufen-Einstellungswerte werden auf 0 oder 1 gerundet.

### Parameter

* **Height** extrudieren: *0.0 -* 1.0\
  Stärke, um die Form von der Mitte aus nach oben zu extrudieren.
* **Tiefe** extrudieren: *0.0 - 1.0* Menge zum Extrudieren der Form um Downwatds von der Mitte aus.
* **Form** extrudieren: *Cube, Cylinder, Benutzerdefinierte Eingabe* Verwenden Sie entweder integrierte Formen oder geben Sie Ihre eigene benutzerdefinierte Form extern ein.
* **Formgröße extrudieren**: *0.0 - 1.0* Wird nur mit integriertem Würfel und Zylinder verwendet, bestimmt die Grundformgröße, kann ungleichmäßig skaliert werden.
* **Skalierung**: *0.0 - 1.0*\
  Legen Sie die globale Skalierung für den Effekt fest. Bei integrierten Formen handelt es sich um eine einheitliche Grundformskala, die sich nicht auf das Height oder die Tiefe auswirkt.\
  Mit &quot;Benutzerdefinierte Eingabe&quot; wird das gesamte Endergebnis einheitlich skaliert.
* **Profiltyp**: *Linearer, vertikaler Verlauf, Maske* Hauptsteuerung, um das Verhalten des Effekts zu bestimmen und optionale zusätzliche Eingabemaps zu verwenden.\
  &quot;Gerade&quot; ist das Standardverhalten bei der Extrusion, &quot;Vertikaler Verlauf&quot; ermöglicht benutzerdefinierte Skalierungswerte entlang der gesamten Achse, &quot;Maske&quot; ermöglicht das Ausblenden von Abschnitten entlang der Achse durch Maske.
* **Height abschrägen**: *0.0 - 1.0* Legen Sie fest, wie weit die Abschrägung entlang der Extrusionsachse reicht.
* **Abschrägungsintensität**: *0.0 - 1.0* Legen Sie fest, wie stark die Abschrägung von der ursprünglichen Form zurückgezogen wird.
* **Abgeflachte Kurve**: *-1.0 - 1.0* Legen Sie die konvexe oder konkave Kurve des Effekts &quot;Abgeflachte Kante&quot; fest. Ein Wert von 0 bedeutet gerade, keine Kurve.
* **Abgeflachte Kante spiegeln**: *Falsch/Wahr* Schalten Sie um, um &quot;Abgeflachte Kante&quot; sowohl auf den oberen als auch auf den unteren Rand der Form anzuwenden.
* **Multilplier herunterskalieren**: *0 - 2* Integrierte einfache Downskalierungssteuerung. Kann verwendet werden, um schnell Anti-Aliasing hinzuzufügen; Stellen Sie sicher, dass Sie auch die Knotenauflösung erhöhen.
* **Position**:\
  Hauptsteuerung zum Drehen führt zum 3D-Raum. Korreliert mit dem interaktiven Gizmo in der 2D-Ansicht.
* **Ausgabebereich**: *[0, 1], [-1, 1]*Festlegen der Min.- und Max.-Werte für die Ausgabe. Wenn der Bereich auf [-1,1] festgelegt ist, werden negative Werte als schwarz dargestellt.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

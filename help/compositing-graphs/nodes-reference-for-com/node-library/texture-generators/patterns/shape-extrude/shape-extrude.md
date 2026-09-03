---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Form-Extrudieren , um Formen zu extrudieren und 3D-ähnliche Tiefe-Effekte in Substance 3D Designer-Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Form > Extrudieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# Form > Extrudieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude-01.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein erweiterter Knoten, mit dem 2D-, binäre &quot;Shape&quot;-Eingaben in 3D-gedrehte Höhenkarten gerendert werden können. Funktioniert ähnlich wie beim Extrudieren in einem 3D-Paket, bei dem eine Form entlang ihrer Achse extrudiert wird, um ein Volumen zu erstellen. In Kombination mit der Profilverlaufsmaske können auch Körper vom Typ Revolution/Drehmaschine erzeugt werden. Sehr nützlich zum Erstellen komplexer künstlicher Formen für Höhenkarten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Formeingabe extrudieren</b> <i>Graustufen-Eingabe</i> | Wenn die Option &quot;Form extrudieren&quot; auf &quot;Benutzerdefiniert&quot; eingestellt ist, schließen Sie hier Ihre eigene (vorzugsweise) binäre Formmaske an. |
| <b>Profilverlauf</b> <i>Graustufen-Eingabe</i> | Wenn als Profiltyp &quot;Vertikaler Verlauf&quot; festgelegt ist, können Sie die Skalierung der Form entlang der Achse für Revolutionskörper definieren. |
| <b>Profilmaske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Ausblenden oder Anzeigen der extrudierten Form entlang ihrer Achse. Kann verwendet werden, um die Kontinuität der Form entlang ihrer Achse zu unterbrechen. Nur als binär interpretiert: Graustufen-Einstellungswerte werden auf 0 oder 1 gerundet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Height extrudieren</b> <i>0.0 - 1.0</i> | Stärke, um die Form von der Mitte aus nach oben zu extrudieren. |
| <b>Tiefe extrudieren</b> <i>0.0 - 1.0</i> | Menge, um die Form aus der Mitte heraus in Watt zu extrudieren. |
| <b>Form extrudieren</b> <i>Cube, Cylinder, Benutzerdefinierte Eingabe</i> | Verwenden Sie entweder integrierte Formen oder geben Sie eine eigene benutzerdefinierte Form extern ein. |
| <b>Formgröße extrudieren</b> <i>0.0 - 1.0</i> | Nur mit integriertem Würfel und Zylinder verwendet, bestimmt die Grundformgröße, kann ungleichmäßig skaliert werden. |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Legen Sie die globale Skalierung für den Effekt fest. Mit integrierten Formen ist dies eine einheitliche Grundformskala, die sich nicht auf Height oder Tiefe auswirkt.<br><br>Mit benutzerdefinierter Eingabe wird das gesamte Endergebnis einheitlich skaliert. |
| <b>Profiltyp</b> <i>Gerade, Vertikaler Verlauf, Maske</i> | Hauptsteuerung zur Bestimmung des Effektverhaltens und Verwendung von optionalen zusätzlichen Eingabe-Map.<br><br>Straight ist das Standardextrusionsverhalten. Der vertikale Verlauf ermöglicht benutzerdefinierte Skalierungswerte entlang der gesamten Achse. Die Maske ermöglicht das Ausblenden von Abschnitten entlang der Achse durch Maske. |
| <b>Height abschrägen</b> <i>0.0 - 1.0</i> | Legen Sie fest, wie weit die abgeflachte Kante entlang der Extrusions-Achse reicht. |
| <b>Abgeflachte Intensität</b> <i>0.0 - 1.0</i> | Legen Sie fest, wie stark die abgeflachte Kante von der ursprünglichen Form zurückgezogen wird. |
| <b>Abgeflachte Kurve</b> <i>-1.0 - 1.0</i> | Legen Sie die konvexe oder konkave Kurve des Effekts &quot;Abgeflachte Kante&quot; fest. Ein Wert von 0 bedeutet gerade, keine Kurve. |
| <b>Abgeflachte Kante spiegeln</b> <i>False/True</i> | Klicke auf &quot;Abgeflachte Kante&quot;, um die Form sowohl oben als auch unten anzuwenden. |
| <b>Multicalup-Multiplikator herunterskalieren</b> <i>0 - 2</i> | Integrierte, einfache Downskalierungssteuerung. Kann verwendet werden, um schnell Anti-Aliasing hinzuzufügen; Stellen Sie sicher, dass Sie auch die Knotenauflösung erhöhen. |
| <b>Position</b> | Hauptsteuerung zum Drehen führt zum 3D-Raum. Korreliert mit interavtice Gizmo in der 2D-Ansicht. |
| <b>Ausgabebereich</b> <i>[0, 1], [-1, 1]</i> | Legen Sie die Minimal- und Maximalwerte für die Ausgabe fest. Wenn der Bereich auf [-1,1] festgelegt ist, werden negative Werte als schwarz dargestellt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-02.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill Mapper", um Werte über verbundene Regionen mithilfe von Flutfüllungsalgorithmen für die Verarbeitung von Texturen zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Flood Fill Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/flood-fill-mapper-01.png)![](flood-fill-mapper.resources/flood-fill-mapper-02.png)

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Flood Fill Mapper ermöglicht die Neuzuordnung eines bestehenden Patterns oder einer Textur auf jede einzelne Zelle von einem [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Sie unterscheidet sich von anderen Flood Fill-Konvertierungen wie [Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) oder [Gradient](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) insofern, als sie keine Volltonfarben oder -werte generiert, sondern Ihnen ermöglicht, Ihre eigenen Eingabe-Map zu verwenden. Es kann als eine Art Kombination aus [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) und [Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) oder [Formenzuordnung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md) angesehen werden, da es einige ähnliche Steuerelemente und Schnittstellen bietet.

Die Farbversion verfügt über zusätzliche Steuerelemente für die Arbeit mit Normalen-Map, wobei [die Normap-Drehungen im Tangente-Raum kompensieren kann](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Bbox für Flood Fill</b> <i>Farbeingabe</i> | Standardeingabe des Flood Fills, erforderlich. |
| <b>Mustereingabe 1-8</b> <i>Graustufen-/Farbeingabe</i> | Benutzerdefinierte Musterbildeingabe. |
| <b>Musterverteilungszuordnung</b> <i>Graustufen-Eingabe</i> | ID-Map, um festzustellen, welches Muster zu welcher Zelle führt. Kann von anderen Indexzuordnungen stammen, z. B. vom Flood Fill zum Flood Fill. |
| <b>Zuordnungsskalierung</b> <i>Graustufen-Eingabe</i> | Zuordnen, um die Skalierung pro Zelle zu bestimmen. |
| <b>Rotation Map</b> <i>Graustufen-Eingabe</i> | Karte zur Bestimmung der Drehung pro Zelle. |
| <b>Luminanzen-Offset-Map</b> <i>Graustufen-Eingabe</i> | Zuordnen, um die Luminanz pro Zelle festzulegen |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kachelmodus</b> <i>Keine Kachelung, H+V</i> | Legen Sie fest, ob Kachelung verwendet werden soll oder nicht. Nur sichtbar, wenn Größe oder Skalierung unter 1 eingestellt sind. |
| <b>Muster</b> |  |
| <b>Mustereingabenummer</b> <i>1 - 8</i> | Menge der zu verwendenden benutzerdefinierten Mustereingaben festlegen. |
| <b>Musterverteilungsmodus</b> <i>Zufällig, Formgröße, Verteilungszuordnungseingabe</i> | Legen Sie die Methode fest, um zu bestimmen, welches Muster in einer Zelle angezeigt wird. |
| <b>Musterverteilung-Jittering</b> <i>0.0 - 1.0</i> | Ermöglicht eine leichte Variation oder einen Offset in der Musterverteilung, ohne alles durch die Zufallsverteilung zu ändern. |
| <b>Größe</b> |  |
| <b>Größenmodus</b> <i>Relativ zur Textur, Relativ zur Form BSphere, Relativ zur größten Form, Relativ zur kleinsten Form, Formfeld anpassen</i> | Legen Sie fest, wie die Größe des Musters in jeder Zelle bestimmt wird. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Ermöglicht eine ungleichmäßige Skalierung des Musters. |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Legen Sie die globale (einheitliche) Skalierung für den Effekt fest. |
| <b>Zuordnungsmultiplikator skalieren</b> <i>0.0 - 1.0</i> | Legen Sie den Einfluss der optionalen Skalierungszuordnung fest. |
| <b>Zufällige Skalierung</b> <i>-1.0 - 1.0</i> | Legen Sie die Stärke der zufälligen Variation innerhalb der Musterskala fest. |
| <b>Drehung</b> |  |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Legen Sie die globale, einheitliche Drehung für jede Zelle fest. |
| <b>Rotation Map-Multiplikator</b> <i>0.0 - 1.0</i> | Legen Sie den Einfluss des optionalen Rotation Map fest. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Legen Sie den Grad der zufälligen Drehung für jede Zelle fest. |
| <b>Automatische Drehungsskalierung</b> <i>False/True</i> | Festlegen, ob ein Muster seine Skalierung so anpassen soll, dass es beim Drehen in eine Zelle passt. |
| <b>Position</b> |  |
| <b>Positionsversatz</b> <i>0.0 - 1.0</i> | Globaler Positionsoffset für jede Zelle festlegen. |
| <b>Ausrichtung des Positionsversatzes</b> <i>Textur, Muster</i> | Bei Auswahl dieser Option wird der Abstand 0 Punkt entweder an der Zelle Muster oder an der Textur ausgerichtet. |
| <b>Positionsversatz zufällig</b> <i>0.0 - 1.0</i> | Legen Sie den Umfang der Positions-Offset-Randomisierung pro Zelle fest. |
| <b>Farbe (nur für Graustufenversion)</b> |  |
| <b>Luminanzen </b> <i>0.0 - 1.0</i> | Legt den globalen Kontrast auf der Textur fest, wobei 0 zu Mittelgrau wird. |
| <b>Zufälliger Luminanzen-Bereich</b> <i>0.0 - 1.0</i> | Legt den Grad der Zufallsverteilung für den Bereich der Luminanz fest. |
| <b>Luminanzen-Offset</b> <i>-1.0 - 1.0</i> | Legt den Offset für die Luminanz fest. Er funktioniert als Helligkeitsregler. |
| <b>Luminanzen-Offset zufällig</b> <i>0.0 - 1.0</i> | Legt den Grad der Zufallsverteilung für den Luminanz-Offset fest. |
| <b>Luminanzen-Versatzzuordnungs-Multiplikator</b> <i>0.0 - 1.0</i> | Legt den Einfluss der optionalen Luminanz-Offset-Map fest. |
| <b>Hintergrundfarbe</b> <i>(Graustufenwert)</i> | Legt die Hintergrundfarbe fest, mit der Texturen überblendet werden. |
| <b>Farbe (nur für Farbversion)</b> |  |
| <b>Ist Normalen-Map</b> <i>False/True</i> | Legt fest, dass die Mustereingabe als Normalen-Map interpretiert wird. Ausgleich und Korrektur der normalen Tangenten-Raumdrehung. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechseln zwischen verschiedenen Normalen-Map-Format (invertiert den grünen Kanal). Nur aktiv, wenn &quot;Ist Normalmap&quot; auf &quot;True&quot; gesetzt ist. |
| <b>HSL</b> <i>-1.0 - 1.0</i> | Globale HSL. |
| <b>HSL zufällig</b> <i>-1.0 - 1.0</i> | Legen Sie HSL Zufallsverteilung pro Zelle fest. |
| <b>Alpha-Korrektur</b> <i>-1.0 - 1.0</i> | Globale Alpha-Anpassung einstellen, Alpha-Kontrast reduzieren. |
| <b>Alpha zufällig</b> <i>-1.0 - 1.0</i> | Legen Sie die Alpha Adjustment-Randomisierung pro Zelle fest. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Legt die Hintergrundfarbe fest, mit der Texturen überblendet werden. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-04.jpg" />
        </td>
    </tr>
</table>

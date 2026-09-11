---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Verwenden Sie den Formknoten, um grundlegende geometrische Formen zum Erstellen von Mustern und Texturen in Substance 3D Designer zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Form
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# Form

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape.resources/shape-2.png){width="128px"}

<b>In:</b> Texturen > Muster generieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Vielzahl prozeduraler Formen mit Optionen zum Ändern von Grundformen. Die Formen sind immer perfekt interpoliert und präzise.

Trotz seiner Einfachheit ist dies ein sehr nützlicher Knoten: Es ist der Baustein der prozeduralsten Höhenkartengeneration! Wenn Sie Grundformen mit transformieren Knoten kombinieren, können Sie eine vollständig prozedurale Höhenkarte erstellen, die viel präziser ist als jede Bitmap.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kachelung</b> <i>1 - 16</i> | Legt fest, wie oft das Ergebnis gekachelt werden soll. |
| <b>Muster</b> <i>Quadrat, Datenträger, Paraboloid, Glocke, Gaußsch, Dorn, Pyramide, Ziegel, Abstufung, Wellen, Halbglocke, Rändelglocke, Kreskant, Kapsel, Kegel, Hemisphäre</i> | Wählt die zu verwendende Musterform aus. |
| <b>Musterspezifisch</b> <i>0.0 - 1.0</i> | Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab. |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Skaliert die gesamte Form. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Ermöglicht eine ungleichmäßige Skalierung über die X- oder Y-Achse. |
| <b>Winkel</b> <i>0.0 - 1.0</i> | Dreht die gesamte Form. |
| <b>Drehung 45°</b> <i>False/True</i> | Dreht sich bei voreingestellten 45 Grad. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |
| <b>Nicht quadratische Kachelung</b> <i>False/True</i> | Wenn die Quadratische Ausbreitung aktiviert ist, wird die Form ohne Quetschen gekachelt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape.resources/shape-ex.gif" />
        </td>
    </tr>
</table>

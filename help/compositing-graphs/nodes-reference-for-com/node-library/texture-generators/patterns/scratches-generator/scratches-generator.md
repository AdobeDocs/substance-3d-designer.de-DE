---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
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
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# Scratches Generator

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](scratches-generator.resources/scratches-generator.png)

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies setzt zufällige Kratzer mit vielen Anpassungsoptionen, zum Beispiel, die es Ihnen ermöglichen, die Richtung, den Abstand und die Verzerrung festzulegen.

Es gibt eine Sonderversion von Scratches Generator, Scratches Generator Normal, die Normalmaps generiert, die auf der Tiefe dieser Kratzer basieren. Die meisten Optionen sind identisch, aber es gibt einige zusätzliche Parameter, die für die normalen Einstellungen deutlich gekennzeichnet sind (siehe unten).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Spline-Nummer</b> <i>1 - 512</i> | Anzahl der zu platzierenden Kratzer (Splines). |
| <b>Max. Segmente pro Spline</b> <i>2 - 256</i> | Anzahl der Segmente/Unterteilungen über die Länge eines Kratzers. Ermöglicht glattere Kurven und Verzerrungen. Dieser Effekt ist bei höheren Verzerrungen deutlicher zu erkennen. |
| <b>Spline-Drehung</b> <i>0.0 - 1.0</i> | Gleichmäßige Drehung aller Splines, um sie in einer Richtung auszurichten. |
| <b>Spline-Drehung zufällig</b> <i>0.0 - 1.0</i> | Variation des Winkels, dreht jede Spline zufällig. |
| <b>Spline-Skalierung</b> <i>0.0 - 1.0</i> | Skaliert alle Splines gleichmäßig. |
| <b>Spline-Skalierung zufällig</b> <i>0.0 - 1.0</i> | Skaliert jeden Spline zufällig einzeln. |
| <b>Spline-Verzerrung</b> <i>0.0 - 1.0</i> | Einheitliche Verzerrung über alle Splines hinweg. |
| <b>Spline-Verzerrung zufällig</b> <i>0.0 - 1.0</i> | Die Verzerrung jedes Splines wird per Randomisierung angepasst. |
| <b>Häufigkeit der Spline-Verzerrung</b> <i>0.0 - 1.0</i> | Legt die Häufigkeit der Verzerrung fest und steuert die Detailskala der Verzerrung. |
| <b>Spline-Breite</b> <i>0.0 - 2.0</i> | Legt die Breite aller Splines gleichmäßig fest. |
| <b>Spline Width Random</b> <i>0.0 - 1.0</i> | Die Spline-Breite jedes Splines wird einzeln zufällig angepasst. |
| <b>Spline-Position zufällig</b> <i>0.0 - 1.0</i> | Die Position jedes Splines wird individuell zufällig geändert. Je niedriger dieser Wert ist, desto mehr Splines werden in die Mitte der Arbeitsfläche Cluster. Kann verwendet werden, um Flecken von Kratzern zu erstellen. |
| <b>Spline-Breite in px</b> festlegen <i>False/True</i> | Bestimmt die Einheiten, die für die Einstellungen der Spline-Breite verwendet werden. |
| <b>Luminanz zufällig (nur Graustufenversion)</b> <i>0.0 - 1.0</i> | Die Luminanz jedes Splines wird einzeln zufällig geändert. |
| <b>Normalintensität (nur normale Version)</b> <i>0.0 - 1.0</i> | Legt die Stärke des Effekts &quot;Normal&quot; für jeden Spline global fest. |
| <b>Zufällige Normalintensität (nur normale Version)</b> <i>0.0 - 1.0</i> | Randomisiert die normale Stärke für jeden Spline einzeln. |
| <b>Normales Format (nur normale Version)</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Verblassen-Modus</b> <i>Keine, Start, Ende, Start + Ende</i> | Legt fest, ob und in welcher Richtung die Splines Verblassen. |
| <b>Verblassen Länge</b> <i>0.0 - 1.0</i> | Legt die Länge des Verblassen-Effekts fest, sofern oben aktiviert. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex2.png" />
        </td>
    </tr>
</table>

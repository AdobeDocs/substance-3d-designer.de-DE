---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Richtungsbezogene Scratches , um gerichtete Kratzmuster zu erstellen, um Material Abnutzungs- und Schadenseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsverkratzungen
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%
---

# Richtungsverkratzungen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Richtungsabhängige Kratzer - Symbol](directional-scratches.resources/directional_scratches.png "Richtungsabhängige Kratzer - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine zufällige Streuung von Kratzmustern mit einstellbarem Winkel und Größe.

</td>
</tr>
</table>

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das erzeugte Rauschen als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>Integer</i> | Die Unterteilung des Rasters, das zum Erzeugen der Rauschkacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Anisotropie der Störung</b> <i>Gleitend</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Winkel</b> <i>Gleitend</i> | Der Winkel, der verwendet wird, um die Richtung der Kratzer festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Gleitend</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Mustermenge</b> <i>Gleitend</i> | Ein Multiplikator für die Anzahl der gestreuten Kratzmuster. |
| <b>Mustergröße</b> <i>Float2</i> | Die Größe des Begrenzungsrahmens für das neue Muster.    Der Y-Wert steuert die maximale Länge der Kratzer. |
| <b>Zufällige Mustergröße</b> <i>Float2</i> | Ein Multiplikator für den zufälligen Umfang der Downskalierung, der auf die Kratzer angewendet wird.    Der Y-Wert wird auf die Länge der Kratzer angewendet. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Behält bei nicht quadratischen Bildern das erzeugte Kachelquadrat bei und erweitert die Rauschen-Generation auf die Grenzen des Bildes. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="directional-scratches.resources/directional_scratches_1.png" class="modal-image" alt="Richtungsverkratzungen - Beispiel 1" />
        </td>
        <td style="border: 0;">
            <img src="directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.gif" class="modal-image" alt="Richtungsverkratzungen - Beispiel 2" />
        </td>
        <td style="border: 0;">
            <img src="directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.6.gif" class="modal-image" alt="Richtungsverkratzungen - Beispiel 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="directional-scratches.resources/noise-directional-scrat-1.gif" class="modal-image" alt="Richtungsverkratzungen - Beispiel 4" />
        </td>
        <td style="border: 0;">
            <img src="directional-scratches.resources/noise-directional-scrat-2.gif" class="modal-image" alt="Richtungsverkratzungen - Beispiel 5" />
        </td>
        <td style="border: 0;"></td>
    </tr>
</table>

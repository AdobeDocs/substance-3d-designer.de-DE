---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Verwenden Sie den Knotenpunkt Material-Auswahl , um Material auf der Grundlage von Mesh-Daten zum Erstellen von Textur-Effekten mit mehreren Materialien auszuwählen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialauswahl
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Materialauswahl

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector-01.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert eine Vollfarben-ID-Map in eine binäre Schwarz-weiße Maske. Ermöglicht das Mischen und Kombinieren verschiedener Farben zu einer Maske.

Dies ist praktisch, wenn Sie [Multi-Material-Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) nicht verwenden möchten und die Maske lieber manuell verwenden möchten, oder alternativ, wenn Sie dieselben Masken manuell an anderen Speicherorten verwenden möchten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Materials</b> <i>1 - 16</i> | Legt die Anzahl der Materialien fest, für die das Kombinieren aktiviert ist. |
| <b>Material aktivieren #1-16</b> <i>False/True</i> | Schaltet das Mischen und Kombinieren von Farben in die endgültige Ausgabemaske um. Kann für so viele Farben aktiviert werden, wie Sie kombinieren möchten. |
| <b>Material #1-16</b> <i>(Farbwert)</i> | Farbwähler für die Farbe des Materials, die in Schwarzweiß konvertiert wird. |
| <b>Farbwählerparameter</b> | Ändert die Füllmethode und die Konvertierung der Farbe in Schwarzweiß. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Wie viel Farben Sie mit den Nachbarfarben mischen können. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Die Schärfe des Übergangs ist wie &quot;Kontrast&quot;. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/material-selector-02.png" />
        </td>
    </tr>
</table>

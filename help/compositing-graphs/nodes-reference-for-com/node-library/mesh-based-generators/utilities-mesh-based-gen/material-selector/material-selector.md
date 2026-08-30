---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialauswahl , um Materialien basierend auf Gitterdaten auszuwählen, um Textureffekte aus mehreren Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialauswahl
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Materialauswahl

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert eine Vollfarben-ID-Map in eine binäre Schwarzweiß-Maske. Ermöglicht das Mischen und Kombinieren verschiedener Farben zu einer Maske.

Dies ist praktisch, wenn Sie [Multi-Material Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) nicht verwenden möchten und die Maske lieber manuell verwenden möchten, oder alternativ, wenn Sie dieselben Masken manuell an anderen Speicherorten verwenden möchten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Materialien</b> <i>1 - 16</i> | Legt die Anzahl der Materialien fest, für die das Kombinieren aktiviert ist. |
| <b>Material aktivieren #1-16</b> <i>False/True</i> | Schaltet das Mischen und Kombinieren von Farben in die endgültige Ausgabemaske um. Kann für so viele Farben aktiviert werden, wie Sie kombinieren möchten. |
| <b>Material #1-16</b> <i>(Farbwert)</i> | Farbwähler für die Materialfarbe, die in Schwarz-Weiß konvertiert wird. |
| <b>Farbwählerparameter</b> | Ändert die Füllmethode und die Konvertierung der Farbe in Schwarzweiß. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Wie viel Farben Sie mit den Nachbarfarben mischen können. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Die Schärfe des Übergangs ist wie &quot;Kontrast&quot;. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>

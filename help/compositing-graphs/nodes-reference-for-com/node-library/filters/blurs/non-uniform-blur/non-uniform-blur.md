---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Uneinheitlicher Weichzeichner", um einen Weichzeichner mit unterschiedlichen Intensitäten in X- und Y-Richtungen anzuwenden und so anisotrope Effekte zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uneinheitlicher Weichzeichner
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# Uneinheitlicher Weichzeichner

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Weichzeichner mit hoher Qualität durch, bei dem die Intensität durch eine Eingabemaske gesteuert wird. Mit den Optionen können Anisotropie und Asymetrie hinzugefügt werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Weichzeichnerzuordnung</b> <i>Graustufen-Eingabe</i> | Maskenzuordnung zur Stärke von Effekten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 50.0</i> | Maximale Stärke, mit der der Weichzeichner angewendet wird. Maskiert durch die Weichzeichnermatrix, sodass diese Einstellung keine Auswirkungen auf schwarze Bereiche der Karte hat. |
| <b>Anisotropie</b> <i>0.0 - 1.0</i> | Optional können Sie dem Unschärfe-Effekt Richtungseigenschaften hinzufügen. Gesteuert durch den Parameter Winkel. |
| <b>Asymmetrie</b> <i>0.0 - 1.0</i> | Fügt optional eine Verzerrung zur Aufnahme hinzu. Gesteuert durch den Parameter Winkel. |
| <b>Winkel</b> <i>0.0 - 1.0</i> | Winkel zur Einstellung der Richtungsabhängigkeit und des Sampling-Bias. |
| <b>Beispiele</b> <i>1 - 16</i> | Menge der Proben, bestimmt die Qualität. Multipliziert mit der Anzahl der Blades. |
| <b>Blades</b> <i>1 - 9</i> | Die Anzahl der Stichprobensektoren bestimmt die Qualität. Multipliziert mit der Anzahl der Samples. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            Das Beispiel <img src="../../../../../../assets/nonuniform-example.gif" /><br><i>Unten wird von einer Verlaufsrampe (bei 90 Grad) im Steckplatz "Weichzeichnermatrix" gesteuert.</i>
        </td>
    </tr>
</table>

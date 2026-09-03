---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D Linear gradient, um lineare Farbverläufe zu erstellen, die auf der 3D-Weltposition für räumliche Effekte basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient-01.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erstellt einen volumetrischen Farbverlauf basierend auf der Eingabe-Positions-Map. Erzeugt im 3D-Raum effektiv einen Übergang von Schwarz zu Weiß zwischen 2 Punkten. Wird nur für die Verwendung mit der GPU-Engine konzipiert.

Siehe auch [3D-Volumenmaske](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) für einen ähnlichen Effekt.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Punktpositionsmodus</b> <i>UV-Positionen, Welt-Raum-Positionen</i> | Wählen Sie aus, ob die Verlaufspunkte in &quot;UV-Raum&quot; (funktioniert am besten, wenn Sie sie in der 2D-Ansicht festlegen) oder in 3D-Koordinaten funktionieren, wenn Sie manuell eine exakte Position eingeben möchten. |
| <b>Punkt 1</b> | Startpunkt des Verlaufs. Kann 2D- oder 3D-Koordinaten basierend auf dem Positionsmodus sein. |
| <b>Punkt 2</b> | Endpunkt des Verlaufs. Kann 2D- oder 3D-Koordinaten basierend auf dem Positionsmodus sein. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-linear-gradient-02.gif" />
        </td>
    </tr>
</table>

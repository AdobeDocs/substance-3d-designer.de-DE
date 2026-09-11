---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Trapezform , um Texturen eine trapezförmige Verzerrung zuzuweisen, um perspektivische Korrektureffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trapezform
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Trapezform

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapeze-transform.png){width="128px"}

![](trapezoid-transform.resources/trapeze-transform-grayscale.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Spezieller Transformationsknoten, der die Eingabe perspektivisch/trapezförmig verzerrt ändert. Verfügt über Steuerelemente für die Dehnung Oben und Unten. Werte können über Grenzen hinaus verschoben werden, um stärkere Effekte zu erzielen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Top Dehn</b> <i>0.0 - 1.0</i> | Lege die Stärke des dehn- oder Squashs oben fest. |
| <b>Unten Gedehnt</b> <i>0.0 - 1.0</i> | Stellen Sie die dehn- oder Squash-Menge an der Schaltfläche ein. |
| <b>Hintergrundfarbe</b> <i>(Graustufen-/Farbwert)</i> | Legen Sie eine einfarbige Hintergrundfarbe fest, falls die Unterteilung deaktiviert ist. |
| <b>Sampling</b> <i>Bilinear, nächstgelegen</i> | Legen Sie die Samplingqualität fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapeze-example.gif" />
        </td>
    </tr>
</table>

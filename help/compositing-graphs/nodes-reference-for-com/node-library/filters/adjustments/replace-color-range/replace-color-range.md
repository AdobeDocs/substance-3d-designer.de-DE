---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Farbbereich ersetzen", um Farben innerhalb eines bestimmten Bereichs zur Farbkorrektur durch neue Farben zu ersetzen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbbereich ersetzen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Farbbereich ersetzen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range-01.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ersetzt die Quellfarbe durch die Zielfarbe mit zusätzlichen Steuerelementen. Kann zum Beispiel verwendet werden, um Teile einer Material-ID-Map (Baking) neu einzufärben.

Eine erweiterte Version finden Sie unter [Farbabgleich.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Quellfarbe</b> <i>(Farbwert)</i> | Farbe, die ersetzt werden soll |
| <b>Zielfarbe</b> <i>(Farbwert)</i> | Farbe, die ersetzt werden soll. |
| <b>Quellbereich</b> <i>0.0 - 1.0</i> | Bereich oder Toleranz der ausgewählten Quelle. Kann erhöht werden, damit auch weitere benachbarte Farben farblich verschoben werden. |
| <b>Schwellenwert</b> <i>0.0 - 1.0</i> | Abfall/Kontrast für den Bereich. Wählen Sie &quot;Niedrig&quot;, um nur die Quellfarbe zu ersetzen, und &quot;Hoch&quot;, um auch die Farben zu ersetzen, die in die Quelle übergehen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-02.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Schwellenwert", um Graustufenmasken anhand eines Schwellenwerts für das Erstellen von Texturen in Schwarzweiß umzuwandeln.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schwellenwert
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# Schwellenwert

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-2.png){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Gibt Weiß zurück, wenn die im Parameter **Modus** festgelegten *Vergleichskriterien* für den Eingabepixelwert im Verhältnis zum Wert **Schwellenwert** erfüllt sind.\
Ähnlich wie [Histogrammscan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), jedoch mit Kontrast immer auf maximaler Ebene. Dient als präzisere und schnellere Möglichkeit, ähnliche Ergebnisse wie bei der Histogrammsuche zu erhalten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Schwellenwert</b> <i>0.0 - 1.0</i> | Luminanz, mit der der eingegebene Pixelwert verglichen wird. |
| <b>Modus</b> | Das Kriterium, nach dem der Eingabepixelwert mit dem Wert **Schwellenwert** verglichen werden soll:<br><br>- *Größer*<br>- *Größer oder gleich*<br>- *Niedriger*<br>- *Niedriger oder gleich* |

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Schwellenwert", um Graustufen-Texturen anhand eines Schwellenwerts für das Erstellen von Masken in Schwarzweiß zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schwellenwert
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# Schwellenwert

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## Schwellenwert

**In:** *Filter/Korrekturen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Gibt Weiß zurück, wenn die im Parameter **Modus** festgelegten *Vergleichskriterien* für den Eingabepixelwert im Verhältnis zum Wert **Schwellenwert** erfüllt sind.\
Ähnlich wie [Histogrammscan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), jedoch mit Kontrast immer auf maximaler Ebene. Dient als präzisere und schnellere Möglichkeit, ähnliche Ergebnisse wie bei der Histogrammsuche zu erhalten.

### Parameter

* **Schwellenwert**: *0.0 - 1.0*\
  Luminanzwert, mit dem der Eingangspixelwert verglichen wird.
* **Modus**:\
  Das Kriterium, nach dem der Eingabepixelwert mit dem **Schwellenwert**-Wert verglichen werden soll:
  * *Größer*
  * *Größer oder gleich*
  * *Niedriger*
  * *Niedriger oder gleich*

## Beispielbilder

</td>
</tr>
</table>

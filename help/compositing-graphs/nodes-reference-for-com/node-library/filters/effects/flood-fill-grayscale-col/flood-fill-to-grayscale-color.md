---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill in Graustufenfarbe", um verknüpfte Bereiche mit Graustufenfarben zu füllen, um monochrome Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill zu GraustufenFarbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fill in Graustufen/Farbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/floodfill-to-grayscale.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/floodfill-to-color.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verwendet Flood Fill-Daten, um Graustufen- oder Farbwertfelder zu generieren. Im Gegensatz zu [Flood Fill zu zufälligem Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) ermöglichen diese beiden Knoten mehr Kontrolle über das Festlegen der exakten Variation und Farbtöne sowie eine zusätzliche Eingabezuordnung, um den Basiswert zu bestimmen, der auf Zellbasis zufällig zugewiesen werden soll.

Es ist ein leistungsstarkes System, um jeder Zelle einen eindeutigen Wert oder eine Farbe zu geben, aber dennoch die Kontrolle zu behalten und sie auf einer vorbestimmten Eingabe zu basieren.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Farbeingabe</i> |  |
| <b>Graustufen-/Farbeingabe</b> <i>Graustufen-/Farbeingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Luminanz-/Farbkorrektur</b> <i>-1.0 - 1.0</i> | Legen Sie den Bias- oder Basiswert für den Knoten fest. Wenn eine Graustufen- oder Farbeingabe verwendet wird, wird dies verwendet, um den Anfangswert als Ausgangspunkt zu ändern. |
| <b>Luminanz/Farbzufall</b> <i>-1.0 - 1.0</i> | Legen Sie den Umfang der Abweichung fest. |

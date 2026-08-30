---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Wechseln", um zwischen zwei Eingabetexturen zu wechseln, die auf einer Maske für die Auswahl einer bedingten Textur basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Wechseln
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# Wechseln

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-1.png){width="128px"}

![](switch.resources/switch-grayscale.png){width="128px"}

<b>In:</b> Filters > Blending

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Einfacher 2-Positions-Schaltknoten. Gibt je nach Einstellung des Switch-Parameters entweder Input 1 oder Input 2 zurück. Ergebnis ist unverändert. Eine erweiterte Version finden Sie unter [Multi Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).

Sehr nützlich zum Anzeigen einer booleschen (True/False) Auswahl in einem Diagramm, bei der Sie nur eine einzelne Schaltfläche und keine komplexe Dropdown-Liste für eine ganze Auswahl von Optionen benötigen.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Schalter&quot; für Farbeingaben, &quot;Graustufen wechseln&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1 (Wahr)</b> <i>Farb- oder Graustufeneingabe</i> |  |
| <b>Eingabe 2 (falsch)</b> <i>Farb- oder Graustufeneingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Switch</b> <i>False/True</i> | Wechselt zwischen Eingang 1 (True) und 2 (False). |

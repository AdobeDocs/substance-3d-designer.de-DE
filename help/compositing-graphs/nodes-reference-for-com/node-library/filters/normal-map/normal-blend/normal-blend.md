---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normale Überblendung , um Normalmaps miteinander zu überblenden und so glatte Übergänge zwischen Oberflächendetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Normale Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Mit &quot;Normale Überblendung&quot; können Sie zwei Normalmaps mit einer optionalen Maske überblenden, während Sie gleichzeitig sicherstellen, dass alle Werte normalisiert bleiben. Er unterscheidet sich nicht sehr von einem [atomaren Mischknoten](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), hat aber interne Berechnungen für Normalmaps hinzugefügt.

&quot;Normale Überblendung&quot; ist nicht zum Kombinieren (Überlagern) von Normalmaps gedacht, wobei die obere Karte der unteren Karte Details hinzufügt. Verwenden Sie stattdessen [Normale Kombination](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>Farbeingabe</i> | Vordergrund-/obere Normalmap. |
| <b>NormalBG</b> <i>Farbeingabe</i> | Hintergrund/untere Normalmap |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske verwenden&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode zwischen Vorder- und Hintergrund |
| <b>Maske verwenden</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normalblend-ex.gif" /><br><i>(.gif-Format führt Dithering im Beispiel ein, Anwendungsinterne Ergebnisse sind glatt)</i>
        </td>
    </tr>
</table>

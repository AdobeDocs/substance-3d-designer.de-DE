---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normale Überblendung , um Normalen-Map übereinander zu legen und so nahtlose Übergänge zwischen Oberflächendetails zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Normale Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Mit der Option &quot;Normale Überblendung&quot; können Sie zwei Normalmaps mit einer optionalen Maske überblenden, während Sie gleichzeitig sicherstellen, dass alle Werte normalisiert bleiben. Er unterscheidet sich nicht sehr von einem [Atomknoten für Überblendungen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), hat aber interne Berechnungen für Normalmaps hinzugefügt.

Normale Überblendung ist nicht für die Kombination (Überlagerung) von Normalmaps gedacht, wobei die oberste Karte der untersten Karte weitere Details hinzufügt. Verwenden Sie stattdessen [Normale Kombination](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

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
            <img src="../../../../../../assets/normalblend-ex.gif" /><br><i>(.gif-Format führt Dithering im Beispiel ein, Anwendungsinterne Ergebnisse sind glatt)</i>
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Filterknoten "Tiefen", um Schatteneffekte aus Eingabetexturen zu generieren, um Materialien Tiefe und Realismus hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schatten (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Schatten (Filterknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-filter-node-01.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine reine Graustufenversion des Knotens [Shape-Schlagschatten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Es werden nur schwarzweiße, binäre Formen als Eingabe verwendet und nur der Schatten zurückgegeben.

Dies kann nützlich sein, wenn Sie direkt nach dem Schatten arbeiten und nicht mit einem umfassenderen Knoten arbeiten möchten, z. B. beim Erstellen Ihres eigenen Materials oder bei der Hintergrundbeleuchtung.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Schattenentfernung</b> <i>0.0 - 1.0</i> | Steuert, wie weit der Schatten fallen soll. |
| <b>Lichtwinkel</b> <i>0.0 - 1.0</i> | Steuert den Einfallswinkel des Lichts. |
| <b>Kanten weich</b> <i>0.0 - 1.0</i> | Legt fest, wie hart oder weich die Schattenkanten sind. |
| <b>Beispiele</b> <i>1 - 16</i> | Legt die Qualität für die Einstellung &quot;Kanten weichzeichnen&quot; fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadows-filter-node-02.png" />
        </td>
    </tr>
</table>

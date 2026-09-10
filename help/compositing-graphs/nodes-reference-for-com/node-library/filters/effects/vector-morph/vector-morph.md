---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Vektormorph", um Texturen zwischen zwei Eingängen zu morphen, indem Sie Vektorfelder für glatte Übergänge verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vektormorph
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# Vektormorph

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-morph.resources/vector-morph-grayscale.png)![](vector-morph.resources/vector-morph.png)

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verzerrt ein Eingabebild durch eine Vektorgrafik. Der Effekt ähnelt der UV-Verzerrung mit einer Normalmap oder der Verwendung einer &quot;Flow Map&quot; in Videospielschattierungen. Eingabepixel werden durch die Vektoren verschoben, die in den roten und grünen Werten der Vektorgrafik definiert sind.

Dieser Knoten selbst ist nicht der am schwierigsten zu verwendende, aber das Erstellen einer geeigneten Vektorkarte ist vorsichtig. Es wird empfohlen, die höchstmöglichen Bit-Tiefen zu verwenden, um beim Morphing Präzision zu gewährleisten.

Der Vektormorph ist [Vektorverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) sehr ähnlich: der Hauptunterschied besteht darin, dass dieser Morph-Knoten das Ergebnis nicht &quot;wiederholt&quot; oder &quot;unterteilt&quot;, wenn es außerhalb der Arbeitsflächengrenzen verschoben wird. Stattdessen werden die Ränder festgeklemmt und wiederholt.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farb-/Graustufeneingabe</i> | Die Quelleingabe, die das Ziel für die Verkrümmung sein sollte. |
| <b>Vektorfeld</b> <i>Farbeingabe</i> | Die Vektorkarte, die zum Antrieb der Verkrümmung verwendet wurde. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Betrag</b> <i>0.0 - 1.0</i> | Legt die Intensität des Verkrümmungseffekts fest und fungiert als Multiplikator für die Vektorkarte. |

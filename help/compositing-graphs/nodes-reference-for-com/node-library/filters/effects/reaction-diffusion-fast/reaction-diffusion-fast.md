---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Reaktionsdiffusionsgeschwindigkeit", um organische Muster mithilfe von schnellen Reaktionsdiffusionsalgorithmen für prozedurale Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Reaktionsdiffusionsgeschwindigkeit
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# Reaktionsdiffusionsgeschwindigkeit

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Reaktions-Diffusionsknoten](reaction-diffusion-fast.resources/reaction-diffusion-fast-01.png "Symbol für Reaktions-Diffusionsknoten")

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten führt einen Reaktions-Diffusionseffekt auf ein Graustufenbild durch.

Die Reaktions-Diffusion ist ein Prozess, bei dem sich Materie ausbreitet (diffundiert) und mit anderer Materie interagiert (reagiert). Es ist ein mathematisches Modell, das simuliert, was in der Natur passiert, wenn bestimmte Muster auf Tierhaut gebildet werden, zum Beispiel.

Dieser Knoten ist für die Leistung optimiert und bietet ein gewisses Maß an Präzision für die Geschwindigkeit.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> | Das Graustufenbild, auf das der Effekt &quot;Diffusion/Reaktion&quot; angewendet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Graustufenbild, das den auf das Eingabebild angewendeten Effekt &quot;Diffusion/Reaktion&quot; darstellt. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Radius</b> *Gleitend* | Wie weit sollte sich der Effekt ausbreiten? |
| <b>Kontrast</b> *Gleitend* | Passt den Kontrast der Eingabe an und dient als eine Art Schwellenwert. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Beispiel 1](reaction-diffusion-fast.resources/reaction-diffusion-fast-02.png "Beispiel 1")

</td>
<td style="border: 0;" valign="top">

![Beispiel 2](reaction-diffusion-fast.resources/reaction-diffusion-fast-03.png "Beispiel 2")

</td>
<td style="border: 0;" valign="top">

![Beispiel 3](reaction-diffusion-fast.resources/reaction-diffusion-fast-04.gif "Beispiel 3")

</td>
</tr>
</table>

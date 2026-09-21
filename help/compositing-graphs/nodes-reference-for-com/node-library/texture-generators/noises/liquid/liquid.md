---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Flüssigkeit", um Flüssigkeits- und Fluidmuster zum Erstellen von Wasser-, Öl- und anderen Flüssigkeitsoberflächeneffekten zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liquid
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%
---

# Liquid

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](liquid.resources/liquid.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist eine einfache Variante von [Gaußschem Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), die [sich ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) mit sich selbst verzieht, um einen flüssigkeitsähnlichen Effekt zu erzeugen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>1 - 128</i> | Legt die globale Skalierung für den Effekt fest. |
| <b>Störung</b> <i>0.0 - 1.0</i> | Phasenverschiebung des Rauschen zur Einführung kleiner Variationen |
| <b>Verkrümmungsintensität</b> <i>0.0 - 1.0</i> | Legt die Intensität des Verkrümmungseffekts fest. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Squash und dehn mit nicht quadratischen Verhältnissen. |

## Beispiele

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="liquid.resources/liquid-ex.gif" class="modal-image" alt="Liquid - Beispiel 1" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flüssigkeit", um Flüssigkeits- und Fluidmuster zum Erstellen von Wasser-, Öl- und anderen Flüssigkeitsoberflächeneffekten zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liquid
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Liquid

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/liquid.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist eine einfache Variante des [Gaußschen Rauschens](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), das [sich &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) selbst verkrümmt, um einen flüssigkeitsähnlichen Effekt zu erzeugen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>1 - 128</i> | Legt die globale Skalierung für den Effekt fest. |
| <b>Störung</b> <i>0.0 - 1.0</i> | Phasenverschiebung des Rauschens, um kleine Schwankungen zu erzeugen |
| <b>Verkrümmungsintensität</b> <i>0.0 - 1.0</i> | Legt die Intensität des Verkrümmungseffekts fest. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/liquid-ex.gif" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/plasma.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Plasma", um plasmaähnliche Rauschmuster zu erzeugen, um organische und flüssige Textureffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Plasma
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plasma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 7%

---


# Plasma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plasma.resources/plasma.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dadurch wird eine etwas andere Variante von [Gaußschem Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md) erzeugt, mit längeren dunklen Streifen als Täler. Es verfügt über eine ähnliche Abstandssteuerung für die Skalierung, die die Unterteilung beibehält.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>1 - 128</i> | Legt die globale Skalierung für den Effekt fest. |
| <b>Störung</b> <i>0.0 - 1.0</i> | Phasenverschiebt das Rauschen, um kleine Schwankungen einzuführen. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plasma.resources/plasma-ex.gif" />
        </td>
    </tr>
</table>

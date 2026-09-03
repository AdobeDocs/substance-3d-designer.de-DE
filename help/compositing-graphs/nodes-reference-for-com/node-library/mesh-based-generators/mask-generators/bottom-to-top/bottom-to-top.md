---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Unten nach oben", um Verlaufsmasken von unten nach oben basierend auf der Gitterweltposition zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Von unten nach oben
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# Von unten nach oben

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top-01.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) in [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home).

Dadurch wird ein weißer bis schwarzer Übergang vom unteren zum oberen Rand eines Modells erzeugt. Das ist nützlich, um geometriebasierte Abweichungen und Auswahlen vorzunehmen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Position</b> <i>Farbeingabe</i> | Backed-Positions-Map. Erforderlich! |
| <b>Raueit</b> <i>Graustufen-Eingabe</i> | Dies hat nichts mit der PBR-Raueit zu tun, sondern ist eine (optionale) Variationskarte, um die Überblendung aufzubrechen. Wird nur angezeigt, wenn &quot;Raueit&quot; höher als 0 eingestellt ist. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Verschiebt die durchschnittliche Stufe des Ergebnisses zwischen Schwarz und Weiß, wie bei einer Helligkeitsanpassung. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast der Überblendung an. |
| <b>Rauheit_Variation</b> <i>0.0 - 1.0</i> | Bestimmt den Umfang der Rauheiten-Map, die zur Variation eingeblendet werden soll. Wenn Sie diesen Wert auf über 0 erhöhen, wird der Kartenschlitz angezeigt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-02.gif" />
        </td>
    </tr>
</table>

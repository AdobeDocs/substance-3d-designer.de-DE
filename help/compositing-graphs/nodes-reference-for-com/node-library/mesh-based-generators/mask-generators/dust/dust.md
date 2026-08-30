---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Dust", um Dust-Akkumulierungsmasken auf der Grundlage der Geometrie des Meshs zu generieren, um realistische Dust- und Rastereffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt die Dust dar, die sich in verdeckten, abgesenkten Bereichen angesammelt hat, sowie nur in Bereichen, die nach oben Fläche sind. Erfordert ordnungsgemäß Baking geführt AO und Welt-Raum-Normale.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für die Platzierung der Dust. Erforderlich! |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> | Durch Baking erzeugte Map für die Platzierung der Dust. Erforderlich! |
| <b>Rauschen</b> <i>Graustufen-Eingabe</i> | Benutzerdefinierte Dust-Map (optional) wird nur angezeigt, wenn &quot;Rauschen überschreiben&quot; auf &quot;True&quot; festgelegt ist. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt die Gesamtmenge der Dust fest. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast der Dust an. |
| <b>Verdeckung </b> <i>0.0 - 1.0</i> | Legt den Einfluss von AO fest; mehr Dust wird in verdeckten Bereichen erscheinen. |
| <b>Rauschen Deckkraft</b> <i>0.0 - 1.0</i> | Legt die Rauschen fest, die in staubigen Bereichen sichtbar ist. |
| <b>Rauschen überschreiben</b> <i>False/True</i> | Zur Verwendung von benutzerdefinierten Düste-Map-Eingaben. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>

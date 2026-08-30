---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Licht , um Masken basierend auf Gitterlichtbedingungen zu generieren, um realistische Materialvariationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hell
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# Hell

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-2.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske unterscheidet sich ein wenig von anderen Generatoren: Es handelt sich um eine gefälschte Beleuchtung, die auf der Normalmap des Weltraums basiert und eine Schwarz-Weiß-&quot;Lightmap&quot;-Maske zurückgibt.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Horizontaler Winkel</b> <i>0.0 - 1.0</i> | Legt den horizontalen Winkel des falschen Lichts fest. |
| <b>Vertikaler Winkel</b> <i>0.0 - 1.0</i> | Legt den vertikalen Winkel des falschen Lichts fest. |
| <b>Glanzlichter hervorheben</b> <i>0.0 - 0.999</i> | Legt den Abstandsbereich des markierten Bereichs fest. |
| <b>Ebene hervorheben</b> <i>0.0 - 1.0</i> | Legt die Helligkeitsstufe des markierten Bereichs fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-ex.gif" />
        </td>
    </tr>
</table>

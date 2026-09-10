---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Malen Wear, um Malen-Verschleißmasken auf der Grundlage der Mesh-Geometrie zu erstellen, um realistische Malen-Chipping-Effekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lackverschleiß
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# Lackverschleiß

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](paint-wear.resources/paint-wear.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske repräsentiert Malen-Chipping und Abnutzung an Kanten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Variationsmaske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt den Gesamtverschleiß des Malen fest. Dieser Effekt wird nach und nach sichtbar. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Verdeckung</b> <i>0.0 - 1.0</i> | Legt den Effekt fest, den das Baking geführt AO auf die Vermeidung von Verschleiß in dunkleren Bereichen hat. |
| <b>Radius</b> <i>0.0 - 2.0</i> | Legt fest, wie weit sich der Chipping-Effekt von den konvexen Kanten ausbreitet. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Legen Sie die Stärke der Variation (Schmutz) fest, die in den Effekt übergeht. |
| <b>Variationsmaske überschreiben</b> <i>False/True</i> | Ermöglicht benutzerdefinierte Variation (Schmutz) des Karteneingangssteckplatzes. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="paint-wear.resources/paint-wear-ex.gif" />
        </td>
    </tr>
</table>

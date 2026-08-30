---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Verwenden Sie den Dirt, um Dirt-Akkumulierungsmasken basierend auf Krümmung, Position und Verdeckung des Meshs zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verschmutzung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# Verschmutzung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt Dirt in verdeckten und abgesenkten Kanten und Ecken dar, basierend auf Baking geführt AO und Krümmung.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. Erforderlich! |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. Erforderlich! |
| <b>Schmutz-Eingang</b> <i>Graustufen-Eingabe</i> | Benutzerdefinierte Schmutz-Map-Eingabe, optional, aktiviert durch Parameter. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> | Nur für Triplanar verwendet. |
| <b>Position</b> <i>Farbeingabe</i> | Nur für Triplanar verwendet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Dirt-Stufe</b> <i>0.0 - 1.0</i> | Hauptsteuerung für die Menge des Dirts. |
| <b>Kontrast des Dirts</b> <i>0.0 - 1.0</i> | Steuert den Hauptkontrast für den Dirt in der Maske. |
| <b>Schmutz-Betrag</b> <i>0.0 - 1.0</i> | Legt fest, wie schmutzig der Dirt ist. Setzen Sie den Wert auf 0, um einen einwandfreien Dirt zu erzielen. |
| <b>Kanten maskieren</b> <i>0.0 - 1.0</i> | Dirt, der von erhöhten Kanten entfernt werden soll (abhängig vom Krümmungs-Map). |
| <b>Benutzerdefinierten Schmutz verwenden</b> <i>False/True</i> | Ermöglicht die Verwendung einer benutzerdefinierten Schmutz-Map-Eingabe anstelle eines integrierten Schmutz. |
| <b>Schmutz-Skalierung</b> <i>1 - 16</i> | Legt die Skalierung der Kachelung der Schmutz-Details fest. |
| <b>Triplanar verwenden</b> <i>False/True</i> | Verwenden Sie [Triplanare Projektion](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) für die Schmutz-Zuordnung, um Nähte zu entfernen. |
| <b>Triplanarer Mischkontrast</b> <i>0.001 - 1.0</i> | Legt den Kontrast der Triplanare Projektion fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>

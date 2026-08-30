---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Lederbekleidung", um auf der Grundlage von Gitterkrümmung und Kontaktpunkten Verschleißmasken auf Lederoberflächen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lederbekleidung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# Lederbekleidung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske repräsentiert den Verschleiß mit einem Ledermuster, mit mehr Verschleiß an Kanten basierend auf der Krümmung. Die Funktionalität ähnelt der von [Fiber Glass Edge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) und weist meist dieselben Parameter auf.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für die Kantenplatzierung. Erforderlich! |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map hat bestimmte Bereiche verdeckt. Empfohlen, aber nicht erforderlich. |
| <b>Schmutz-Eingabe</b> <i>Graustufen-Eingabe</i> | Optionaler Schmutz-Map-Eingangssteckplatz, der über den Parameter &quot;Benutzerdefinierten Schmutz verwenden&quot; umgeschaltet werden kann. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Verschleißstufe</b> <i>0.0 - 1.0</i> | Stellt den globalen Verschleißgrad ein und zeigt ihn allmählich auf. |
| <b>Kontrast tragen</b> <i>0.0 - 1.0</i> | Legt den Kontrast des Effekts fest. |
| <b>Schmutz-Betrag</b> <i>0.0 - 1.0</i> | Legt den Schmutz (Standardledermuster) fest, der zwischen den Rändern verblendet werden soll. |
| <b>Ambient occlusion-Maskierung</b> <i>0.0 - 1.0</i> | Legt fest, inwieweit die AO die Verschleißeffekte maskiert. |
| <b>Krümmung Weight</b> <i>0.0 - 1.0</i> | Legt fest, inwieweit die Kanten der Krümmung das Endergebnis beeinflussen. Selbst wenn der Wert auf 0 gesetzt ist, benötigen Sie immer noch eine Krümmungskarte. |
| <b>Benutzerdefinierten Schmutz verwenden</b> <i>False/True</i> | Aktiviert das Überschreiben des integrierten Standardledermusters. Verwenden Sie stattdessen einen benutzerdefinierten Eingabefach. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-ex.gif" />
        </td>
    </tr>
</table>

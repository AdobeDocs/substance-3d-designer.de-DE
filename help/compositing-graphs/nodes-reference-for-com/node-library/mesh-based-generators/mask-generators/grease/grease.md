---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Fett", um Fettansammlungsmasken basierend auf der Gittergeometrie und den Kontaktflächen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fett
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Fett

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grease.resources/grease.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske ist speziell für Schriftarten und andere spezifische Bereiche vorgesehen. Generiert eine Hautfettmaske für Bereiche mit geringer Thickness.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Graustufen-Eingabe</i> | Thickness-Map, auf der der gesamte Effekt basiert. Erforderlich! |
| <b>Rauschen</b> <i>Graustufen-Eingabe</i> | Optionale Rauschkarte zum Überschreiben von Fett-Schmutz mit. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt die Gesamtmenge des Effekts fest, der angezeigt werden soll. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Schwellenwert für Thickness</b> <i>0.0 - 1.0</i> | Legt eine Thickness fest, bei der der Effekt mindestens auftreten soll. ebenso wichtig wie die Stufe; Passe dies an deinen Dicken-Map an. |
| <b>Rauschen überschreiben</b> <i>False/True</i> | Setzen Sie diese Option ein, um den internen Schmutz-Schmierplan mit benutzerdefiniertem Eingangssteckplatz zu überschreiben. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grease.resources/grease-ex.gif" />
        </td>
    </tr>
</table>

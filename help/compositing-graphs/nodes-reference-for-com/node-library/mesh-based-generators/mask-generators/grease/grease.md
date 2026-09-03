---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Verwenden Sie den Fettknoten, um Fettansammlungsmasken auf der Grundlage der Geometrie des Meshs und der Kontaktflächen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fett
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Fett

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grease.resources/grease-01.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske ist speziell für Zeichenbereiche und andere spezifische Flächen vorgesehen. Generiert eine Hautfettmaske für Bereiche mit geringer Thickness.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Graustufen-Eingabe</i> | Baking geführt Dicken-Map, auf dem der gesamte Effekt basiert. Erforderlich! |
| <b>Rauschen</b> <i>Graustufen-Eingabe</i> | Optionale Rauschen-Map zum Überschreiben von Fett-Schmutz mit. |
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
            <img src="grease.resources/grease-02.gif" />
        </td>
    </tr>
</table>

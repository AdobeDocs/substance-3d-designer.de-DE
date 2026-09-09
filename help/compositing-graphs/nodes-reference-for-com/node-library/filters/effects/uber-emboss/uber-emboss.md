---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Uber-Relief, um erweiterte Reliefeffekte mit anpassbaren Steuerelementen für Tiefe, Winkel und Beleuchtung zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Relief
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Uber Relief

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erweiterte, funktionsreiche Version von [Relief](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Führt einen aufwändigen gefälschten 2D-Beleuchtungseffekt auf der Grundlage einer Höhenkarte durch.

Nützlich, wenn du bei bestimmten Texturierungs-Stilen eine Beleuchtung einbauen möchtest, die du nicht brauchst, aber viel Kontrolle erfordert.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Farbe</b> <i>Farbeingabe</i> | Zu änderndes Basis-Image. |
| <b>Height</b> <i>Graustufen-Eingabe</i> | Als Treiber für den Effekt verwendete Höhenkarte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Umgebungsfarbe</b> <i>(Farbwert)</i> | Farbe, die in schattierten Bereichen verwendet wird. |
| <b>Diffuse </b> <i>(Farbwert)</i> | Farbe, die in beleuchteten Bereichen verwendet wird. |
| <b>Specular-Farbe</b> <i>(Farbwert)</i> | Farbe für Specular-Reflexionen |
| <b>Lichtintensität</b> <i>0.0 - 1.0</i> | Intensität des (gefälschten) Lichts. |
| <b>Lichtwinkel</b> <i>0.0 - 1.0</i> | Einfallswinkel des (gefälschten) Lichts |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Intensität der Specular-Reflexionen. |
| <b>Specular-Glanz</b> <i>0.0 - 1.0</i> | Größe des Specular-Highlights. |
| <b>Diffuse Rauheit</b> <i>0.0 - 1.0</i> | Rauheit, die zur Berechnung der diffusen Beleuchtung verwendet wird. |
| <b>Schattendeckkraft</b> <i>0.0 - 1.0</i> | Deckkraft der schattierten Bereiche. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uberemboss-ex.png" />
        </td>
    </tr>
</table>

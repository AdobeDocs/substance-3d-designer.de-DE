---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Hochpass", um hochfrequente Details aus Texturen zu extrahieren, um Schärfe- und Detailverbesserungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hochpass
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Hochpass

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/highpass-01.png){width="128px"}

![](highpass.resources/highpass-02.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Hochpassfilter durch, der sowohl in Farbe als auch in Graustufen verfügbar ist. Ähnlich wie bei der Photoshop-Aktion mit demselben Namen.\
Diese Option ist nützlich, um große Unterschiede bei der Luminanz von Bildern zu entfernen, z. B. beim Bereinigen von Texturen für die Kachelung.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Hochpass&quot; für Farbeingaben, &quot;Hochpass-Graustufen&quot; für Graustufen-Eingaben.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Radius</b> <i>0.0 - 64.0</i> | Filterradius: Ein kleiner Radius entfernt kleine Unterschiede, ein größerer Radius entfernt große Bereiche. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-04.png" />
        </td>
    </tr>
</table>

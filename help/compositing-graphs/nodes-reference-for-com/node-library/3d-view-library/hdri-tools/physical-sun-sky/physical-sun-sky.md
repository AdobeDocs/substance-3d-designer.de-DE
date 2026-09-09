---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Physical SunSky, um physikalisch genaue Sonne- und Himmelslichtumgebungen für eine realistische Materialvorschau zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Physische SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# Physische Sonne/Himmel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/panorama-physical-sun-sky.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Implementierung von physischer Sonne und Himmel auf Basis des Hosek-Wikie-Skylight-Modells. Bietet eine hervorragende Basis für eine künstliche HDRI.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Sun-Position</b> | Bereich = [0,1]x[0,1] (Längengrad-Breitenwinkel) |
| <b>Trübung</b> <i>1.0 - 10.0</i> | Die Trübung reicht von 1 bis 10 |
| <b>Albedo</b> <i>0.0 - 1.0</i> | Die Albedo reicht von 0 bis 1. |
| <b>Farbe des Bodens</b> <i>(Farbwert)</i> | Farbe der Grundebene. |
| <b>Belichtung (EV)</b> <i>-1.0 - 4.0</i> | Belichtungswert der resultierenden Ausgabe. |
| <b>Sun-Größe</b> <i>0.0 - 4.0</i> | Skalierung der Sonne, jeder Wert, der sich von 1 unterscheidet, ist physikalisch nicht korrekt. Wert hat subtile Effekte! |
| <b>Sonnenintensität</b> <i>0.0 - 1.0</i> | Intensität der Sonnenscheibe. Die Sun-Festplatte ist relativ klein, sodass der Effekt nicht sofort sichtbar ist. |
| <b>Himmelsintensität</b> <i>0.0 - 1.0</i> | Intensität des Himmels. Wirkt sich auch auf die Sonneneruption am Himmel aus, nicht auf die Scheibe selbst. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/sky-ex.gif" />
        </td>
    </tr>
</table>

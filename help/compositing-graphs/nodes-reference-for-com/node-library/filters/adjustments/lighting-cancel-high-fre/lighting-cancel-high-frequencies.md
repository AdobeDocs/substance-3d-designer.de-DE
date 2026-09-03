---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Beleuchtung > Hochfrequenzen abbrechen", um hochfrequente Beleuchtungsdetails aus Texturen für die Material-Analyse zu entfernen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Beleuchtung > Hohe Frequenzen abbrechen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# Beleuchtung > Hohe Frequenzen abbrechen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies-01.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ähnlich wie [Hochpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), aber besser geeignet für Vollfarbbilder (das Ergebnis wird dadurch nicht so stark entsättigt), versucht dieser Knoten, hochfrequente, kleine Lichtdetails abzubrechen.

Weitere Informationen finden Sie unter [Abbrechen der tiefen Frequenzen bei der Beleuchtung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md), und der erweiterte, empfohlene [Luminanzen-Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 1.0</i> | Stärke der Beleuchtung, um den Effekt aufzuheben. |
| <b>Radius</b> <i>0.0 - 10.0</i> | Radius oder Größe der Beleuchtungsdetails, die storniert werden sollen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies-02.png" />
        </td>
    </tr>
</table>

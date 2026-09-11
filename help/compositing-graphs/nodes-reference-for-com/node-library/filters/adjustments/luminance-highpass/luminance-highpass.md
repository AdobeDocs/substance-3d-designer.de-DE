---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Luminanz-Hochpass", um hochfrequente Luminanzen aus Texturen zu extrahieren, um Oberflächendetails zu verbessern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminanzen-Highpass
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Luminanzen-Highpass

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Bricht Beleuchtungsinformationen ab, indem ein [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) für die Luminanz der Eingabe ausgeführt wird. Nützlich, um fotografierte Texturen mit Beleuchtungsinformationen zu korrigieren. Kann in [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) mit mehreren Durchläufen kombiniert werden, um unterschiedliche Lichtfrequenzen zu entfernen.

Erweist sich als etwas besser bei der Farberhaltung als [Beleuchtung Niederfrequenzen abbrechen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Radius</b> <i>0.0 - 64.0</i> | Radius des Hochpasseffekts. Ein kleinerer Radius annulliert eine kleinere Beleuchtung und passt sie an die Eingabebilds an. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>

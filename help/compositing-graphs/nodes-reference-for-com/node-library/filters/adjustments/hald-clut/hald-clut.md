---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Hald CLUT, um Farbtabellen mit dem Format Hald CLUT für Farbkorrektur und -abstufung anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine LUT auf das Eingabebild an. Die LUT muss im Hald-Format mit einer Auflösung von 4096\*4096 vorliegen. Weitere Informationen finden Sie unter <http://www.quelsolaar.com/technology/clut.html>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbeingabe</i> | Bild, auf das die LUT angewendet werden soll. |
| <b>lut</b> <i>Farbeingabe</i> | Steckplatz am Eingang freigeben. Muss 4096x4096 sein. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>LUT-Intensität nach Alpha</b> <i>False/True</i> | Definiert, ob der LUT-Effekt vom Alphakanal gewichtet wird. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/content-hald-clut.jpg" />
        </td>
    </tr>
</table>

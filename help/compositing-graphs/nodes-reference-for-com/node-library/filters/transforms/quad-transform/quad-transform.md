---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Quad-Transformieren-Knoten, um Texturen mit vierseitigen Transformationen für perspektivische Korrekturen und Verkrümmungen zu versehen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quad Transform
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# Quad Transform

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-grayscale.png){width="128px"}

![](quad-transform.resources/quad-transform.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Spezieller Transformationsknoten, der die Transformation einer Quad-Form durch Interaktion mit ihren Eckpunkten ermöglicht. Ermöglicht sehr spezifische Transformationen in einer praktischen Weise.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>p00</b> | Punkt oben links. |
| <b>p01</b> | Punkt unten links |
| <b>p10</b> | Oberer rechter Punkt. |
| <b>p11</b> | Unten rechts. |
| <b>Ausrechnen</b> <i>Nur Vorderseite, Nur Rückseite, Vorne über Rückseite, Hinten über Vorderseite</i> | Legen Sie das Keulen/Ausblenden der Form fest, wenn sich Punkte überkreuzen. |
| <b>Kachelung aktivieren</b> <i>False/True</i> |  |
| <b>Hintergrundfarbe</b> <i>(Graustufenwert)</i> | Durchgehende Hintergrundfarbe, wenn die Kachelung deaktiviert ist. |
| <b>Sampling</b> <i>Bilinear, nächstgelegen</i> | Legen Sie die Samplingqualität fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-example.gif" />
        </td>
    </tr>
</table>

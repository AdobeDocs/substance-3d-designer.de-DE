---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal in Height, um Normalmaps in Height-Maps zu konvertieren, um Informationen zur Tiefe der Flächen zu extrahieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal zu Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Normal zu Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein Umkehrkonvertierungsknoten, der versucht, eine Normalmap des Tangentenraums zurück in eine Höhenkarte zu konvertieren. Dies ist die etwas einfachere Version. [Das HQ von Normal bis Height ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) verfügt über mehr Optionen.

Dies ist nützlich, wenn Sie nur eine Normalmap-Quelle haben, diese aber dennoch mit einer Heightmap kombinieren möchten. Beachten Sie, dass dies niemals zu 100 % zu einem korrekten Ergebnis führen kann, da Informationen aufgrund der Natur des Prozesses verloren gehen, wenn das Height in &quot;Normal&quot; konvertiert wird. Wenn Sie die Einstellungen entsprechend einstellen, leistet diese Nicht-HQ-Version eine anständige Arbeit bei der Konvertierung einfacher Details.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Relief-Saldo</b> <i>0.0 - 1.0</i> | Passen Sie an, wie stark die verschiedenen Frequenzen das Endergebnis beeinflussen. Dies hängt weitgehend von der Eingabemap ab und erfordert ein gutes Stück Feinabstimmung. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Globale Deckkraft</b> <i>0.0 - 1.0</i> | Passt die globale Deckkraft des Effekts an. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal2heightex.png" />
        </td>
    </tr>
</table>

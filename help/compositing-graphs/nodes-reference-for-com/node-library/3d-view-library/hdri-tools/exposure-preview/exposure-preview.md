---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Belichtungsvorschau", um eine Vorschau der Belichtungskorrekturen in HDRI-Umgebungen vor dem endgültigen Rendern anzuzeigen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Belichtungsvorschau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Belichtungsvorschau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Helfer-Knoten zur Vorschau der Belichtungsschritte. Benutzer legen einen Min- und einen Max-Wert fest. Der Knoten generiert ein viel größeres Bild mit einer Reihe verschiedener gelegt Versionen der Originaleingabe. Die verschiedenen Versionen sind immer horizontal gestapelt, der Umfang hängt von der Auflösung des Knotens oder Grafen ab.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Maximale Belichtung (EV)</b> <i>-8.0 - 8.0</i> | Maximale Belichtung des oberen, hellsten Bildes. |
| <b>Min. Belichtung (EV)</b> <i>-8.0 - 8.0</i> | Minimale Belichtung für das dunkelste Bild am unteren Rand. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/exp-preview-ex.png" />
        </td>
    </tr>
</table>

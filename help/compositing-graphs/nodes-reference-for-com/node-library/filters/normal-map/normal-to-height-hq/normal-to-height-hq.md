---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Normal in Height", um Normalen-Map in hochwertige Höhen-Map für die Oberflächendetailextraktion zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal bis Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Normal bis Height HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein Umkehrkonvertierungsknoten, der versucht, eine Normalmap des Tangentenraums zurück in eine Höhenkarte zu konvertieren. Dies ist der fortgeschrittenere Knoten. [Normal zu Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) hat weniger Optionen und verwendet unterschiedliche Berechnungen.

Dies ist nützlich, wenn Sie nur eine Normalmap-Quelle haben, diese aber dennoch mit einer Heightmap kombinieren möchten. Beachten Sie, dass dies niemals zu 100 % zu einem korrekten Ergebnis führen kann, da Informationen aufgrund der Natur des Prozesses verloren gehen, wenn das Height in &quot;Normal&quot; konvertiert wird. Es kann niemals eine korrekt generierte Höhenkarte ersetzen!

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Relief-Saldo</b> <i>0.0 - 1.0</i> | Überblendungen zwischen Nieder- und Hochfrequenzvorspannung. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Intensität oder der Multiplikator für die Höhenkarte funktioniert ein bisschen wie die globale Deckkraft. |
| <b>Height normalisieren</b> <i>False/True</i> | Skaliert den Höhenkartenbereich automatisch, um den vollen Kontrast zu verwenden, z. B. eine [Auto-Ebene](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md). |
| <b>Qualität</b> <i>Normal, Hoch</i> | Wechselt zwischen Geschwindigkeit oder Qualität. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal2height-hq-ex.png" />
        </td>
    </tr>
</table>

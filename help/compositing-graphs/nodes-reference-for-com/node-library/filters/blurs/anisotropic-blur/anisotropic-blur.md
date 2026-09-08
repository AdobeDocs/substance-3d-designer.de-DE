---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Anisotropischer Weichzeichner", um Richtungseffekte zum Erstellen von Bewegungsunschärfe- und Streueffekten anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anisotropischer Weichzeichner
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# Anisotropischer Weichzeichner

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt eine qualitativ hochwertige [Richtungsunschärfe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) durch, mit einigen Einstellungen zum Anpassen des Erscheinungsbilds. Auch als &quot;Bewegungsunschärfe&quot; bezeichnet.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Anisotropischer Weichzeichner&quot; für Farbeingaben bzw. &quot;Anisotropischer Weichzeichner, Graustufen&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 16.0</i> | Stärke (Radius) der Weichzeichnung. Je höher dieser Wert ist, desto weiter reicht die Weichzeichnung. |
| <b>Anisotropie</b> <i>0.0 - 1.0</i> | Richtung der Weichzeichnung. Der Wert 0,0 entspricht dem normalen Weichzeichnen. |
| <b>Winkel</b> <i>0.0 - 1.0</i> | Legt den Winkel für die Weichzeichnungsrichtung fest. |
| <b>Qualität</b> <i>0 - 1</i> | Wechselt intern zwischen einer [Box-Weichzeichnung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) und einer HQ-Weichzeichnung. Schneller Trading für Qualität. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/aniso-blur-example.gif" />
        </td>
    </tr>
</table>

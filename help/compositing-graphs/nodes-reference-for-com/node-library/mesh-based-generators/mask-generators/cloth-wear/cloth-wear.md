---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Stoffverschleiß", um auf der Grundlage der Krümmung des Meshs und der Kontaktflächen Verschleißmasken auf den Oberflächen der Stoffgewebe zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tuchbekleidung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Tuchbekleidung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Die Maske zeigt die Ränder von Materialien an. Es verwendet eine Stoffdetail-Höhenkarte, die den größten Teil des Aussehens bestimmt; ohne entsprechende Karte sieht der Effekt sehr einfach aus.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Cloth-Height</b> <i>Graustufen-Eingabe</i> | Height nur für das Stoffmuster. Dies ist nicht das Height Ihres (Baking geführt) Objekts, sondern ein Detailmuster der Kachelung. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Baking geführt/generierte Krümmung zur Bestimmung erhöhter Kanten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Anzahl der harten Kanten</b> <i>0.0 - 1.0</i> |  |
| <b>Weiche Kante tragen</b> <i>0.0 - 5.0</i> | Legt fest, wie weichgezeichnet/weich die abgenutzten Kanten sind. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-ex.gif" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kantenkerbe", um Kerbmuster an Kanten von Meshs zu generieren, um realistische Kantenbeschädigungen und Einrückungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kantenkerbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# Kantenkerbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-notch.resources/edge-notch.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine Schwarz-weiße Maske basierend auf durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Intelligente Masken](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt eine einfache Maske für erhöhte Kanten dar, die durch einen Hochfrequenz-Rauschen unterbrochen wird. Weitere Optionen finden Sie unter [Edge Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) oder [Edge Damages](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map zum Hervorheben von Kanten. Erforderlich! |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt die Ebene des Effekts &quot;Kantenkerbung&quot; fest. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-notch.resources/edge-notch-ex.gif" />
        </td>
    </tr>
</table>

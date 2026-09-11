---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Verwenden Sie den Edge Speckle -Knoten, um fleckige Verschleißmuster an Kanten von Meshs zu erzeugen, um realistische Kantenschädigungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-speckle.resources/edge-speckle.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske zeigt die Kanten an, an denen leicht Flecken hinzugefügt wurden, um sie zu zerlegen. Siehe auch [Edge-Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für die Kantenmarkierung. Erforderlich! |
| <b>Variationsmaske</b> <i>Graustufen-Eingabe</i> | Optionaler Maskenschlitz zum Maskieren der Effekte des Knotens. Aktivieren Sie diese Option mit &quot;Variationsmaske überschreiben&quot;. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt den Gesamtbetrag der Kantenhervorhebung fest. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Kantenauswahl</b> <i>0.0 - 1.0</i> | Legt den Einfluss konvexer Kanten fest. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Legt fest, in welchem Umfang die Variationsmaske den Effekt aufbricht. |
| <b>Variationsmaske überschreiben</b> <i>False/True</i> | Übersteuert die integrierte Maske mit benutzerdefiniertem Eingabeschacht. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-speckle.resources/edge-speckle-ex.gif" />
        </td>
    </tr>
</table>

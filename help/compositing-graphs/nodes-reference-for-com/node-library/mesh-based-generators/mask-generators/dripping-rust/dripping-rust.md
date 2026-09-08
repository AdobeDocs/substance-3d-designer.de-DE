---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Tropfender Rost", um Tropfmuster des Rosts auf der Grundlage der Geometrie des Meshs und der Schwerkraftrichtung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tropfender Rost
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# Tropfender Rost

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine Schwarz-weiße Maske basierend auf durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Intelligente Masken](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt Rost-Flocken und Flecken dar, wobei die Lecks nach unten verlaufen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Baking geführt oder generierte Map, die bei der Platzierung von Rosten behilflich sein soll. |
| <b>Ambient occlusion</b> <i>Graustufen-Eingabe</i> | Baking geführt oder generierte Map, die bei der Platzierung von Rosten behilflich sein soll. |
| <b>Position</b> <i>Graustufen-Eingabe</i> | Baking geführt oder generierte Karte für Tropfrichtungen. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Rost-Verteilung</b> <i>0.0 - 1.0</i> | Hauptsteuerung für die Menge des Rosts. |
| <b>Kontrast des Rosts</b> <i>0.0 - 1.0</i> | Legt den Kontrastumfang in generierten Rost-Flecken fest (wirkt sich nicht auf Tropfen aus). |
| <b>Smoothness wird verteilt</b> <i>0.0 - 1.0</i> | Stärke des Weichzeichnungs-/Verschmierungseffekts, der auf die Flecken des Rosts angewendet werden soll. |
| <b>Tropfintensität</b> <i>0.0 - 1.0</i> | Legt die Stärke und Länge der Tropfen von Flecken fest. |
| <b>Drips-Smoothness</b> <i>0.0 - 1.0</i> | Weichzeichnungs- und Glättungsgrad, der auf Tropfen angewendet wird. |
| <b>Anzahl der Drips-Samples</b> <i>0 - 32</i> | Legt die Qualitätsstufe (Schritte) für den Tropfeneffekt fest. Hat einen leichten Einfluss auf die Geschwindigkeit. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>

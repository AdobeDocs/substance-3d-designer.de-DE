---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Rock-Verwitterung , um Verwitterung auf Felsoberflächen auf Basis der Mesh-Geometrie zu generieren, um realistische Erosionseffekte zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rock-Verwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 16%

---


# Rock-Verwitterung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Verwitterung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Ambient occlusion</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Normaler WS</b> <i>Farbeingabe</i> | Baking geführt Welt-Raum Normalmap wird für interne Effekte und Maskierung verwendet. |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Material-Kanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanz-Maps anstelle von &quot;Metallic/Rauheit&quot; verwenden. |
| <b>Erweitert</b> |  |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Maske</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |
| <b>Effekt</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Schmutzigkeit</b> <i>0.0 - 1.0</i> |  |
| <b>Kanten, die </b> tragen <i>0.0 - 1.0</i> |  |
| <b>Verwendeter Stein</b> <i>0.0 - 1.0</i> |  |
| <b>Skalierung der Risse</b> <i>1.0 - 60.0</i> |  |
| <b>Intensität der Risse</b> <i>0.0 - 1.0</i> |  |
| <b>Alter</b> <i>0.0 - 1.0</i> |  |
| <b>Altersschwellenwert</b> <i>0.0 - 1.0</i> |  |
| <b>Scratches mit scharfen Kanten skalieren</b> <i>1.0 - 32.0</i> |  |
| <b>Intensität der Verkrümmung der scharfen Kanten der Scratches</b> <i>0.0 - 1.0</i> |  |
| <b>Steinsättigung verwendet</b> <i>0.0 - 1.0</i> |  |
| <b>Rockhelligkeit verwendet</b> <i>0.0 - 1.0</i> |  |
| <b>Überblenden</b> |  |
| <b>Diffuse-Intensität</b> <i>0.0 - 1.0</i> | Mischungsstärke des Diffusors. |
| <b>Intensität der Grundfarbe</b> <i>0.0 - 1.0</i> | Mischungsstärke der Grundfarbe. |
| <b>Normalintensität</b> <i>0.0 - 64.0</i> | Die Füllkraft von &quot;Normal&quot;. |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Speculars. |
| <b>Glanz-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Glanzes beim Mischen. |
| <b>Intensität der Rauheit</b> <i>0.0 - 1.0</i> | Die Stärke der Raueit. |
| <b>Ambient occlusion-Intensität</b> <i>0.0 - 1.0</i> | Mischfestigkeit der Ambient-Verdeckung. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Heights beim Mischen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/rock-ex.gif" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Felsverwitterung", um Wettermuster auf Felsoberflächen basierend auf der Gittergeometrie für realistische Erosionseffekte zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Steinverwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 16%

---


# Steinverwitterung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rock-weathering.resources/rock-weathering.png){width="128px"}

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
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Normaler WS</b> <i>Farbeingabe</i> | Baked World Space Normalmap wird für interne Effekte und Maskierung verwendet. |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
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
| <b>Diffuse-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke der Diffuse. |
| <b>Intensität der Grundfarbe</b> <i>0.0 - 1.0</i> | Die Stärke der Grundfarbe. |
| <b>Normalintensität</b> <i>0.0 - 64.0</i> | Die Stärke der Normalverteilung. |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Speculars verschmelzen. |
| <b>Glanz-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Glanzes. |
| <b>Intensität der Rauheit</b> <i>0.0 - 1.0</i> | Die Stärke der Rauheit. |
| <b>Ambient occlusion-Intensität</b> <i>0.0 - 1.0</i> | Stärke der Ambient occlusion. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Heights. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rock-weathering.resources/rock-ex.gif" />
        </td>
    </tr>
</table>

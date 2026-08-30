---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D-Knoten "Simplex Noise", um 3D-Simplex-Rauschmuster zu generieren, um glatte, natürlich aussehende volumetrische Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Einfaches 3D-Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---


# Einfaches 3D-Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-simplex-noise.resources/3d-simplex-noise.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt ein prozedurales Rauschen, wenn eine eingebettete Positionsabbildung an den Eingangssteckplatz angeschlossen wird. Es ist nur für die Verwendung mit der GPU-Engine vorgesehen.\
Ähnlich wie [3D Perlin Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), jedoch schneller und einfacher, für Fälle, in denen Leistung und Geschwindigkeit wichtig sind.

Dieses Rauschen kann mit [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) als Eingabe anstelle einer tatsächlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>0.0 - 64.0</i> | Legen Sie die globale Skalierung für den Effekt fest. |
| <b>Größe</b> <i>0.0 - 2.0</i> | Führen Sie eine ungleichmäßige Skalierung auf X-, Y- und Z-Achsen separat durch. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-simplex-noise.resources/3d-simplex.gif" />
        </td>
    </tr>
</table>

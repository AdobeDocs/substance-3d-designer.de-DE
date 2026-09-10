---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Saisonfilter", um saisonale Effekte auf Materialien anzuwenden, um Variationen für den Frühling, den Sommer, den Herbst und den Winter zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Saisonfilter
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# Saisonfilter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten fügt Effekte wie einen animierten Wasserstand, Schnee, Eis und/oder Moos hinzu.

Beachten Sie, dass es sich um einen älteren Filter handelt, der nicht vollständig auf PBR-Richtigkeit ausgelegt ist. Es wird hauptsächlich aus Legacy-/Kompatibilitätsgründen beibehalten, kann aber in einigen Fällen immer noch nützlich sein. Neuere PBR-richtige Versionen finden Sie in [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) und [Wasserstand](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Der Knoten benötigt einen richtigen Satz von Materialeingaben, hauptsächlich mit einer ausreichend detaillierten Höhen- oder Normalmap.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Erweitert</b> |  |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Maske</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |
| <b>Lichtintensität</b> <i>0.0 - 1.0</i> | Intensität des (gefälschten) Lichts. |
| <b>Lichtwinkel</b> <i>0.0 - 1.0</i> | Einfallswinkel des (gefälschten) Lichts |
| <b>Effekt</b> |  |
| <b>Effekt aus Height oder Normal</b> <i>Height, Normal</i> | Legt fest, welche Eingabe-Map die Effekte unterstützt. |
| <b>Wasserstand</b> <i>0.0 - 1.0</i> | Erhöht oder senkt den Wasserstand auf Basis von Height-/Normalinformationen. |
| <b>Wasserdetails</b> <i>0.0 - 1.0</i> | Legt die Anzahl der Details im Wasser fest. |
| <b>Brechung</b> <i>0.0 - 1.0</i> | Legt den Grad der falschen Brechung im Effekt fest. |
| <b>Spiegelung</b> <i>0.0 - 1.0</i> | Legt den Umfang der falschen Spiegelung im Effekt fest. |
| <b>Reflexionsabstand</b> <i>0.0 - 1.0</i> | Steuert die Reflexionsvisualisierung. |
| <b>Reflexionswinkel</b> <i>0.0 - 1.0</i> | Steuert die Reflexionsvisualisierung. |
| <b>Flussrichtung</b> <i>0.0 - 1.0</i> | Steuert den Animationsfluss (Visualisierung mithilfe von Substance Player). |
| <b>Eis</b> <i>0.0 - 1.0</i> | Legt fest, wie gefroren das Wasser ist. |
| <b>Eisdetails</b> <i>0.0 - 1.0</i> | Legt die Anzahl der Details im Eis fest. |
| <b>Snow</b> <i>0.0 - 1.0</i> | Legt die Schneedecke fest. |
| <b>Moos</b> <i>0.0 - 1.0</i> | Legt den Umfang der Moosbedeckung fest. |
| <b>Moosskala</b> <i>1 - 4</i> | Legt den Maßstab der generierten Moos-Textur fest. |
| <b>Moosfarbe</b> <i>(Farbwert)</i> | Legt die Farbe des Mooses fest. |
| <b>Wasserfarbe</b> <i>(Farbwert)</i> | Legt die Wasserfarbe fest, einschließlich Alpha/Deckkraft. |
| <b>Überblenden</b> |  |
| <b>Diffuse-Intensität</b> <i>0.0 - 1.0</i> | Mischungsstärke des Diffusors. |
| <b>Intensität der Grundfarbe</b> <i>0.0 - 1.0</i> | Mischungsstärke der Grundfarbe. |
| <b>Normalintensität</b> <i>0.0 - 1.0</i> | Die Füllkraft von &quot;Normal&quot;. |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Speculars. |
| <b>Glanz-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Glanzes beim Mischen. |
| <b>Intensität der Rauheit</b> <i>0.0 - 1.0</i> | Die Stärke der Raueit. |
| <b>Ambient occlusion-Intensität</b> <i>0.0 - 1.0</i> | Mischfestigkeit der Ambient-Verdeckung. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Heights. |

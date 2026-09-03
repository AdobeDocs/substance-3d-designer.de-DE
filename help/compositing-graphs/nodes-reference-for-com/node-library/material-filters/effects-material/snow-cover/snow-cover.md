---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Verwenden Sie den Snow-Deckknoten, um Material Schneeakkumulationseffekte basierend auf Oberflächenwinkel und -position hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Snow Cover
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Snow Cover

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](snow-cover.resources/snow-cover-01.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Mit dem All-in-One-Effekt wird Schnee auf einem ganzen Material aufgestaut. Verlässt sich stark auf eine gute, qualitativ hochwertige Heightmap, z. B. von einem Fotoscan. Das Ergebnis soll PBR-korrekt sein.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Neuer Snow</b> <i>0.0 - 1.0</i> | Legt die Schneemenge in den erhöhten Bereichen fest. Das Ergebnis ist an den Parameter &quot;Geschmolzener Snow&quot; gebunden. |
| <b>geschmolzener Snow</b> <i>0.0 - 1.0</i> | Legt die Menge des geschmolzenen Schnees in abgesenkten Ecken fest. |
| <b>Buildup</b> <i>0.0 - 1.0</i> | Hauptsächlich beeinflusst Height-Ausgabe, bestimmt Height-Stau-Effekt. |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | Stellt die Glättung von Details im Height nach Schneeaufbau ein. |
| <b>Flakes-Intensität</b> <i>0.0 - 1.0</i> | Hauptsächlich beeinflusst Normalmap, Intensität der Flockendetails. |

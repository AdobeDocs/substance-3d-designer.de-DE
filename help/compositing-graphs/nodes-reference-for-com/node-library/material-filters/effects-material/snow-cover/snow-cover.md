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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Snow Cover

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Snow Cover

**In:** *Materialfilter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Mit dem All-in-One-Effekt wird Schnee auf einem ganzen Material aufgestaut. Verlässt sich stark auf eine gute, qualitativ hochwertige Heightmap, z. B. von einem Fotoscan. Das Ergebnis soll PBR-korrekt sein.

## Parameter

### Eingaben

* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Kanäle**\
  Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Neuer Snow**: *0.0 - 1.0* Legt die Schneemenge in den erhöhten Bereichen fest. Das Ergebnis ist an den Parameter &quot;Geschmolzener Snow&quot; gebunden.
* **geschmolzener Snow**: *0.0 - 1.0* Setzt die Menge des geschmolzenen Schnees in abgesenkten Ecken.
* **Build**: *0.0 - 1.0* Wirkt sich hauptsächlich auf die Height-Ausgabe aus und bestimmt den Height-Stau-Effekt.
* **Smoothness**: *0.0 - 1.0* Legt die Glättung der Details des Heights nach Schneeaufbau fest.
* **Flakes-Intensität**: *0.0 - 1.0* wirkt sich hauptsächlich auf die Normalmap und die Intensität der Flockendetails aus.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

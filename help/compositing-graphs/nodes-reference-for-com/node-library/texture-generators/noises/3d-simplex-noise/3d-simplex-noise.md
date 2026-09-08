---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D Simplex Rauschen-Knoten, um 3D-Simplex-Rauschen-Muster zu generieren, um sanfte, natürlich aussehende volumetrische Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Simplex Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 3D Simplex Rauschen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## 3D Simplex Rauschen

**In:** *Texturgeneratoren**/Noises*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine prozedurale Rauschen, wenn eine Baking geführt Positionszuordnung in den Eingangssteckplatz gesteckt wird. Es ist nur für die Verwendung mit dem GPU-Engine vorgesehen.\
Ähnlich wie [3D Perlin Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), jedoch schneller und einfacher, für Fälle, in denen Leistung und Geschwindigkeit wichtig sind.

Diese Rauschen kann mit [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) als Eingabe anstelle einer eigentlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

## Parameter

* **Skalierung**: *0.0 - 64.0*\
  Legen Sie die globale Skalierung für den Effekt fest.
* **Größe**: *0.0 - 2.0* Führen Sie eine ungleichmäßige Skalierung auf X-, Y- und Z-Achsen separat durch.

## Beispielbilder

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>

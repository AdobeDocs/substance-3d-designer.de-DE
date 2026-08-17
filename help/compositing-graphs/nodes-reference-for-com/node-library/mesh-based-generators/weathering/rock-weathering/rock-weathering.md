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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Steinverwitterung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## Steinverwitterung

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

## Parameter

### Eingaben

* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Normaler WS**: *Farbeingabe*\
  Baked World Space Normalmap wird für interne Effekte und Maskierung verwendet.
* **Maske** : *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Erweitert**
  * **Normales Format**: *DirectX, OpenGL*\
    Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
  * **Maske**: *False/True*\
    Schaltet die Verwendung der Maskenkarte ein oder aus.
* **Effekt**
  * **Dust**: *0.0 - 1.0*
  * **Schmutzigkeit**: *0.0 - 1.0*
  * **Kanten, die** tragen: *0.0 - 1.0*
  * **Verwendeter Rock**: *0.0 - 1.0*
  * **Skalierung der Risse**: *1.0 - 60.0*
  * **Intensität der Risse**: *0.0 - 1.0*
  * **Alter**: *0.0 - 1.0*
  * **Altersgrenze**: *0.0 - 1.0*
  * **Scratches mit scharfen Kanten skalieren**: *1.0 - 32.0*
  * **Intensität der Verkrümmung der scharfen Kanten der Scratches**: *0.0 - 1.0*
  * **Rock-Entsättigung verwendet**: *0.0 - 1.0*
  * **Rockhelligkeit verwendet**: *0.0 - 1.0*
* **Überblenden**
  * **Diffuse Intensität**: *0.0 - 1.0*\
    Mischungsstärke des Diffusors.
  * **Grundfarbintensität**: *0.0 - 1.0*\
    Mischungsstärke der Grundfarbe.
  * **Normalintensität**: *0.0 - 64.0*\
    Die Füllkraft von &quot;Normal&quot;.
  * **Specular-Intensität**: *0.0 - 1.0*\
    Die Stärke des Speculars.
  * **Glanzintensität**: *0.0 - 1.0*\
    Die Stärke des Glanzes beim Mischen.
  * **Intensität der Raueit**: *0.0 - 1.0*\
    Die Stärke der Raueit.
  * **Umgebungsintensität der Verdeckung**: *0.0 - 1.0*\
    Mischfestigkeit der Ambient-Verdeckung.
  * **Height-Intensität**: *0.0 - 1.0*\
    Die Stärke des Heights beim Mischen.

## Beispielbilder

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>

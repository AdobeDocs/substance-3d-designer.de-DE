---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Metal Weathering", um metallischen Werkstoffen auf Basis der Gittergeometrie realistische Rost- und Korrosionseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metallverwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---


# Metallverwitterung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

## Metallverwitterung

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

## Parameter

### Eingaben

* **Normaler WS**: *Farbeingabe*\
  Baked World Space Normalmap wird für interne Effekte und Maskierung verwendet.
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Maske** : *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Erweitert**
  * **Normales Format**: *Direct X, Open GL*\
    Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
  * **Maske**: *False/True*\
    Schaltet die Verwendung der Maskenkarte ein oder aus.
* **Effekt**
  * **Dust**: *0.0 - 1.0*
  * **Schmutzigkeit**: *0.0 - 1.0*
  * **Kanten, die** tragen: *0.0 - 1.0*
  * **Farbe schälen**: *0.0 - 1.0*
  * **Rost**: *0.0 - 1.0*
  * **Rost-Peeling**: *0.0 - 1.0*
  * **Rost Verdigris**: *Rost, Verdigris*
  * **Skalierung der Paint-Risse**: *1.0 - 16.0*
  * **Verkrümmungsintensität der Risse**: *0.0 - 1.0*
  * **Scratches mit scharfen Kanten skalieren**: *1.0 - 32.0*
  * **Intensität der Verkrümmung der scharfen Kanten der Scratches**: *0.0 - 1.0*
  * **Rohmetallfarbe**: *(Farbwert)*
  * **Raw Metal Specular Color**: *(Farbwert)*
  * **Rohmetall-Glanzwert**: *(Graustufenwert)*
  * **Rohmetallrauheitswert**: *(Graustufenwert)*
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
  * **Metallische Intensität**: *0.0 - 1.0*\
    Mischfestigkeit des Metallic.
  * **Umgebungsintensität der Verdeckung**: *0.0 - 1.0*\
    Mischfestigkeit der Ambient-Verdeckung.
  * **Height-Intensität**: *0.0 - 1.0*\
    Die Stärke des Heights beim Mischen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

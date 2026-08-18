---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Saisonfilter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## Saisonfilter

**In:** *Materialfilter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten fügt Effekte wie einen animierten Wasserstand, Schnee, Eis und/oder Moos hinzu.

Beachten Sie, dass es sich um einen älteren Filter handelt, der nicht vollständig auf PBR-Richtigkeit ausgelegt ist. Es wird hauptsächlich aus Legacy-/Kompatibilitätsgründen beibehalten, kann aber in einigen Fällen immer noch nützlich sein. Neuere PBR-richtige Versionen finden Sie in [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) und [Wasserstand](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Der Knoten benötigt einen richtigen Satz von Materialeingaben, hauptsächlich mit einer ausreichend detaillierten Höhen- oder Normalmap.

## Parameter

### Eingaben

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
  * **Lichtintensität**: *0.0 - 1.0*\
    Intensität des (gefälschten) Lichts.
  * **Lichtwinkel**: *0.0 - 1.0*\
    Einfallswinkel des (gefälschten) Lichts
* **Effekt**
  * **Effekt aus Height oder Normal**: *Height, Normal* Wählt, welche Eingabemap die Effekte steuert.
  * **Wasserstand**: *0.0 - 1.0* Erhöht oder senkt den Wasserstand auf der Grundlage von Height-/Normalinformationen.
  * **Wasserdetails**: *0.0 - 1.0* Legt die Anzahl der Details im Wasser fest.
  * **Brechung**: *0.0 - 1.0* Legt die Stärke der gefälschten Brechung im Effekt fest.
  * **Reflexion**: *0.0 - 1.0* Legt den Umfang der falschen Reflexion im Effekt fest.
  * **Reflexionsabstand**: *0.0 - 1.0* Steuert Reflexionsvisuals.
  * **Reflexionswinkel**: *0.0 - 1.0* Steuert Reflexionsvisuals.
  * **Flussrichtung**: *0.0 - 1.0* Steuert den Animationsfluss (verwenden Sie zur Visualisierung Substance Player).
  * **Eis**: *0.0 - 1.0* Legt fest, wie gefroren das Wasser ist.
  * **Eisdetails**: *0.0 - 1.0* Legt die Anzahl der Details im Eis fest.
  * **Snow**: *0.0 - 1.0* Legt die Schneedecke fest.
  * **Moos**: *0.0 - 1.0* Legt den Umfang der Moosbedeckung fest.
  * **Moosskala**: *1 - 4* Legt die Skalierung der erzeugten Moostextur fest.
  * **Moosfarbe**: *(Farbwert)*Legt die Farbe des Mooses fest.
  * **Wasserfarbe**: *(Farbwert)*Legt die Wasserfarbe fest, einschließlich Alpha/Deckkraft.
* **Überblenden**
  * **Diffuse Intensität**: *0.0 - 1.0*\
    Mischungsstärke des Diffusors.
  * **Grundfarbintensität**: *0.0 - 1.0*\
    Mischungsstärke der Grundfarbe.
  * **Normalintensität**: *0.0 - 1.0*\
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

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

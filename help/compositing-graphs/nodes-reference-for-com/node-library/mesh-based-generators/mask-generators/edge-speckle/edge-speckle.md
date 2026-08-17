---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Verwenden Sie den Edge Speckle -Knoten, um fleckige Verschleißmuster an Netzkanten zu generieren, um realistische Kantenschädigungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## Edge Speckle

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske zeigt die Kanten an, an denen leicht Flecken hinzugefügt wurden, um sie zu zerlegen. Siehe auch [Edge-Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für die Kantenmarkierung. Erforderlich!
* **Variationsmaske**: *Graustufen-Eingabe*\
  Optionaler Maskenschlitz zum Maskieren der Effekte des Knotens. Aktivieren Sie diese Option mit &quot;Variationsmaske überschreiben&quot;.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt den Gesamtbetrag der Kantenhervorhebung fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Kantenauswahl**: *0.0 - 1.0* Legt den Einfluss konvexer Kanten fest.
* **Variation**: *0.0 - 1.0* Legt fest, inwieweit die Variationsmaske den Effekt auflöst.
* **Variationsmaske überschreiben**: *Falsch/Wahr*&#x200B;Übersteuert die integrierte Maske mit benutzerdefiniertem Eingabebereich.

## Beispielbilder

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>

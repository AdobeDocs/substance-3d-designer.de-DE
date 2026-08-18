---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Selektiver Dirt", um für eine realistische Bewitterung Akkumulationsmasken für selektiven Dirt auf der Grundlage der Gittergeometrie zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selektiver Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Selektiver Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## Selektiver Dirt

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html)-Maske stellt einen einfachen Dirt-Effekt auf konvexe Kanten dar.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Variationsmaske**: *Graustufen-Eingabe*\
  Optionale Variationszuordnung kann über Parameter aktiviert werden.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Gesamtstärke des Effekts fest, die nach und nach zum Vorschein kommt.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Variation**: *0.0 - 1.0* Legt den Grad der Variation/den Schmutz fest, der in den Effekt übergeht.
* **Variationsmaske überschreiben**: *Falsch/Wahr* Aktiviert das Überschreiben der Variation mit einem benutzerdefinierten Eingabebereich.

## Beispielbilder

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>

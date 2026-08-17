---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kantenunschärfe", um Kantenmasken zu verwischen, um weiche Übergänge und glatte kantenbasierte Verwitterungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kantenunschärfe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Kantenunschärfe

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## Kantenunschärfe

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske hebt Kanten auf Basis einer Karte mit gebackenen Krümmungen hervor. Es ist einer der einfacheren Maskengeneratoren.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map, auf dem der Effekt basiert.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt den Grad der Kantenhervorhebung fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Weichzeichnungsradius**: *0.0 - 8.0* Legt den Grad der Weichzeichnung an den hervorgehobenen Kanten fest.

## Beispielbilder

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>

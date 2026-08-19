---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kante-Dirt", um Dirt-Akkumulierungsmasken an Gitterkanten zu generieren, um realistische Kantenverwitterungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge-Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# Edge-Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## Edge-Dirt

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt einen Dirt-Effekt dar, der sich um Kanten herum ansammelt und ausschließlich auf einer Krümmungskarte basiert.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map zur Platzierung von Effekten. Erforderlich!
* **Variationsmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte, wird nur verwendet, wenn der Parameter &quot;override&quot; aktiviert ist.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Menge des Dirts fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Variation**: *0.0 - 1.0*&#x200B;Überblendungen, wie viel Maskierung/Aufteilung im großen Maßstab erfolgen soll.
* **Variationsmaske überschreiben**: *False/True*

## Beispielbilder

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>

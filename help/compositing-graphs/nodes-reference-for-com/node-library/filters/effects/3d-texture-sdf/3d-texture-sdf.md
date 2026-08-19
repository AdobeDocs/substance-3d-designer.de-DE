---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D Texture SDF-Knoten, um Feldtexturen mit Vorzeichen aus 3D-Daten zu generieren, um glatte Formen und Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Texture SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# 3D Texture SDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**In:** *Filter/Effekt*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Texture SDF** generiert das *vorzeichenbehaftete Abstandsfeld* einer Form aus der *3D-Textur* der **Eingabe**, die die Slices des *Volumes* der Form darstellt.

</td>
</tr>
</table>

## Parameter

### Eingaben

* **Maskeneingabe** *Graustufen*\
  Die *3D-Textur*-Maske, die die Slices des *Volumes* einer Form darstellt.

### Parameter

* **Schwellenwert** *Gleitkomma*\
  Wenn das Formvolumen durch einen *verblassenden Verlauf* beschrieben wird, wird der Verlaufswert festgelegt, bei dem die *Oberfläche* der Form *erkannt* wird.
* **Ausgabe** *Ganzzahl*\
  Der Typ des Distanzfelds, das ausgegeben werden soll:
  * *Entfernungsfeld*: gibt ein Abstandsfeld aus, das die Abstände *außerhalb* der Form beschreibt.
  * *Vorzeichenbehaftetes Abstandsfeld*: gibt ein Abstandsfeld aus, das die Abstände *außerhalb* (positiv) und *innerhalb* (negativ) der Form beschreibt.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Height-Normalmischer, um Height- und Normalzuordnungen zu mischen, um Oberflächendetailinformationen zu kombinieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Normal Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Height Normal Blender

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Height Normal Blender

**In:** *Filters/Normal Map*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Ein Shortcut-Knoten, der eine Graustufen-Heightmap mit einer Normalmap verbindet. Die Height-Eingabe wird intern in eine Normalmap konvertiert und dann korrekt mit der Normal-Eingabe überblendet.

Auf diese Weise lassen sich Details schneller überblenden als manuell mit separaten Knoten. Es fehlt jedoch möglicherweise an der nötigen Kontrolle und Verfeinerung für bestimmte Anforderungen.

## Parameter

### Eingaben

* **Height**: *Graustufen-Eingabe*\
  Graustufen-Höhenkarte zum Überblenden.
* **Normal**: *Farbeingabe*\
  Grundlegende Normalmap zum Überblenden.

### Parameter

* **Normalintensität**: *0.0 - 16.0* Intensität der normalen Konvertierung der Height-Eingabe.
* **Normales Format**: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

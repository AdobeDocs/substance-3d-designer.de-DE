---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Height Normal , um Height und Normalen-Map zu mischen, um Oberflächendetails zu kombinieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Normal Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Height Normal Blender

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein Tastaturbefehl-Knoten, der eine Graustufen-Heightmap mit einer Normalmap verbindet. Die Height-Eingabe wird intern in eine Normalmap konvertiert und dann korrekt mit der Normal-Eingabe überblendet.

Auf diese Weise lassen sich Details schneller überblenden als manuell mit separaten Knoten. Es fehlt jedoch möglicherweise an der nötigen Kontrolle und Verfeinerung für bestimmte Anforderungen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Height</b> <i>Graustufen-Eingabe</i> | Graustufen-Höhenkarte zum Überblenden. |
| <b>Normal</b> <i>Farbeingabe</i> | Grundlegende Normalmap zum Überblenden. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normalintensität</b> <i>0.0 - 16.0</i> | Intensität der normalen Umrechnung des Height-Eingangs. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |

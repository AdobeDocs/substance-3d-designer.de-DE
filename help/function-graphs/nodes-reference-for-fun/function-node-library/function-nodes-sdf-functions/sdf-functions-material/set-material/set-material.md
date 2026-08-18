---
title: Material festlegen
description: Legen Sie die Grundfarbe, die Raueit und die Metallität des Materials einer SDF-Szene fest.
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# Material festlegen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Materialsymbol festlegen](set-material.png "Material festlegen")

<b>In:</b> 3D-Funktion > Material

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Legen Sie die Grundfarbe, die Raueit und die Metallität des Materials einer SDF-Szene fest.

Diese Werte können dann für alle verstreuten SDF-Formen in den Ausgaben des [Shape-Splatters v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) abgerufen werden.

</td>
</tr>
</table>

>[!INFO]
> 
> Weitere Informationen zu Konzepten und Workflows mit SDF-Funktionen finden Sie auf der entsprechenden Seite: [Arbeiten mit SDF-Funktionen](../../working-with-sdf-functions.md)

## Eingaben

|                            |                                  |
|----------------------------|----------------------------------|
| <b>SDF-Szene</b> *Gleitend* | Die Eingabe-SDF-Szene. |
| <b>Grundfarbe</b> *Float3* | Der festzulegende RGB-Grundfarbwert. |
| <b>Metalität</b> *Gleitend* | Der festzulegende Metalitätswert. |
| <b>Raueit</b> *Gleitend* | Der festzulegende Raueitswert. |

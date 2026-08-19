---
title: Pyramide
description: Designer > Substance-Kompositionsgrafiken > Knotenreferenz für Substance-Kompositionsgrafiken > Knotenbibliothek > SDF-Funktion > Primitiv > Pyramide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# Pyramide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Pyramidensymbol](./3d-sdf-pyramid.png "Pyramide")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine Pyramide mit verstellbarem Height, Basisgröße und Basislage.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Weitere Informationen zu Konzepten und Workflows mit SDF-Funktionen finden Sie auf der entsprechenden Seite: [Arbeiten mit SDF-Funktionen](../../working-with-sdf-functions.md)

## Eingaben

|  |  |
| :--- | :--- |
| <b>Height</b> *Gleitend* | Das Z-Up-Height des Scheitelpunkts der Pyramide von ihrer Basis.<br><br><i>Standard: 1</i> |
| <b>Basisgröße</b> *Float2* | Die Größe der Pyramidenbasis in X und Y.<br><br><i>Standard: (1, 1)</i> |
| <b>Basisposition</b> *Float3* | Die Weltraumposition der Pyramidenbasis.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

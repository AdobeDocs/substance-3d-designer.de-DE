---
title: Pyramidenquadrat
description: Designer > Substance-Compositing-Grafiken > Knotenreferenz für Substance-Compositing-Grafiken > Knotenbibliothek > SDF-Funktion > Primitiv > Pyramidenquadrat
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# Pyramidenquadrat

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Pyramidenquadrat](./3d-sdf-pyramid-square.png "Symbol für Pyramidenquadrat")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine Pyramide mit quadratischer Grundfläche, mit verstellbarem Height und Grundposition.

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
| <b>Basisgröße</b> *Gleitend* | Die Länge der Basiskanten der Pyramide.<br>Alle Kanten sind gleich lang.<br><br><i>Standard: 1</i> |
| <b>Basisposition</b> *Float3* | Die Weltraumposition der Pyramidenbasis.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

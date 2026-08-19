---
title: Zylinder 2 Punkte
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Zylinder 2 Punkte
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Zylinder 2 Punkte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Zylinder 2 Punkte](./3d-sdf-cylinder-2-points.png "Zylinder 2 Punkte")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen Zylinder mit einstellbarem Radius, der durch die Lage seiner Start- und Endscheiben definiert ist.

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
| <b>Start</b> *Float3* | Die Position der Startdiskette des Zylinders.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Ende</b> *Float3* | Die Position der Endscheibe des Zylinders.<br><br><i>Standard: (0, 0, 1)</i> |
| <b>Radius</b> *Gleitend* | Der Radius des Zylinders.<br><br><i>Standard: 0,25</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

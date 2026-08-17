---
title: Ellipsoid
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Ellipsoid
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# Ellipsoid

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ellipsoidsymbol](./3d-sdf-ellipsoid.png "Ellipsoid")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für ein Ellipsoid, das eine abgerundete Form mit einstellbarem dreidimensionalen Radius ist.

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
| <b>Radius</b> *Float3* | Der Radius des Ellipsoids in X, Y und Z.<br><br><i>Standard: (0,35, 0,35, 0,5)</i> |
| <b>Mittenposition</b> *Float3* | Die Weltraumposition des Drehpunkts des Ellipsoids.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

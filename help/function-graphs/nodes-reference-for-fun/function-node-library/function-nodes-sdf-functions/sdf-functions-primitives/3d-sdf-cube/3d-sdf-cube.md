---
title: Würfel
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Cube
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Würfel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cube-Symbol](./3d-sdf-cube.png "Cube")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen Würfel, mit anpassbarer XYZ-Größe und Abrundung der Kanten.

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
| <b>Größe</b> *Float3* | Die Größe des Würfels auf X, Y und Z.<br><br><i>Standard: (1, 1, 1)</i> |
| <b>Rundung</b> *Gleitend* | Der Radius der abgerundeten Bögen, die auf die Kanten des Würfels angewendet werden.<br><br><i>Hinweis:</i> harte Kanten können an den Schnittpunkten der abgerundeten Radien auftreten.<br><br><i>Standard: 0</i> |
| <b>Pivot-Position (lokal)</b> *Float3* | Die Position des lokalen Drehpunkts des Welt-Raums, in der (0, 0, 0) den Drehpunkt in der Mitte des Würfels platziert.<br><br><i>Standard: (0, 0, -0,5)</i> |
| <b>Mittenposition</b> *Float3* | Die Position des Welt-Raums des Drehpunkts des Würfels.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

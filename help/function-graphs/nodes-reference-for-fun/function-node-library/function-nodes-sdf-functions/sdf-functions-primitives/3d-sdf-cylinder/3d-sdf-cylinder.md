---
title: Zylinder
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Zylinder
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Zylinder

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Zylindersymbol](./3d-sdf-cylinder.png "Zylinder")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen Zylinder mit verstellbarem Height, Radius und Rundung der Kanten.

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
| <b>Height</b> *Fließkommazahl* | Das Z-Up-Height des Zylinders von seiner Basis.<br><br><i>Standard: 1</i> |
| <b>Radius</b> *Fließkommazahl* | Der Radius des Zylinders.<br><br><i>Standard: 0,5</i> |
| <b>Rundung</b> *Fließkommazahl* | Der Radius der abgerundeten Bögen, die auf die Kanten des Zylinders angewendet werden.<br><br><i>Hinweis:</i> harte Kanten können an den Schnittpunkten der abgerundeten Radien auftreten.<br><br><i>Standard: 0</i> |
| <b>Pivot-Position (lokal)</b> *Fließkommazahl3* | Die Zylinderposition des lokalen Drehpunkts des Welt-Raums, wobei (0, 0, 0) den Drehpunkt in der Zylindermitte platziert.<br><br><i>Standard: (0, 0, -0,5)</i> |
| <b>Mittenposition</b> *Fließkommazahl3* | Die Zylinderposition des Drehpunkts des Welt-Raums.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

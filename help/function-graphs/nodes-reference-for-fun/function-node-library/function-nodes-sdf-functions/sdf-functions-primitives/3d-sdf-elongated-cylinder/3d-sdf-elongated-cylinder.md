---
title: Langzylinder
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Langer Zylinder
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Langzylinder

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für lang gestreckten Zylinder](./3d-sdf-elongated-cylinder.png "Langgestreckter Zylinder")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen länglichen Zylinder mit einstellbarer Länge, Radius und Rundung der Kanten.<br>Der längliche Zylinder ist das Ergebnis der Überbrückung zweier Zylinder.

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
| <b>Height</b> *Gleitend* | Das Z-Up-Height der Anfangs- und Endzylinder von ihrer Basis.<br><br><i>Standard: 0,5</i> |
| <b>Radius</b> *Gleitend* | Der Radius des Anfangs- und des Endzylinders.<br><br><i>Standard: 0,5</i> |
| <b>Rundung</b> *Gleitend* | Der Radius der abgerundeten Bögen, die auf die Kanten des langgestreckten Zylinders angewendet werden.<br><br><i>Hinweis:</i> harte Kanten können an den Schnittpunkten der abgerundeten Radien auftreten.<br><br><i>Standard: 0</i> |
| <b>Mittenposition</b> *Float3* | Die Position des Welt-Raums des Drehpunkts des langgestreckten Zylinders.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Verlängerungsdistanz</b> *Gleitend* | Die Strecke, auf der der Startzylinder verlängert wird.<br>D.h. der Abstand zwischen den Mittelpunkten des Anfangs- und des Endzylinders.<br><br><i>Standard: 0,5</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

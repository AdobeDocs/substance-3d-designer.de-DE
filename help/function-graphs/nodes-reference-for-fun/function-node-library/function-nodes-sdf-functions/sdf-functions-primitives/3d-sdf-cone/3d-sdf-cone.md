---
title: Kegel
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Kegel
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# Kegel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Kegel-Symbol](./3d-sdf-cone.png "Kegel")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen Konus mit einstellbarem Height, Radius und Lage.

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
| <b>Radius</b> *Fließkommazahl* | Der Radius der Kegelbasis.<br><br><i>Standard: 0,5</i> |
| <b>Height</b> *Fließkommazahl* | Das Z-Up-Height des Scheitelpunkts des Kegels von seiner Basis.<br><br><i>Standard: 1</i> |
| <b>Mittenposition</b> *Fließkommazahl3* | Die Position des Welt-Raums des Drehpunkts des Kegels.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

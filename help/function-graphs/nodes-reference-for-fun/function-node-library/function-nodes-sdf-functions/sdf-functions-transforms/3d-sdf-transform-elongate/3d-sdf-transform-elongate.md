---
title: länglich
description: Designer > Substance-Kompositionsgrafiken > Knotenreferenz für Substance-Kompositionsgrafiken > Knotenbibliothek > SDF-Funktion > Transformieren > Elongate
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# länglich

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Langgestrecktes Symbol](./3d-sdf-transform-elongate.png "Langgestreckt")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Längen Sie eine SDF-Form von einer einstellbaren Position aus.<br>Hiermit wird das Volumen einer SDF-Form ausgehend von einem anpassbaren Slice linear erweitert.

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
| <b>SDF</b> *Gleitend* | Die Eingabe-SDF-Form. |
| <b>Verlängerung</b> *Float3* | Die Dehnungslänge auf der X-, Y-, Z-Achse. |
| <b>Mittenposition</b> *Float3* | Die Weltraum-Position, von der die Form verlängert wird.<br>D.h. die Position der Scheibe wird verlängert. |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

---
title: Drehung (ungenau)
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Transformieren > Twist (ungenau)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Drehung (ungenau)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Drehung (ungenau)](./3d-sdf-transform-twist.png "Drehung (ungenau)")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Drehen Sie eine SDF-Form um ihre lokale Z-Achse zwischen einem Start- und einem Endpunkt in einem einstellbaren Winkel.<br><br><i>Hinweis:</i>Da diese Transformationsfunktion ungenau ist, können beim Rendern Artefakte auftreten.

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
| <b>Winkel</b> *Gleitend* | Der Winkel der Drehung am Ende der Drehung in Windungen. |
| <b>Start</b> *Gleitend* | Die Weltposition auf der Z-Achse, an der die Drehung beginnt. Das gesamte darunter liegende Volumen ist nicht verdreht. |
| <b>Ende</b> *Gleitend* | Die Weltposition auf der Z-Achse, wo die Verdrillung endet. Das gesamte oben genannte Volumen wird gleichmäßig um den angegebenen Winkel gedreht. |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

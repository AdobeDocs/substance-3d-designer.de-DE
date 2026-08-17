---
title: Biegung (ungenau)
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > Biegen (ungenau)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Biegung (ungenau)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Biegen (ungenau)&quot;](./3d-sdf-transform-bend.png "Biegen (ungenau)")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Biegt eine SDF-Form um ihre lokale Y-Achse zwischen einem Start- und Endpunkt in einem Winkel.<br><br><i>Hinweis:</i>Da diese Transformationsfunktion ungenau ist, können beim Rendern Artefakte auftreten.

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
| <b>Winkel</b> *Gleitend* | Der Winkel der Drehung am Ende der Biegung in Windungen. |
| <b>Start</b> *Gleitend* | Die Weltposition auf der Z-Achse, an der die Biegung beginnt. Das gesamte darunter liegende Volumen ist nicht gebogen. |
| <b>Ende</b> *Gleitend* | Die Weltposition auf der Z-Achse, an der die Biegung endet. Das gesamte oben genannte Volumen wird gleichmäßig um den angegebenen Winkel gedreht. |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

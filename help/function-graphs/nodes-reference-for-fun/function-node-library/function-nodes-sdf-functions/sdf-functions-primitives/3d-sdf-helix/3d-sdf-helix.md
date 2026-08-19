---
title: Helix (ca.)
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Helix (ca.)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Helix (ca.)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Helix (ca.) Symbol](./3d-sdf-helix.png "Helix (ca.)")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für die Näherung einer Helix, bei der es sich um eine Form handelt, die durch Ziehen eines Kreises entlang einer Kurvenwicklung entlang einer Aufwärtskurve um eine Achse gebildet wird.<br><br><i>Hinweis:</i>Da es sich bei dieser SDF-Funktion um eine Näherung handelt, können beim Rendern Artefakte auftreten.

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
| <b>Hauptradius</b> *Gleitend* | Der Abstand der Wickelkurve von der Achse.<br><br><i>Standard: 0.4</i> |
| <b>Geringfügiger Radius</b> *Gleitend* | Der Radius des Kreises, der entlang der Kurve gezogen wird, um die Oberfläche der Helix zu bilden.<br><br><i>Standard: 0.1</i> |
| <b>Height</b> *Gleitend* | Das Z-Up-Height der Helix.<br><br><i>Standard: 0,5</i> |
| <b>Wicklungen</b> *Gleitend* | Die Anzahl der vollen Windungen der Kurve um die Achse in 0,5.<br>Schritten, d. h. wie oft die Helix innerhalb eines Heights von 0,5.<br><br><i>Standard: 4</i> |
| <b>Mittenposition</b> *Float3* | Die Weltraumposition des Drehpunkts der Helix.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

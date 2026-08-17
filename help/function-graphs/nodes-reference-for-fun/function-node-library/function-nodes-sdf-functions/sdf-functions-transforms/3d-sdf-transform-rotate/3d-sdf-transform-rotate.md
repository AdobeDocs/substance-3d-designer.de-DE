---
title: Drehen
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > Drehen
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Drehen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol drehen](./3d-sdf-transform-rotate.png "Drehen")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Drehen Sie eine SDF-Form abwechselnd um eine oder mehrere Achsen von einem einstellbaren Drehpunkt aus.<br>Verwenden Sie den <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers</b>, um die ausgeführte Drehung zu visualisieren.

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
| <b>Winkel</b> *Gleitend* | Der Winkel, in dem die SDF-Form gedreht wird.<br><br>Der Winkel wird durch einen Kreis im <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers angezeigt</b>. Richten Sie die Kamera so aus, dass der Pfeil <b>Achse</b> als Mittelpunkt dieses Kreises angezeigt wird, um den Winkel Ihrer Drehung als Bruchteil einer Drehung deutlich zu sehen.<br><br><i>Standard: 0</i> |
| <b>Achse</b> *Float3* | Der normalisierte Vektor, der die Achse definiert, um die die SDF-Form gedreht wird.<br>Z. (0, 1, 0) dreht die SDF-Form um die Y-Achse ihres lokalen Drehpunkts.<br><br>Die Achse wird durch einen Pfeil im <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers</b> angezeigt. Die Farbe des Pfeils wird den XYZ-Komponenten dieses Vektors zugeordnet.<br><br><i>Standard: (0, 1, 0)</i> |
| <b>Pivot-Position</b> *Float3* | Die Weltraum-Position des lokalen Drehpunkts der SDF-Form, wobei (0, 0, 0) den Drehpunkt in der Mitte der SDF-Form platziert. Definiert den Ursprung der Drehung.<br><br>Der Pivot wird durch den Anfang des Pfeils im <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers</b> angezeigt. |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

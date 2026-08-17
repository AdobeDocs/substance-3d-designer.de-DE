---
title: P drehen
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > P drehen
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# P drehen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![P-Symbol drehen](./3d-sdf-transform-rotate-p.png "P drehen")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Drehen Sie den Weltraum um eine Achse in einem einstellbaren Winkel.<br>Die transformierte Ausgangsweltposition kann mit dem <b>P</b>-Eingang der meisten SDF-Funktionen verbunden werden, um sie in diesem transformierten Weltraum zu definieren.<br><br>Verwenden Sie den <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers</b>, um die ausgeführte Drehung anzuzeigen.<br><br><i>Tipp:</i> P-Transformationen können verkettet werden, aber beachten Sie, dass die Ergebnisse von der Reihenfolge der Vorgänge abhängen.

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
| <b>Winkel</b> *Gleitend* | Der Winkel, in dem sich der Weltraum dreht.<br><br>Der Winkel wird durch einen Kreis im <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers angezeigt</b>. Richten Sie die Kamera so aus, dass der Pfeil der <b>Achse</b> als Mittelpunkt dieses Kreises angezeigt wird, damit der Winkel Ihrer Drehung als Bruchteil einer Drehung deutlich erkennbar ist. |
| <b>Achse</b> *Float3* | Der normalisierte Vektor, der die Achse definiert, um die der Weltraum gedreht wird.<br>Z. (0, 1, 0) den Weltraum um die Y-Achse des Drehpunkts drehen.<br><br>Die Achse wird durch einen Pfeil im <b>Transformations-Pivot</b>-Helfer des <b>3D-Viewers</b> angezeigt. Die Farbe des Pfeils wird den XYZ-Komponenten dieses Vektors zugeordnet.<br><br><i>Standard: (0, 1, 0)</i> |
| <b>Pivot-Position</b> *Float3* | Die Weltraumposition des Drehpunkts, der den Ursprung der Drehung definiert.<br><br>Der Drehpunkt wird durch den Anfang des Pfeils im <b>Transformations-Drehpunkt</b>-Helfer des <b>3D-Viewers</b> angezeigt. |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

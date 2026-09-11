---
title: P drehen
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Transformieren > P drehen
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

Drehen Sie den Welt-Raum um eine Achse in einem einstellbaren Winkel.<br>Die transformieren Ausgangsposition kann mit dem <b>P</b>-Eingang der meisten SDF-Funktionen verbunden werden, um sie in diesem transformieren Welt-Raum zu definieren.<br><br>Verwenden Sie den <b>Transformieren-Pivot</b>-Helfer des <b>3D-Viewers</b>, um die ausgeführte Drehung anzuzeigen.<br><br><i>Tipp:</i> P transformieren, kann verkettet werden, aber beachten Sie, dass die Ergebnisse von der Reihenfolge der Vorgänge abhängen.

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
| <b>Winkel</b> *Fließkommazahl* | Der Drehwinkel des Welt-Raums.<br><br>Der Winkel wird durch einen Kreis im <b>Transformieren-Pivot</b>-Helfer des <b>3D-Viewers</b> angezeigt. Richten Sie die Kamera so aus, dass der Pfeil <b>Achse</b> als Mittelpunkt dieses Kreises angezeigt wird, um den Drehwinkel deutlich als Bruchteil einer Drehung zu sehen. |
| <b>Achse</b> *Fließkommazahl3* | Der normalisierte Vektor, der die Achse definiert, um die der Welt-Raum gedreht wird.<br>Z. (0, 1, 0) dreht den Welt-Raum um die Y-Achse des Drehpunkts.<br><br>Die Achse wird durch einen Pfeil im Helfer <b>Transformieren Pivot</b> des <b>3D-Viewers</b> dargestellt. Die Farbe des Pfeils wird den XYZ-Komponenten dieses Vektors zugeordnet.<br><br><i>Standard: (0, 1, 0)</i> |
| <b>Pivot-Position</b> *Fließkommazahl3* | Die Drehpunktposition des Drehpunkts, die den Welt-Raum der Drehung definiert.<br><br>Der Drehpunkt wird am Anfang des Pfeils im Helfer <b>Transformieren Pivot</b> des <b>3D-Viewers</b> angezeigt. |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

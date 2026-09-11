---
title: Torus
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Torus
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# Torus

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Torussymbol](./3d-sdf-torus.png "Torus")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen Torus, eine Form, die durch Ziehen eines kleineren Kreises entlang eines größeren Kreises gebildet wird.<i>Beide Kreise haben einen einstellbaren Radius.

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
| <b>Radius major</b> *Gleitend* | Der Radius des Kreises, entlang dem die kleinere Festplatte zur Bildung der Oberfläche des Torus geschwungen wird.<br><br><i>Standard: 0,5</i> |
| <b>Radius-Minor</b> *Gleitend* | Der Radius des Kreises, der entlang des Hauptkreises gefegt wird, um die Oberfläche des Torus zu bilden.<br><br><i>Standard: 0.2</i> |
| <b>Mittenposition</b> *Float3* | Die Position des Welt-Raums des Drehpunkts des Torus.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

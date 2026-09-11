---
title: Kapsel
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Kapsel
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Kapsel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Kapsel-Symbol](./3d-sdf-capsule.png "Kapsel")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine Kapsel mit einstellbarer Länge und einstellbarem Radius.<br>Die Kapsel ist das Ergebnis der Überbrückung zweier Sphären.

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
| <b>Start</b> *Float3* | Die Position der Startkugel.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Ende</b> *Float3* | Die Position der Endkugel.<br><br><i>Standard: (0, 0, 1)</i> |
| <b>Radius</b> *Gleitend* | Der Radius der Anfangs- und Endkugeln.<br><br><i>Standard: 0,25</i> |
| <b>Start/Ende an Tipp</b> *Boolescher Wert* | Steuert, ob die Positionen <b>Anfang</b> und <b>Ende</b> an den Enden der Kugeln liegen sollen.<br>Das heißt, steuert, ob das Height der Kapsel den Radius der Kugeln enthalten soll.<br><br><i>Standard: False</i> |
| <b>Mittenposition</b> *Float3* | Die Position des Welt-Raums des Drehpunkts der Kapsel.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

---
title: Stein
description: Designer > Substance-Kompositionsgrafiken > Knotenreferenz für Substance-Kompositionsgrafiken > Knotenbibliothek > SDF-Funktion > Primitiv > Felsen
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Stein

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rock-Symbol](./3d-sdf-rock.png "Rock")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine parametrische und randomisierbare Gesteinsform, die mit SDF-Funktionen gebaut wurde.

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
| <b>Max. facets</b> *Integer* | Die maximale Anzahl der Facetten des Felsens (bis zu 32).<br><br><i>Standard: 8</i> |
| <b>Smoothness</b> *Gleitend* | Der Radius der abgerundeten Bögen, die auf die Felskanten angewendet werden.<br><br><i>Standard: 0</i> |
| <b>Zufälligkeit</b> *Gleitend* | Zittert die Ausrichtung der Gesichter und den Abstand zur Mitte.<br>Daher führen größere Werte zu einem kleineren Felsen.<br><br><i>Standard: 0</i> |
| <b>Seed</b> *Gleitend* | Seed für den Parameter <b>Zufälligkeit</b>.<br><br><i>Standard: 0</i> |
| <b>Skalierung</b> *Gleitend* | Globale Skalierung der Gesteinsform.<br>Angewendet nach <b>Zufälligkeit</b> und vor <b>Smoothness</b>.<br><br><i>Standard: 0,5</i> |
| <b>Mittenposition</b> *Float3* | Die Weltraumposition des Drehpunkts des Felsens.<br><br><i>Standard: (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

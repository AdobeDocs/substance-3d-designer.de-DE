---
title: Torus capped
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Begrenzter Torus
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Torus capped

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Torus-Symbol begrenzt](./3d-sdf-capped-torus.png "Torus begrenzt")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen gedeckten Torus, bei der das Überstreichen des kleineren Kreises entlang eines größeren Kreises schräg gedeckt werden kann.<br>Beide Kreise haben einen einstellbaren Radius.

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
| <b>Hauptradius</b> *Gleitend* | Der Radius des Hauptkreises, entlang dem der Nebenkreis gefegt wird, um die Oberfläche des Torus zu bilden.<br><br><i>Standard: 0,5</i> |
| <b>Geringfügiger Radius</b> *Gleitend* | Der Radius des kleineren Kreises, der entlang des größeren Kreises gefegt wird, um die Oberfläche des Torus zu bilden.<br><br><i>Standard: 0.2</i> |
| <b>Winkel</b> *Gleitend* | Der zentrale Winkel, der abwechselnd den Trimmbogen des Hauptkreises definiert, entlang dem der Nebenkreis nicht gefegt wird.<br><br><i>Standard: 0,75</i> |
| <b>Winkelversatz</b> *Gleitend* | Der Versatz entlang des Hauptradius des Trimmbogens, entlang dem der Nebenkreis nicht überstrichen wird.<br><br><i>Standard: 0</i> |
| <b>Symmetrisch</b> *Boolescher Wert* | Steuert, ob der Trimmbogen in eine oder zwei Richtungen gezeichnet werden soll.<br><br><i>Standard: Wahr</i> |
| <b>Mittenposition</b> *Float3* | Die Weltraumposition des Drehpunkts des gedeckelten Torus.<br><br><i>Standard: (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

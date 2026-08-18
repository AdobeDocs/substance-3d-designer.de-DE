---
title: Spiegelbereich wiederholen
description: Designer > Substance-Kompositionsgrafiken > Knotenreferenz für Substance-Kompositionsgrafiken > Knotenbibliothek > SDF-Funktion > Operator > Spiegelungsbereich wiederholen
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Spiegelbereich wiederholen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Spiegelbereich wiederholen](./3d-sdf-op-repeat-mirror.png "Spiegelbereich wiederholen")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Spiegelt und dupliziert eine SDF-Form beliebig oft in einem regelmäßigen Abstand in der positiven oder negativen X-, Y- und Z-Achse.<br>Jedes Mal, wenn dieser Operator eine Form wiederholt, spiegelt er sie auch. Dies führt visuell zu einem Wechsel zwischen der ursprünglichen Ausrichtung der Form und einer gespiegelten Kopie.

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
| <b>Betrag +</b> *Integer3* | Die Anzahl der Duplikate entlang der positiven X-, Y-, Z-Achse.<br><br><i>Standard: (2, 0, 0)</i> |
| <b>Betrag -</b> *Integer3* | Die Anzahl der Duplikate entlang der negativen X-, Y-, Z-Achsen.<br><br><i>Standard: (2, 0, 0)</i> |
| <b>Abstand</b> *Float3* | Der Abstand zwischen den einzelnen Duplikaten.<br><br>Der Abstand wird durch einen kubischen Helfer dargestellt, dessen Größe der Abstand zwischen den Duplikaten in X-, Y- und Z-Richtung ist. Der Abstand beginnt an der <b>Ursprungsposition</b> und wird symmetrisch von dieser erhöht.<br><br><i>Standard: (2, 2, 2)</i> |
| <b>Ursprungsposition</b> *Float3* | Definiert die Mitte der SDF-Form, die dupliziert wird.<br><br>Die Ausgangsposition wird durch die Mittelposition des kubischen Helfers angezeigt.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

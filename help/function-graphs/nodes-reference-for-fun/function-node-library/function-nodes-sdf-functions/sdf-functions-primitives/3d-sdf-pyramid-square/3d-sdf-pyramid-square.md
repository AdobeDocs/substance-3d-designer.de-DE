---
title: Pyramide Square
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Pyramide Quadrat
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# Pyramide Square

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Pyramiden-Quadrat](./3d-sdf-pyramid-square.png "Symbol für Pyramiden-Quadrat")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine Pyramide mit quadratischer Grundfläche, mit verstellbarem Height und Grundposition.

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
| <b>Height</b> *Fließkommazahl* | Das Z-Up-Height des Scheitelpunkts der Pyramide von ihrer Basis.<br><br><i>Standard: 1</i> |
| <b>Basisgröße</b> *Fließkommazahl* | Die Länge der Basiskanten der Pyramide.<br>Alle Kanten sind gleich lang.<br><br><i>Standard: 1</i> |
| <b>Basisposition</b> *Fließkommazahl3* | Die Position des Welt-Raums der Pyramidenbasis.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

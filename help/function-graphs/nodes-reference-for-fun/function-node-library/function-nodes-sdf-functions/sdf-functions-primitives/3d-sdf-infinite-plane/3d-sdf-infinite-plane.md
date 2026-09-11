---
title: Unendliche Ebene
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Unendliche Ebene
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# Unendliche Ebene

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für unendliche Ebene](./3d-sdf-infinite-plane.png "Symbol für unendliche Ebene")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine unendliche Ebene mit verstellbarer Ausrichtung und Lage.

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
| <b>Normal</b> *Fließkommazahl3* | Der Welt-Raum-Normale-Vektor der unendlichen Ebene, der seine Ausrichtung steuert.<br>Der Vektor ist normalisiert.<br><br><i>Standard: (0, 0, 1)</i> |
| <b>Mittenposition</b> *Fließkommazahl* | Die Position des Welt-Raums des Drehpunkts der Ebene als Abstand vom Weltursprung entlang der Normalen der Ebene.<br><br><i>Standard: 0</i> |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

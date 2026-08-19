---
title: Fläche
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Primitiv > Ebene
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Fläche

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ebenensymbol](./3d-sdf-plane.png "Ebene")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für eine Ebene mit verstellbarer Ausrichtung, Lage und Größe.

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
| <b>Normal</b> *Float3* | Der Normalenvektor des Weltraums der Ebene, der seine Ausrichtung steuert.<br>Der Vektor ist normalisiert.<br><br><i>Standard: (0, 0, 1)</i> |
| <b>Größe</b> *Float2* | Die Größe der Ebene in X und Y.<br><br><i>Standard: (1, 1)</i> |
| <b>Thickness</b> *Gleitend* | Die Thickness der Ebene, die in alle Richtungen angewendet wird.<br>Die Ebene wird gerundet, wenn die Thickness erhöht wird.<br><br><i>Standard: 0</i> |
| <b>Mittenposition</b> *Float3* | Die Weltraumposition des Drehpunkts der Ebene.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

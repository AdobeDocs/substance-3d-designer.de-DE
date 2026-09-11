---
title: Union reibungslos
description: Designer > Substance-Compositing-Grafen > Knotenreferenz für Substance-Compositing-Grafen > Knotenbibliothek > SDF-Funktion > Operator > Union Smooth
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Union reibungslos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Unions-glattes Symbol](./3d-sdf-op-union-smooth.png "Union glatt")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Gibt die hinzugefügten Volumina von zwei SDF-Formen zurück, mit einer anpassbaren Glättung der Kanten ihrer Schnittmenge.

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
| <b>SDF 1</b> *Gleitend* | Die erste SDF-Form. |
| <b>SDF 2</b> *Gleitend* | Die zweite SDF-Form. |
| <b>Smoothness</b> *Gleitend* | Der Ausgleichungsradius, beginnend mit den Schnittkanten.<br><br><i>Standard: 0</i><br><br><i>Hinweis:</i> harte Kanten können dort auftreten, wo sich die Glättungsradien überschneiden. |

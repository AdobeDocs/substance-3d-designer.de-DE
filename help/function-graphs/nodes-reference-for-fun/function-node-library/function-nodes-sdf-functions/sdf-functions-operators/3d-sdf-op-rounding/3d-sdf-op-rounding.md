---
title: Abrunden
description: Designer > Substance-Compositing-Grafen > Knotenreferenz für Substance-Compositing-Grafen > Knotenbibliothek > SDF-Funktion > Operator > Abrunden
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# Abrunden

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rundungssymbol](./3d-sdf-op-rounding.png "Rundungssymbol")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erweitert eine SDF-Form, bläst sie auf und glättet ihre harten Kanten.

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
| <b>Radius</b> *Gleitend* | Der Radius der abgerundeten Bögen, die auf die Kanten der Form angewendet werden.<br><br><i>Hinweis:</i> harte Kanten können an den Schnittpunkten der abgerundeten Radien auftreten.<br><br><i>Standard: 0,05</i> |

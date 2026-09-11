---
title: 'Subtraktionsglättung '
description: 'Designer > Substance-Compositing-Grafen > Knotenreferenz für Substance-Compositing-Grafen > Knotenbibliothek > SDF-Funktion > Operator > Subtraktionsablauf '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Subtraktionsglättung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für glatte Subtraktion](./3d-sdf-op-subtraction-smooth.png "Symbol für glatte Subtraktion ")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Subtrahiert das Volumen der SDF 1 -Form von der SDF 2 -Form, wobei eine anpassbare Glättung an der Schnittstelle der beiden angewendet wird.

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
| <b>SDF 1</b> *Gleitend* | Die SDF-Form, von der subtrahiert wird. |
| <b>SDF 2</b> *Gleitend* | Die SDF-Form wird von der SDF 1-Form subtrahiert. |
| <b>Smoothness</b> *Gleitend* | Die Glättung, die am Schnittpunkt der beiden Formen angewendet wird.<br><br><i>Hinweis:</i> harte Kanten können an den Schnittpunkten der Glättungsradien auftreten. |

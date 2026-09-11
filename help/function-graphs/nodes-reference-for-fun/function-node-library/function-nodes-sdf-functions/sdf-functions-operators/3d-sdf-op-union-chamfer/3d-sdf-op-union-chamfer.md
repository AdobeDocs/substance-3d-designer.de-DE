---
title: Unionsfase
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Operator > Verbund-Fase
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Unionsfase

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Unions-Fase](./3d-sdf-op-union-chamfer.png "Unions-Fase")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Gibt die hinzugefügten Volumina zweier SDF-Formen zurück, mit einem zusätzlichen Volumen mit anpassbarem Radius entlang der Kanten ihrer Schnittmenge.

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
| <b>Radius</b> *Gleitend* | Der Radius des Volumens, das an den Rändern des Schnittpunkts der Formen hinzugefügt wurde.<br><br><i>Standard: 0</i> |

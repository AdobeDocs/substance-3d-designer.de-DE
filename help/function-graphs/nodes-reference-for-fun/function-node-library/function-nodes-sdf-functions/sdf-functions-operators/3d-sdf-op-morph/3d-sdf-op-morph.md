---
title: Morph
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Operator > Morph
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Morph

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Morph-Symbol](./3d-sdf-op-morph.png "Morph")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Gibt die lineare Interpolation zwischen einer Basis-SDF-Form und einer Ziel-SDF-Form entsprechend einem anpassbaren Mischfaktor zurück.

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
| <b>Basis-SDF</b> *Gleitend* | Die Basis-SDF-Form. |
| <b>Ziel-SDF</b> *Gleitend* | Die SDF-Zielform. |
| <b>Mischfaktor</b> *Gleitend* | Der Mischfaktor, der zum Morph der Eingangsformen verwendet wird, wobei 0 die Grundform und 1 die Zielform ist. |

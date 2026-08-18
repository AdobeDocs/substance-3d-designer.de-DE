---
title: Schnittfläche
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Operator > Schnittfläche
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Schnittfläche

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Schnittfläche](./3d-sdf-op-intersection-surface.png "Schnittfläche")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Gibt die Fläche des Bereichs einer SDF-Grundform zurück, der von einer anderen SDF-Form mit anpassbarer Thickness geschnitten wird.

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
| <b>Basis-SDF</b> *Gleitend* | Die SDF-Form, auf der die resultierende Oberfläche basiert. |
| <b>Schnittmenge mit SDF</b> bilden *Gleitend* | Die SDF-Form, die die Basis-SDF-Form schneidet. |
| <b>Thickness</b> *Gleitend* | Die Thickness der resultierenden Fläche.<br><br><i>Standard: 0,02</i> |

---
title: Skalieren
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > Skalieren
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# Skalierung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Skalierungssymbol](./3d-sdf-transform-scale.png "Skalierung")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Einheitliche Skalierung einer SDF-Form.

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
| <b>Skalierung</b> *Gleitend* | Der einheitliche Skalierungsfaktor.<br><br><i>Standard: 1</i> |
| <b>Pivot-Position</b> *Float3* | Die Weltraum-Position des lokalen Drehpunkts der SDF-Form, wobei (0, 0, 0) den Drehpunkt in der Mitte der SDF-Form platziert. <br>Definiert den Ursprung der Skalierung.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

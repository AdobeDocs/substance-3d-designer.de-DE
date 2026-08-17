---
title: Spiegeln
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > Spiegeln
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# Spiegeln

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol spiegeln](./3d-sdf-transform-flip.png "Spiegeln")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine Spiegeltransformation auf die Eingabe-SDF-Form an.<br>Führt im Wesentlichen eine negative Skalierung für die ausgewählten Achsen aus.

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
| <b>Spiegelachse</b> *Integer3* | Verwenden Sie einen Integer3-Wert, um den gewünschten Spiegelachse festzulegen.<br>Z. (1, 0, 0) spiegelt die X-Achse.<br><br><i>Standard: (1, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

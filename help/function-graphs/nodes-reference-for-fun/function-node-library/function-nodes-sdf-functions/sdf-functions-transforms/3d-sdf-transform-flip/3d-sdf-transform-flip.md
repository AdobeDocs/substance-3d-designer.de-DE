---
title: Spiegeln
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Transformieren > Spiegeln
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

Wendet eine Spiegelung an, die der Eingabe-SDF-Form transformieren ist.<br>Führt im Wesentlichen eine Negativskalierung für die ausgewählten Achsen aus.

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
| <b>SDF</b> *Fließkommazahl* | Die Eingabe-SDF-Form. |
| <b>Spiegelachse</b> *Ganzzahl3* | Verwenden Sie eine Ganzzahl3, um den gewünschten Spiegelachse festzulegen.<br>Z. (1, 0, 0) spiegelt die X-Achse.<br><br><i>Standard: (1, 0, 0)</i> |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

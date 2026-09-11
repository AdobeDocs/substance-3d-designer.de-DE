---
title: Versatz P
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Transformieren > Offset P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Versatz P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Offset P-Symbol](./3d-sdf-transform-offset-p.png "Offset P")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verschiebt den Welt-Raum entlang eines Vektors.<br>Die transformieren Ausgangsposition kann mit dem <b>P</b>-Eingang der meisten SDF-Funktionen verbunden werden, um sie in diesem transformieren Welt-Raum zu definieren.<br><br><i>Tipp:</i> P transformieren verkettet werden, aber beachten Sie, dass die Ergebnisse von der Reihenfolge der Vorgänge abhängen.

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
| <b>Offset</b> *Fließkommazahl3* | Die Entfernung, um die der Welt-Raum in X-, Y- und Z-Richtung versetzt ist. |
| <b>P</b> *Fließkommazahl3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die Position des nicht transformierten Welt-Raums.</i> |

---
title: Symmetrie
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Operator > Symmetrie
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Symmetrie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symmetrie-Symbol](./3d-sdf-op-symmetry.png "Symmetrie")

<b>In:</b> SDF-Funktion > Operator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Spiegelt und dupliziert eine SDF-Form über eine Spiegelebene und gibt dann die Vereinigung der SDF-Basisform und ihrer Duplikate zurück.<br>Die Symmetrie kann auf alle Achsen gleichzeitig angewendet werden.

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
| <b>Position der Spiegelebene</b> *Float3* | Die Position des Welt-Raums in der Mitte der Spiegelebene.<br>Diese Position wird von allen Spiegelebenen gemeinsam genutzt, wenn die Symmetrie auf mehrere Achsen angewendet wird.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Spiegelachse</b> *Integer3* | Legt die gewünschten Spiegelachse fest.<br><br>Beispiel: (1, 0, 0) wendet Symmetrie auf die X-Achse an.<br><br><i>Standard: (1, 0, 0)</i> |
| <b>Achse spiegeln</b> *Integer3* | Legt fest, welche Achsen gespiegelt werden sollen.<br><br>Beispiel: (1, 0, 0) spiegelt die Symmetrie auf der X-Achse.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Vorversatz</b> *Float3* | Der Versatz auf der X-, Y-, Z-Achse, der auf die Form angewendet wurde, bevor der Operator &quot;Symmetrie&quot; angewendet wurde. |

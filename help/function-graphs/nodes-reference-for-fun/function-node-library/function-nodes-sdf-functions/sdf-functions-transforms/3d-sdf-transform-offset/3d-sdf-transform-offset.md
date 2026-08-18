---
title: Verschiebung
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > SDF-Funktion > Transformieren > Offset
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---


# Verschiebung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Offset-Symbol](./3d-sdf-transform-offset.png "Offset")

<b>In:</b> SDF-Funktion > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Versatz einer SDF-Form entlang eines Vektors.

</td>
</tr>
</table>

<a name='inputs'></a>

|  |  |
| :--- | :--- |
| <b>SDF</b> *Gleitend* | Die Eingabe-SDF-Form. |
| <b>Offset</b> *Float3* | Der Abstand der SDF-Form wird in X-, Y-, Z-Richtungen versetzt.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>P</b> *Float3* | Die veränderte Weltraumposition. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

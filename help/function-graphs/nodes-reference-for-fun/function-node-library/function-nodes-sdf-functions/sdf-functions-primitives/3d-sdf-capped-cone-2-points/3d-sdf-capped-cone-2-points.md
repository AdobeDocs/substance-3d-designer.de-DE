---
title: Kegel mit Kappe 2 Punkte
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > SDF-Funktion > Primitiv > Capped-Kegel 2 Punkte
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Kegel mit Kappe 2 Punkte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für begrenzten Kegel 2 Punkte](./3d-sdf-capped-cone-2-points.png "Symbol für begrenzten Kegel 2 Punkte")

<b>In:</b> SDF-Funktion > Primitiv

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine SDF-Funktion für einen kappenförmigen Kegel, der durch die Lage von Boden und Oberseite definiert ist.<br>Die Basis und die Oberseite haben einstellbare Radien.

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
| <b>Positionsbasis</b> *Float3* | Die Position der Basis des Kappenkonus.<br><br><i>Standard: (0, 0, 0)</i> |
| <b>Oberkante positionieren</b> *Float3* | Die Position der Oberseite des Kappenkonus.<br><br><i>Standard: (0, 0, 1)</i> |
| <b>Radius Basis</b> *Gleitend* | Der Radius der Basis des Kegelstumpfs.<br><br><i>Standard: 0,5</i> |
| <b>Radius top</b> *Gleitend* | Der Radius des oberen Endes des Kegels.<br><br><i>Standard: 0.2</i> |
| <b>P</b> *Float3* | Die transformieren Position des Welt-Raums. Verwenden Sie diese Eingabe, um zusätzliche Transformationen mit den Knoten <b>Offset P</b> und <b>Rotate P</b> anzuwenden.<br><br><i>Standard: Die nicht transformierte Weltraumposition.</i> |

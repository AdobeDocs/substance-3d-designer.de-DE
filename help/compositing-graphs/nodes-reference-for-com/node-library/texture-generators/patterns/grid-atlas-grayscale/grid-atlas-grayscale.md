---
title: Rasteratlas-Graustufen
description: Designer > Substance-Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > Generator > Muster > Rasteratlas-Graustufen
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Rasteratlas-Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Graustufen-Symbol für Rasteratlas](grid-atlas-grayscale.resources/grid-atlas-grayscale.png "Graustufen für Rasteratlas")

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Lege bis zu 16 Graustufenbilder auf einem Raster mit anpassbarer XY-Größe an.<br>Das Ausgabeatlas-Bild kann von einem [Shape-Splatter v2](../shape-splatter-v2/shape-splatter-v2.md) oder einem [Shape-Splatter-Mapper-Graustufen](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)-Knoten gesampelt werden.

Siehe auch [Farbe des Rasteratlas](../grid-atlas-color/grid-atlas-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|                             |                                |
|:----------------------------|:-------------------------------|
| <b>Eingabe 1</b> *Graustufen* | Die #1 für Graustufenbilder. |
| <b>Eingabe 2</b> *Graustufen* | Die #2 für Graustufenbilder. |
| <b>Eingabe 3</b> *Graustufen* | Die #3 für Graustufenbilder. |
| <b>Eingabe 4</b> *Graustufen* | Die #4 für Graustufenbilder. |
| <b>Eingabe 5</b> *Graustufen* | Die #5 für Graustufenbilder. |
| <b>Eingabe 6</b> *Graustufen* | Die #6 für Graustufenbilder. |
| <b>Eingabe 7</b> *Graustufen* | Die #7 für Graustufenbilder. |
| <b>Eingabe 8</b> *Graustufen* | Die #8 für Graustufenbilder. |
| <b>Eingabe 9</b> *Graustufen* | Die #9 für Graustufenbilder. |
| <b>Eingabe 10</b> *Graustufen* | Die #10 für Graustufenbilder. |
| <b>Eingabe 11</b> *Graustufen* | Die #11 für Graustufenbilder. |
| <b>Eingabe 12</b> *Graustufen* | Die #12 für Graustufenbilder. |
| <b>Eingabe 13</b> *Graustufen* | Die #13 für Graustufenbilder. |
| <b>Eingabe 14</b> *Graustufen* | Die #14 für Graustufenbilder. |
| <b>Eingabe 15</b> *Graustufen* | Das Graustufenbild-#15. |
| <b>Eingabe 16</b> *Graustufen* | Das Graustufenbild-#16. |

<a name="outputs"></a>

## Ausgaben

|               |                                  |
|:--------------|:---------------------------------|
| <b>Ausgabe</b> | Der Graustufen-Rasteratlas für die Ausgabe. |

<a name="parameters"></a>

## Parameter

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Rastergröße X</b> *Integer* | Die Größe des Rasters auf der X-Achse.<br>D.h. die Anzahl der Bilder, die auf der X-Achse gepackt werden. |
| <b>Rastergröße Y</b> *Integer* | Die Größe des Rasters auf der Y-Achse.<br>D.h. die Anzahl der Bilder, die auf der Y-Achse gepackt werden. |
| <b>Ausgabegrößenmodus</b> *Integer* | Die Methode zum Definieren der Größe des Ausgabebilds gemäß dem Basisparameter &quot;Ausgabegröße&quot; des Knotens:<br><br>- <b>Manuell:</b> Verwenden Sie die Größe wie vorhanden.<br>- <b>Automatisches Verhältnis:</b> Passen Sie das Bildverhältnis gemäß der Rastergröße an, um die Bildgröße zu minimieren. Bei nicht quadratischen Rastern mit 3 Zeilen oder Spalten, z. B. 3, 2, 4, 3 |

## Beispiele

<img src="./grid-atlas-grayscale.resources/grid-atlas-grayscale-graph.png" alt="Rasteratlas-Graustufenknoten im Kontext eines Grafen" style="width: 50%"><br>
<i>Rasteratlas-Graustufenknoten im Kontext eines Grafen</i>

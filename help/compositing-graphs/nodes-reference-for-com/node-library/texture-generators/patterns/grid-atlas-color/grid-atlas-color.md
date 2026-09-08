---
title: Farbe des Rasteratlas
description: Designer > Substance-Compositing-Graf > Knotenreferenz für Substance-Compositing-Graf > Knotenbibliothek > Rasteratlas > Mustergenerator > Knotenfarbe
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Farbe des Rasteratlas

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Rasteratlas-Farbe](grid-atlas-color.resources/grid-atlas-color.png "Symbol für Rasteratlas-Farbe")

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Legen Sie auf einem Raster mit anpassbarem XY-Format bis zu 16 Farbbilder ab.<br>Das Ausgabeatlas-Bild kann von einem [Shape-Splatter v2](../shape-splatter-v2/shape-splatter-v2.md) oder einem [Shape-Splatter-Zuordnungsfarben](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)-Knoten gesampelt werden.

Siehe auch [Rasteratlas grayscale](../grid-atlas-grayscale/grid-atlas-grayscale.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|                         |                            |
|:------------------------|:---------------------------|
| <b>Eingabe 1</b> *Farbe* | Die #1 für die Farbbildeingabe. |
| <b>Eingabe 2</b> *Farbe* | Die #2 für die Farbbildeingabe. |
| <b>Eingabe 3</b> *Farbe* | Die #3 für die Farbbildeingabe. |
| <b>Eingabe 4</b> *Farbe* | Die #4 für die Farbbildeingabe. |
| <b>Eingabe 5</b> *Farbe* | Die #5 für die Farbbildeingabe. |
| <b>Eingabe 6</b> *Farbe* | Die #6 für die Farbbildeingabe. |
| <b>Eingabe 7</b> *Farbe* | Die #7 für die Farbbildeingabe. |
| <b>Eingabe 8</b> *Farbe* | Die #8 für die Farbbildeingabe. |
| <b>Eingabe 9</b> *Farbe* | Die #9 für die Farbbildeingabe. |
| <b>Eingabe 10</b> *Farbe* | Die #10 für die Farbbildeingabe. |
| <b>Eingabe 11</b> *Farbe* | Die #11 für die Farbbildeingabe. |
| <b>Eingabe 12</b> *Farbe* | Die #12 für die Farbbildeingabe. |
| <b>Eingabe 13</b> *Farbe* | Die #13 für die Farbbildeingabe. |
| <b>Eingabe 14</b> *Farbe* | Die #14 für die Farbbildeingabe. |
| <b>Eingabe 2</b> *Farbe* | Die #15 für die Farbbildeingabe. |
| <b>Eingabe 2</b> *Farbe* | Die #16 für die Farbbildeingabe. |

<a name="outputs"></a>

## Ausgaben

|               |                              |
|:--------------|:-----------------------------|
| <b>Ausgabe</b> | Der Rasteratlas der Ausgabefarbe. |

<a name="parameters"></a>

## Parameter

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Rastergröße X</b> *Integer* | Die Größe des Rasters auf der X-Achse.<br>D.h. die Anzahl der Bilder, die auf der X-Achse gepackt werden. |
| <b>Rastergröße Y</b> *Integer* | Die Größe des Rasters auf der Y-Achse.<br>D.h. die Anzahl der Bilder, die auf der Y-Achse gepackt werden. |
| <b>Ausgabegrößenmodus</b> *Integer* | Die Methode zum Definieren der Größe des Ausgabebilds gemäß dem Basisparameter &quot;Ausgabegröße&quot; des Knotens:<br><br>- <b>Manuell:</b> Verwenden Sie die Größe wie vorhanden.<br>- <b>Automatisches Verhältnis:</b> Passen Sie das Bildverhältnis gemäß der Rastergröße an, um die Bildgröße zu minimieren. Bei nicht quadratischen Rastern mit 3 Zeilen oder Spalten, z. B. 3, 2, 4, 3 |

## Beispiele

<img src="./grid-atlas-color.resources/grid-atlas-color-graph.png" alt="Rasteratlas-Farbknoten im Kontext eines Graphen" style="width: 50%"><br>
<i>Rasteratlas-Farbknoten im Kontext eines Diagramms</i>
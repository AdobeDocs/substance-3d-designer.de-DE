---
title: Shape Splater v2 Mapper-Farbe
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > Generator > Muster > Formspritzer v2 Mapper-Farbe
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '1948'
ht-degree: 0%

---


# Shape Splater v2 Mapper-Farbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für die v2-Zuordnungsfarbe für Shape-Splatter](shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color.png "Symbol für die v2-Zuordnungsfarbe für Shape-Splatter")

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ordnet Farbbilder Formen zu, die mit dem Knoten [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) generiert und gestreut wurden, und verwendet dabei die vom Knoten bereitgestellten zusätzlichen Daten.<br><br>Bilder werden als separate Mustereingaben bereitgestellt oder in einen Rasteratlas verpackt und können mithilfe von UV-Mapping, triplanarer Projektion oder benutzerdefinierter Mapping auf die Formen angewendet werden.<br><br>Formen können getönt werden und ihre Farben können gleichmäßig oder zufällig pro Form angepasst werden.

Siehe auch [Shape splatter v2 mapper grayscale](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

</td>
</tr>
</table>

>[!INFO]
>
> Dieser Knoten erfordert Eingabedaten, die vom Knoten [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) generiert werden.
> 
> Weitere Knoten in der Shape-Splatter-V2-Familie:
> * [Form platzieren v2 auf Maske ](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
>
> Mit den [Rasteratlas color](../grid-atlas-color/grid-atlas-color.md) können Sie Bilder in einen Atlas mit benutzerdefinierter Größe packen, bis zu 16 Muster in 4*4 Zellen.

>[!TIP]
> 
> Das [**-Materialmuster &quot;Rusty bolts&quot;**](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) ist verfügbar, um mit Shape-Splatter v2-Knoten zu beginnen.
> 
> Weitere Informationen zu Konzepten und Workflows mit SDF-Funktionen finden Sie auf der entsprechenden Seite: [Arbeiten mit SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Eingaben

|                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:--------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Rasteratlas-Eingabe</b> *Farbe* | Ein Farbbild mit Mustern, die in einem Rasterlayout zusammengefasst sind.<br><br>Die Rastergröße muss mit der Größe übereinstimmen, die vom Knoten [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) verwendet wird.<br><br>Verwenden Sie den Knoten [Rasteratlas color](../grid-atlas-color/grid-atlas-color.md), um separate Muster in einen Rasteratlas zu packen. |
| <b>Mustereingabe 1</b> *Farbe* | Das Farbbild für das #1, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 2</b> *Farbe* | Das Farbbild für das #2, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 3</b> *Farbe* | Das Farbbild für das #3, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 4</b> *Farbe* | Das Farbbild für das #4, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 5</b> *Farbe* | Das Farbbild für das #5, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 6</b> *Farbe* | Das Farbbild für das #6, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 7</b> *Farbe* | Das Farbbild für das #7, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Mustereingabe 8</b> *Farbe* | Das Farbbild für das #8, das den Formen zugeordnet ist.<br><br><i>Tipp:</i> Verwenden Sie eine Auflösung, die der maximalen Größe des Musters beim Streuen nahe kommt. |
| <b>Hintergrundeingabe</b> *Farbe* | Das Farbbild, das als Hintergrund für die zugeordneten Formen verwendet wird. |
| <b>Farbeingabe</b> *Farbe* | Das Farbbild, das zum Aufhellen der zugeordneten Formen entsprechend ihrer Pivot-Position verwendet wird.<br><br>Verwenden Sie den Parameter <b>Deckkraft für Farbeingabe</b>, um die Intensität des Beitrags dieser Farben zur Formenfarbe anzupassen. |
| <b>Normal</b> *Farbe* | Die für die verstreuten Formen berechneten Normalen, maskiert gemäß der Überblendung mit dem Hintergrund-Height.<br><br> Wenn der <b>Shape-Typ</b> &#39;Rasteratlas&#39; ist, werden die für die <b>Rasteratlas-Normal</b>-Eingabe bereitgestellten Normalen direkt verwendet. |
| <b>Splatter UVW</b> *Farbe* | <b>R</b> - U-Komponente der UVs der Formen.<br><b>G</b> - V-Komponente der UVs der Formen.<br><b>B</b> - Height der Formen. (W)<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> Der eindeutige Bezeichner der Formen. (ID)<br> - <i>Bruchteil:</i> hängt vom <b>Formtyp ab</b>: Materialkennung bei SDF/primitive, Musterkennung* bei Mustereingabe/Rasteratlas.<br><br><b>*:</b> Die Musterkennung ist der Indexwert der Form in der Liste/im Atlas. |
| <b>Splatter-Daten 1</b> *Farbe* | <b>R</b> - X-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>G</b> - Y-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>B</b> - Z-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> U-Komponente der UV-Koordinaten für die Daten der Formen in den Datenausgaben 2/3.<br> - <i>Bruchteil:</i> V-Komponente der UV-Koordinaten für die Daten der Formen in den Daten 2/3-Ausgaben.<br> - <i>Signieren:</i> Binärmaske zum Mischen der Formen mit dem Hintergrund-Height. |
| <b>Splatter-Daten 2</b> *Farbe* | <b>R</b> - X-Komponente der 3D-Drehung der Formen.<br><b>G</b> - Y-Komponente der 3D-Drehung der Formen.<br><b>B</b> - Z-Komponente der 3D-Drehung der Formen.<br><b>A</b> - Drehung der Formen um ihre Normale.<br><br>Alle Drehungen sind in der Anzahl der Umdrehungen definiert. |
| <b>Splatter-Daten 3</b> *Farbe* | <b>R</b> - X Komponente der Position der Formen.<br><b>G</b> - Y Komponente der Position der Formen.<br><b>B</b> - Der Versatz der Formen entlang ihrer Normalen.<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> Die ID der Form.<br> - <i>Bruchteil:</i>Der Index des Formenmusters im Quellatlas. (Bei Verwendung eines Rasteratlas-Mustertyps) |
| <b>Splatter-Daten 4</b> *Farbe* | <i>Pixel 1</i><br><b>R</b> - X-Größe der Datenausgabebilder 2/3.<br><b>G</b> - Y-Größe der Datenausgabebilder 2/3.<br><b>B</b> - X-Größe des Datenausgabebildes 4.<br><b>A</b> - Y-Größe des Datenausgabebildes 4.<br><br><i>Pixel 2</i><br><b>R</b> - Der Formtyp. (E.g. Würfel, Zylinder, ...)<br><b>G</b> - Packedaten:<br> - <i>Absoluter Wert:</i> Die Mustereingabenummer.<br> - <i>Signieren:</i> Normales Format der normalen Ausgangszuordnung. (positiv: DirectX / Negativ: OpenGL)<br><b>B</b> - X-Größe des Rasteratlas. (d. h. die Anzahl der Spalten)<br><b>A</b> - Y-Größe des Rasteratlas. (d. h. die Anzahl der Zeilen) |

<a name="outputs"></a>

## Ausgaben

|               |                     |
|:--------------|:--------------------|
| <b>Ausgabe</b> | Die farbigen Formen. |

<a name="parameters"></a>

## Parameter

|                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Projektionsmodus</b> *Integer* | Die Methode zum Projizieren der Eingabebilder auf die Formen:<br><br>- <b>Von Spritzer-UVs:</b> Verwenden Sie die UVs, die vom Knoten &#39;Shape Spritzer v2&#39; bereitgestellt werden.<br>- <b>Triplanar:</b> Verwenden Sie die triplanare Projektion, um die Bilder auf den lokalen XYZ-Achsen der Formen zuzuordnen.<br>- <b>Benutzerdefinierte Funktion:</b> Erstellen Sie ein Funktionsdiagramm, um die Zuordnung der Bilder zu den Formen zu definieren. |
| <b>Benutzerdefinierte Funktion</b> *Float4* | Gibt die RGBA-Farbe pro Pixel der Formen als Float4 an.<br><br>Die folgenden Variablen sind verfügbar:<br>- <code>shape.position.os</code> (Float3) Die Position der Formoberfläche im Objektraum.<br>- <code>shape.position.ws</code> (Float3) Die Position der Formoberfläche im Weltraum*.<br>- <code>shape.normal.os</code> (Float3) Die Normalen der Formoberfläche im Objektraum.<br> - <code>shape.normal.ws</code> (Float3) Die Normalen der Formoberfläche im Weltraum*.<br>- <code>shape.id</code> (Float) Eindeutiger Bezeichner der Form.<br>- <code>material.id</code> (Float) Die Material-ID der Formoberfläche, definiert durch den Knoten &quot;Shape splatter v2&quot;.<br><br>*: Der Weltraum der Form ist auf ihrem Drehpunkt zentriert und berücksichtigt nicht das Height der Form. Das bedeutet, dass der einzige Unterschied zum Objektraum die Ausrichtung ist.<br><br>Wenn die Eingaben des Knotens &#39;Shape Splater v2 Mapper Color&#39; gesampelt werden müssen, können die folgenden <b>Sample color</b>-Knoteneingabeslots verwendet werden:<br>- 0: Rasteratlas <br>- 1-8: Mustereingabe 1-8 |
| <b>Ist normale Karte</b> *Boolescher Wert* | Gibt an, ob es sich bei den für die <b>Rasteratlas-Eingabe</b> oder die <b>Mustereingabe #</b> bereitgestellten Bildern um Normalzuordnungen handelt.<br><br>Dies ist erforderlich, um die Verarbeitung zu aktivieren, die für die korrekte Verarbeitung der normalen Vektoren und deren Anwendung auf die Formen erforderlich ist. |
| <b>Normales Eingabeformat</b> *Integer* | Das Format der normalen Zuordnungen, die für den <b>Kanaleingang</b> oder den <b>Mustereingang #</b> bereitgestellt werden.<br><br>Kehrt den grünen Rasteratlas effektiv um.<br><br>- <b>DirectX:</b> Die Y-Achse zeigt nach oben.<br>- <b>OpenGL:</b> Die Y-Achse zeigt nach unten. |
| <b>Füllkontrast</b> *Gleitend* | Die Schärfe der Übergänge zwischen planaren Vorsprüngen, wobei 1 keinen Überblendungsgradienten bedeutet. |
| <b>Bildprojektion</b> *Integer* | Die Anzahl von <b>Mustereingabebildern #</b>, die über die planaren Projektionen verteilt sind und zur dreiplanaren Zuordnung beitragen.<br><br>Um alle Seiten einer Form abzudecken, wird eine vordere (+) und hintere (-) planare Projektion auf jede Achse mit insgesamt 6 Projektionen durchgeführt.<br><br>- <b>1 Bild:</b> Der Mustereintrag 1 wird für alle planaren Projektionen verwendet.<br>- <b>3 Bilder:</b> Für die +/- Projektion jeder Achse wird ein separater Mustereingang verwendet.<br>- <b>6 Bilder:</b> Jede Projektion verwendet einen separaten Mustereingang.<br>- <b>1 Bild pro Material :</b> Verwenden Sie eine separate Mustereingabe pro Material-ID, wobei jedes Bild für alle planaren Projektionen verwendet wird. |
| <b>Projektionszentrum</b> *Float3* | Verschiebt die triplanare Projektion pro Achse im Objektraum.<br><br>Der Versatz wird auf den <i>gesamten Projektionsraum </i> angewendet, sodass ein Versatz auf einer Achse die Positionierung der Texturen beeinflusst, die auf die <i>anderen zwei</i> Achsen projiziert werden. |
| <b>Projektionsskala</b> *Gleitend* | Passt die Skalierung der projizierten Texturen auf <i>allen Achsen</i> um den angegebenen Faktor an. |
| <b>Eingabeauswahlmodus</b> *Integer* | Die Methode zum Auswählen, welche der Eingabebilder den Formen zugeordnet werden sollen.<br><br>Der <b>Shape-Typ</b>, der im Quellknoten &#39;Shape splatter v2&#39; ausgewählt ist, ändert die Art und Weise, wie Rasteratlasse Formen zugewiesen werden:<br><br>- <b>Rasteratlas</b> bedeutet, dass die Bilder in der &#39;Mustereingabe&#39; durch übereinstimmende Rasterindizes abgerufen werden (beide Atlanten sollten die gleiche Rastergröße verwenden)<br>- <b>Mustereingabe</b> bedeutet, dass die Bilder in den Eingaben der &#39;Mustereingabe #&#39; durch übereinstimmende Indizes abgerufen werden.<br>- <b>Andere Formtypen:</b> werden indem die Indizes mit den Material-IDs der Form abgeglichen werden.<br><br>Die verfügbaren Auswahlmethoden sind:<br>- <b>Aus Spritzdaten:</b> Abgleichen der Indizes der Rasteratlas &quot;Mustereingabe #&quot; oder &quot;Mustereingabe&quot; mit den Indizes der Formen, die vom Knoten &quot;Form spritzen v2&quot; zugewiesen werden.<br>- <b>Manuell:</b> Verwenden Sie den durch den Parameter &quot;Bildindex&quot; angegebenen .<br>- <b>-}Zufällig:</b> Verwenden Sie einen zufälligen Index in dem Bereich, der durch den Parameter &quot;Zufälliger Bereich&quot; angegeben wird. |
| <b>Mustereingabenummer</b> *Integer* | Die Menge von <b>Mustereingabebildern #</b>, die den Formen zugeordnet werden sollen. |
| <b>Image index</b> *Integer* | Der Index des Eingabemusters aus der <b>Mustereingabe #</b> oder <b>Rasteratlas-Eingabe </b>, der den Formen zugeordnet werden soll. |
| <b>Zufallsbereich</b> *Integer2* | Der Indexbereich von der <b>Mustereingabe #</b> oder <b>Mustereingabe </b>, in die das Rasteratlas zufällig ausgewählt werden soll, um den Formen zugeordnet zu werden. |
| <b>HSL-Anpassung</b> *Float3* | Ein Versatz, der gleichmäßig auf den Farbton, die Sättigung und die Luminanz (HSL) aller Formen angewendet wird. |
| <b>HSL zufällig</b> *Float3* | Ein zufälliger positiver oder negativer Versatz, der auf den Farbton, die Sättigung und die Luminanz (HSL) der Formen bis zu den angegebenen Werten angewendet wird. |
| <b>Deckkraft für Farbeingabe</b> *Gleitend* | Die Intensität des Beitrags der <b>Farbeingabe</b> zu den Farben der Formen gemäß dem ausgewählten <b>Farbeingabe-Mischmodus</b>. |
| <b>Farbeingabe-Mischmodus</b> *Integer* | Die Farbüberblendung, die zum Kombinieren von Vorder- und Hintergrundbildern verwendet wird.<br><br>Diese Vorgänge sind mit ihren Entsprechungen im Knoten <b>Blend</b> identisch.<br><br>Verfügbare Modi:<br>- <b>Kopieren</b><br>- <b>Hinzufügen (linear abwedeln)</b><br>- <b>Subtrahieren</b><br>- <b>Multiplizieren</b><br>- <b>Überlagerung</b> |
| <b>Normaler zufälliger Winkel</b> *Gleitend* | Ein Richtungsvektor wird vom Ursprung des Normalvektors zu einem zufälligen Punkt auf der Basis eines Kegels um den Normalvektor erzeugt, dann wird der Normalvektor mit diesem Zufallsrichtungsvektor vermischt.<br><br>Mit diesem Parameter wird der Winkel <i> des Kegels </i> angepasst, wobei 1 eine Halbkugel ist und 0 bedeutet, dass der Richtungsvektor gleich dem Normalenvektor ist. |
| <b>Mustermodus</b> *Integer* | Die Achsen, entlang denen die Textur wiederholt werden soll:<br> - <b>Keine Unterteilung</b><br> - <b>Horizontale Unterteilung</b><br> - <b>Vertikale Unterteilung</b><br> - <b>H und V Unterteilung</b>: Kombinierte horizontale und vertikale Kachelung. |
| <b>UV-Kachelung</b> *Gleitend* | Passt die globale Unterteilung der Bilder an, die den Formen zugeordnet werden.<br><br>Höhere Werte führen zu mehr Wiederholungen. |
| <b>UV-Skalierung</b> *Float2* | Passt die Unterteilung der Bilder, die den Formen zugeordnet sind, nach dem angegebenen Faktor an, mit separaten Steuerelementen für die U- und V-Skalierung. Höhere Werte führen zu mehr Wiederholungen. |
| <b>UV-Versatz</b> *Float2* | Wendet einen Versatz auf die Zuordnung der Bilder zwischen den Formen an, wodurch eine Feinanpassung der Positionierung der Bilder auf den Formen möglich ist.<br><br>Dieser Offset wird dem <b>zufälligen Offset</b> hinzugefügt, falls vorhanden. |
| <b>Zufälliger Versatz</b> *Gleitend* | Wendet einen zufälligen positiven oder negativen Versatz <i> pro Form </i> auf die Zuordnung der Bilder zwischen den Formen an, bis zum angegebenen Wert.<br><br>Dieser Offset wird dem <b>UV-Versatz</b> hinzugefügt, falls vorhanden. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0; background: transparent">
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-triplanar-02.gif" /><br><i>Triplanare Zuordnung</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-normal.gif" /><br><i>Normale Zuordnung</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-02.jpg" /><br><i>Zuordnung pro Material-ID aus SDF-Formen</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-tiling.gif" /><br><i>Kachelanpassung mit triplanarer Zuordnung</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-01.jpg" /><br><i>Zuordnung pro Material-ID aus Zylinderform</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-graph.png" /><br><i>Knoten im Kontext eines Diagramms</i>" /&gt;
        </td>
    </tr>
</table>


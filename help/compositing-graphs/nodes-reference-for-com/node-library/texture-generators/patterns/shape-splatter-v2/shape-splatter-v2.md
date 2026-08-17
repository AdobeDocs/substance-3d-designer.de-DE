---
title: Form-Splätter v2
description: Designer > Substance von Compositing-Graphen > Knotenreferenz für Substance-Compositing-Graphen > Knotenbibliothek > Generator > Muster > Formspritzer v2
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '4234'
ht-degree: 0%

---


# Form-Splätter v2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für Shape-Splatter v2](shape-splatter-v2.resources/shape-splatter-v2.png "Symbol für Shape-Splatter v2")

<b>In:</b> Generator > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Streuung von Formen auf einem Hintergrund-Height mit erweiterten Streuungsfunktionen in einem virtuellen <b>3D-Raum</b>, mit Steuerelementen für Position, Drehung, Skalierung und Zufälligkeit.<br><br>Der Knoten bietet einfache primitive 3D-Formen an und unterstützt benutzerdefinierte Formen, die entweder als <b>Musterbild</b>, als <b>Atlas</b> oder als <b>signiertes Distanzfeld (SDF)</b>-Funktion für komplexe benutzerdefinierte 3D-Formen bereitgestellt werden.<br><br>Es sind mehrere <b>Methoden zum Verteilen von Formen </b> verfügbar, einschließlich des Erstellens einer benutzerdefinierten Funktion für vollständige Kontrolle.<br><br>Formen können mithilfe einer benutzerdefinierten <b>Dichte-Map</b> in bestimmte Bereiche gezogen werden.<br><br><i>Hinweis:</i> Dieser Knoten ist nicht für die Verwendung mit den CPU-Versionen der Substance-Engine vorgesehen, d. h. SSE2 (Windows, Linux) und NEON (macOS).

</td>
</tr>
</table>

>[!INFO]
>
> Die von diesem Knoten generierten Daten können mit den anderen Knoten in der Shape-Splatter-V2-Familie verwendet werden:
> * [Zuordnungsfarbe für Shape-Splatter v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)
> * [Graustufen-Zuordnungs-Splatter v2](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
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

|                                      |                                                                                                                                                                                                                                                                                                                                                                  |
|:-------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Hintergrund-Height</b> *Graustufen* | Die Grundkarte des Heights, in der Formen gestreut sind. Die Heights werden jeweils mit einem &quot;Max blend&quot; kombiniert, wobei das höhere der beiden verwendet wird.<br><br>Der Beitrag des Hintergrund-Heights zum Ausgabe-Height wird durch den Parameter <b>Hintergrundeingabe-Deckkraft</b> gesteuert. |
| <b>Dichte-Map</b> *Graustufen* | Eine Graustufenkarte, die den Versatz von Formen gemäß ihrer Luminanz steuert, indem Formen in ihren helleren Bereichen gesammelt werden.<br><br>Die Intensität des Versatzes von Formen wird durch den <b>Dichte-Map-Multiplikator</b>-Parameter gesteuert. |
| <b>Height-Offsetzuordnung</b> *Graustufen* | Eine Graustufenzuordnung, bei der den Formen entsprechend dem Drehpunkt der Formen Werte gleichmäßig hinzugefügt werden.<br><br>Der Beitrag der Map wird durch den <b>Height-Offset-Map-Multiplikator</b> gesteuert. |
| <b>Height-Skalierungszuordnung</b> *Graustufen* | Eine Graustufenzuordnung, bei der Werte als Faktor für das Height der Formen verwendet werden.<br><br>Der Beitrag der Map wird durch den <b>Height-Skalierungsmapmultiplikator</b> gesteuert. |
| <b>Formskalierungszuordnung</b> *Graustufen* | Eine Graustufen-Map, deren Werte als Faktor für die Skalierung der Formen verwendet werden.<br><br>Der Beitrag der Karte wird durch den <b>Skalierungszuordnungsvervielfacher</b>-Parameter gesteuert. |
| <b>Formdrehung</b> *Graustufen* | Eine Graustufenzuordnung, bei der der 3D-Drehung von Formen Werte hinzugefügt werden, die durch die Faktoren pro Achse angepasst werden, die durch den <b>3D-Rotation Map-Multiplikator</b> bereitgestellt werden. |
| <b>Vektorzuordnung</b> *Farbe* | Eine Map, die Richtungsvektoren beschreibt, die verwendet werden können, um die Drehung und/oder Position von Formen mithilfe der folgenden Parameter zu steuern:<br><br>- <b>Der Vektorzuordnungs-Versatz</b> passt die Auswirkungen der Map zum Verschieben der Formen an.<br>- <b>Der Rotationseingang der Steigung</b> kann auf &quot;Vektorzuordnung&quot; festgelegt werden, um diese Map zum Drehen der Formen mithilfe der zugehörigen Parameter zu verwenden. |
| <b>Maskenzuordnung</b> *Graustufen* | Das Bild, das zum Maskieren von Formen gemäß dem Schwellenwert <b>Maskenzuordnung</b>.<br><br>verwendet wird, d. h. Formen, die sich in Bereichen der Karte befinden, in denen die Luminanz unter diesem Schwellenwert liegt, werden maskiert. |
| <b>Mustereingabe 1</b> *Graustufen* | Die Musterzuordnung für das #1, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 2</b> *Graustufen* | Die Musterzuordnung für das #2, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 3</b> *Graustufen* | Die Musterzuordnung für das #3, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 4</b> *Graustufen* | Die Musterzuordnung für das #4, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 5</b> *Graustufen* | Die Musterzuordnung für das #5, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 6</b> *Graustufen* | Die Musterzuordnung für das #6, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 7</b> *Graustufen* | Die Musterzuordnung für das #7, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Mustereingabe 8</b> *Graustufen* | Die Musterzuordnung für das #8, das gestreut wird, wenn <b>Mustertyp</b> auf &quot;Mustereingabe&quot; festgelegt ist.<br><br><i>Tipp:</i> Verwenden Sie eine Height-Auflösung, die der Maximalgröße des gestreuten Musters nahe kommt. |
| <b>Rasteratlas-Height</b> *Graustufen* | Das Bild, das das Height von Mustern beschreibt, die in einen Atlas gepackt wurden.<br><br>Verwenden Sie den Rasteratlas <b>ATLANS size</b>, um die Rastergröße des Atlas anzugeben. |
| <b>Rasteratlas normal</b> *Farbe* | Das Bild, das die Normalen von Mustern beschreibt, die in einen Atlas gepackt wurden.<br><br>Verwenden Sie den Rasteratlas <b>ATLANS size</b>, um die Rastergröße des Atlas anzugeben. |

<a name="outputs"></a>

## Ausgaben

|                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Height</b> | Die berechnete Height-Map für die verstreuten Formen, einschließlich des Hintergrund-Heights, falls verwendet und sichtbar. |
| <b>SDF-Farbe</b> | Die Farben der Form, die von der <b>SDF-Funktion</b> erzeugt wurde.<br><br>Verwenden Sie den Knoten &quot;<a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-color/set-color.md">Farbe festlegen</a>&quot; im Farbdiagramm, um eine SDF-Funktion für jede Komponente der Form zu definieren. |
| <b>SDF-Metalität</b> | Die Farben der Form, die von der <b>SDF-Funktion</b> erzeugt wurde.<br><br>Verwenden Sie den Knoten <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-metalness/set-metalness.md">Metalness festlegen</a> im Komponentendiagramm, um einen Metalitätswert pro SDF-Funktion der Form zu definieren. |
| <b>SDF-Raueit</b> | Die Farben der Form, die von der <b>SDF-Funktion</b> erzeugt wurde.<br><br>Verwenden Sie den Knoten <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-roughness/set-roughness.md">Raueit festlegen</a> im Komponentendiagramm, um einen Raueitswert pro SDF-Funktion der Form zu definieren. |
| <b>Normal</b> | Die für die verstreuten Formen berechneten Normalen, maskiert gemäß der Überblendung mit dem Hintergrund-Height.<br><br> Wenn der <b>Shape-Typ</b> &#39;Rasteratlas&#39; ist, werden die für die <b>Rasteratlas-Normal</b>-Eingabe bereitgestellten Normalen direkt verwendet. |
| <b>Splatter UVW</b> | <b>R</b> - U-Komponente der UVs der Formen.<br><b>G</b> - V-Komponente der UVs der Formen.<br><b>B</b> - Height der Formen. (W)<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> Der eindeutige Bezeichner der Formen. (ID)<br> - <i>Bruchteil:</i> hängt vom <b>Formtyp ab</b>: Materialkennung bei SDF/primitive, Musterkennung* bei Mustereingabe/Rasteratlas.<br><br><b>*:</b> Die Musterkennung ist der Indexwert der Form in der Liste/im Atlas. |
| <b>Splatter-Daten 1</b> | <b>R</b> - X-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>G</b> - Y-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>B</b> - Z-Komponente der Position auf der Formoberfläche, im Objektraum.<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> U-Komponente der UV-Koordinaten für die Daten der Formen in den Datenausgaben 2/3.<br> - <i>Bruchteil:</i> V-Komponente der UV-Koordinaten für die Daten der Formen in den Daten 2/3-Ausgaben.<br> - <i>Signieren:</i> Binärmaske zum Mischen der Formen mit dem Hintergrund-Height. |
| <b>Splatter-Daten 2</b> | <b>R</b> - X-Komponente der 3D-Drehung der Formen.<br><b>G</b> - Y-Komponente der 3D-Drehung der Formen.<br><b>B</b> - Z-Komponente der 3D-Drehung der Formen.<br><b>A</b> - Drehung der Formen um ihre Normale.<br><br>Alle Drehungen sind in der Anzahl der Umdrehungen definiert. |
| <b>Splatter-Daten 3</b> | <b>R</b> - X Komponente der Position der Formen.<br><b>G</b> - Y Komponente der Position der Formen.<br><b>B</b> - Der Versatz der Formen entlang ihrer Normalen.<br><b>A</b> - Packed data:<br> - <i>Integer part:</i> Der eindeutige Bezeichner der Form.<br> - <i>Bruchteil:</i>Der Index des Formenmusters im Quellatlas. (Bei Verwendung eines Rasteratlas-Mustertyps) |
| <b>Splatter-Daten 4</b> | <i>Pixel 1</i><br><b>R</b> - X-Größe der Datenausgabebilder 2/3.<br><b>G</b> - Y-Größe der Datenausgabebilder 2/3.<br><b>B</b> - X-Größe des Datenausgabebildes 4.<br><b>A</b> - Y-Größe des Datenausgabebildes 4.<br><br><i>Pixel 2</i><br><b>R</b> - Der Formtyp. (E.g. Würfel, Zylinder, ...)<br><b>G</b> - Packedaten:<br> - <i>Absoluter Wert:</i> Die Mustereingabenummer.<br> - <i>Signieren:</i> Normales Format der normalen Ausgangszuordnung. (positiv: DirectX / Negativ: OpenGL)<br><b>B</b> - X-Größe des Rasteratlas. (d. h. die Anzahl der Spalten)<br><b>A</b> - Y-Größe des Rasteratlas. (d. h. die Anzahl der Zeilen) |

<a name="parameters"></a>

## Parameter

|                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Positionsverteilungsmodus</b> *Integer* | Die Methode zum Verteilen der Formen im Raum:<br><br>- <b>2D-Raster:</b> Ein einfaches einheitliches Raster.<br>- <b>Poisson-Festplatte:</b> Eine Simulation, die darauf abzielt, die Zellen eines Rasters zufällig zu versetzen, um Überlappungen zu verhindern, während der verfügbare Platz genutzt wird.<br>- <b>Gleichmäßig:</b> Eine gleichmäßige Verteilung einer angegebenen Anzahl von Formen. Erfordert intensivere Berechnungen.<br>- <b>Benutzerdefinierte Funktion:</b> Erstellen Sie ein Funktionsdiagramm, um die Verteilung von Formen zu definieren. Verfügbare Variablen werden in der Knotenbeschreibung aufgelistet. |
| <b>Positionsfunktion</b> *Float2* | Der Funktionsgraph, der zum Definieren der Verteilung von Formen verwendet wird.<br><br>Das Diagramm gibt einen Float2-Wert für die normalisierte XY-Position der Formen im Bild aus.<br><br>Verfügbare Variablen:<br> - <code>shape.id</code> (Gleitkomma) Eindeutige Kennung der Form.<br> - <code>shape.amount</code> (Gleitkomma) Die Anzahl der im Parameter <b>Betrag</b> angegebenen Formen. |
| <b>X Betrag</b> *Integer* | Die Anzahl der Spalten im Verteilungsraster.<br><br>D.h. die Anzahl der auf der X-Achse erzeugten Formen. |
| <b>Y Betrag</b> *Integer* | Die Anzahl der Zeilen im Verteilungsraster.<br><br>D.h. die Anzahl der auf der Y-Achse erzeugten Formen. |
| <b>Betrag</b> *Integer* | Die Anzahl der generierten Formen. |
| <b>Normales Ausgabeformat</b> *Integer* | Das Format der Ausgabe-Normalmap.<br><br>Kehrt den grünen Kanal effektiv um.<br><br>- <b>DirectX:</b> Die Y-Achse zeigt nach oben.<br>- <b>OpenGL:</b> Die Y-Achse zeigt nach unten. |
| <b>Nicht quadratische Erweiterung</b> *Boolescher Wert* | Bei nicht quadratischen Bildern wird das Formverhältnis beibehalten und die Generierung wird auf die Grenzen des Bildes erweitert. |
| <b>Formtyp</b> *Integer* | Es gibt mehrere Arten von Formen, die verteilt werden können, wobei jede spezifische Merkmale aufweist.<br><br>Die <b>SDF-Funktion</b> ist ein Funktionsdiagramm, das ein vorzeichenbehaftetes Abstandsfeld (SDF) generiert, das die Oberfläche einer 3D-Form beschreibt. Dies ermöglicht die 3D-Streuung komplexer prozeduraler Formen, die dynamisch variieren können.<br><br><b>Grundformen</b>, berechnet mit einfachen Funktionen für Rayon-/Oberflächenschnittstellen, können jetzt verwendet werden: Cube, Kugel, Zylinder, Ebene, Festplatte<br><br><b>Eingabemuster</b> sind vom Diagramm bereitgestellte Bilder. Diese werden Ebenen zugeordnet und können <i>extrudiert</i> in 3D-Formen werden:<br> - Bildeingabe: Die Muster, die mit den <b>Eingangspins des </b>-Musters verbunden sind.<br> - Rasteratlas: Die Muster werden in ein Atlasbild gepackt, das mit den <b>Rasteratlas</b>-Eingängen verbunden ist. |
| <b>Größe des Rasteratlas</b> *Integer2* | Die Anzahl der Zeilen und Spalten des Atlas, die für die <b>Rasteratlas</b>-Bildeingaben bereitgestellt werden.<br><br><i>Hinweis:</i> Leere Zellen im Atlas führen zu Lücken in der Formverteilung. |
| <b>Rasteratlas normal erneut berechnen</b> *Boolescher Wert* | Wenn <i>True</i>, wird die Normalzuordnung, die für die <b>Rasteratlas-Normal</b>-Bildeingabe bereitgestellt wurde, ignoriert, und die Normalen für die für das <b>Rasteratlas-Height</b> bereitgestellten Muster werden von Grund auf neu berechnet.<br><br>Wenn <i>False</i>, wird die Normalmap, die dem <b>Rasteratlas normal</b> bereitgestellt wird, wie vorhanden verwendet.<br><br><i>Hinweis:</i> Die Intensität der Normalen wird gemäß dem <b>Shape extrude-Height angepasst</b>. |
| <b>Normalformat des Rasteratlas</b> *Integer* | Das Format der Normalzuordnung, das für die <b>Rasteratlas-Normalbildeingabe &quot;</b>&quot; bereitgestellt wird.<br><br>Kehrt den grünen Kanal effektiv um.<br><br>- <b>DirectX:</b> Die Y-Achse zeigt nach oben.<br>- <b>OpenGL:</b> Die Y-Achse zeigt nach unten. |
| <b>Mustereingabenummer</b> *Integer* | Die Anzahl von Mustern, die als Eingabebilder bereitgestellt werden.<br><br>Fügt dem Knoten so viele <b>Mustereingabe-Pins #</b> hinzu. |
| <b>Formextrude aktivieren</b> *Boolescher Wert* | Schaltet die Extrusion von Eingabemustern um, indem sie als Height Maps interpretiert werden, was zu komplizierten prozeduralen 3D-Formen führt. |
| <b>Form extrudiert Symmetrie</b> *Boolescher Wert* | Ermöglicht die symmetrische Vor-/Rückwärtsextrusion der Eingabemuster.<br><br>Die Symmetrieachse ist der <i>Mittelpunkt</i> der Extrusion, was bedeutet, dass sich ihre Position je nach Pivot-Position der Formen ändern kann. |
| <b>Height für Shape-Extrusion</b> *Gleitend* | Die maximale Entfernung der Extrusion im Bildraum, wobei 1 die längste Seite des Bildes ist.<br><br>Dieser Abstand wird auf den Wert <b>Formskalierung</b> skaliert. |
| <b>Beispiele für das Extrudieren von Formen</b> *Integer* | Die Anzahl von Proben, die zum Zeichnen der Extrusion der Eingabemuster ausgeführt wurden.<br><br>Eine größere Anzahl führt zu glatteren, definierteren Extrusionen auf Kosten einer gewissen Leistung. |
| <b>Musterfunktion</b> *Gleitend* | Das verfasste Substance-Funktionsdiagramm, das zum Berechnen des Musters verwendet wird, das einer 3D-Ebene SDF zugeordnet ist.<br><br>Diese Muster können auch mithilfe von <b>Shape-Extrusion aktivieren</b> extrudiert werden. |
| <b>Pattern-SDF-Funktion</b> *Gleitend* | Das Substance-Funktionsdiagramm, das das vorzeichenbehaftete Abstandsfeld (SDF) erstellt, das die Oberfläche eines 3D-Objekts im Raum beschreibt.<br><br>Durchsuchen Sie die integrierte Auflistung von [SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) in der Library, um ein komplexes Objekt zu erstellen, indem Sie mehrere SDF <i>primitive</i> mit den verfügbaren <i>Operatoren</i> und <i>Transformationen</i> kombinieren.<br><br>Eine SDF-Form ist vollständig prozeduraler Art und kann dynamisch angepasst werden. Dadurch kann jede verstreute Form <i>eindeutig</i> sein.<br><br>Verwenden Sie den Knoten [3D viewer](../../../filters/effects/3d-viewer/3d-viewer.md), um das Ergebnis einer SDF-Funktion anzuzeigen.<br><br><i>Hinweis:</i> Um Zufälligkeit in SDF-Funktionen anzuwenden, verwenden Sie anstelle von &quot;Zufällig&quot; die Knoten [Hash](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#random). |
| <b>SDF-Begrenzungsrahmengröße</b> *Float3* | Definiert die maximale Größe des Begrenzungsrahmens (Bbox) der SDF-Form, die wiederum zur Berechnung des 2D-Rahmens verwendet wird.<br><br>Formen werden nur innerhalb der Grenzen des 2D-Rahmens gezeichnet, der Rest wird zugeschnitten. |
| <b>Ausschnitt aktivieren</b> *Boolescher Wert* | Schaltet das Zuschneiden von Mustern um, wobei alle Werte unter dem <b>Ausschnitt-Schwellenwert</b> ignoriert werden. Dadurch wird sichergestellt, dass nur die gewünschte Silhouette der Muster verwendet wird. |
| <b>Schwellenwert für das Ausschneiden</b> *Gleitend* | Der Graustufenwert, unter dem die Werte in den Mustern zugeschnitten werden. Der Wert, der als Rahmen der Silhouette für die Muster verwendet wird. |
| <b>Normalisierter Arbeitsablauf</b> *Boolescher Wert* | Wenn diese Option aktiviert ist, wird das Height der Formen automatisch angepasst, sodass die ursprünglichen Proportionen <i>erhalten bleiben</i>, wenn sie vergrößert oder verkleinert werden.<br><br>Wenn diese Option deaktiviert ist, wird das Height der Formen unabhängig von ihren ursprünglichen Proportionen im gesamten Height des Bildes ausgedrückt.<br><br>Das Height der Formen kann weiterhin manuell angepasst werden, indem die <b>Parameter für die Height-Skalierung</b> verwendet werden. |
| <b>Die Formskalierung wirkt sich auf die Height-Skalierung aus</b> *Boolescher Wert* | Wenn <i>True</i>, wird die Skalierung des Heights einer Form angepasst, wenn sich ihre Skalierung ändert, um ihre Proportionen beizubehalten.<br><br>Wenn <i>Falsch</i>, ist die Height-Skala unabhängig von der Formskala, was zu einer Deformation führt. |
| <b>Height-Skalierung</b> *Gleitend* | Ein Multiplikator für das Height der Form, wobei 1 das vollständige Height der Form ist, das im gesamten Height-Bereich des Heights der Form ausgedrückt wird. (Siehe <b>Normalisierter Workflow</b>) |
| <b>zufällige Skalierung des Heights</b> *Gleitend* | Verkleinert das Height jeder Form zufällig auf das angegebene Seitenverhältnis, wobei 1 bedeutet, dass das Height einer Form vollständig auf 0 verkleinert werden kann. |
| <b>Height-Skalierungszuordnungsvervielfacher</b> *Gleitend* | Die Intensität der bereitgestellten <b>Height-Skalierungskarte</b>, wobei 1 bedeutet, dass der vollständige Kartenwert mit dem Height der Form multipliziert wird. |
| <b>Deckkraft für Hintergrundeingabe</b> *Gleitend* | Die Intensität des bereitgestellten <b>Hintergrund-Heights</b>, das in die endgültige Height-Map eingegeben wurde.<br><br>Die Height der Formen und des Hintergrunds werden mit einer &quot;Max. Überblendung&quot; kombiniert, wobei das höhere der beiden verwendet wird. |
| <b>Height-Offset vom Hintergrund</b> *Gleitend* | Das Height des Hintergrunds, das dem Height der Formen hinzugefügt werden soll. 1 bedeutet, dass das gesamte Height des Hintergrunds hinzugefügt wird.<br><br>Dies kann verwendet werden, um die Formen auf dem Hintergrund-Height &quot;ruhen&quot; zu lassen. |
| <b>Mit Hintergrund konform</b> *Gleitend* | Die Stärke der Verformung, die auf das Height der Formen angewendet wird, um das Hintergrundpixel pro Height abzugleichen, wobei 1 eine exakte Übereinstimmung bedeutet.<br><br><i>Hinweis:</i> Dieser Parameter hat keine Auswirkungen, wenn <b>Height vom Hintergrund versetzt</b> = 0 ist. |
| <b>Steigung im Hintergrund glätten</b> *Gleitend* | Die Intensität der Glättung, die auf das Hintergrundkorrektur-Height angewendet wird, das für die Korrekturen des <b>Height-Versatzes vom Hintergrund</b> und <b>Mit Hintergrund</b> übereinstimmen verwendet wird.<br><br>Dadurch werden die Verformungsfrequenzen und der Height-Offset weicher, was härter als erwünscht sein kann. |
| <b>Height-Offset</b> *Gleitend* | Ein Wert, der dem Height der Formen hinzugefügt wird und zu einem geraden Versatz führt.<br><br>Der Wert wird im gesamten Height-Bereich des Bildes ausgedrückt. |
| <b>zufälliger Height-Offset</b> *Gleitend* | Wendet einen zufälligen Versatz bis zum angegebenen Wert auf das Height der Formen an.<br><br>Der Wert wird im gesamten Height-Bereich des Bildes ausgedrückt. |
| <b>Height-Offset von ID</b> *Gleitend* | Der Versatz, der auf das Height der Formen gemäß ihrem Verteilungsindex angewendet wird, wobei der Versatz linear von einer Form zur nächsten bis zum angegebenen Wert zunimmt.<br><br>Der Wert kann manuell über den Wert <code>[0, 1] hinaus festgelegt werden.</code> Bereich. |
| <b>Height-Offset-Zuordnungsmultiplikator</b> *Gleitend* | Passt die Intensität des Versatzes an, der von der <b>Height-Versatzkarte</b> angewendet wird, und zwar unter Verwendung des angegebenen Faktors, wobei 1 bedeutet, dass die Intensitätswerte der Karte unverändert angewendet werden.<br><br>Das gesamte Height der Form wird versetzt, indem der Wert in der Versatzzuordnung an der XY-Schwenkposition hinzugefügt wird.<br><br>Der Multiplikatorwert kann manuell über <code>[0, 1] hinaus festgelegt werden.</code> Bereich. |
| <b>Größenmodus</b> *Integer* | Die Methode zum Definieren der Größe der gestreuten Formen:<br><br>- <b>Auto:</b> Größe wird als Faktor der Formzellgröße ausgedrückt.<br>- <b>Absolut (Texturraum):</b> Größe wird als Faktor der längsten Seite des Bildes ausgedrückt. |
| <b>Größenverhältnis beibehalten</b> *Boolescher Wert* | Passt die Größe der Formen an, um die ursprünglichen Proportionen in nicht quadratischen Rastern und Bildgrößen beizubehalten. |
| <b>Formskalierung</b> *Gleitend* | Die Größe der Form als Faktor, der durch den <b>Größenmodus</b> definiert wird.<br><br><i>Hinweis:</i> Bei Verwendung der <b>Poisson-Festplatte</b>-Verteilung führt das Anpassen der Größe der Formen dazu, dass sie verschoben werden, um den verfügbaren Speicherplatz zu nutzen. Verwenden Sie den Parameter <b>Shape scale post Poisson</b>, um Formen an Ort und Stelle zu skalieren. |
| <b>Zufällige Formskalierung</b> *Gleitend* | Verkleinert die Formen nach dem Zufallsprinzip auf den angegebenen Wert, wobei 1 dazu führen kann, dass einige Formen bis auf die Größe Null verkleinert werden. |
| <b>Zuordnungsmultiplikator skalieren</b> *Gleitend* | Die Intensität des Multiplizierens der Werte in der <b>Form-Skalierungszuordnung</b> mit der Größe der Formen. |
| <b>Formskalierung nach Poisson</b> *Gleitend* | Ein Skalierungsfaktor, der nach der Poisson-Plattensimulation angewendet wird. |
| <b>Formgröße</b> *Float3* | Separate Skalierungsfaktoren pro Achse für die Anpassung der Größe der Formen. |
| <b>Zufällige Formgröße</b> *Float3* | Verkleinert die Formen um den Zufallsfaktor <i> pro Achse </i> auf den angegebenen Wert, wobei 1 dazu führen kann, dass einige Formen bis auf die Größe Null verkleinert werden. |
| <b>Zylinderradius</b> *Gleitend* | Der Radius der gestreuten Zylinder SDFs. Der Radius wird als Faktor ausgedrückt, der durch den <b>Größenmodus</b> definiert wird. |
| <b>Formgröße</b> *Float2* | Separate Skalierungsfaktoren pro Achse für die Anpassung der Größe der Formen. |
| <b>Zufällige Formgröße</b> *Float2* | Verkleinert die Formen um den Zufallsfaktor <i> pro Achse </i> auf den angegebenen Wert, wobei 1 dazu führen kann, dass einige Formen bis auf die Größe Null verkleinert werden. |
| <b>Position zufällig</b> *Gleitend* | Wendet einen zufälligen Versatz auf den XY-Achsen bis zum angegebenen Wert an, wobei 1 die Länge der längsten Seite des Bildes ist. |
| <b>Zufallsmultiplikator für Position</b> *Float2* | Separate Faktoren pro Achse für den zufälligen Versatz, der auf die Formen auf den XY-Achsen angewendet wird. |
| <b>Positionsverteilungssequenz</b> *Integer* | Der Algorithmus, mit dem die Formen gleichmäßig im Raum verteilt werden. <br><br>- <b>R2</b>: Auf Basis des goldenen Schnitts. Es ist schnell und bietet gleichmäßigere und scheinbar zufällige Verteilungen, unabhängig von der Anzahl der Formen.<br>- <b>Halton</b>: Basierend auf Primzahlen. Es liefert großartige Ergebnisse für dünne Verteilungen, wird aber langsamer und kann zu sichtbaren Linien führen, wenn die Anzahl der Formen zunimmt.<br><br>Diese Algorithmen werden als <i>quasirandom</i> und <i>low-disppancy</i> bezeichnet, indem sie einer deterministischen Sequenz (quasirandom) folgen, die darauf abzielt, einen Raum gleichmäßig abzudecken (low-disppancy). |
| <b>Dichte-Map-Multiplikator</b> *Gleitend* | Ein Faktor für den Versatz, der auf die Formen angewendet wird, damit sie in den hellsten Bereichen der <b>Dichte-Map</b> gesammelt werden. |
| <b>Versatz entlang der Normalen</b> *Gleitend* | Verschiebt die Formen entlang ihrer Normalen, d. h. ihrer lokalen Z-Achse. |
| <b>Versatz entlang des normalen Zufalls</b> *Gleitend* | Fügt den Formen entlang ihrer Normalen zufällig Versatz hinzu.<br><br>Der zufällige Betrag kann bis zum angegebenen Wert positiv oder negativ sein oder bis zum negativen Wert. |
| <b>Versatz der Vektorzuordnung</b> *Gleitend* | Ein Faktor für den auf die Formen angewendeten Versatz, indem die RGB-Werte in der <b>Vektorzuordnung</b> zu den XYZ-Koordinaten der Form hinzugefügt werden.<br><br>Der Versatz wird als Faktor für die längste Seite des Bildes angegeben.<br>Beispiel: Ein RGB-Wert von (0,5, 0,5, 0) verschiebt die Formen um die Hälfte ihrer Größe entlang der X- und Y-Achse.<br><br>Ein Parameterwert von 1,0 bedeutet, dass der volle Wert hinzugefügt wird. |
| <b>Vector Versatz Multiplier</b> *Float3* | Passt den <b>Versatz für die Vektorzuordnung</b> um einen separaten Faktor pro Achse an, wobei 0,0 bedeutet, dass kein Versatz auf diese Achse angewendet wird. |
| <b>Globaler Offset</b> *Float2* | Ein Versatz, der auf die Position jeder Form &quot;<i>&quot; angewendet wird, nachdem </i> ein beliebiger Height-Versatz, zufällige Versätze und andere Versatz angewendet wurden.<br><br>Das bedeutet, dass das Verschieben der Formen mithilfe dieses Parameters ihre Position, Ausrichtung und Skalierung nicht ändert. |
| <b>Zeilenpositionsoffset</b> *Gleitend* | Ein Versatz, der gemäß dem Versatzmodus <b>Zeilenposition auf Linien von Formen im Raster angewendet wird.</b> |
| <b>Offsetmodus für Zeilenposition</b> *Integer* | Die Methode zum Anwenden des <b>Zeilenpositionsoffsets</b> auf die Formen.<br><br>Die <b>All</b>-Methoden wenden den Versatz als Faktor der längsten Seite des Bildes an (d. h. im Texturraum).<br>- <b>All - Horizontal:</b> fügt den Versatzwert schrittweise horizontal zeilenweise um einen Faktor des Zeilenindex hinzu.<br>- <b>All - Vertical:</b> fügt den Versatzwert schrittweise vertikal spaltenweise um einen Faktor des Spaltenindex hinzu.<br><br>Die <b>Quincunx</b>-Methoden wenden den Versatz als Faktor der Zellengröße der Formen an.<br>- <b>Quincunx - Horizontal:</b> Fügt den Versatzwert gleichmäßig in jeder zweiten Zeile hinzu.<br>- <b>Quincunx - Vertikal:</b> Fügt den Versatzwert gleichmäßig in jeder zweiten Spalte hinzu. |
| <b>Pivot-Position (lokal)</b> *Float3* | Passt die Position des Drehpunkts im lokalen Raum der Form an, der sich auf den Ursprung der Transformationen auswirkt. (d. h. Positionsversatz, Drehung und Skalierung)<br><br>Passen Sie beispielsweise die Z-Pivot-Position so an, dass Formen um ihre Grundlinie geschwenkt werden. |
| <b>3D-Drehung</b> *Float3* | Wendet eine Drehung pro Achse gleichmäßig auf alle Formen in der Anzahl der Windungen an. |
| <b>zufällige 3D-Drehung</b> *Gleitend* | Ein Faktor für den zufälligen Umfang der Drehung, die auf die Formen bis zum angegebenen Wert (im Uhrzeigersinn oder gegen den Uhrzeigersinn) in der Anzahl der Windungen angewendet wird. |
| <b>Zufallsmultiplikator für 3D-Drehung</b> *Float3* | Passt den Umfang der zufälligen Drehung an, die durch <b>3D-Drehung zufällig</b> um einen separaten Faktor pro Achse angewendet wird. |
| <b>3D-Rotation Map-Multiplikator</b> *Float3* | Die Intensität, mit der die Werte in der <b>Form-Drehung</b>-Map zur Drehung jeder Form pro Achse hinzugefügt werden, wobei 1 bedeutet, dass die gesamte Drehung hinzugefügt wird. |
| <b>Drehung um den Normalwert</b> *Gleitend* | Der Betrag der Drehung, die gleichmäßig auf alle Formen um ihre Normale - d.h. ihre lokale Z-Achse - in der Anzahl der Windungen angewendet wird. |
| <b>Drehung um den normalen Zufallswert</b> *Gleitend* | Wendet eine zufällige Drehung auf jede Form um ihre Normale - d. h. ihre lokale Z-Achse - im Uhrzeigersinn oder gegen den Uhrzeigersinn an, bis zu einer vollen Drehung. |
| <b>Drehung der Steigung</b> *Gleitend* | Dreht die Formen entsprechend der Steigung des Hintergrunds an ihrer Position.<br>D.h. wendet eine Drehung an, die der des globalen Z-Up-Vektors auf die Normalität des Hintergrund-Heights entspricht.<br><br>Dieser Parameter ist ein Faktor für diese Drehung, wobei 1 bedeutet, dass die volle Drehung angewendet wird.<br><br>Diese Drehung wird anderen Drehungen hinzugefügt, die auf die Formen angewendet werden können. |
| <b>Eingabe für Drehung der Steigung</b> *Integer* | Die Quelle der Steigung, die zum Antreiben der <b>Steigungen-Drehung verwendet wird</b>.<br><br>- <b>Hintergrund:</b> Die Hintergrundvektortextur wird verwendet, die aus dieser Heights-Map berechnete Normalität ist die Zielrichtung für die Drehung.<br>- <b>Vektorkarte:</b> Die durch die Vektormaptextur angegebenen Heights werden wie für die Zielrichtung der Drehung verwendet.</b> |
| <b>Vektorzuordnungsvervielfacher</b> *Gleitend* | Dreht die Formen um die Achse, die durch <b>Rotationsachse der Vektorzuordnung</b> angegeben wird, um die Richtung der Vektoren anzupassen, die durch die <b>Textur der Vektorzuordnung</b> beschrieben werden.<br>D.h. wendet eine Drehung an, die gleich der des globalen X-Rechts-Vektors auf die Vektoren in der Textur ist.<br><br>Dieser Parameter ist ein Faktor für diese Drehung, wobei 1 bedeutet, dass die volle Drehung angewendet wird.<br><br>Diese Drehung wird anderen Drehungen hinzugefügt, die auf die Formen angewendet werden können. |
| <b>Rotationsachse der Vektorzuordnung</b> *Integer* | Die Achse, um die die in der <b>Vektorzuordnung</b> angegebene Drehung ausgeführt werden soll.<br><br>- <b>Normal:</b> Dreht die Formen um ihre Normale, ähnlich wie bei Verwendung des Parameters &quot;Drehung um die Normale&quot;.<br>- <b>Z Achse:</b> Dreht die Formen um die globale Z Achse, ähnlich wie die Z Komponente des Parameters &quot;3D-Drehung&quot; verwendet wird. |
| <b>Zufallsmaske</b> *Gleitend* | Blendet das angegebene Verhältnis der Gesamtmenge der Formen in zufälliger Reihenfolge aus, wobei 1 bedeutet, dass alle Formen ausgeblendet sind.<br><br>Dieser Parameter wird mit der Maskenzuordnung kombiniert. (falls verwendet) |
| <b>Schwellenwert für Maskenzuordnung</b> *Gleitend* | Der Graustufenwert in der <b>Maskenzuordnung</b>, unter dem Formen ausgeblendet sind.<br><br>Die Karte wird mit dem Parameter <b>Zufällige Maske</b> kombiniert. |
| <b>UV-Skalierung</b> *Float2* | Ein Multiplikator pro Achse für die UVs der Formen, wobei die Unterteilung mit den Werten zunimmt. |
| <b>Cap-UV-Skalierung</b> *Float2* | Ein Vervielfacher pro Achse für die UVs der Zylinderdeckel, bei dem die Neigung mit den Werten zunimmt. |
| <b>UV-Modus beenden</b> *Integer* | Die Methode zum Berechnen der UVs für die Kappen des Zylinders.<br><br>- <b>Polar:</b> Verwenden Sie Polarkoordinaten, wobei U um die Z-Achse des Zylinders zunimmt und V zunimmt, wenn sich der Zylinder weiter von ihm entfernt.<br>- <b>Planar:</b> Verwenden Sie eine planare Projektion, bei der die UVs mithilfe des Begrenzungsrahmens der Kappen abgebildet werden (d. h. ein Rechteck, das auf die Größe der Kappen angepasst ist) |
| <b>Form 2D-Feld anzeigen</b> *Boolescher Wert* | Überlagert eine Darstellung des Begrenzungsrechtecks der Form im Bild. Das ist der Bereich, in dem Formen gezeichnet werden. |
| <b>Form 3D-Box anzeigen</b> *Boolescher Wert* | Overlays sind eine Visualisierung des Begrenzungsvolumens der Form im 3D-Raum. Dies ist der Bereich, in dem die SDF-Formen und extrudierten Ebenen gezeichnet werden.<br><br>Bei SDF-Formen entspricht dieser Bereich der Größe des <b>SDF-Begrenzungsrahmens</b>.<br><br>Diese Visualisierung hilft bei der Bewertung der Spanne und Ausrichtung der Form. |
| <b>Form-Pivot anzeigen</b> *Boolescher Wert* | Overlays eine Visualisierung der Formen Pivot, als eine Kombination der lokalen XYZ-Achsenvektoren.<br><br>Diese Visualisierung hilft, die Ausrichtung der Form sowie den Ursprung ihrer Transformationen zu bewerten. (d. h. Offset, Drehung, Skalierung) |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-poisson.gif" /><br><i>Poisson-Verteilung</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-uniform.gif" /><br><i>Einheitliche Verteilung</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-density-map.gif" /><br><i>Dichte-Map</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-rotation.gif" /><br><i>Zufällige 3D-Drehung</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-background-slope.gif" /><br><i>Drehung der Steigung</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-shape-extrusion.gif" /><br><i>Formextrusion</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-sdf.jpg" /><br><i>3D-SDF-Formen</i>
        </td>
        <td style="border: 0; background: transparent">
        </td>
        <td style="border: 0; background: transparent">
        </td>
    </tr>
</table>


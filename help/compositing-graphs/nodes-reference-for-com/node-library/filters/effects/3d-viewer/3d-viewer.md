---
title: 3D-Viewer
description: Designer > Substance-Compositing-Grafen > Knotenreferenz für Substance-Compositing-Grafen > Knotenbibliothek > Filter > Effekt > 3D-Viewer
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 0%
---

# 3D-Viewer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![3D-Viewer-Symbol](./3d-viewer.resources/3d-viewer.png "3D-Viewer")

<b>In:</b> Filter > Effekt

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet ein 3D-Rendering für ein angegebenes SDF oder eine durch einen Funktions-Graf definierte Schnittmenge mit einer benutzerdefinierten Kamera und einem benutzerdefinierten Umgebungslicht. Szene:<br><br>Dieser Knoten eignet sich zum Erstellen und Visualisieren von [SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), die im Knoten [Shape splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) verwendet werden sollen.<br><br>Helfer sind verfügbar, um Schlüsselattribute von Formen im Raum zu visualisieren.<br><br>Für fortgeschrittene Benutzer können benutzerdefinierte Funktionen erstellt werden, um die Kamera und/oder das 3D-Rendering pro Pixel einzurichten.

</td>
</tr>
</table>

>[!INFO]
> 
> Weitere Informationen zu Konzepten und Workflows mit SDF-Funktionen finden Sie auf der entsprechenden Seite: [Arbeiten mit SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Eingaben

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Umgebung</b> *Farbe* | Das Bild, das auf die unendliche Kugel projiziert werden soll, wird als Umgebung der Szene verwendet und für die Umgebungsbeleuchtung verwendet.<br><br>Die Projektion ist <i>äquirektangulär</i>. Sie wird von den Standardbibliotheken von Designer verwendet, die in der Umgebungs-Map-Kategorie <b>3D-Ansicht > HDRI-Umgebungen</b> der Library verfügbar sind.<br><br>Wenn keine Verbindung besteht, wird eine Standardumgebung verwendet.<br><br><i>Tipp:</i> Verwenden Sie ein HDR (32-Bit) für eine präzise . |
| <b>Eingabe 1</b> *Farbe* | Ein Bild, das im Funktionsknoten <b>Benutzerdefinierte Ausgabe</b> gesampelt werden kann, wenn der Graf <b>Ausgabe</b> auf &#39;Benutzerdefiniert&#39; festgelegt ist.<br><br>Verwenden Sie einen Knoten [Beispielfarbe](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), der auf &#39;Bildeingabe 0&#39; festgelegt ist, um aus diesem Bild zu scannen. |
| <b>Eingabe 2</b> *Farbe* | Ein Bild, das im Funktionsknoten <b>Benutzerdefinierte Ausgabe</b> gesampelt werden kann, wenn der Graf <b>Ausgabe</b> auf &#39;Benutzerdefiniert&#39; festgelegt ist.<br><br>Verwenden Sie einen Knoten [Beispielfarbe](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), der auf &#39;Bildeingabe 1&#39; festgelegt ist, um aus diesem Bild zu scannen. |

<a name="outputs"></a>

## Ausgaben

|               |                                                                                                                                                                                                                                    |
|:--------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Ausgabe</b> | Die gerenderte Szene verwendet den AOV, der im <b>Output</b>-Parameter ausgewählt wurde.<br><br><i>Hinweis:</i> Stellen Sie zum präzisen Lesen in einigen AOVs sicher, dass die 2D-Ansicht einen linearen Farbraum verwendet und der Knoten ein HDR. 32-Bit-Ausgabeformat verwendet. |

<a name="parameters"></a>

## Parameter

|                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Szene Typ</b> *Integer* | Der Funktionstyp, der zum Beschreiben der zu rendernden Oberflächen und Formen verwendet wird:<br>- <b>SDF:</b> Verwenden Sie eine SDF-Funktion (Signed Distance Field), die komplexe Formen beschreiben kann.<br>- <b>Schnittmenge bilden:</b> Verwenden Sie Schnittmengen bilden, die schneller sind, wenn nur einfache Grundformen benötigt werden. |
| <b>SDF-Szene</b> *Fließkommazahl* | Die Funktion für vorzeichenbehaftete Abstandsfelder (SDF), die die Flächen und Formen in der Szene beschreibt.<br><br>Verwenden Sie die Knoten in der Kategorie [SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) der Bibliothek, um die Funktion zu erstellen. |
| <b>Szene überschneiden</b> *Fließkommazahl* | Die Schnittfunktion, die die Flächen und Formen in der Szene beschreibt.<br><br>In den Ordnern <b>3d_intersection</b> des Bibliothekspakets <b>3d_functions.sbs</b> sind Schnittstellenfunktionen für einfache Grundelemente und Operatoren verfügbar.<br><br><i>Tipp:</i> Sie können auf das Paket zugreifen, indem Sie einen beliebigen SDF-Knoten aus der Bibliothek in den Explorer ziehen. |
| <b>Ausgabe</b> *Ganzzahl* | Der Typ des 3D-Renderings, der vom Knoten ausgegeben werden soll, wird im Allgemeinen als AOVs (Arbitrary output variables) bezeichnet.<br><br>Verfügbare AOVs sind:<br>- <b>Schönheit:</b> Das Endergebnis des 3D-Renderings mit kunstorientierten Tangenten und Effekten.<br>- <b>Normale WS:</b> Die Welt-Raum-Normale der Formen in der Szene.<br>- <b>Normale TS:</b> Die Standardfarbräume der Formen in der Szene.<br> 0&rbrace;- <b>Welt-Raum:</b> Die Oberflächenposition der Formen in der Szene.<br>- <b>Abstand:</b> Der Rohabstand von der Kamera zu den Formen in der Szene<br>- <b>Tiefe:</b> Der vorzeichenbehaftete Abstand der Formen von der Kamera-Zielebene, in der die Ebene immer die Fläche Kamera.<br>- <b>Farbe:</b> Die Grundfarbe &quot;Formen&quot; (verwenden) den Knoten &quot;Farbe festlegen&quot; zum Zuweisen von Farben zu Formen in der Szene)<br>- <b>Material-ID:</b> Die auf die Formoberflächen angewendeten Material-IDs (Verwenden Sie den Knoten &quot;Material-ID festlegen&quot; zum Zuweisen von Material-IDs zu Formen in der Szene)<br>- <b>Sphären-Nachzeichneschritten:</b> Eine Visualisierung der Schrittanzahl, die zum Definieren der Fläche einer Form erforderlich ist. Hellere Werte bedeuten, dass mehr Schritte erforderlich sind.<br>- <b>Benutzerdefiniert:</b> Erstellen Sie eine benutzerdefinierte Funktion, um die Farbe des Renderings pro Pixel zu berechnen.<br><br><i>Hinweis:</i> Stellen Sie zum präzisen Lesen in einigen AOVs sicher, dass die 2D-Ansicht einen linearen Farbraum verwendet und der Knoten ein HDR. 32-Bit-Ausgabeformat verwendet. |
| <b>Benutzerdefinierte Ausgabe</b> *Fließkommazahl4* | Der Graf, der die RGBA-Pixelfarben der gerenderten Szene als Fließkommazahl4-Wert definiert.<br><br>Verfügbare Variablen:<br>- <code>Szene.position</code> (Fließkommazahl3) Die Position des Welt-Raums der Flächen der Szene.<br>- <code>Szene.normal</code> (Fließkommazahl3) Die Welt-Raum-Normale der Flächen der Szene.<br>- <code>Szene.hit</code> (Boolesche Wert) Gibt &quot;True&quot; zurück, wenn eine Fläche von einem Kamera-Strahl getroffen wird.<br>- <code>view.origin</code> (Fließkommazahl3) Die Pixelposition des Welt-Raums pro Pixel in der Kamera.<br>- <code>view.direction</code> (Fließkommazahl3) Der Vorwärtsvektor pro Pixel der Kamera-Ansicht gemäß dem Projektion-Modus. (E.g. Perspektive oder orthografisch)<br>- <code>Material.color</code> (Fließkommazahl3) Die Grundfarbe der Flächen der Szene.<br>- <code>Material.Metalness</code> (Fließkommazahl) Die Metallität der Flächen der Szene.<br>- <code>Material.Rauheit</code> (Fließkommazahl) Die Rauheit der Flächen der Szene.<br>- <code>Material.id</code> (Ganzzahl) Die Material-IDs der Flächen der Szene.<br><br>Die Bildeingaben des Knotens können durch Auswahl der folgenden [Beispielfarbe](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) Knotensteckplätze aufgenommen werden: <br>- <b>Bildeingabe 0</b> Samples Eingabe 1.<br>- <b>Bildeingabe 1</b> Samples Eingabe 2. |
| <b>Umgebungsrotation</b> *Fließkommazahl* | Die Drehung der <b>Umgebung</b> in der Anzahl der Umdrehungen. |
| <b>Hintergrundmodus</b> *Ganzzahl* | Gibt die Quelle des Hintergrunds der Szene an, der gezeichnet wird, wenn keine Formoberflächen sichtbar sind.<br><br>- <b>Farbe:</b> Die ebene &quot;Hintergrundfarbe&quot;.<br>- <b>Umgebung:</b> Das Bild, das für den Eingang &quot;Umgebung&quot; bereitgestellt wird und auf eine unendliche Kugel mit äquirektangulärer Projektion angewendet wird.  (Wenn der Eingang nicht angeschlossen ist, wird eine Standardumgebung verwendet.) |
| <b>Hintergrundfarbe</b> *Fließkommazahl4* | Die als Hintergrund für die Szene verwendete Flächenfarbe. |
| <b>IBL-Beispiele</b> *Ganzzahl* | Die Anzahl der Lichtproben pro Kamera.<br><br>Ein höherer Wert führt zu einer gleichmäßigeren, präziseren Beleuchtung auf Kosten der Leistung. |
| <b>Beispiele für Kameras</b> *Ganzzahl* | Die Anzahl der Kamera-Samples pro Pixel.<br><br>Dieser Parameter beeinflusst die Qualität des Anti-Alias-Effekts und die Tiefe des Feldeffekts.<br><br>Ein höherer Wert führt zu einem deutlicheren, weniger lauten Bild auf Kosten der Leistung. |
| <b>Schritte zum Strahlenmarschieren</b> *Ganzzahl* | Die Anzahl der Schritte, die im Sphäre-Tracing-Prozess ausgeführt werden, die Raymarching-Technik, die zum Erkennen und Zeichnen der Oberflächen der Formen verwendet wird.<br><br>Ein höherer Wert führt zu genauen, konsistenten Oberflächen (insbesondere bei komplexen Formen), und zwar auf Kosten der Leistung.<br><br><i>Tipp:</i> Legen Sie den Parameter <b>Ausgabe</b> auf die AOV &quot;Sphäre-Tracing-Schritte&quot; fest, um die Bereiche der Formen anzuzeigen, die weitere Schritte erfordern. Diese Bereiche werden zunächst durch die Reduzierung der Anzahl der Schritte betroffen sein. |
| <b>Schritte zum Markieren sekundärer Strahlen</b> *Ganzzahl* | Die Anzahl der Schritte, die im Sphäre-Tracing-Prozess ausgeführt werden, um die Diffusion- und Specular-Verdeckung zu berechnen, um Geworfen Schatten zu zeichnen.<br><br>Ein höherer Wert führt zu präziseren Schatten auf Kosten der Leistung. |
| <b>Kamera-Modus</b> *Ganzzahl* | Die Methode zum Projizieren der Szene auf das Renderbild:<br><br>- <b>Perspektive:</b> Diese Projektion vermittelt Tiefe und ermöglicht Linseneffekte wie die Tiefe des Felds.<br>- <b>Orthografisch:</b> Diese Projektion reduziert die Szene und hebt die Tiefe auf.<br>- <b>Benutzerdefinierte Funktion:</b> Erstellen Sie einen Funktions-Graf, um eine benutzerdefinierte Kamera einzurichten. |
| <b>Kamera-Funktion</b> *Fließkommazahl3* | Der Graf der Funktion, der den transformieren der Kamera definiert. Dies kann zum Einrichten einer benutzerdefinierten Kamera verwendet werden.<br><br>Die Funktion sollte <b>diese Variablen setzen</b>:<br>- <code>view.origin</code> (Fließkommazahl3) Die Pixelposition des Welt-Raums pro Pixel in der Kamera.<br>- <code>view.direction</code> (Fließkommazahl3) Der Vorwärtsvektor pro Pixel der Kamera-Ansicht gemäß dem Projektion-Modus. (E.g. Perspektive oder orthografisch)<br><br>Die folgenden Variablen sind für <b>get</b> verfügbar:<br>- <code>Kamera.origin</code> (Fließkommazahl3) Die Position des Welt-Raums der Kamera. (Kamera.richtung * Kamera_Entfernung + Kamera.Ziel)<br>- <code>Kamera.richtung</code> (Fließkommazahl3) Die Welt-Raumrichtung der Kamera, d. h. der Y-Vorwärtsvektor der Kamera.<br>- <code>Kamera.right</code> (Fließkommazahl3) Der X-Right-Vektor der Kamera.<br>- <code>Kamera.up</code> (Fließkommazahl3) Z-Up-Vektor der Kamera.<br>- <code>Kamera.target</code> (Fließkommazahl3) Die Position des Welt-Raums der Kamera. |
| <b>UV-Position</b> *Fließkommazahl2* | Die Position im 2D-Bildbereich, die zum Ableiten der Position und der Kamera verwendet wurde, die die <b>Zielposition</b> umkreisen.<br><br><i>Tipp:</i> Dieser Parameter kann intuitiv angepasst werden, indem das <i>Positions-Gizmo</i> verwendet wird, das bei Auswahl des 2D-Ansicht verfügbar ist. |
| <b>FOV</b> *Fließkommazahl* | Das Sichtfeld der orthografischen Kamera (FOV), das sich auf den Zoomfaktor auswirkt. |
| <b>Brennweite</b> *Fließkommazahl* | Die Brennweite der Kamera, die den Zoomfaktor und die Tiefe des Feldeffekts beeinflusst. |
| <b>Entfernung vom Ziel</b> *Fließkommazahl* | Die Entfernung, die die Kamera von der <b>Zielposition</b> ruhen soll.<br><br>Durch Anpassen dieser Option wird die Kamera entlang der Kamera-Ziel-Richtung verschoben. |
| <b>Zielposition</b> *Fließkommazahl3* | Die Lage des Kamera-Ziels, auf das die Kamera immer ausgerichtet ist. |
| <b>Tonemapper</b> *Ganzzahl* | Der Tonzuordnungsalgorithmus, der auf das Rendering der Szene angewendet werden soll.<br><br>- <b>Keine (Raw)<br>- <b>sRGB</b><br>- <b>AgX</b><br>- <b>ACE</b> |
| <b>Tiefe des Felds aktivieren</b> *Boolesche Wert* | Simuliert den Effekt der Kamera der Tiefe des Halbbilds für die Kamera der Perspektive.<br><br>Verwenden Sie die <b>F-Zahl</b> und den <b>Fokusabstand</b>, um die Blende bzw. den Fokus des Effekts anzupassen.<br><br>Das Ergebnis ist auch auf die <b>Brennweite</b> ausgewirkt. |
| <b>F-number</b> *Fließkommazahl* | Die <i>Blende</i>.<br><br>Ein niedrigerer Wert der Kamera führt zu einer geringeren <i>Tiefe des Felds</i>, d. h. einem geringeren Abstandsbereich für scharfe Objekte und einem stärkeren Weichzeichnungseffekt, wenn der Abstand von diesem Bereich zunimmt. |
| <b>Fokusentfernung</b> *Fließkommazahl* | Legt die Entfernung des Fokuspunkts von der Kamera entlang des Vorwärtsvektors fest.<br><br>Flächen innerhalb dieses Abstandsbereichs erscheinen scharf, dieser Bereich — die <i>Tiefe des Feldes </i> — wird durch die <b>F-Zahl</b> definiert. |
| <b>Belichtung (EV)</b> *Fließkommazahl* | Die Lichtmenge, die den Lichtsensor erreicht, d. h. die Kamera der Beleuchtung im Rendering.<br><br>Ein niedrigerer Wert führt zu einer dunkleren gerenderten Szene.<br><br>Der &#39;Belichtungswert&#39; (EV) bezieht sich speziell darauf, wie viel Kamera der Lichtsensor <i>gelegt</i> hat. |
| <b>Grundfarbe</b> *Fließkommazahl3* | Die Standardfarbe für Flächen, bei denen diese Grundfarbe nicht durch ihre SDF- oder Schnittfunktion definiert ist. |
| <b>Rauheit</b> *Fließkommazahl* | Der Standardwert für die Rauheit von Flächen, bei denen dieser Wert nicht durch ihre SDF- oder Schnittfunktion definiert ist. |
| <b>Metalität</b> *Fließkommazahl* | Der Metalitätswert für Flächen, bei denen dieser Wert nicht durch die SDF- oder Schnittfunktion definiert ist. |
| <b>Deckkraft der Helfer</b> *Fließkommazahl* | Die Deckkraft der 3D-Helfer, wobei ein niedrigerer Wert zu schwächeren Helfern führt. |
| <b>Begrenzender Rahmen</b> *Boolesche Wert* | Eine Visualisierung eines sechsseitigen Käfigs, der die Grenzen der gesamten Szene definiert. Sollte idealerweise die kleinstmögliche Größe sein, die die Szene vollständig einschließt.<br><br>Verwenden Sie den Rahmen <b>Größe des Begrenzungsrahmens</b>, um die Größe des Käfigs anzupassen.<br><br>Mit dem Parameter <b>Aus Rahmen einfärben</b> können Sie die Flächen außerhalb dieses Käfigs leicht sichtbar machen, was sich auf das Ergebnis der Verwendung dieser Szene im Knoten [Form splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) auswirkt. (Siehe QuickInfo zum Umfang des Begrenzungsrahmens.) |
| <b>Größe des begrenzenden Rahmens</b> *Fließkommazahl3* | Legt die XYZ-Größe des umgebenden Rahmens fest.<br><br>Passen Sie den Rahmen an Ihre Szene an, und wenden Sie dann dieselben Werte auf den Rahmen size</b> mit <b>SDF-Bindung des Knotens [Shape splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) an, um sicherzustellen, dass alle Formen in der Szene korrekt von diesem  eingeschlossen und gezeichnet werden. |
| <b>Aus Rahmen einfärben</b> *Boolesche Wert* | Wendet einen Rotton auf die Flächen außerhalb des Begrenzungsrahmens an. Rahmen:<br><br>Dadurch kann überprüft werden, ob die Szene vollständig in ihrem Begrenzungs-Rahmen enthalten ist. |
| <b>Achse</b> *Boolesche Wert* | Eine Visualisierung der XYZ-Achsen der Szene als farbige Linien, die am Ursprung der Szene beginnen. |
| <b>Raster</b> *Boolesche Wert* | Eine Visualisierung eines Rasters auf den XY-Achsen, wobei die Szene einer Zelle in X und Y eine Zelleinheit ist. |
| <b>Helfer Transformieren</b> *Boolesche Wert* | Eine Visualisierung der zuletzt angewendeten Drehung.<br><br>Die Visualisierung umfasst <br>- <b>einen Pfeil</b>, der den Drehwinkelrichtungsvektor darstellt und nach den Achsen jeder Welt-Raum-Achse eingefärbt ist.<br>- <b>Ein Bogen</b>, der den Drehwinkel darstellt, der orthogonal zu dem Pfeil steht, der mit seiner Farbe übereinstimmt. |
| <b>SDF-Isolinien</b> *Boolesche Wert* | Eine farbige Visualisierung der Funktionsisolinen für das vorzeichenbehaftete Distanzfeld (SDF).<br><br>Die Isolinien sind regelmäßig wiederholende Linien, die das <i>Abstandsfeld</i> der Form auf der XY-Ebene in einem bestimmten Height darstellen.<br><br>Diese sind nützlich, um die <i>Gleichmäßigkeit des durch die SDF-Funktion definierten Leerzeichens</i> zu überprüfen.<br><br>Verwenden Sie die Parameter <b>SDF-Isolinienfrequenz</b> und <b>SDF-Isolinienposition</b>, um die Dichte und das Height der Isolinien anzupassen. |
| <b>Häufigkeit der SDF-Isolinien</b> *Fließkommazahl* | Die Anzahl der Isolinienwiederholungen innerhalb einer bestimmten Entfernung.<br><br>Ein höherer Wert führt zu dichteren, dünneren Linien. |
| <b>SDF-Isolinienposition</b> *Fließkommazahl* | Das Weltraum-Height der XY-Ebene, mit dem die Isolinien gezeichnet wurden.<br><br>Verwenden Sie diese Option, um das Abstandsfeld der Form in verschiedenen Höhen zu überprüfen. |
| <b>Min. Trefferabstand </b> *Gleitend* | Definiert die minimale Entfernung, die sich in einen Treffer für den SDF-Strahlmarching-Prozess übersetzt.<br><br>Ein niedriger Wert erhöht die Anzahl der Strahlmarching-Schritte. |

## Beispiele

<table style="border: none;">
    <tr style="width: 50%;">
        <td style="text-align: center">
            <img src="3d-viewer.resources/3d-viewer-example-01.jpg" alt="Beispiel 1" />
        </td>
        <td style="width: 50%;">
            <table style="border: none;">
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02a.jpg" alt="Beispiel 1" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02b.jpg" alt="Beispiel 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02c.jpg" alt="Beispiel 3" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02d.jpg" alt="Beispiel 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>

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
| <b>SDF-Szene</b> *Gleitend* | Die Funktion für vorzeichenbehaftete Abstände (SDF), die die Oberflächen und Formen in der Szene beschreibt.<br><br>Verwenden Sie die Knoten in der Kategorie [SDF-Funktionen](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) der Bibliothek, um die Funktion zu erstellen. |
| <b>Szene schneiden</b> *Gleitend* | Die Schnittfunktion, die die Flächen und Formen in der Szene beschreibt.<br><br>Schnittstellenfunktionen für einfache Grundelemente und Operatoren sind in den Ordnern <b>3d_intersection</b> des Bibliothekspakets <b>3d_functions.sbs</b> verfügbar.<br><br><i>Tipp:</i> Sie können auf das Paket zugreifen, indem Sie einen beliebigen SDF-Knoten aus der Bibliothek in den Explorer ziehen. |
| <b>Ausgabe</b> *Integer* | Der Typ des 3D-Renderings, der vom Knoten ausgegeben werden soll, wird im Allgemeinen als AOVs (Arbitrary output variables) bezeichnet.<br><br>Verfügbare AOVs sind:<br>- <b>Schönheit:</b> Das Endergebnis des 3D-Renderings mit kunstorientierten Farben und Effekten.<br>- <b>Normale WS:</b> Die Weltraum-Normalen der Formen in der Szene.<br>- <b>Normale TS:</b> Die Tangenten-Leerräume der Formen in der Szene.{1 0}- <b>Position:</b> Die Weltraumposition der Flächen der Formen in der Szene.<br>- <b>Abstand:</b> Der unformatierte Abstand zwischen der Kamera und den Formen in der Szene<br>- <b>Tiefe:</b> Der vorzeichenbehaftete Abstand der Formen von der Kamerazielebene, auf der die Ebene immer zur Kamera zeigt.<br>- <b>Farbe:</b> Die Grundfarbe der Formen (Verwenden Sie den Knoten &quot;Farbe festlegen&quot; zum Zuweisen von Farben zu Formen in der Szenenfunktion)<br>- <b>Material ID:</b> Die Material IDs, die auf die Formoberflächen angewendet werden (Verwenden Sie den Knoten &quot;Material-ID festlegen&quot;, um Formen in der Szenenfunktion Material IDs zuzuweisen)<br>- <b>Schritte zum Nachzeichnen von Sphären:</b> Eine Visualisierung der Anzahl von Schritten, die zum Definieren der Oberfläche einer Form erforderlich sind. <br>Hellere Werte bedeuten, dass mehr Schritte erforderlich sind.<br>- <b>Benutzerdefiniert:</b> Erstellen Sie eine benutzerdefinierte Funktion, um die Farbe des Renderings pro Pixel zu berechnen.<br><br><i>Hinweis:</i> Stellen Sie für genaue Werte in einigen AOVs sicher, dass die 2D-Ansicht einen linearen Farbraum verwendet und der Knoten ein HDR-32-Bit-Ausgabeformat verwendet. |
| <b>Benutzerdefinierte Ausgabe</b> *Float4* | Das Funktionsdiagramm, das die RGBA-Farben pro Pixel der gerenderten Szene als Float4-Wert definiert.<br><br>Verfügbare Variablen:<br>- <code>scene.position</code> (Float3) Die Weltraumposition der Oberflächen der Szene.<br>- <code>scene.normal</code> (Float3) Die Weltraum-Normalen der Oberflächen der Szene.<br>- <code>scene.hit</code> (Boolescher Wert) Gibt &quot;True&quot; zurück, wenn eine Fläche von einem Kamerastrahl getroffen wird.<br>- <code>view.origin</code> (Float3) Die Weltraumposition der Kameraansicht pro Pixel.<br>- <code>view.direction</code> (Float3) Der Vorwärtsvektor pro Pixel der Kameraansicht gemäß dem Projektionsmodus. (E.g. Perspektive oder orthografisch)<br>- <code>material.color</code> (Float3) Die Grundfarbe der Oberflächen der Szene.<br>- <code>material.metalness</code> (Float) Die Metallität der Oberflächen der Szene.<br>- <code>Material.Raueit</code> (Float) Die Raueit der Oberflächen der Szene.<br>- <code>Material.id</code> (Integer) Die Material-IDs der Oberflächen der Szene.<br><br>Die Bildeingaben des Knotens können durch Auswahl der folgenden [Beispielfarbe](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) Knotensteckplätze aufgenommen werden: <br>- <b>Bildeingabe 0</b> Samples Eingabe 1.<br>- <b>Bildeingabe 1</b> Samples Eingabe 2. |
| <b>Umgebungsrotation</b> *Gleitend* | Die Drehung der <b>Umgebung</b> in der Anzahl der Umdrehungen. |
| <b>Hintergrundmodus</b> *Integer* | Gibt die Quelle des Hintergrunds der Szene an, der gezeichnet wird, wenn keine Formoberflächen sichtbar sind.<br><br>- <b>Farbe:</b> Die ebene &quot;Hintergrundfarbe&quot;.<br>- <b>Umgebung:</b> Das Bild, das für den Eingang &quot;Umgebung&quot; bereitgestellt wird und auf eine unendliche Kugel mit äquirektangulärer Projektion angewendet wird.  (Wenn der Eingang nicht angeschlossen ist, wird eine Standardumgebung verwendet.) |
| <b>Hintergrundfarbe</b> *Float4* | Die als Hintergrund für die Szene verwendete Flächenfarbe. |
| <b>IBL-Beispiele</b> *Integer* | Die Anzahl der Lichtproben pro Kamera.<br><br>Ein höherer Wert führt zu einer gleichmäßigeren, präziseren Beleuchtung auf Kosten der Leistung. |
| <b>Beispiele für Kameras</b> *Integer* | Die Anzahl der Kamera-Samples pro Pixel.<br><br>Dieser Parameter beeinflusst die Qualität des Anti-Alias-Effekts und die Tiefe des Feldeffekts.<br><br>Ein höherer Wert führt zu einem deutlicheren, weniger lauten Bild auf Kosten der Leistung. |
| <b>Schritte zum Strahlenmarschieren</b> *Integer* | Die Anzahl der Schritte, die im Sphäre-Tracing-Prozess ausgeführt werden, die Raymarching-Technik, die zum Erkennen und Zeichnen der Oberflächen der Formen verwendet wird.<br><br>Ein höherer Wert führt zu genauen, konsistenten Oberflächen (insbesondere bei komplexen Formen), und zwar auf Kosten der Leistung.<br><br><i>Tipp:</i> Legen Sie den Parameter <b>Ausgabe</b> auf die AOV &quot;Sphäre-Tracing-Schritte&quot; fest, um die Bereiche der Formen anzuzeigen, die weitere Schritte erfordern. Diese Bereiche werden zunächst durch die Reduzierung der Anzahl der Schritte betroffen sein. |
| <b>Schritte zum Markieren sekundärer Strahlen</b> *Integer* | Die Anzahl der Schritte, die im Sphäre-Tracing-Prozess ausgeführt werden, um die Diffusion- und Specular-Verdeckung zu berechnen, um Geworfen Schatten zu zeichnen.<br><br>Ein höherer Wert führt zu präziseren Schatten auf Kosten der Leistung. |
| <b>Kameramodus</b> *Integer* | Die Methode zum Projizieren der Szene auf das Renderbild:<br><br>- <b>Perspektive:</b> Diese Projektion überträgt die Tiefe und ermöglicht Linseneffekte wie die Tiefe des Halbbildes.<br>- <b>Orthographisch:</b> Diese Projektion reduziert die Szene und hebt die Tiefe auf.<br>- <b>Benutzerdefinierte Funktion:</b> Erstellen Sie ein Funktionsdiagramm, um eine benutzerdefinierte Kamera einzurichten. |
| <b>Kamerafunktion</b> *Float3* | Das Funktionsdiagramm, das die Transformation der Kamera definiert. Dies kann für die Einrichtung einer eigenen Kamera verwendet werden.<br><br>Die Funktion sollte <b>diese Variablen setzen</b>:<br>- <code>view.origin</code> (Float3) Die Weltraumposition der Kameraansicht pro Pixel.<br>- <code>view.direction</code> (Float3) Der Vorwärtsvektor pro Pixel der Kameraansicht gemäß dem Projektionsmodus. (E.g. Perspektive oder Orthografie)<br><br>Die folgenden Variablen sind für <b>get</b> verfügbar:<br>- <code>camera.origin</code> (Float3) Die Weltraumposition der Kamera. (camera.direction * camera_distance + camera.target)<br>- <code>camera.direction</code> (Float3) Die Weltraumrichtung der Kamera, d. h. der Y-Vorwärtsvektor der Kamera.<br>- <code>camera.right</code> (Float3) Der X-Right-Vektor der Kamera.<br>- <code>camera.up</code> (Float3) Z-Up-Vektor der Kamera.<br>- <code>camera.target</code> (Float3) Die Weltraumposition des Kameraziels. |
| <b>UV-Position</b> *Float2* | Die Position im 2D-Bildbereich, die verwendet wurde, um die Kameraposition und -richtung abzuleiten, die die <b>Zielposition</b> umkreist.<br><br><i>Tipp:</i> Dieser Parameter kann intuitiv angepasst werden, indem das <i>Positions-Gizmo</i> verwendet wird, das in der 2D-Ansicht verfügbar ist, wenn der Knoten ausgewählt ist. |
| <b>FOV</b> *Gleitend* | Das Blickfeld der orthogonalen Kamera (FOV), das sich auf den Zoomfaktor auswirkt. |
| <b>Brennweite</b> *Gleitend* | Die Brennweite der Kamera, die den Zoomfaktor und die Tiefe des Feldeffekts beeinflusst. |
| <b>Entfernung vom Ziel</b> *Gleitend* | Die Entfernung, die die Kamera von der <b>Zielposition</b> halten soll.<br><br>Durch Anpassen dieser Option wird die Kamera entlang der Zielrichtung der Kamera bewegt. |
| <b>Zielposition</b> *Float3* | Die Position des Kamerazieles, auf das die Kamera immer ausgerichtet ist. |
| <b>Tonemapper</b> *Integer* | Der Tonzuordnungsalgorithmus, der auf das Szenenrendern angewendet werden soll.<br><br>- <b>Keine (RAW)<br>- <b>sRGB</b><br>- <b>AgX</b><br>- <b>ACES</b> |
| <b>Tiefe des Felds aktivieren</b> *Boolescher Wert* | Simuliert den Kameraobjektiveffekt &quot;Tiefe des Halbbilds&quot; für die Perspektivkamera.<br><br>Verwenden Sie die Parameter <b>F number</b> und <b>Fokusabstand</b>, um die Blende bzw. den Fokus des Effekts anzupassen.<br><br>Das Ergebnis ist auch auf die <b>Brennweite</b> ausgewirkt. |
| <b>F-number</b> *Gleitend* | Die <i>Blendenöffnung</i>.<br><br>Ein niedrigerer Wert führt zu einer geringeren <i>Tiefe des Halbbildes</i>, d. h. einem geringeren Entfernungsbereich für scharfe Objekte und einem stärkeren Weichzeichnungseffekt, wenn der Abstand von diesem Bereich zunimmt. |
| <b>Fokusentfernung</b> *Gleitend* | Legt den Abstand des Fokuspunkts von der Kamera entlang des Vorwärtsvektors fest.<br><br>Flächen innerhalb dieses Abstandsbereichs erscheinen scharf, dieser Bereich — die <i>Tiefe des Feldes </i> — wird durch die <b>F-Zahl</b> definiert. |
| <b>Belichtung (EV)</b> *Gleitend* | Die Lichtmenge, die den Kamerasensor erreicht, d. h. die Intensität der Beleuchtung im Rendering.<br><br>Ein niedrigerer Wert führt zu einer dunkleren gerenderten Szene.<br><br>Der &#39;Belichtungswert&#39; (EV) bezieht sich speziell darauf, wie viel Licht der Kamerasensor <i>belichtet</i> hat. |
| <b>Grundfarbe</b> *Float3* | Die Standardgrundfarbe für Flächen, bei denen diese Farbe nicht durch ihre SDF- oder Schnittfunktion definiert ist. |
| <b>Raueit</b> *Gleitend* | Der Standardrauhheitswert für Flächen, bei denen dieser Wert nicht durch die SDF- oder Schnittfunktion definiert ist. |
| <b>Metalität</b> *Gleitend* | Der Metalitätswert für Flächen, bei denen dieser Wert nicht durch die SDF- oder Schnittfunktion definiert ist. |
| <b>Deckkraft der Helfer</b> *Gleitend* | Die Deckkraft der 3D-Helfer, wobei ein niedrigerer Wert zu schwächeren Helfern führt. |
| <b>Begrenzungsrahmen</b> *Boolescher Wert* | Eine Visualisierung eines sechsseitigen Käfigs, der die Grenzen der gesamten Szene definiert. Sollte idealerweise die kleinstmögliche Größe sein, die die Szene vollständig einschließt.<br><br>Verwenden Sie den Parameter <b>Größe des Begrenzungsrahmens</b>, um die Größe des Käfigs anzupassen.<br><br>Mit dem Parameter <b>Aus Bild einfärben</b> können Sie die Oberflächen außerhalb dieses Käfigs ganz einfach sichtbar machen, was sich auf das Ergebnis der Verwendung dieser Szene im Knoten [Form splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) auswirkt. (Siehe QuickInfo zu &quot;Begrenzungsrahmengröße&quot;) |
| <b>Begrenzte Framegröße</b> *Float3* | Legt die XYZ-Größe des Begrenzungsrahmens fest.<br><br>Passen Sie den Frame an Ihre Szene an und wenden Sie dann dieselben Werte auf den <b>SDF-gebundenen Frame-Größe</b>-Parameter des [Shape-Splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)-Knotens an, um sicherzustellen, dass alle Formen in der Szene korrekt von diesem Knoten eingeschlossen und gezeichnet werden. |
| <b>Aus Bild einfärben</b> *Boolescher Wert* | Wendet eine rote Farbe auf die Flächen außerhalb des Begrenzungsrahmens an.<br><br>Dies hilft zu überprüfen, ob die Szene vollständig in ihrem Begrenzungsrahmen enthalten ist. |
| <b>Achse</b> *Boolescher Wert* | Eine Visualisierung der XYZ-Achsen der Szene als farbige Linien, die an ihrem Ursprung beginnen. |
| <b>Grid</b> *Boolescher Wert* | Eine Visualisierung eines Rasters, das auf den XY-Achsen angeordnet ist, wobei die Größe einer Zelle in X und Y eine Szeneneinheit ist. |
| <b>Transformieren-Helfer</b> *Boolescher Wert* | Eine Visualisierung der zuletzt angewendeten Drehung.<br><br>Die Visualisierung enthält <br>- <b>einen Pfeil</b>, der den Rotationsachsenrichtungsvektor darstellt und nach den Gewichten jeder Weltraumachse gefärbt ist.<br>- <b>Ein Bogen</b>, der den Rotationswinkel darstellt, der orthogonal zu dem Pfeil ist, der seiner Farbe entspricht. |
| <b>SDF-Isolinien</b> *Boolescher Wert* | Eine farbige Visualisierung der Funktionsisolinen für das vorzeichenbehaftete Distanzfeld (SDF).<br><br>Die Isolinien sind regelmäßig wiederholende Linien, die das <i>Abstandsfeld</i> der Form auf der XY-Ebene in einem bestimmten Height darstellen.<br><br>Diese sind nützlich, um die <i>Gleichmäßigkeit des durch die SDF-Funktion definierten Leerzeichens</i> zu überprüfen.<br><br>Verwenden Sie die Parameter <b>SDF-Isolinienfrequenz</b> und <b>SDF-Isolinienposition</b>, um die Dichte und das Height der Isolinien anzupassen. |
| <b>Häufigkeit der SDF-Isolinien</b> *Gleitend* | Die Anzahl der Isolinienwiederholungen innerhalb einer bestimmten Entfernung.<br><br>Ein höherer Wert führt zu dichteren, dünneren Linien. |
| <b>SDF-Isolinienposition</b> *Gleitend* | Das Weltraum-Height der XY-Ebene, mit dem die Isolinien gezeichnet wurden.<br><br>Verwenden Sie diese Option, um das Abstandsfeld der Form in verschiedenen Höhen zu überprüfen. |
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

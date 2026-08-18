---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über die Pfadformatspezifikationen und die Datenstruktur, die von Pfad- und Spline-Knoten verwendet werden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spezifikationen zum Pfadformat
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# Spezifikationen zum Pfadformat

Auf dieser Seite wird das Pfadeformat beschrieben. Dort finden Sie Anleitungen zum Bearbeiten der Daten in diesem Format mithilfe der Funktionen, die in den Pfadewerkzeugen enthalten sind.

## Formatspezifikationen

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

In diesem Abschnitt wird erläutert, wie ein <b>Pfadedokument</b> (oder ein Bild) codiert wird:

Ein Pfadedokument ist eine Liste von Pfaden, von denen jeder eine Liste von Segmenten beschreibt, die in einer <b>32-Bit-Gleitkomma-Farbstruktur codiert sind</b>.

Die Textur wird in den oberen (*$pos.y &lt; 0.5*) und den unteren (*$pos.y > 0.5*) Teil aufgeteilt.

Alle Daten in einem Pixel im oberen Teil sind semantisch eng mit dem entsprechenden Pixel im unteren Teil verknüpft und umgekehrt.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Pfade Polygon-codierte Daten](../../../../../../assets/PathsPolygon_Data.jpg "Pfade Polygon-codierte Daten")

</td>
</tr>
</table>

>[!NOTE]
>
> Pfade erfordern eine 32-Bit-Genauigkeit, und wenn Sie eine geringere Bittiefe verwenden, erhalten Sie falsche Ergebnisse.
> 
> Stellen Sie daher sicher, dass Sie den Parameter &quot;Ausgabeformat&quot; von Knoten, die Pfade generieren, auf &quot;HDR High Precision (32F)&quot; setzen.

`*uv\_pos*` soll eine 2D-Adresse (z. B. *$pos*) eines Pixels des oberen Teils sein.

Im restlichen Dokument:

* <b>top[uv\_pos].XYZW</b> bezieht sich auf die 4 schwebenden Elemente, die im Pixel des oberen Teils gespeichert sind.\
  top[uv\_pos] == sample\_color(paths, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b> bezieht sich auf die 4 schwebenden Elemente, die im entsprechenden Pixel des unteren Teils gespeichert sind.\
  bottom[uv\_pos] == sample\_color(paths, uv\_pos + Float2(0, 0.5))

top[uv\_pos] und bottom[uv\_pos] bilden zusammen eine semantische Einheit U[uv\_pos] des Dokuments, die aus 8 Gleitkommas besteht.

### Dokumentkopfzeile

Jedes Pfade-Dokument beginnt mit einer Dokumentkopfzeile. Es ist die erste semantische Einheit U[(0,0)]:

+++Oben
<b>X</b>

Die Anzahl der Pfade (sollte eine positive ganze Zahl in [0; 16777216]).

Wenn einige Pfade leer sind, zählen sie hier trotzdem. Man kann sich das als &quot;Anzahl der zu decodierenden Pfade&quot; vorstellen.

<b>YZ</b>

Die Pixelgröße für dieses Dokument (also genau `Float2(1,1) / $size`).

Dies ist nützlich, wenn Sie die Pfade beispielsweise von einem [Pixelprozessor](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) oder einer [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) lesen, deren Ausgabegröße unterschiedlich ist.

<b>W</b>

1/16 = 0,0625 (Header-Flag)

+++

+++Unten
<b>XY</b>

Die Adresse des letzten in diesem Dokument definierten Scheitelpunkts. Dies ist nützlich, um neue Daten anzufügen.

Es kann also tatsächlich eine beliebige Adresse sein, die größer ist (in Scannline-Reihenfolge) als die Adresse des letzten Scheitelpunktes. Es muss im Bereich &rbrack;0, 1[×]0,.5&lbrack; liegen

<b>ZW</b>

Nicht verwendet, sollte Float2(0, 1) sein

+++

### Path Headers

Auf die Dokumentkopfzeile folgt unmittelbar die Pfadanzahl = top[(0,0)].X Pfadkopfzeilen, eine nach semantischen Einheiten.\
E.g. Wenn das Dokument 3 Pfade enthält, werden sie in U[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size] und U[(0,3)\*pixel\_size] (mit pixel\_size = top[(0,0)].YZ) gespeichert.

Wenn es mehr Pfade gibt, als eine Zeile Pixel enthalten kann, werden die restlichen Pfad-Header in die nächste Zeile(n) geschrieben, und zwar in der eingescannten Reihenfolge.\
Es darf keine Pfad-Header (`top[...].XYZW = Float4(0,0,0,0)`) enthalten. Ein solcher Pfad könnte immer noch einen leeren Pfad enthalten.

Der Pfad-Header des N-ten Pfads wird an der Adresse `path\_addr` definiert und wird wie folgt definiert:

+++Oben
<b>X</b>

Anzahl der Scheitelpunkte in diesem Pfad. Muss im Bereich [0, 16777216] liegen.

Wenn die Anfangs- und Endscheitelpunkte eines geschlossenen Pfads sich an derselben Position befinden, werden sie weiterhin für 2 Scheitelpunkte gezählt.\
Ein Pfad mit 0 Scheitelpunkten ist ohnehin ein gültiger Pfad.

<b>J</b>

*Is\_closed* Flag: 1, wenn der Pfad geschlossen ist (z. B. ein Kreis), andernfalls 0 (z. B. eine gerade Linie).

<b>Z</b>

Der Pfadindex *N.* Es muss absolut mit *path\_addr* übereinstimmen (siehe Hinweis unten).

<b>W</b>

Das Header-Flag: 1/16 = 0.0625.

+++

+++Unten
<b>XY</b>

Anfangsscheitelpunktadresse (oder erste Scheitelpunktadresse)

<b>ZW</b>

Endpunktadresse (oder letzte Scheitelpunktadresse).

+++

>[!NOTE]
>
> Sie können `path\_addr` aus N mithilfe der Funktion `Utils/pixel\_index\_to\_position` in den Pfaden\_tools.sbs berechnen: 2`path\_addr = pixel\_index\_to\_position(N+1)`

### Vertices-Informationen

Scheitelpunkte befinden sich an beliebiger Stelle im Bild nach den Kopfzeilen (Dokument- oder Pfadkopfzeilen). Eckpunkte können verschiedene &quot;Typen&quot; (Start, Mid oder End) sein und werden explizit mit 2 Adresszeigern (&quot;Links&quot;) miteinander verknüpft.

<b>Start</b>- und <b>End</b>-Scheitelpunkte sind in dieser Hinsicht besonders: Um die Darstellung geschlossener Pfade oder eines beliebigen Netzes von miteinander verknüpften Pfaden zu ermöglichen, wird einer der Links tatsächlich verwendet, um eine kreisförmige, nach vorne verknüpfte Liste aller anderen Start- oder Endscheitelpunkte zu bilden, die denselben Scheitelpunkt darstellen. Solche Scheitelpunkte, die zueinander passen, werden als &quot;Geschwister&quot; bezeichnet. [Illustration begrüßt]

Formell ist jeder Scheitelpunkt an der Adresse `*vert\_addr*` wie folgt definiert:

+++Oben
<b>XY</b>

Die Scheitelpunktposition. Koordinaten können beliebige Gleitkommawerte sein, die nicht NaN oder ±inf sind. Es gibt keine Vorstellung von Fliesen auf dieser Ebene (es kann von der Implementierung jedes Filters gehandhabt werden oder nicht), also sollen Pfade auf der euklidischen Ebene definiert werden.

<b>Z</b>

Der Scheitelpunkt-Pfadindex. Ein Scheitelpunkt kann nur zu einem Pfad gehören. (Wie bereits erwähnt, können Start- und End-Scheitelpunkte gleichrangig sein.) Der Pfadindex kann verwendet werden, um den Pfad-Header abzurufen (siehe Abschnitt Path Headers oben). Stellen Sie daher sicher, dass er synchron bleibt.

<b>W</b>

Scheitelpunkttyp. Es wird zwischen dem Vorzeichen des Werts und seinem absoluten Wert aufgeteilt:

Auf der Vorzeichenseite würde ein Wert von 0 bedeuten, dass es hier keinen Scheitelpunkt gibt (alle anderen Komponenten sollten ebenfalls 0 sein). Ein negativer Wert bedeutet, dass der Scheitelpunkt als &quot;Ecke&quot; gekennzeichnet ist. ein positives Zeichen, dass der Scheitelpunkt &quot;glatt&quot; ist. &quot;Ecke vs. glatter Scheitelpunkt&quot; ist ein reines, isoliertes Attribut und hat keine Auswirkungen oder Bedeutung auf den Rest der Pfade-Codierung.

Auf der Absolutwertkomponente werden die Art des Pixels (Anfang, Mitte oder Ende) und ein weiteres Flag (trivial\_link) codiert:

* *0.125*: Endscheitelpunkt (letzter Scheitelpunkt der Form; immer nicht triviale Links, siehe unten)

* *0.25*: Anfangsscheitelpunkt (der erste Scheitelpunkt der Form; immer nicht triviale Links, siehe unten)

* *0.5*: Mittlerer Scheitelpunkt mit nicht trivialen Verknüpfungen

* *1*: Mittlerer Scheitelpunkt mit trivialen Verknüpfungen

&quot;Triviale Links&quot; bezieht sich auf die Tatsache, dass der vorherige und der nächste Scheitelpunkt (in der Liste der Scheitelpunkte des aktuellen Pfads) im Pixel links (vert\_addr-(0,pixel\_size)) bzw. rechts (vert\_addr+(0,pixel\_size)) gespeichert werden, während &quot;nicht triviale Links&quot; bedeutet, dass mindestens einer dieser Scheitelpunkte an einem anderen Ort gespeichert wird.

+++

+++Unten
Unabhängig von der &quot;Trivialität&quot; der Links werden vertrauenswürdige Werte der Links im unteren Teil gespeichert:

<b>XY</b>

Die Adresse des vorherigen Scheitelpunkts dieses Pfads. Bei &quot;Start&quot;-Scheitelpunkten verweist dies auf den nächsten gleichgeordneten Scheitelpunkt.\
wenn |top[vert\_addr].W| = 1, dann bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

Die Adresse des nächsten Scheitelpunktes dieses Pfades. Bei Endscheitelpunkten verweist dieser Punkt auf den nächsten gleichgeordneten Scheitelpunkt.\
wenn |top[vert\_addr].W| = 1, dann bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## Informationen zu Pfaden lesen und schreiben

Wenn Sie eigene Knoten zur Pfadverarbeitung erstellen möchten, stehen Ihnen verschiedene Tools zur Verfügung.

Die Grundlagen werden von den Knoten [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) und [Paths Vertex Processor Simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md) bereitgestellt, die im Grunde wie ein [Pixelprozessor](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) verwendet werden können.

Wenn Sie Features benötigen, die über die Möglichkeiten der Knoten des Pfade-Scheitelpunkts hinausgehen (mehr Eingabetexturen oder mehr vorherige oder nächste Scheitelpunkte), kann das Kopieren der Implementierung dieses Diagramms ein guter Ausgangspunkt sein (vorausgesetzt, Sie ersetzen den Knoten <b>Get(&quot;%perVertex&quot;)</b> durch Ihre benutzerdefinierte Verarbeitung).

Aber für den Fall, dass Sie etwas Außerirdischeres tun möchten, als eine Pro-Vertex-Funktion anzuwenden, gibt es hier eine detaillierte Erklärung der Werkzeuge, die Sie verwenden können. Dies sind normalerweise kleine Hilfsfunktionen, die im selben Paket wie die anderen Pfade-Knoten (*Pfade\_tools.sbs)* gefunden werden können. (Diese Funktionen werden nicht im [<b>Bibliotheks</b>](../../../../../../interface/the-library/the-library.md) und <b>Knotenmenü</b> verfügbar gemacht.)

### Lesen-Funktionen

Unter dem Ordner &quot;`Read`&quot; finden Sie mehrere dieser Optionen, die hilfreich sind, um Informationen über die Pfade zu sammeln:

Einige können Ihnen Informationen zu einem bestimmten Pixel geben. Sie alle nehmen den abgetasteten Float4-Wert im \*top\* Teil als Eingabe. Wenn man sich ihre Implementierung ansieht, sind sie supereinfach. Es geht darum, mehr Bedeutung zu vermitteln als nur Atomknoten:

+++is_header
Vergewissern Sie sich, dass der aktuelle Vorlagewert entweder eine Pfadkopfzeile oder eine Dokumentkopfzeile ist.

+++

+++path_is_closed
Überprüfen Sie das Flag Is\_Closed (.Y) in einem Pfadkopf. Es wird \*vorausgesetzt, dass Sie bereits überprüft haben, dass es sich um einen Pfad\* mit `is\_header` handelt und dass `current\_pixel\_is\_document\_header` &quot;false&quot; zurückgegeben hat.

+++

+++is_vertex
Überprüfen Sie, ob der aktuelle Vorlagewert ein Scheitelpunkt ist, d. h. keine Kopfzeile und kein leeres Pixel.

+++

+++is_start_vertex
Überprüfen Sie, ob es sich bei einem \*obersten Teil des abgetasteten\* Werts um einen Startscheitelpunkt handelt (Sie müssen `is\_vertex` nicht zuerst überprüfen).

+++

+++is_mid_vertex
Überprüfen Sie, ob es sich bei einem \*top-part sampling\*-Wert um einen Scheitelpunkt handelt, der weder Start noch End-Scheitelpunkt ist (Sie müssen `is\_vertex` nicht zuerst überprüfen).

+++

+++is_end_vertex
Überprüfen Sie, ob es sich bei einem \*top-part sampling\*-Wert um einen End-Scheitelpunkt handelt (Sie müssen `is\_vertex` nicht zuerst überprüfen).

+++

+++is_segment_start
Kurzhand für `is\_start\_vertex || is\_mid\_vertex`. Nützlicher für die [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)-basierte Verarbeitung, um jedes Segment maximal einmal zu verarbeiten.

+++

+++is_corner
Überprüfen Sie das Eckflag des Scheitelpunkts (es ist nicht erforderlich, zuerst `is\_vertex` zu überprüfen: wenn die Antwort wahr ist, sind Sie sicher an einem Scheitelpunkt). Bitte erinnern Sie daran, dass dieses Flag noch nicht von offiziellen Knoten unterstützt wird.

+++

+++has_trivial_links
Wenn es sich um einen Scheitelpunkt handelt, wird angegeben, ob Sie die Position des vorherigen und nächsten Scheitelpunkts mühelos ableiten können, ohne den unteren Teil mit einem Sampling zu versehen. (Hinweis: Ein Nicht-Vertex gibt immer false zurück.)

Wahrscheinlich möchten Sie dies nicht direkt verwenden, sondern eine der `sample\_next\*`- oder `sample\_prev\*`-Funktionen verwenden, die sich darum kümmern.

+++

+++sample_next, sample_prev
Gibt den nächsten (bzw. vorherigen) Scheitelpunkt des obersten Teils des Abtastwerts &quot;`*sampled*`&quot; und seine Position &quot;`*sampled\_position*`&quot; zurück und legt eine Float2-Variable &quot;`*next\_sampled\_pos*`&quot; auf die Position (im obersten Teil) dieses Nachbarn fest (d. h. &lt;Rückgabewert> = SampleColor(next\_sampling\_pos, image0). `*input0PixSize*` muss der Pixelgröße des Pfades entsprechen (top[(0,0)].YZ).

Wenn das aktuelle Pixel (`*sampled*`) ein <b>Start</b>-Scheitelpunkt ist, gibt *sample\_prev* das nächste gleichgeordnete Element dieses Scheitelpunkts zurück. ebenfalls, wenn es sich um einen <b>End</b>-Scheitelpunkt handelt, gibt *sample\_next* das nächste gleichgeordnete Element dieses Scheitelpunkts zurück (d. h. möglicherweise nicht das, was Sie möchten). Siehe `*sample\_next\_advanced*` und `*sample\_prev\_advanced*` unten, um dieses Problem zu lösen.

Bitte beachten Sie, dass aus Gründen der Einfachheit davon ausgegangen wird, dass <b>Pfade-Informationen in input0!</b> gespeichert sind. Außerdem müssen Sie im Gegensatz zu den Dokumentstatus der Funktion `*next\_sampled\_pos*` nicht vorab deklarieren. `*[out]next\_sampled\_pos*` ist ein Dummy-Parameter, der Sie daran erinnert, dass dieser zweite &quot;Rückgabewert&quot; vorhanden ist.

Sie können `*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) im Parameter &quot;Iterationen&quot; des 3. Iterate-Knotens nach einem Beispiel für dessen Verwendung durchsuchen.

![Minimaler Anwendungsfall von sample_next](../../../../../../assets/paths-spec_fxmap-sample-next_02.png "Minimaler Anwendungsfall von sample_next")



![Anwendungsfall von sample_next in Vorschaupfaden (path_trace)](../../../../../../assets/paths-spec_fxmap-sample-next_01.png "Anwendungsfall von sample_next in Vorschaupfaden (path_trace)")



+++

+++sample_next_advanced, sample_prev_advanced
Dies soll auf geschlossenen Wegen arbeiten. Bei offenen Pfaden ist der Scheitelpunkt &quot;Anfang&quot; oder &quot;Ende&quot; nicht gleichrangig. In diesem Fall geben beide Funktionen den gleichen Wert zurück und nur einen Nachbarn. Bei Start- oder End-Scheitelpunkten mit mehr als einem gleichrangigen Element (als Netzwerk verbundene Pfade) würde dies den benachbarten Scheitelpunkt des nächsten gleichrangigen Elements in der verknüpften Liste zurückgeben.

+++

### Write-Funktionen

Im Ordner &quot;`Write`&quot; finden Sie kleine Helfer, die einen Float4 erstellen, der von einer [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b> geschrieben werden kann.<b>

Tatsächlich multipliziert die [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) RGB vor dem Zeichnen mit Alpha, sodass die tatsächlichen Werte nicht vormultipliziert werden, um dies zu kompensieren. Wenn Sie diese Funktion z. B. in einem [Pixelprozessor](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) verwenden möchten, empfehlen wir Ihnen, die Vormultiplikation erneut anzuwenden oder eine benutzerdefinierte Version zu schreiben (besser für Ihren Anwendungsfall optimiert und einfacher zu verwenden).

+++document_header
Erstellt den oberen Teil der Dokumentkopfzeile und deklariert die Anzahl der von Ihnen angegebenen Pfade.

+++

+++document_last_vertex_spec
Erstellt den Teil \*bottom\* der Dokumentkopfzeile, der die letzte Scheitelpunktadresse angibt (siehe A.1.).

+++

+++path_header
Erstellt den oberen Teil eines Pfadheaders entsprechend der Anzahl der Scheitelpunkte im Pfad &quot;`*nbVertices*`&quot;, dem Flag &quot;`*isClosed*`&quot; und dem Flag &quot;`*pathIndex*`&quot;.

+++

+++start_vertex, mid_vertex, end_vertex
Erstellt den oberen Teil eines Scheitelpunkts und legt die Position, den Typ und andere Optionen entsprechend fest.

Über *mid\_vertex* und den *hasTrivialLinks*-Parameter: Idealerweise sollten Sie den entsprechenden Wert festlegen, aber wenn Sie aus irgendeinem Grund nicht sagen können, ob Links trivial sind oder nicht, können Sie ihn sicher auf &quot;false&quot; setzen (auf Kosten einer langsameren Verarbeitung des generierten Pfads).

+++

Es gibt keinen Bottom-Part-Generator für Pfadkopfzeilen oder Scheitelpunkte: Beide codieren zwei Verknüpfungen zum oberen Teil, sodass diese Funktion im Wesentlichen ein Vector Float4-Konstruktor aus zwei Float2 wäre. Vergessen Sie nicht, XYZ durch W zu teilen, wenn Sie unter Verwendung einer [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) schreiben (W ist das Y einer Adresse, es sollte nie Null sein).

Ein entsprechendes Beispiel für die Verwendung dieser Funktionen finden Sie im Paket <b>*Pfade\_polygon.sbs* </b>mit dem Knoten [Pfade Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md).

### Verfahren zum Verarbeiten von Pfaden

Sie werden wahrscheinlich entweder einen Pixelprozessor oder eine Fx-Map verwenden, um Ihre benutzerdefinierte Verarbeitung zu implementieren, von denen jede ihre Stärken und Schwächen hat:

+++FX-Map
Die [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)-basierte Lösung wird in der Regel bevorzugt, wenn ein Vorgang auf hoher Ebene durchgeführt wird, der eine globale Kenntnis des gesamten Pfades (oder Pfade) oder eines kumulativen Pfades erfordert (z. B. Umpacken von Scheitelpunkten nach Dezimierung oder Tesselierung). Es ist auch der einfachste Ansatz. Wenn Sie also zum ersten Mal eine benutzerdefinierte Verarbeitung durchführen, sollten Sie möglicherweise eine Fx-Map verwenden, obwohl *möglicherweise* langsamer ist.

Sie müssen sich zunächst mit Fx-Map auskennen. Wenn dies nicht der Fall ist, überprüfen Sie die [spezifische Dokumentation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md).

Es wird empfohlen, sich die Implementierung von [Preview Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) in <b>*Pfaden\_trace.sbs*</b> und [Pfade Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) in <b>*Pfaden\_polygon.sbs*</b> anzusehen, um eine Vorstellung davon zu erhalten, wie ein Pfad mit einer Fx-Map gelesen bzw. geschrieben werden kann.

+++

+++Pixel-Prozessor
Die Lösung für den [Pixelprozessor](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) passt, wenn Sie nur &quot;lokale&quot; Informationen benötigen. Hier meinen wir &quot;lokal&quot; nicht räumlich (der Abstand zwischen Elementen), sondern topologisch (miteinander verbundene Eckpunkte). So wird der Vertex-Prozessor implementiert. Der Pixelprozessor ist bei dieser Art von Operation in der Regel schneller als die Fx-Map, da die Funktion jedes Pixels parallel ausgewertet wird, während nur eine begrenzte Datenmenge abgerufen wird. Der Implementierungsaufwand könnte jedoch weitaus wichtiger sein, da Sie nur das aktuelle Pixel ändern können.

Wir werden nicht ins Detail gehen, da es je nach Anwendungsfall so viel zu sagen gibt, aber als Erstes müssen wir überprüfen, wo Sie sich befinden:

Sind Sie im oberen ($pos.y &lt; 0,5) oder unteren ($pos.y > 0,5) Teil? Wir empfehlen, sich daran zu erinnern, dass in einer dedizierten Variablen (z. `*isTop*`), und dass Sie einen `*vert.addr*`-Float2 erstellen, ist dieser Wert `*$pos*` für den oberen Teil und `$pos - (0,0.5)` für den unteren Teil.

Was befindet sich unter *vert.addr*? Nehmen Sie es auf und prüfen Sie, ob etwas vorhanden ist (W != 0), wenn es etwas gibt, was genau. Ein Header (W = 0,0625) (mit `*Read/is\_header*` prüfen) oder ein Scheitelpunkt (mit `Read/is\_vertex` prüfen)? Und wenn es eine Kopfzeile ist, ist es die Dokumentkopfzeile oder eine Pfadkopfzeile? (Sie können `*Read/current\_pixel\_is\_document\_header*` verwenden, um dies zu überprüfen.) Verwenden Sie eine oder mehrere der Hilfsfunktionen, um das für Sie interessante zu finden.

+++

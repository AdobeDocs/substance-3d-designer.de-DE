---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: Erfahren Sie Richtlinien zur Leistungsoptimierung für Substance 3D Designer, um die Diagrammleistung zu verbessern und die Verarbeitungszeit zu reduzieren.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtlinien zur Leistungsoptimierung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 0%

---


# Richtlinien zur Leistungsoptimierung

## Substance-Graphen

Je komplexer Ihre [Substance-Diagramme](../../compositing-graphs/substance-compositing-graphs.md) sind, desto mehr Verarbeitungsleistung benötigen Sie zum Rendern. Sie sollten versuchen, <b>ein Gleichgewicht zwischen Komplexität und Rendering-Geschwindigkeit herzustellen</b>.\
Dies ist *besonders* wichtig, wenn Sie sie in Echtzeit-Grafikanwendungen wie Spielen verwenden.

Im Allgemeinen sollten Knoten mit benutzerdefinierten Parametern, die zur Laufzeit geändert werden können - <b>, so nah wie möglich am Ende des Diagramms platziert werden</b>.

Dies liegt daran, dass die Ausgabe jedes Knotens nach Möglichkeit zwischengespeichert wird. Je höher der Graph des anpassbaren Knotens ist, desto mehr Ausgaben müssen verarbeitet werden, wenn einer dieser exponierten Parameter geändert wird. Wenn sich der angezeigte Knoten nahe am Ende des Diagramms befindet, müssen nur die wenigen Knoten zwischen ihm und den Ausgabeknoten neu berechnet werden.

Wenn Sie beispielsweise eine einheitliche Farbe am Anfang Ihres Diagramms anpassen, werden alle folgenden Knoten neu berechnet. Wenn Sie einen HSL-Knoten direkt vor der Ausgabe optimieren, wird nur dieser Knoten neu berechnet, wodurch die Leistung des Diagramms erheblich verbessert wird.

Bitte beachten Sie die folgenden Richtlinien:

### ALLGEMEINE LEISTUNGSBEZOGENE EINSTELLUNGEN

+++GPU-Engine ist viel schneller als CPU-Engine
Verwenden Sie die GPU-Substance-Engine (mit Hotkey F9 wechseln), es sei denn, Sie haben eine nicht unterstützte (integrierte) Grafikkarte.

+++

+++Das Wechseln der übergeordneten Auflösung des Diagramms ist langsam
Es berechnet Graph, Cache und alle Miniaturansichten neu. Es ist besser, [die Registerkarte <b>Batch </b> des Exportdialogs ](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) zu verwenden, da dadurch eine umfangreiche, nicht benötigte Neuberechnung vermieden wird (z. B. beim Export in die Auflösung 8192).

+++

+++In Extremfällen kann ein erhöhter Speicher-Cache erforderlich sein
Die Anwendung &quot;[&quot; begrenzt den Arbeitsspeicher, der ](../../interface/preferences-window/preferences-window.md) für den Bildcache verwendet werden kann. Sie können diesen jedoch überschreiben und erhöhen (mit Vorsicht).

+++

### DIAGRAMMOPTIMIERUNG

+++Achten Sie auf die Knotenauflösungen und die Vererbung im Allgemeinen!
Hohe Werte wirken sich stark auf die Leistung aus. Überlege dir also, wie das Material voraussichtlich verwendet wird und ob du die Datengröße reduzieren kannst.

Es wird empfohlen, mehr über die [Knotenauflösung (Ausgabegröße)](../../compositing-graphs/output-size/output-size.md) und die [Vererbung in Substance-Graphen](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) zu erfahren.

+++

+++Verwenden von Graustufen, wenn keine Farbe erforderlich ist
Farbvorgänge dauern viermal länger als Graustufenvorgänge. Versuchen Sie außerdem, die Typkonvertierung zwischen Farb- und Graustufendarstellung zu minimieren.

+++

+++8 Bit verwenden, wenn 16 Bit nicht benötigt wird
Die CPU-Version des Substance Engine (SSE2) *unterstützt weder 16-Bit-Farbton noch 8-Bit-Graustufen.* Die GPU-Engine unterstützt alle 4 Kombinationen von 8/16 Bit und Graustufen/Farbe. *Derzeit wird nur das CPU-Modul in Unity- und Unreal Engine-Plug-ins verwendet*.

+++

+++Minimieren der Knotenausgabegröße, wann immer möglich
Manchmal wirkt sich die Verkleinerung einiger Knoten nicht auf das Endergebnis aus, sondern auf die Leistung. Beispielsweise ist die Verwendung eines Knotens mit einheitlicher Farbe, der auf dieselbe Ausgabegröße wie das Dokument festgelegt ist, sinnlos: Die einheitliche Farbe sollte auf &quot;Absolut [16px x 16px]&quot; und der nachfolgende Knoten auf &quot;Relativ zur übergeordneten Farbe&quot; gesetzt werden. Im Allgemeinen eignet sich dieser Trick gut für Bilder mit niedriger Frequenz, wie zum Beispiel Perlin-Rauschen.

+++

+++Verwenden Sie keine Bilder, die kleiner als 16 x 16 Pixel sind.
Dies verlangsamt die Rendering-Leistung.

+++

+++Deaktivieren Sie bei Verwendung des Überblendungsknotens die Alpha-Überblendung, wenn sie nicht erforderlich ist.


+++

+++Weichzeichner und Verkrümmungen sind die prozessorintensivsten Knoten.


+++

+++Einige Geräuscherzeuger sind von der Anzahl der gezeichneten Muster betroffen.
Der Knoten &quot;[Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)&quot; wird beispielsweise langsamer, wenn Sie mehr Muster verarbeiten möchten, die Sie ihm hinzufügen.

+++

+++Einige Geräusche werden durch einen Skalierungsfaktor beeinflusst
Dieser Faktor wird in der Tat mehr Muster ziehen. Zu den betroffenen Nodes gehören Geräusche, Zellen usw. Wenn Sie ein weißes Rauschmuster benötigen, verwenden Sie kein Rauschen mit einem sehr hohen Skalierungswert und verwenden Sie stattdessen die Knoten [Weißes Rauschen](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md) oder [Weißes Rauschen schnell](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md).

+++

+++Umgekehrt gibt es einige sehr schnelle Geräuscherzeuger
Dazu gehören [White Noise Fast](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md), [Fraktalsumme Base](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md) und [Anisotropic Noise](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md).

+++

+++In manchen Fällen solltest du auf umfangreiche Bildaufnahmefunktionen achten
Mit Ausnahme von [Pixelprozessoren](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) werden Funktionen auf der CPU-Engine ausgeführt. Wenn Sie in [Value Processors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) oder [FXmaps](../../function-graphs/fxmaps/fxmaps.md) viele Bildberechnungen (Ändern der $pos-Koordinaten) durchführen, kommt es zu einem großen Austausch zwischen VRAM und CPU-RAM, was zu Leistungsverzögerungen führt.

+++

### OPTIMIERUNGEN FÜR DIE MOBILNUTZUNG

+++Es wird nicht empfohlen, Warps und FX-Maps zu verwenden.
Sie sind sehr leistungsintensiv.

+++

+++Weichzeichnungsknoten vermeiden
Verwenden Sie stattdessen Downscale-Transformationen.

+++

+++Arbeiten Sie so viel wie möglich in Graustufen
Wechseln Sie am Ende des Diagramms in den Farbmodus.

+++

+++Knotenpunkte so weit wie möglich zwischen den Ausgaben freigeben


+++

### GRÖSSENOPTIMIERUNGEN FÜR EINGEBETTETE BITMAPS

Bei [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md) ist die [Ausgabegröße](../../compositing-graphs/output-size/output-size.md) standardmäßig auf [&#39;Absolut&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) festgelegt. Das bedeutet: Wenn die Bitmap über die Knotenkette mit einer Ausgabe verbunden ist, erzwingt sie, dass die endgültige Ausgabe die Größe der eingebetteten Bitmap hat.\
Für einen Knoten, der nach der Bitmap eingefügt wird, wird die Ausgabegröße auf &quot;[&#39;Relativ zur Eingabe&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)&quot; festgelegt. Dies bedeutet, dass der Knoten auch die Größe der Bitmap besitzt und diese Größe in der Knotenkette bis zu den Ausgaben hinunter trägt. Um dies zu korrigieren, müssen Sie den Knoten nach der Bitmap so festlegen, dass seine Ausgabegröße auf [&#39;Relativ zu übergeordnetem&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) festgelegt wird.

Wenn das Diagramm auf eine dynamische Auflösung eingestellt ist, können Sie die Ausgabegröße für die eingebettete Bitmap in &quot;Relativ zu übergeordnetem Element&quot; ändern.\
Auf diese Weise ändert sich die Bitmapgröße basierend auf dem übergeordneten Diagramm. Sie werden nicht in eine Situation kommen, in der das Diagramm eine höhere Auflösung in der Bitmap verarbeitet, als dies erforderlich ist.

>[!WARNING]
>
> Durch Festlegen eines Knotens vom Typ [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) auf &quot;Relativ zum übergeordneten Knoten&quot; und [Veröffentlichen](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) des Diagramms in einem Substance 3D-Asset (SBSAR) wird die Bitmap mit einer Auflösung von **256x256** anstelle ihrer Originalgröße gespeichert. Es wird empfohlen, stattdessen die [Vererbungsmethode](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) der Bitmapknoten &quot;[Ausgabegröße](../../compositing-graphs/output-size/output-size.md)&quot; als &quot;Absolut&quot; zu behalten und einen [Transformations 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)-Knoten auf &quot;Relativ zum übergeordneten Knoten&quot; direkt nach dem Bitmapknoten festzulegen.

![Eingebettete Bitmapoptimierung 1](../../assets/input-1.jpg "Eingebettete Bitmapoptimierung 1")

![Eingebettete Bitmapoptimierung 2](../../assets/relativetoparent.jpg "Eingebettete Bitmapoptimierung 2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Außerdem wird empfohlen, das Format von Bitmap-Ressourcen auf JPEG festzulegen, um die Größe von [veröffentlichten](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) Substance 3D Assets (SBSAR) zu minimieren.

</td>
<td style="border: 0;" valign="top">

![Eingebettete Bitmapoptimierung 3](../../assets/format.jpg "Eingebettete Bitmapoptimierung 3")

</td>
</tr>
</table>

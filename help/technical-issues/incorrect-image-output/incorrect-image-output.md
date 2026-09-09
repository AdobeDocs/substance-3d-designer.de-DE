---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/technical-issues/incorrect-image-output.html"
breadcrumb-title: ''
description: Beheben Sie Fehler bei der Bildausgabe in Substance 3D Designer und erfahren Sie, wie Sie Rendering-Probleme beheben können.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Incorrect image output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Falsche Bildausgabe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---


# Falsche Bildausgabe

Auf dieser Seite werden technische Probleme in Substance 3D Designer aufgelistet, die zu einer fehlerhaften Bildausgabe führen, und für jeden Fehler werden entsprechende Schritte zur Fehlerbehebung angezeigt.

## Sichtbares Stepping/Banding

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(Fehler)](../../assets/error.svg) Problem**

Farbverläufe in der Bildausgabe werden gestuft anstelle von &quot;Glatt&quot; dargestellt. Der Schritt wird dadurch verursacht, dass der vom Bild verwendete Wertebereich *zu eng ist*.\
Das bedeutet, dass nicht genügend Werte für einen fließenden Übergang von einem Schritt eines Verlaufs zum nächsten vorhanden sind.

Luminanz-/RGBA-Werte können mit Ganzzahlen oder Gleitkommawerten codiert werden, was sich auf ihre *Genauigkeit* auswirkt:

* **Integer** bietet 8-Bit-Genauigkeit (0-255, also 256 mögliche Werte) und 16-Bit-Genauigkeit (0-65535 so 65536 mögliche Werte), um einen Wert im Bereich von 0-1 zu speichern.
* **Gleitkomma** bietet eine Präzision von 16 Bit (HDR 16F) und 32 Bit (HDR 32F), wobei Werte außerhalb des Bereichs von 0 bis 1 gespeichert werden können, einschließlich negativer Werte. So kannst du mit High Dynamic Range-Bildern (HDR) arbeiten, bei denen der Luminanzwert weit über 1,0 liegen kann.

Wenn Sie nicht speziell mit HDR-Bildern arbeiten müssen, geben die meisten Ihrer Knoten wahrscheinlich Werte im Bereich von 0-1 aus, die mit Ganzzahlen codiert sind. Wenn das Ausgabeformat des Bildes 8 Bit ist, kann das Bild nur 256 Werte verwenden, was häufig zu sichtbaren Schritten bei Farbverläufen führt. Dies kann sich besonders auf die Ausgabe von Normal-Knoten auswirken.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/demo-stepping-8-bit.png){width="256px"}![](../../assets/demo-stepping-8-bit-2.png){width="256px"}![](../../assets/demo-stepping-8-bit-3.png){width="256px"}

</td>
</tr>
</table>

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Überprüfen Sie das **Ausgabeformat** (d. h. die Bittiefe) des Knotens und aller Knoten im Upstream, und stellen Sie sicher, dass dieser Knoten *mit einer Integer-Genauigkeit von mindestens 16 Bit verwendet*.

Der Ausgabeformatparameter ist häufig auf die *Relativ zur Eingabe* [Vererbungsmethode](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) festgelegt, die die niedrige Genauigkeit im gesamten Diagramm propagieren kann. Im Idealfall finden Sie die Ursache des Problems, indem Sie im Diagramm stromaufwärts gehen.

Sie können die Genauigkeit der Ausgabe eines Knotens schnell identifizieren, indem Sie sich die Textinformationen ansehen, die unter dem Knoten angezeigt werden:

* **L/C** bezieht sich auf das Bild, das Graustufen (d. h. Luminanz) oder Farbe ist
* **8/16** bedeutet Ganzzahlcodierung
* **16F/32F** bedeutet Gleitkommakodierung

Beispiel:

* L8: 8-Bit-Ganzzahl in Graustufen
* C16: 16-Bit-Ganzzahl für Farbe
* C32F: Farbe 32-Bit-Gleitkomma (HDR.)

## Qualitätsverlust in der veröffentlichten SBSAR

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

<b>![(Fehler)](../../assets/error.svg) Problem </b>

Die Qualität der von einem Substance 3D-Archiv (SBSAR) ausgegebenen Bilder ist deutlich niedriger als der Graf der Substance 3D-Datei, aus der sie veröffentlicht wird (siehe Abbildung rechts).\
Die Ausgabe erscheint in niedriger Auflösung.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/issues-sbsar-bitmap-relative-to.jpg){width="256px"}

</td>
</tr>
</table>

<b>![(tick)](../../assets/check.svg) Empfohlene Schritte</b>

Stellen Sie sicher, dass die Eigenschaft [Ausgabegröße](../../compositing-graphs/output-size/output-size.md) aller [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)-Knoten auf die *Absolute* [Vererbungsmethode](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) festgelegt ist.

Ist dies nicht der Fall, wird die referenzierte [Bitmapressource](../../resources/bitmap-resource/bitmap-resource.md) mit der Standardauflösung 256\*256 im veröffentlichten Substance 3D-Archiv gespeichert, was sich* auf die Qualität* einer oder mehrerer Ausgaben auswirkt.

## Bild ist verschwommen

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(Fehler)](../../assets/error.svg) Problem**

Formen werden nach Verwendung einiger Knoten leicht unscharf dargestellt, z. B. [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) oder [Überblendung](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md).

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/issues-bilinear.jpg){width="256px"}

</td>
</tr>
</table>

**![(tick)](../../assets/check.svg) Empfohlene Schritte**

Wenn Sie Pixel in einem Bild neu anordnen, z. B. wenn Sie die Größe einer Form ändern oder die Auflösung eines Bildes ändern, gibt es zwei Möglichkeiten zu bestimmen, wie Pixel aus der Quelle *dem Ziel zugeordnet werden sollen*:

* **Nächste**: Das Pixel wird dem Ziel &quot;*wie besehen*&quot; an der entsprechenden Koordinate zugeordnet. Wenn das Ziel eine niedrigere Auflösung hat, kann das Pixel vollständig ignoriert werden. wenn das Ziel eine höhere Auflösung hat; es wird allen Pixeln zugeordnet, die seine Spanne abdecken. Die Ausgabe ist *schärfer* und sieht leicht *verzerrt* aus.
* **Bilineare Filterungen**: Eine Filterung wird auf das Quellbild angewendet, sodass seine Pixel der Zielauflösung auf eine Weise zugeordnet werden, dass *die Übergänge zwischen den Pixeln glättet*. Die Ausgabe ist *glatter* und sieht leicht *unscharf* aus.

Der Knoten [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) stellt eine **Filterung-Methode** bereit, mit der ausgewählt werden kann, welche dieser beiden Zuordnungsmethoden verwendet werden soll.

Die meisten Knoten - z. [Überblendung](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) - Standard für *bilineare Filterung*, wenn eine Eingabeauflösung mit einer anderen Textur gesampelt wird, was zu einer unerwünschten Unschärfe führen kann.\
Da der 2D-Transformationsknoten *atomar* - also sehr leicht - ist, kann er *verwendet werden, selbst wenn keine Transformationen erforderlich sind*, um eine Textur mithilfe der Eigenschaft [Ausgabegröße](../../compositing-graphs/output-size/output-size.md) zu ändern, bevor die Textur an einen anderen Knoten gesendet wird. Sie können daher *die Auswirkungen* dieser Größenänderung steuern.

Im [Funktions-Graf](../../function-graphs/function-graphs.md) des [Pixelprozessor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)-Knotens enthalten die **Sample**-Knoten die *gleiche Option*, um zu steuern, wie die aufgenommene Textur der Knotenauflösung zugeordnet werden soll.

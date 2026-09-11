---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie die Dateigröße von Substance-Grafen reduzieren können, um Performance- und Speicheranforderungen zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtlinien zur Dateigrößenreduzierung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# Überblick

In einigen Fällen kann die Gesamtdateigröße von [Substance 3D Assets (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) ein wichtiger Faktor sein. Auf dieser Seite werden einige wichtige Bereiche und Einstellungen beschrieben, die Sie beim Verringern der Dateigröße berücksichtigen sollten.

Die Dateigröße wird hauptsächlich durch [eingebettete Bitmaps bestimmt.](../../resources/bitmap-resource/bitmap-resource.md) Es handelt sich um Dateien, die verknüpft, eingebettet oder Baking geführt und der Datei &quot;[Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html)&quot; (SBS) als Ressource hinzugefügt wurden. Nur Bitmaps, die in einem Graf verwendet werden, d. h. entweder direkt oder über die Knotenkette mit einer Ausgabe verbunden sind, werden im Substance 3D-Element veröffentlicht. In einer Substance 3D-Datei haben Bitmaps keine Auswirkungen auf die Dateigröße, da alle Bitmapressourcen immer noch außerhalb der Datei gespeichert werden.

>[!IMPORTANT]
>
> Stellen Sie sicher, dass die Eigenschaft [Ausgabegröße](../../compositing-graphs/output-size/output-size.md) aller [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)-Knoten auf die *Absolute* [Vererbungsmethode](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) festgelegt ist. Ist dies nicht der Fall, wird die referenzierte [Bitmapressource](../../resources/bitmap-resource/bitmap-resource.md) in der veröffentlichten Substance 3D-Asset-Datei mit der Standardauflösung von 256\*256 gespeichert, was sich* auf die Qualität * einer oder mehrerer Ausgaben auswirkt.

## Dateigrößenfaktoren

Es gibt einige verschiedene Faktoren, die die Gesamtdateigröße der SBSAR beeinflussen. Sie sind unten mit einer kurzen Erläuterung aufgelistet.

+++Auflösung
Offensichtlich hat eine große Wirkung. Verwenden Sie die kleinstmögliche Auflösung, da Sie möglicherweise auch möchten, dass Ihre Substance-Datei in großen Auflösungen funktioniert. Sie können standardmäßige Tricks zum Maskieren der Auflösung verwenden, um kleinere Bitmaps größer erscheinen zu lassen.

*Gefunden in: externe Software oder Importieren/Wiederexportieren von Bitmaps in Designer.*

+++

+++Dateifarbmodus
Der Farbmodus, der vor dem Export im Bildeditor eingestellt wurde, hat auch bei Verwendung des Raw-Bitmap-Formats Auswirkungen auf die Dateigröße. Nur Graustufenbitmaps sind kleiner als RGB(A)-Bilder.

*Gefunden in: externe Software oder importieren/exportieren Sie Bitmaps in Designer, während Sie [Ausgabeknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) richtig einrichten.*

+++

+++Dateiformat
Das Dateiformat Ihrer Bilder macht einen Unterschied, kann aber in manchen Fällen ignoriert werden. Ein Programm wie Photoshop ermöglicht etwas mehr Kontrolle über JPG Komprimierung und kann manchmal einen guten Mittelweg bieten.

*Gefunden in: externe Software oder Importieren/Wiederexportieren von Bitmaps in Designer.*

+++

+++Verwendung in der Graf
Welcher Modus für den Bitmap-Knoten festgelegt wird, hat ebenfalls Auswirkungen darauf, wie Designer die Datei komprimiert. Wenn Sie eine Graustufenmodusdatei als Farbbitmap im Diagramm verwenden, werden größere Dateien erzeugt. Achten Sie darauf, diese richtig einzustellen!

*Gefunden in:[Eigenschaften des Bitmapknotens.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++Bitmapformat im Paket
In den Ressourceneigenschaften können Sie zwischen der Raw- und JPEG-Komprimierung wählen. Dies kann erhebliche Auswirkungen auf das Endergebnis haben.

*Gefunden in: Bitmapressourceneigenschaften über das Explorer-Fenster.*

+++

+++Bitmapkomprimierungsqualität im Paket
Wenn Sie das &quot;JPEG&quot;-Bitmapformat verwenden, kann der unten stehende Schieberegler die Qualität und Dateigröße beeinflussen. Dieser Schieberegler verhält sich nicht sehr vorhersehbar, aber 1 entspricht in der Regel der höchsten Qualität JPG-Komprimierung, und 0,5 gibt in der Regel die kleinste Größe an.

*Gefunden in: Bitmapressourceneigenschaften über das Explorer-Fenster.*

+++

+++Komprimierungsmodus beim Veröffentlichen
Beim Veröffentlichen in SBSAR haben Sie die Wahl zwischen &quot;Auto&quot;, &quot;Best&quot; und &quot;None&quot; zum Komprimieren. Diese können einen erheblichen Unterschied machen, wenn Sie das Bitmapformat &quot;Raw&quot; verwenden. Hat auch einen großen Einfluss auf die Exportgeschwindigkeit. Im Allgemeinen nicht empfohlen, &quot;keine&quot; zu verwenden, da es keine Qualitätssteigerung bietet.

*Gefunden in: endgültige Veröffentlichungseinstellungen für ein SBSAR-Paket.*

+++

## Dateigrößenvergleich

Die folgende Tabelle zeigt den Einfluss aller Einstellungen aufeinander. Die verwendete Bitmap ist ein Bild mit einer Auflösung von 4096 x 4096 Pixel, das aus Photoshop als 24-Bit-TGA oder JPG mit Qualität 8 exportiert wird. TGAs wurden auch als Graustufen- und RGBA-Modus exportiert.

Der Graf platziert lediglich einen einzelnen Bitmapknoten, der mit einem einzelnen Ausgang verbunden ist. Der Bitmapmodus wird entsprechend dem Quelldateimodus festgelegt.

Die Tabelle auf der rechten Seite ist zwar nicht ganz eindeutig, aber beim Vergleich von visuellen Ergebnissen und Dateigrößen kann Folgendes gelernt werden:

* Raw Bitmap + Komprimierung Am besten erhalten Sie die beste Qualität mit einer akzeptablen Dateigröße.
* Vorkomprimierte Quelldateien können in den meisten Fällen zu reduzierten Dateigrößen führen, allerdings zu geringeren Qualitätskosten.
* Kleinste Dateigrößen, aber ungünstigste Qualität wird mit JPG Paketformat bei Qualität 0.5 erzielt.
* Graustufen sind nicht immer kleiner in der Dateigröße, haben aber bei ähnlichen Einstellungen eine höhere Qualität als Farben.

>[!NOTE]
>
> **JPEG-Bitmapformat**
> 
> Es ist wichtig zu beachten, dass Spezialkarten, die eine hohe Genauigkeit erfordern, wie Normalen-Map, Vektorkarten und andere, wahrscheinlich nicht auf JPEG-Komprimierung eingestellt werden sollten, da dies zu viel sichtbareren Artefakten führen wird!

| Quellbild | Farb-TGA | JPG | Graustufen-TGA | JPG |
| --- | --- | --- | --- | --- |
| <b>Raw Bitmap Format</b>-Komprimierungsmodus: *Keine* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>Raw Bitmap Format</b>-Komprimierungsmodus: *Beste* | 9,11 MB | 3,37 MB | 5,06 MB | 4,75 MB |
| <b>JPEG-Bitmapformat</b> Komprimierungsqualität: *1* | 5,09 MB | 1,94 MB | 6,30 MB | 2,49 MB |
| <b>JPEG-Bitmapformat</b> Komprimierungsqualität: *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>JPEG-Bitmapformat</b> Komprimierungsqualität: *0* | 407 KB | 433 KB | 990 KB | 808 KB |

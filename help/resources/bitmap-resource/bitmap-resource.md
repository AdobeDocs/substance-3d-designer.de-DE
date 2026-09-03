---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Erfahre, wie du in Substance 3D Designer Bitmap-Ressourcen importieren, erstellen und verwenden kannst, um auf Texturen basierende Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# Bitmaps

Eine Bitmapressource ist eine Ressource in einem Substance-Paket. Er unterscheidet sich vom [-atomaren Bitmapknoten. Der atomare Bitmapknoten &quot;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)&quot; ist eine bestimmte Darstellung dieser Bitmap in [einem Substance-Diagramm &#x200B;](../../compositing-graphs/substance-compositing-graphs.md).

Bitmaps gehören zu den häufigsten Ressourcen außerhalb des Diagrammbereichs in Substance 3D Designer. Ihre Verwendung fällt in der Regel in eine der folgenden Kategorien:

* Eine durch Baking erzeugte Map, entweder [, intern durch Designer](../../bakers/bakers.md) oder extern durch eine andere Anwendung.
* Eine Hilfsstruktur, wie ein Muster, eine Schmutz-Map oder ein Decal.
* Eine einfache Graustufenmaske zum Mischen, die entweder intern mit [dem Bitmapknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) oder mit einer externen Anwendung erstellt wurde.

## Bitmapspeicher

Bitmaps sind in der Regel die größte Ressource, mit der sich Designer beschäftigt. Deshalb ist es gut zu verstehen, wie Designer diese Dateien mit seinen zwei Hauptdateitypen behandelt.

### In Substance 3D-Dateien (SBS)

Wie Bitmaps in SBS gespeichert werden, hängt davon ab, ob Sie sie verknüpfen oder importieren. Stellen Sie sicher, dass Sie mit dem Konzept vertraut sind.[&#128279;](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) Importierte Bitmaps können mit den [Bitmap-Malwerkzeugen](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) bearbeitet werden.

Im Gegensatz zu Ressourcen für das SVG (Vektorgrafiken) werden Bitmaps immer extern gespeichert, selbst wenn sie als neue Ressource erstellt oder importiert werden. Bei neuen Substance-Paketen werden sie im Speicher gespeichert, bis die .SBS-Datei auf der Festplatte gespeichert wird. Nach dem Speichern auf dem Datenträger werden Bitmaps in einem Ordner &quot;*/resources*&quot; neben der SBS-Datei gespeichert.

### In Substance 3D Assets (SBSAR)

In [SBSAR-Dateien](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) sind Bitmaps eingebettet, was bedeutet, dass sie sich stark auf die endgültige SBSAR-Dateigröße auswirken. Weitere Informationen zu den Auswirkungen auf die Dateigröße finden Sie auf dieser Seite. Wenn SBSAR-Dateien veröffentlicht werden, werden nur Bitmaps eingebettet, die zur Berechnung der Ausgabe eines Diagramms verwendet werden. Nicht verwendete Bitmaps werden optimiert und aus dem endgültigen SBSAR-Paket ausgeschlossen, ohne dass sich dies auf die Dateigröße auswirkt.

## Dateityp, Farbmodus und Auflösung

Substance 3D Designer kann Daten aus Bitmaps problemlos bearbeiten und neu anordnen. Beachten Sie jedoch Folgendes:

* Stellen Sie Ihre Auflösungen auf 2-kompatibel ein, d. h. befolgen Sie die standardmäßige Echtzeit-Texturgröße wie <b>256, 512, 1024, 2048,</b> usw. Designer skaliert Texturen außerhalb dieses Bereichs auf die nächste passende Auflösung. Beachten Sie, dass sie nicht quadratisch sein müssen.
* Viele Dateitypen werden unterstützt, aber wählen Sie einen aus, der am besten für Ihre Anwendung geeignet ist. <b>Verlustfreie Komprimierung oder sogar unkomprimierte </b>-Dateitypen wie PNG oder TGA bieten eine bessere Qualität als JPG oder DDS.
* Stellen Sie sicher, dass <b> Ihren Farbmodus richtig einrichtet</b>, je nachdem, ob Sie Farbe, Graustufen oder einen Alphakanal benötigen.

## Bitmap-Attribute

Bitmap-Ressourcen in einem Paket verfügen über eine Reihe von Attributen, die Sie anpassen können. Die meisten Attribute haben keinen Hauptzweck und sind für Bibliotheksfilter vorgesehen, obwohl eine Minderheit die Dateigröße beeinflusst.

| Attributname | Zweck |
| --- | --- |
| Kennung | Wird zum Verweisen auf die Bitmapressource in einem Paket verwendet, muss eindeutig sein. |
| Dateipfad | Der Pfad der Bitmap, auf die die Ressource verweist, auf dem Datenträger. |
| Beschreibung | Die Beschreibung, die in den Tooltips [Explorer](../../interface/the-explorer-window/the-explorer-window.md) und [Bibliothek](../../interface/the-library/the-library.md) für diese Ressource angezeigt wird. |
| Kategorie | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Label | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Autor | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Autoren-URL | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Tags | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Benutzerdaten | Optionale zusätzliche Daten, nicht für Bitmaps verwendet. |
| In Bibliothek anzeigen | Bestimmt, ob die Bitmap in [der Bibliotheksansicht ausgeblendet werden soll.](../../interface/the-library/the-library.md) |
| Bitmapformat | Raw oder Jpeg hat einen großen Einfluss auf die SBSAR-Dateigröße. Weitere Informationen finden Sie in unseren [Richtlinien zur Dateigrößenreduzierung](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md). |
| Bitmapkomprimierungsqualität | Hat nur Auswirkungen auf die JPEG-Komprimierung und bestimmt die Balance zwischen Qualität und Dateigröße. |

## Dateigrößenreduzierung

Auf der Seite [Richtlinien zur Dateigrößenreduzierung](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) im Abschnitt [Best Practices](../../best-practices/best-practices.md) finden Sie unsere Empfehlungen zum Minimieren der Dateigröße von Bitmaps, die in [veröffentlichte Substance 3D Assets (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) eingebettet sind.

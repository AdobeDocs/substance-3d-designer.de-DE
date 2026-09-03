---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: Importiere und verwende SVG-Vektorgrafiken als Ressourcen in Substance 3D Designer für die prozedurale Materialerstellung.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vektorgrafiken (SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# Vektorgrafiken (SVG)

Substance 3D Designer unterstützt über das Scalable Vector-Grafikformat nur eine äußerst begrenzte Form von Vektorgrafiken. SVG-Dateien können auf unterschiedliche Weise als Ressourcen eingefügt und als Ressourcen für Ihre Grafiken verwendet werden.

SVG-Dateien [&#x200B; können über den atomaren SVG-Knoten erstellt oder bearbeitet werden.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) Sie können auch von [dem UV-to-SVG-Bäcker erstellt werden.](https://experienceleague.adobe.com/de/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)

>[!NOTE]
>
> Adobe Illustrator-Dateien (**.ai**) werden derzeit *nicht* unterstützt.

## SVG-Speicher

Der SVG-Speicher hängt davon ab, ob sie verknüpft oder importiert sind. Importierte SVG-Dateien sind in die SBS-Datei eingebettet, sodass [keine externen Dateien wie Bitmaps](../../resources/bitmap-resource/bitmap-resource.md) erforderlich sind, und können mit den [Vektorbearbeitungswerkzeugen](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) bearbeitet werden.

## SVG-Attribute

SVG-Ressourcen in einem Paket verfügen über eine Reihe von Attributen, die Sie anpassen können. Die meisten Attribute dienen nicht hauptsächlich der Bibliotheksfilterung, aber eine Minderheit beeinflusst die Rendering-Qualität.

| Attributname | Zweck |
| --- | --- |
| Kennung | Wird zum Verweisen auf die SVG-Ressource in einem Paket verwendet und muss eindeutig sein. |
| Dateipfad | Der Pfad der SVG-Datei auf der Festplatte, auf die die Ressource verweist. |
| Beschreibung | Die Beschreibung, die in den Tooltips [Explorer](../../interface/the-explorer-window/the-explorer-window.md) und [Bibliothek](../../interface/the-library/the-library.md) für diese Ressource angezeigt wird. |
| Kategorie | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Label | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Autor | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Autoren-URL | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Tags | Wird zum [Sortieren und Kuratieren der Ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) in der [Bibliothek](../../interface/the-library/the-library.md) verwendet. |
| Benutzerdaten | Optionale zusätzliche Daten, nicht für Vektorgrafiken verwendet. |
| In Bibliothek anzeigen | Bestimmt, ob die SVG-Ressource in [&#x200B; der Bibliotheksansicht ausgeblendet werden soll.](../../interface/the-library/the-library.md) |
| Vektorgrafikqualität | Beeinträchtigt die Rendering-Qualität. Der Bereich ist nicht linear und die beste Qualität wird bei 0,5 erreicht. |

## SVG-Authoring

Da nur eine begrenzte Anzahl von Funktionen unterstützt wird, ist das Authoring-SVG eingeschränkt.

Im Allgemeinen gilt Folgendes:

* Nur einfache Grundformen und Pfade werden garantiert richtig gezeichnet.
* &quot;Kontur&quot; wird unterstützt, führt jedoch nur zu einer Kontur mit einer Breite von 1 Pixel, und die Konturformatierung wird ignoriert.
* Gestrichelte Linienstile werden definitiv umbrochen.
* Text muss in Pfade/Konturen konvertiert werden, um gerendert zu werden.
* [Zusammengesetzte Pfade](https://helpx.adobe.com/ie/illustrator/desktop/manage-objects/reshape-transform-objects/create-compound-paths.html) werden nicht unterstützt.
* Erweiterte Funktionen wie Verläufe werden nicht unterstützt.
* Stilelemente für CSS-Eigenschaften werden nicht unterstützt.

## Empfohlene Exportoptionen

Die Exportoptionen unterscheiden sich leicht von der jeweiligen Anwendung:

### Adobe Illustrator

[Illustrator](https://www.adobe.com/de/products/illustrator.html) bietet die größte Kontrolle über Ihre SVG-Exporte, wenn Sie auf die folgenden Optionen achten.

* Nur <b>Speichern unter</b>, *nicht* Exportieren als! verwenden
* <b>SVG Profile</b> spielt keine große Rolle, obwohl das Winzige Profil (meistens) standardmäßig auf Einstellungen zurückgesetzt wird, die definitiv korrekt sind.
* <b>Schriftarten</b> müssen auf <b>In Kontur konvertieren</b> festgelegt sein, damit sie funktionieren.
* <b>CSS-Eigenschaften</b> sollten *nicht* auf &quot;Stilelemente&quot; festgelegt sein. Alle anderen Optionen funktionieren.
* Deaktivieren Sie <b>Illustrator-Bearbeitungsfunktionen beibehalten</b>;
* Deaktivieren Sie <b>Responsive</b>;
* Konturen funktionieren nicht gut. Verwenden Sie <b>Objekt > Pfad > Konturlinie</b>, damit sie angezeigt werden.

Das Bild auf der rechten Seite zeigt die empfohlenen Exportoptionen. Klicken Sie darauf, um es in voller Größe anzuzeigen.

>[!IMPORTANT]
>
> Zeichenflächen können das Ergebnis der generierten SVG-Datei beeinflussen. Einige Illustrator-Dateivorlagen enthalten mehrere Zeichenflächen.\
> Versuchen Sie, nur eine richtig zugeschnittene Zeichenfläche zu haben und diese beim Speichern als SVG im Zeichenflächenfenster auswählen zu lassen.

![Exportoptionen für Illustrator-SVG](vector-graphics-svg-resource.resources/vector-graphics-svg-resource-01.jpg "Exportoptionen für Illustrator-SVG"){width="512px"}

### Inkscape

Inkscape speichert nativ als SVG, hat jedoch weniger Kontrolle über das Dateiformat. Inkscape-Dateien funktionieren meist nativ in der Anwendung, jedoch mit einigen Einschränkungen:

* Striche werden in Substance 3D Designer nur als 1 px breit angezeigt. Verwenden Sie <b>Pfad > Kontur zu Pfad</b>, um sie zum Arbeiten zu bringen.
* Text funktioniert nicht. Verwenden Sie <b>Pfad > Objekt zu Pfad</b>, um Text zu bearbeiten.

### Adobe Photoshop

Photoshop hat einen sehr eingeschränkten SVG-Exporteur (<b>Datei > Exportieren > Exportieren als...</b>) die derzeit keine korrekten Ergebnisse für Substance 3D Designer erzielen kann. Sie können Ihre Form- und Pfadinformationen abrufen, aber Stil wird immer als Elemente gespeichert, was inkompatibel ist.

Es kann für einfache Schwarzweiß-Formmasken verwendet werden, bei denen eine Lösung darin besteht, das Alpha mithilfe von [Alpha Split](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md) aus der SVG zu extrahieren.

Alternativ kann eine von Photoshop exportierte SVG [Importiert](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) sein, sodass Sie die Stilinformationen anschließend [nativ in der Anwendung bearbeiten können.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

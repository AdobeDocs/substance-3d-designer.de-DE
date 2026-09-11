---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Erfahre, wie du Compositing-Substance als PSD-Dateien exportieren kannst, um sie in Adobe Photoshop und anderen Workflows für die Bildbearbeitung zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportieren von PSD-Dateien
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# Exportieren von PSD-Dateien

Mit Substance 3D Designer können Texturen in ein Adobe Photoshop-Dokument oder eine PSD-Datei exportiert werden.Auf dieser Seite wird die spezielle Benutzeroberfläche erläutert, mit der die Knoten eines Diagramms in Ebenen übersetzt werden.**Dieser Prozess ist nicht automatisch: Sie haben viel Kontrolle, aber es ist begrenzt und oft nicht möglich, eine genaue Übereinstimmung zwischen Knoten und Ebenen zu erzielen.** Darüber hinaus gibt es keine Garantie, dass Ihre PSD die gleichen Ausgaben wie Ihr Diagramm enthält, es sei denn, Sie haben es explizit dafür eingerichtet. Je genauer und korrekter Sie sein möchten, desto mehr Aufwand ist im Allgemeinen vom Benutzer erforderlich. Im Allgemeinen ist der einzige Aspekt, der auf zerstörungsfreie Weise eng repliziert werden kann, [Überblendknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Einstellungsebenen werden nicht unterstützt und Ebenenstile oder andere Dinge, die über die Ebenen-Mischmodi hinausgehen, werden nicht unterstützt.

[Substance 3D Designer kann auch als Bitmapdateien exportiert werden.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## PSD-Exportdialog

Das Dialogfeld &quot;PSD-Export&quot; kann nur mit einem einzigen Verfahren geöffnet werden. Klicken Sie in der [Diagrammansicht](../../interface/the-graph-view/the-graph-view.md) des Diagramms, das Sie auf die PSD exportieren möchten, auf die Schaltfläche ![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>Tools</b> und wählen Sie <b>PSD Exporter</b> aus. Die Schnittstelle wird in der <b>Diagrammansicht</b> sichtbar.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![PSD Exporter-Benutzeroberfläche](exporting-psd-files.resources/psd-dialog.png "PSD Exporter-Benutzeroberfläche")

</td>
<td style="border: 0;" valign="top">

1. <b>Dateiname und Speicherort:</b> Richten Sie den Ordner und den Dateinamen für den Export hier ein. Klicken Sie auf die Schaltfläche Exportieren , um den Exportvorgang auszuführen.
1. <b>Gruppe hinzufügen:</b> Fügt eine Ebenengruppe hinzu.
1. <b>Dropdownliste &quot;Ebene hinzufügen&quot;:</b> Wählen Sie eine von zwei Methoden zum Hinzufügen einer Ebene aus. Ebenen können auch hinzugefügt werden, indem *Knoten mit der rechten Maustaste* in den Stapel gezogen werden.
1. <b>Dropdown-Liste &quot;Ebene entfernen&quot;:</b> Entfernen Sie entweder die ausgewählten oder alle Ebenen.
1. <b>Layerstack:</b> die meisten Einrichtungsarbeiten, wenn sie hier ausgeführt werden. Benutzeroberfläche spiegelt begrenzte Optionen in Photoshop. Richten Sie hier den Ebenennamen, den Mischmodus und die Deckkraft ein. Wenn eine Ebene zwei Miniaturansichten hat, stellt die zweite Miniaturansicht den Alpha-Kanal dar.

</td>
</tr>
</table>

## Workflow

Da Photoshop Multi-Output-Materialien nicht direkt unterstützt, gibt es mehrere Möglichkeiten, Ihren PSD einzurichten. Im Folgenden finden Sie eine Übersicht über die am häufigsten verwendeten Methoden.

* Richten Sie eine Reihe von Ordnern für alle Ihre Ausgaben ein. Ein Ordner für &quot;Grundfarbe&quot;, ein Ordner für &quot;Normal&quot;, ein Ordner für &quot;Raueit&quot; usw.
* Ziehen Sie Ihre Ausgaben mit der rechten Maustaste und legen Sie sie in der entsprechenden Gruppe ab. Wenn Sie die Dinge einfach halten wollen, kann die PSD nur an dieser Stelle belassen werden.
* So erweitern Sie die PSD: Arbeite dich zurück links vom Diagramm, indem du die relevanten Schritte zwischen den Schritten deines Diagramms in der entsprechenden Gruppe ablegst. Es ist nicht möglich, Ebenen zwischen Ausgaben/Gruppen zu teilen.

In den seltenen Fällen, in denen Ihr PSD die wichtigere Ausgabe ist, können Sie Ihr Diagramm so erstellen, dass Sie nur Füllmethoden verwenden. In diesem Fall sollte es möglich sein, eine editierbarere Version Ihres Diagramms als Dokument mit Ebenen neu zu erstellen.

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: Lerne, wie du Texturen und Bitmaps aus Substance-Compositing-Graphen exportieren kannst, um sie in anderen Programmen und Workflows zu verwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportieren von Bitmaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Exportieren von Bitmaps

Auf dieser Seite wird erläutert, wie Substance 3D Designer in viele verschiedene Bitmap-Dateiformate exportieren kann und wie mehrere UV-Kacheln stapelweise exportiert werden.Wenn Sie [&#x200B; in PSD-Dateien &#x200B;](../exporting-psd-files/exporting-psd-files.md) exportieren möchten, gibt es eine separate dedizierte Seite dafür.

![Exportieren vereinfacht](exporting-bitmaps.resources/exporting-bitmaps-01.png "Exportieren vereinfacht")

## Exportieren von Konzepten

Beachten Sie beim Exportieren einer Bitmap Folgendes:

* Sie <b> exportieren aus einem Diagramm </b>, nicht aus einem Paket. Ein Paket generiert keinen Bildinhalt für sich.
* Die Anzahl (und Auflösung) der exportierten Bitmaps wird durch die <b>Ausgaben</b> eines Diagramms bestimmt.
* Filetype ist für alle Ausgaben/Bitmaps festgelegt.
* Das Exportieren unterscheidet sich von [Veröffentlichen](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md). Vergewissern Sie sich, dass Sie den Unterschied gut verstehen!

## Exportmethoden

Sobald Sie zum Exportieren bereit sind, gibt es zwei Möglichkeiten, auf das Dialogfeld &quot;Exportieren&quot; zuzugreifen:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Klicken Sie im Fenster [Explorer](../../interface/the-explorer-window/the-explorer-window.md) mit der rechten Maustaste auf das zu exportierende Diagramm, und wählen Sie **&quot;Ausgaben als Bitmaps exportieren&quot;** aus.

![](exporting-bitmaps.resources/exporting-bitmaps-02.gif)

</td>
<td style="border: 0;" valign="top">

Klicken Sie in der [Diagrammansicht](../../interface/the-graph-view/the-graph-view.md) auf die Schaltfläche &quot;Extras&quot; ![](exporting-bitmaps.resources/exporting-bitmaps-03.png) und wählen Sie **&quot;Ausgaben exportieren...&quot;**.

![](exporting-bitmaps.resources/exporting-bitmaps-04.gif)

</td>
</tr>
</table>

## Exportdialogfeld

Im Dialogfeld &quot;Exportieren&quot; finden Sie einige Optionen zum Anpassen des Exports.

Die auf der rechten Seite angezeigte Version ist das Standarddialogfeld. Die Änderung der Auflösung erfolgt entweder im Diagramm, in den Ausgaben oder durch Festlegen der übergeordneten Auflösung vor dem Öffnen des Dialogfelds.

1. <b>Ziel: </b>Speicherort für alle zu speichernden Dateien.
1. <b>Format:</b> Dateityp wird für alle exportierten Dateien verwendet.
1. <b>Muster</b>: generische Methode zum Generieren von Dateitypen basierend auf Metadaten-Schlüsselwörtern. Ein Beispieldateiname, der auf der ersten Ausgabe basiert, wird unten zur Überprüfung angezeigt.\
   Im Folgenden sind alle verfügbaren Optionen aufgeführt:
   1. *$(Diagramm)* - Name des aktuellen Diagramms
   1. *$(Identifizierung)* - Identifizierung der aktuellen Ausgabe
   1. *$(description)* - Beschreibung der aktuellen Ausgabe
   1. *$(label)* - Bezeichnung der aktuellen Ausgabe
   1. *$(user\_data)* - benutzerdefinierte Benutzerdaten der aktuellen Ausgabe
   1. *$(group)* - Ausgabegruppe der aktuellen Ausgabe
   1. *$(colorspace)* - Farbraum der aktuellen Ausgabe (nur verfügbar für *OCIO* und *Adobe ACE* [Farbmanagement](../../color-management/color-management.md))
1. <b>Ausgaben:</b> Aktivieren oder deaktivieren Sie bestimmte Ausgaben und Ausgabegruppen auf Ihrem Graf. Schaltflächen können alle aktiviert oder deaktiviert werden. Nützlich, wenn nur eine Bitmap geändert wurde.
1. <b>Automatischer Export:</b> Schaltfläche zum Umschalten, um den automatischen erneuten Export von Diagrammausgaben zu aktivieren, sobald eine Änderung vorgenommen wird. Nur für aktuelles Diagramm. Kann je nach Einstellung schwer und langsam sein.
1. <b>Schaltfläche &quot;Exportieren&quot;:</b> Exportiert mit den aktuellen Einstellungen oder schließt das Dialogfeld.

![Dialogfeld für Exportausgaben](exporting-bitmaps.resources/exporting-bitmaps-05.png "Dialogfeld für Exportausgaben")

## Dialogfeld &quot;Exportieren&quot; (Stapel-/UV-Kacheln)

Bei der Arbeit mit UV-Tile-Meshs in Designer kann das Exportdialogfeld etwas anders verwendet werden, sodass mehrere UV-Tiles gleichzeitig exportiert werden können. Vergewissern Sie sich, dass Sie diesen Arbeitsablauf verstehen und ein [Substance-Diagramm](../../compositing-graphs/substance-compositing-graphs.md) ordnungsgemäß einer oder mehreren UV-Kacheln zugewiesen haben.\
Die Registerkarte &quot;Stapel&quot; ist auch eine schnellere Möglichkeit, Ihren Graf mit einer anderen Auflösung als der Arbeitsauflösung (übergeordnete Auflösung) zu exportieren.

Starten Sie das Dialogfeld mit denselben Methoden wie oben beschrieben. Klicken Sie dazu im Explorer *mit der rechten Maustaste auf* auf das Diagramm, das der UV-Kachel zugewiesen ist, oder *öffnen Sie das entsprechende Diagramm, das der UV-Kachel zugewiesen ist*, in der Diagrammansicht, wenn Sie die Schaltfläche &quot;Werkzeuge&quot; verwenden.

1. <b>Registerkarte &quot;Stapel&quot;</b>: Stellen Sie sicher, dass Sie diese Registerkarte anstelle der standardmäßigen <b>From Graph </b>-Methode auswählen. Andernfalls sind die Optionen 2-3 nicht verfügbar.
1. <b>UV-Kacheln:</b> Ebenso wie bei den Ausgaben können Sie den Export bestimmter UV-Kacheln aktivieren oder deaktivieren.
1. <b>[Ausgabegröße](../../compositing-graphs/output-size/output-size.md): </b>Überschreiben Sie die Exportauflösung, sodass Sie kleiner und effizienter arbeiten können, während Sie mit maximaler Größe exportieren.

![Dialogfeld für Batch-Exportausgaben](exporting-bitmaps.resources/exporting-bitmaps-06.png "Dialogfeld für Batch-Exportausgaben")

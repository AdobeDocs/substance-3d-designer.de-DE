---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Rufen Sie das Fenster "Voreinstellungen" in Substance 3D Designer auf, um Anwendungseinstellungen und -verhalten anzupassen.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voreinstellungen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1973'
ht-degree: 1%

---


# Voreinstellungsfenster

![Fenster für Voreinstellungen](preferences-window.resources/image2021-6-22-20-56-1.png "Fenster für Voreinstellungen")

Auf dieser Seite werden das Fenster &quot;<b>Voreinstellungen</b>&quot; und alle zugehörigen Einstellungen angezeigt.

Sie finden das Fenster &quot;Voreinstellungen&quot; im Menü <b>Bearbeiten</b> in der oberen Hauptleiste der Anwendung. In diesem Dialogfeld können Sie eine Reihe von Einstellungen anpassen. Es ist in Registerkarten organisiert, die verschiedene Verhaltens- und Funktionsbereiche abdecken.\
Wir empfehlen, alle diese Einstellungen zu überprüfen, um einen besseren Einblick in die Funktionsweise der Anwendung und ihre Anpassung an Ihren Workflow zu erhalten.

>[!NOTE]
>
> Weitere Informationen dazu, wie diese Voreinstellungen gespeichert werden und wie Sie sie in eine Produktionsumgebung integrieren können, finden Sie auf der Seite [Benutzereinstellungen - Automatisieren des Setups](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) der Dokumentation.

## Allgemein

### Letzte Dokumente

|  |                                                                                                                                         |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------|
| <b>Liste der zuletzt verwendeten Dokumente enthält </b>  *Standard: 10* | Auf diese Weise können Sie die Anzahl der Dokumente auswählen, die im Eintrag <b>Zuletzt verwendete Pakete</b> des Elements <b>Datei</b> im Hauptmenü [aufgelistet werden sollen](../the-main-toolbar/the-main-toolbar.md). |

### Verlauf

|  |  |
| --- | --- |
| **Verlaufsstapelgröße** *Standard: 200* | Dies gibt die Anzahl der verfügbaren Rückgängig-Vorgänge zu einem beliebigen Zeitpunkt im Element &quot;<b>Bearbeiten&quot; > &quot;Rückgängig&quot;</b>&quot; des [Hauptmenüs an](../the-main-toolbar/the-main-toolbar.md).  **Vorsicht:** Je mehr Vorgänge rückgängig gemacht werden müssen, desto mehr Arbeitsspeicher ist für die Anwendung erforderlich. |

### Sprache

|  |  |
| --- | --- |
| **Sprache der Anwendung auswählen** *Standard: System* | Diese Einstellung definiert die in der Anwendungsoberfläche verwendete Sprache. Die Option &quot;*System*&quot; erkennt Sprache automatisch aus den Systemspracheinstellungen. Die verfügbaren Sprachen sind in unseren [Systemanforderungen](../../getting-started/system-requirements/system-requirements.md) aufgeführt.  **Hinweis:** Das Ändern dieser Einstellung wird erst nach dem Neustart der Anwendung wirksam. |

### Ansichten

|  |  |
| --- | --- |
| <b>Zoom in Ansichten umkehren</b>  *Standard: Nicht aktiviert* | Wenn diese Option aktiviert ist, werden die Zoomsteuerungen in der [2D-Ansicht](../../interface/2d-view/2d-view.md), [3D-Ansicht](../../interface/3d-view/3d-view.md) und [Diagrammen](../../interface/the-graph-view/the-graph-view.md) invertiert. |

### Pfade

|  |  |
| --- | --- |
| <b>Pfad speichern/exportieren</b>  *Standard: Letzter Pfad* | Bestimmt, ob der vorgeschlagene Speicher-/Exportpfad der zuletzt ausgewählte Pfad oder der Pfad des [SBS-Pakets](../../getting-started/overview/overview.md) ist. Der zuletzt ausgewählte Pfad wird sitzungsübergreifend gespeichert. |
| <b>Temporärer Ordner</b>  *Standard: Pfad abhängig vom Betriebssystem des Systems* | Wenn die Bilddaten eines Diagramms den zugewiesenen Speicherpool überschreiten (siehe unter <b>Speicher > Bildcache</b>), werden die überlaufenden Daten auf den Datenträger geschrieben. Mit dieser Einstellung können Sie den Speicherort definieren, an dem die überlaufenden Bild-Cache-Daten gespeichert werden.   Dieser Speicherort wird auch verwendet, um eine Kopie des aktuell geöffneten SBS-Pakets mit den neuesten Änderungen seit dem letzten manuellen Speichern zu speichern. |

### Datenspeicher

#### Bildcache

Die Anwendung speichert im Cache ein *unkomprimiertes Bild mit voller Auflösung* für jeden gerenderten Knoten im aktuellen Diagramm.\
Instanzknoten generieren diese Bilder für alle Knoten des Diagramms, auf das sie verweisen, und löschen sie, nachdem ihre [Ausgaben](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) berechnet wurden. Zu diesem Zeitpunkt werden nur die Ausgänge im Speicher gespeichert.

Sie können die maximale Cachegröße festlegen, die Miniaturansichten und Bildern im Systemspeicher zugewiesen wird, und die aktuelle Verwendung anzeigen. Wenn die Cachedaten den zugewiesenen Pool überlaufen, werden die überschüssigen Daten in den <b>Temporary Folder</b> geschrieben (siehe <b>Pfade > Temporary folder</b>).

|  |  |
| --- | --- |
| <b>Arbeitsspeicherbudget</b>  *Standard: Automatisch* | Diese Zuweisung wird automatisch auf ca. 75 % des gesamten Systemspeicherpools berechnet. Um diesen Wert manuell festzulegen, wählen Sie die Option &quot;*Custom*&quot; und legen Sie einen Wert im benachbarten Eingabefeld fest. |

Beachten Sie, dass das Schreiben auf die Festplatte um *Größenordnungen langsamer ist* als das Schreiben in den Systemspeicher. Daher nimmt die Diagrammwiedergabezeit *exponentiell zu*, da überlaufende Daten in den temporären Ordner geschrieben werden müssen.\
Um dies zu verhindern, empfehlen wir, die Vorschläge zum Verringern des Speicherbedarfs eines Diagramms im Abschnitt [Leistungsoptimierungsrichtlinien](../../best-practices/performance-optimization/performance-optimization-guidelines.md) der Dokumentation zu lesen.

#### Jobplaner

Bei bestimmten Aufgaben, wie z. B. der Bildkonvertierung für Miniaturansichten oder der [2D-Ansicht](../../interface/2d-view/2d-view.md), werden aus Gründen der Effizienz separate Aufträge erstellt und auf die Systemverarbeitungskerne verteilt. Jeder Auftrag schreibt Daten in den Systemspeicher, um seine Vorgänge auszuführen.\
Mit dieser Einstellung können Sie den zugewiesenen Speicherpool für *alle gleichzeitigen Aufträge* definieren. Wenn dieser Pool vollständig verwendet wird, werden neue Jobs in die Warteschlange gestellt, bis die aktuellen Jobs abgeschlossen sind.

|  |  |
| --- | --- |
| <b>Arbeitsspeicherbudget</b>  *Standard: Automatisch* | Diese Zuweisung wird automatisch auf ca. 10 % des gesamten Systemspeicherpools berechnet. Um diesen Wert manuell festzulegen, wählen Sie die Option &quot;*Custom*&quot; und legen Sie einen Wert im benachbarten Eingabefeld fest. |

### Benutzeroberfläche

|  |  |
| --- | --- |
| **High DPI deaktivieren** *Standard: Nicht markiert* | Im Modus &quot;<b>High DPI</b>&quot; wird eine konsistente Skalierung von Text- und Benutzeroberflächenelementen &quot;*&quot; unabhängig von den Anzeige- und Skalierungseinstellungen des Systems beibehalten.* Wenn Sie diese Einstellung deaktivieren (d. h. Kontrollkästchen *gefüllt*), kann die Benutzeroberfläche skaliert werden, was auf einigen Bildschirmen zu größerem und besser lesbarem Text führt, aber auch zu Inkonsistenzen in der Textgröße sowie zu anderen Layoutproblemen führen kann.  **Vorsicht:** Designer erfasst die spezifische Skalierung der Benutzeroberflächenelemente *vom Betriebssystem*. Daher sollten alle Anpassungen an der Skalierung der Benutzeroberfläche in den Anzeigeeinstellungen des Betriebssystems vorgenommen werden. Um sicherzustellen, dass die Anzeigeeinstellungen in Designer korrekt angewendet werden, *melden Sie sich von* Ihrer Betriebssystembenutzersitzung ab und melden Sie sich nach Änderung dieser Einstellungen wieder an.  **Hinweis:** Das Ändern dieser Einstellung wird erst nach dem Neustart der Anwendung wirksam. |

### Automatische Sicherungskopie

Standardmäßig ist eine Funktion zum automatischen Speichern enthalten, die Kopien des aktuellen Status von offenen [SBS Paketen ](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion) zu festgelegten Zeitpunkten erstellt. Automatisch gespeicherte Dateien werden in einem Ordner &quot;<b>.autosave</b>&quot; am SBS Speicherort des Pakets abgelegt.

|  |  |
| --- | --- |
| <b>Automatische Sicherung alle # Minuten</b>  *Standard: 5* | Der Zeitraum zwischen jedem automatischen Speichern. |
| <b>Auf dem Laufenden bleiben: # Versionen</b>  *Standard: 6* | Die maximale Anzahl von automatischen Speicherungen, die zu einem bestimmten Zeitpunkt beibehalten werden können. |

Wenn die maximale Anzahl an Versionen erreicht ist, löschen neuere Sicherungen die ältesten Sicherungen.\
Beachten Sie auch, dass automatische Speichervorgänge geöffnet werden sollten *, nachdem sie* an den ursprünglichen Speicherort des SBS-Pakets verschoben wurden. Sie sollten *not* an ihrem aktuellen Speicherort öffnen.

### Veröffentlichen und Senden von SBSAR-Dateien

|  |  |
| --- | --- |
| <b>Speichern Sie die SBS-Datei immer, wenn Sie sie in SBSAR veröffentlichen oder an eine andere Anwendung senden</b>  *Standard: Wahr* | Steuert das automatische Speichern des SBS-Pakets, wenn [es ](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) veröffentlicht oder an eine andere Anwendung gesendet wird. |

### Cooker

|  |                                                                                                                                                                                                                                                                                                 |
| --- |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Begrenzung der Kochgröße</b>  *Standard: 8192 Pixel* | Definiert die maximale Pixelauflösung, die für alle Knoten in einem beliebigen Substance [Diagramm](../../compositing-graphs/substance-compositing-graphs.md) zulässig ist. Da Graphausgaben immer quadratische Bilder mit einer Potenz von 2 Auflösungen sind, definiert der hier festgelegte Wert sowohl die maximale Breite als auch das Height in Pixel. |

### Modul

|  |  |
| --- | --- |
| <b>GPU-Cachebeschränkung</b>  *Standard: 2048 MB* | Mit dieser Einstellung können Sie festlegen, wie viel Speicher für das Zwischenspeichern von Renderstufen reserviert werden soll. Normalerweise speichert das Substance Engine die Ausgabe jedes Nodes in einem Substance-Graf zwischen. |

>[!NOTE]
>
> Wir empfehlen, die Vorschläge zum Verringern des Speicherbedarfs eines Diagramms im Abschnitt [Richtlinien zur Leistungsoptimierung](../../best-practices/performance-optimization/performance-optimization-guidelines.md) der Dokumentation zu lesen.

## Projekte

Weitere Informationen finden Sie auf der Seite [Projekteinstellungen](../../interface/preferences-window/project-settings/project-settings.md).

## Graph

### Allgemein

|  |  |
| --- | --- |
| <b>Die Tabulatortaste zeigt das Knotenmenü </b> an.  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, öffnet die Tabulatortaste das <b>Knotenmenü</b> und repliziert die Funktionalität der Leertaste. |
| <b>Aktivieren der Knotenerstellung durch Klicken und Ziehen von Verbindungen</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, ziehen Sie den Cursor, wenn Sie auf eine Verbindung klicken, und lassen Sie den erstellten Link im leeren Graf los, um das <b>Knotenmenü</b> anzuzeigen.   Das Menü wird auch *gefiltert*, je nach Typ der Verbindung, auf die geklickt wurde. Das bedeutet, dass nur Knoten angezeigt werden, die mit der angeklickten Verbindung kompatibel sind. |
| <b>Anzeigen von Ausgaben in der 3D-Ansicht beim Öffnen eines Grafen</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, werden alle Graphausgaben automatisch in der [3D-Ansicht](../../interface/3d-view/3d-view.md) angewendet, wenn dieser Graf geöffnet wird.   Dies hat auch zur Folge, dass alle Knoten gerendert werden, die Teil eines Streams sind, der zu einem [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)-Knoten führt. |

### Substance Kompositionsgraph

|  |  |
| --- | --- |
| <b>Beim Öffnen eines Grafen automatisch alle Miniaturansichten für Knoten berechnen</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, werden beim Laden des Grafen automatisch alle Knotenminiaturen gerendert. |
| <b>Ausgabe in 2D-Ansicht anzeigen, wenn ein Graf geöffnet wird</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, wird die erste Graphausgabe automatisch in der [2D-Ansicht](../../interface/2d-view/2d-view.md) angezeigt, wenn dieser Graf geöffnet wird. Dies hat auch zur Folge, dass alle Knoten gerendert werden, die Teil eines Streams sind, der zu diesem [Ausgabeknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) führt. |
| <b>Automatisch neu erstellten Compositing-Knoten anzeigen</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, wird die [2D-Ansicht](../../interface/2d-view/2d-view.md) automatisch aktualisiert, um die Ausgabe eines neu erstellten Knotens anzuzeigen. |
| <b>Konvertierungsknoten für Farbe/Graustufen automatisch einfügen</b>  *Standard: Nicht aktiviert* | Wenn diese Option aktiviert ist, werden Farb-/Graustufen-Verbindungstypkonflikte automatisch behoben, indem *bestimmte Knoten platziert werden*, um die entsprechende Konvertierung durchzuführen.   Wenn eine *Grayscale*-Ausgabe (graue Verbindung) mit einem *Color*-Eingang (gelbe Verbindung) verbunden ist, wird automatisch ein [Verlaufs-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)-Knoten zwischen den beiden Verbindungen platziert.   Wenn eine *Color*-Ausgabe (gelbe Verbindung) mit einem *Grayscale*-Eingang (graue Verbindung) verbunden ist, wird automatisch ein [Graustufenkonvertierung](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md)-Knoten zwischen den beiden Verbindungen platziert. |
| <b>Graf-Bearbeitung im Kontext aktivieren</b>  *Standard: Nicht aktiviert* | Wenn Sie einen Graf öffnen, der von einem [Instanzknoten](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) mit einem Rechtsklick auf den Knoten referenziert wird, und <b>Verweis öffnen</b> auswählen, wird dieser Graf standardmäßig geladen und *für sich* bearbeitet.   Wenn diese Option aktiviert ist, können Sie Graf bearbeiten, auf die von Instanzen *verwiesen wird. Dabei werden die Informationen verwendet, die in der Instanz* vom aktuellen Graf übergeben werden. Klicken Sie dazu mit der rechten Maustaste auf einen Instanzknoten und wählen Sie <b>Verweis im Kontext öffnen</b> aus, oder verwenden Sie den Tastaturbefehl Strg+E.   Dies bedeutet, dass ein instanzierter Graf im Kontext des Grafen bearbeitet werden kann, in den er instanziert wird. Dies ist sehr nützlich, um die Auswirkungen der Bearbeitungen auf den Graf zu sehen, in dem Sie gearbeitet haben. Siehe Beispiel unten.  **Hinweis:** Die Registerkarten <b>Vorschau</b> und <b>Vorgaben</b> sind *deaktiviert* in den [Graf-Eigenschaften](../../compositing-graphs/graph-parameters/graph-parameters.md), wenn die kontextbezogene Bearbeitung verwendet wird. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Kontextabhängige Bearbeitung deaktiviert](preferences-window.resources/substance3ddesigner_incontext_no.gif "Kontextabhängige Bearbeitung deaktiviert")

*Verweis öffnen*

</td>
<td style="border: 0;" valign="top">

![Kontextabhängige Bearbeitung aktiviert](preferences-window.resources/substance3ddesigner_incontext_yes.gif "Kontextabhängige Bearbeitung aktiviert")

*Verweis im Kontext öffnen*

</td>
</tr>
</table>

## 3D-Ansicht

### Verschiedenes

|  |  |
| --- | --- |
| <b>Umgebung standardmäßig ausgeblendet</b>  *Standard: Aktiviert* | Bestimmt die Standardsichtbarkeitseinstellung für die [Umgebung](../../interface/3d-view/3d-view.md). Wenn sie ausgeblendet sind, wird der Hintergrund der 3D-Ansicht durch eine *Volltonfarbe* ersetzt. |
| <b>Viewport-Skalierung</b>  *Standard: Auto* | Steuert die Skalierung der Renderauflösung der 3D-Ansicht, wenn das System die Anzeigeskalierung verwendet.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Auto</i>: Die Renderingauflösung basiert auf der <i>skalierten</i> Anzeigeauflösung.</li> <li data-preserve-html="true"><i>Keine</i>: Die Renderingauflösung basiert auf der <i>nativen</i> Anzeigeauflösung.</li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>Beispielanzahl</b>  *Standard: 64* | Wirkt sich auf die Größe der Sample-Tabelle der 3D-Ansicht-Shader aus. Ein höherer Wert führt zu einer höheren Bildqualität auf Kosten der Leistung.  **Hinweis:** Die Beispieltabelle der Shader ist auch von der GPU und dem Betriebssystem des Systems betroffen. |

## Baker

|  |  |
| --- | --- |
| <b>GPU-Raytracing</b>  *Standard: Aktiviert* | Wenn diese Option aktiviert ist, wird Raytracing für [kompatible Bäcker](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) auf der GPU durchgeführt.   Je nach NVIDIA-GPU-Architektur sind die folgenden GPU-Raytracing-Backends die Standardeinstellungen:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>: Touring und neuer</li> <li data-preserve-html="true"><i>Optix</i>: Pascal und Maxwell</li> </ul>  **Hinweis:** Weitere Informationen zu GPU-betriebenen Bäckereien finden Sie im Abschnitt [GPU-Raytracing](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) der Dokumentation [Substance Bakers](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).  **Tipp:** Sie können die folgenden *Befehlszeilenargumente* verwenden, wenn Sie die Anwendung starten, um *die Verwendung eines anderen GPU-Raytracing-Backends zu erzwingen*: <ul data-preserve-html="true"> <li data-preserve-html="true"><code>—force-optix</code> : Erzwingen der Verwendung von Optix auf Nvidia Turing oder neueren GPUs</li> <li data-preserve-html="true"><code>—force-dxr</code> : erzwingen der Verwendung von DXR auf Nvidia Pascal-GPUs</li> </ul> |

## Bibliothek

|  |  |
| --- | --- |
| <b>Miniaturansichten neu erstellen</b> | Die Option löst eine Neuberechnung aller [Bibliotheks](../../interface/the-library/the-library.md)-Miniaturansichten aus, die automatisch die vorherigen ersetzen. |

## Kürzel

Sie können benutzerdefinierte Tastaturbefehle zum Erstellen von Knoten in Diagrammen zuweisen.

Verknüpfungen können für Knoten in allen Diagrammtypen zugewiesen werden: [Substance graphs](../../compositing-graphs/substance-compositing-graphs.md), [Substance function graphs](../../function-graphs/function-graphs.md) und [FX-Map graphs](../../function-graphs/fxmaps/fxmaps.md).

Jedem Knoten kann eine Verknüpfung zugewiesen werden, sogar benutzerdefinierte Bibliotheksknoten. Dieselbe Tastenkombination kann in verschiedenen Diagrammtypen zugewiesen werden. Standardmäßig sind keine Tastaturbefehle zugewiesen, Sie können dies nach Ihren Wünschen anpassen.

Bei einem Konflikt mit einem anderen Knoten-Tastaturbefehl oder einem integrierten Programmbefehl wird der Eintrag hervorgehoben und eine Warnung wird angezeigt. Der Tastaturbefehl hat *keine Auswirkungen*, bis der Konflikt gelöst ist.

>[!IMPORTANT]
>
> Von Python-Plug-ins überschriebene Tastaturbefehle
> 
> Wenn ein Python-Plug-in einen Tastaturbefehl definiert, der einem Knoten zugewiesen ist, überschreibt das Plug-in diesen Tastaturbefehl. Das bedeutet, dass die Taste die Plug-in-Aktion auslöst, anstatt einen Knoten zu erstellen.
> 
> Dies ist bereits bei den Tasten H, S und V der Fall, die von den [Knotenausrichtungstools](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md) verwendet werden.

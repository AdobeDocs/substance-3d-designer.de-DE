---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Lerne, wie du in Substance 3D Designer Ressourcen für deine Materialprojekte importierst, verknüpfst und neu erstellst.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressourcen importieren/verknüpfen und neue Ressourcen erstellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 2%

---


# Ressourcen importieren/verknüpfen und neue Ressourcen erstellen

[Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) unterstützt drei Modi zum Einbringen oder Erstellen neuer Ressourcen für die Verwendung in Ihrem Diagramm. Diese Ressourcen können von vielen verschiedenen Typen sein, einschließlich, aber nicht beschränkt auf [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md), [Vektorgrafiken](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [3D-Szenen](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html) und [Schriften](../../resources/font-resource/font-resource.md). Auf dieser Seite werden die verschiedenen Methoden und der jeweils am besten geeignete Zeitpunkt erläutert.

Auf alle Methoden wird zugegriffen, indem [Sie auf RMB in einem Paket im Explorer klicken](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)[.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)

Die folgende Tabelle gibt einen kurzen Überblick über die unterschiedlichen Funktionen der Methoden.

|                                                                                                                                                                         | Neu | Importieren | Verknüpfung |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Diagramme ([Substance Diagramme](../../compositing-graphs/substance-compositing-graphs.md), [Substance Funktionsdiagramme](../../function-graphs/function-graphs.md) | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md),[ Vektorgrafiken (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| [3D-Szenen](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html), [Schriften](../../resources/font-resource/font-resource.md) | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| Wird neben der SBS-Datei erstellt | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| Bearbeitbar in Designer | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| Externe Bearbeitungen werden automatisch synchronisiert | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| Eingebettet in veröffentlichte SBSAR-Dateien | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> |

## Neue Ressourcen

Wenn Sie eine neue Ressource erstellen, wird eine Ressource in Ihrem Paket von Grund auf neu erstellt. Alle Designer-Ressourcen können nur auf diese Weise erstellt werden, z. B. Substance-Graphen und Substance-Funktionsdiagramme.

Ein Sonderfall liegt vor, wenn Sie eine neue [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) oder [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) erstellen: Diese Dateien werden in Ihrem Explorer angezeigt und verhalten sich wie eine importierte Ressource, jedoch ohne dass eine externe Datei erforderlich ist. Sie können in Designer geändert werden. Neue Bitmaps und SVG, die auf diese Weise erstellt werden, sind gut, wenn Sie sich nicht auf einen externen Editor verlassen müssen: zum Beispiel, wenn du nur eine schnelle und einfache Vektorform brauchst, oder eine einfache gemalte 2D-Bitmap-Maske.

## Importierte Ressourcen

Das Importieren einer Ressource bedeutet, dass neben der SBS-Datei (im Ordner &quot;*Graphname*.resources&quot;) ein Duplikat der Ressourcendatei erstellt wird, [mit Ausnahme von SVG-Dateien](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). Es wird manchmal auch als &quot;Einbetten&quot; einer Ressource bezeichnet.

Eine importierte Ressource kann dann in Designer mit den [Bitmap-Malwerkzeugen](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) oder [Vektorbearbeitungswerkzeugen](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) in der [2D-Ansicht](../../interface/2d-view/2d-view.md) bearbeitet werden, nachdem sie im Diagramm platziert wurde. Importierte Ressourcen sind nicht mehr mit ihren ursprünglichen Quelldateien verknüpft: Wenn Sie also die ursprünglich importierte Datei ändern, entfernen oder aktualisieren, hat dies keine Auswirkungen auf die Ressource in Designer.

Bei [AxF-Dateien](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) ist der Vorgang etwas komplizierter. Substance-Graphen und Bitmap-Ressourcen werden aus dem AxF-Paket erstellt. Alle diese können jedoch weiterhin in ihren jeweiligen Editoren bearbeitet werden: Diagrammansicht oder 2D-Ansicht.

>[!WARNING]
>
> Bei neuen Paketen werden importierte und neue Ressourcen erst auf der Festplatte gespeichert, wenn Sie das Paket speichern.

## Verknüpfte Ressourcen

Das Verknüpfen einer Ressource bedeutet, dass Designer die Quelldatei an ihrem ursprünglichen Speicherort auf der Festplatte referenziert, sie jedoch im Explorer weiterhin so anzeigt, als wäre sie Teil Ihres Pakets. Sie können die Ressource nicht direkt in Designer bearbeiten, sondern nur als Komponente in Ihrem Diagramm oder als Quelle für Backmaps verwenden.

Das Verknüpfen ist ideal, wenn Sie wissen, dass Sie einen externen Editor verwenden müssen, um Ihre Ressource zu aktualisieren, während Sie gleichzeitig in Designer arbeiten. Backmaps sind ein Paradebeispiel: Sie können Designer Referenz-Bitmaps aus einer externen Backup-Anwendung verwenden, die Ihr Diagramm automatisch neu laden und aktualisieren, sobald diese Dateien geändert werden. Entsprechend können 3D-Szenen nur verknüpft werden, sodass Designer jedes Mal, wenn Sie eine neue FBX-Datei aus Ihrer 3D-Anwendung exportieren, automatisch das in der 3D-Ansicht verwendete Gitter aktualisiert. Wenn Sie Maps aus diesem Gitter backen, müssen Sie den Backvorgang manuell starten, idealerweise, indem Sie auf RMB klicken und &quot;Alle durch Baking erzeugte Map aktualisieren&quot; auswählen.

## Ressourcen werden gelöscht

Beim Löschen einer Ressource aus einem Paket wird das Dialogfeld <b>Entfernen des Elements bestätigen</b> angezeigt. Wenn Elemente, die gerade entfernt werden, von anderen Ressourcen *referenziert werden (z. B. [Grapheninstanzen](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) und [Bitmapressourcen](../../resources/bitmap-resource/bitmap-resource.md), die in [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md) verwendet werden), enthält das Dialogfeld eine* Warnung und eine Liste *dieser Elemente.*

>[!NOTE]
>
> Wir empfehlen, diese Elemente zu berücksichtigen und die erforderlichen Maßnahmen zu ergreifen, um *beschädigte Abhängigkeiten zu antizipieren*, die sich aus dem Löschen von Elementen aus einem Paket ergeben würden.\
> Diese Aktionen können *das Entfernen aller Benutzer* dieser Ressourcen vor dem Löschen umfassen.

![ &#39;Gelöschte verwendete Ressource&#39; Warnung](../../assets/confirm-item-removal.png " &#39;Gelöschte verwendete Ressource&#39; Warnung"){width="512px"}

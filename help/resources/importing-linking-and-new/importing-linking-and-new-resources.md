---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Hier erfahren Sie, wie Sie in Substance 3D Designer neue Ressourcen für Ihre Material-Projekte importieren, verknüpfen und erstellen.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressourcen importieren/verknüpfen und neue Ressourcen erstellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---


# Ressourcen importieren/verknüpfen und neue Ressourcen erstellen

[Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) unterstützt drei Modi zum Einbringen oder Erstellen neuer Ressourcen für die Verwendung in Ihrem Graf. Diese Ressourcen können von vielen verschiedenen Typen sein, einschließlich, aber nicht beschränkt auf [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md), [Vektorgrafiken](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [3D Szenen](../3d-scene-resource/3d-scene-resource.md) und [Schriften](../../resources/font-resource/font-resource.md). Auf dieser Seite werden die verschiedenen Methoden und der jeweils am besten geeignete Zeitpunkt erläutert.

Auf alle Verfahren kann durch Klicken auf RMB auf einem Paket im Explorer zugegriffen werden.

Die folgende Tabelle gibt einen kurzen Überblick über die unterschiedlichen Funktionen der Methoden.

|                                                                                                                                                                         | Neu | Importieren | Verknüpfung |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Graf ([Substance Graf](../../compositing-graphs/substance-compositing-graphs.md), [Substance-Graf](../../function-graphs/function-graphs.md) | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md),[Vektorgrafiken (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 3D-Szenen, [Schriften](../../resources/font-resource/font-resource.md) | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Häkchen)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Wird neben SBS Datei erstellt | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Bearbeitbar in Designer | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Fehler)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Externe Bearbeitungen werden automatisch synchronisiert | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Fehler)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(Häkchen)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Eingebettet in veröffentlichte SBSAR-Dateien | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(Häkchen)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |

## Neue Ressourcen

Wenn Sie eine neue Ressource erstellen, wird eine Ressource in Ihrem Paket von Grund auf neu erstellt. Alle Designer-Ressourcen können nur auf diese Weise erstellt werden, z. B. Substance-Graf und Substance-Funktions-Graf.

Ein Sonderfall liegt vor, wenn Sie eine neue [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) oder [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) erstellen: Diese Dateien werden in Ihrem Explorer angezeigt und verhalten sich wie eine importierte Ressource, jedoch ohne dass eine externe Datei erforderlich ist. Sie können in Designer geändert werden. Neue Bitmaps und SVG, die auf diese Weise erstellt werden, sind gut, wenn Sie sich nicht auf einen externen Editor verlassen müssen: zum Beispiel, wenn du nur eine schnelle und einfache Vektorform brauchst, oder eine einfache gemalte 2D-Bitmap-Maske.

## Importierte Ressourcen

Das Importieren einer Ressource bedeutet, dass neben der SBS (im Ordner &quot;*Graphname*.resources&quot;) ein Duplikat der Ressourcendatei erstellt wird, mit Ausnahme von SVG-Dateien [&#128279;](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). Es wird manchmal auch als &quot;Einbetten&quot; einer Ressource bezeichnet.

Eine importierte Ressource kann dann in Designer mit den [Bitmap-Malwerkzeugen](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) oder [Vektorbearbeitungswerkzeugen](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) in der [2D-Ansicht](../../interface/2d-view/2d-view.md) bearbeitet werden, nachdem sie in den Graf platziert wurde. Importierte Ressourcen sind nicht mehr mit ihren ursprünglichen Quelldateien verknüpft: Wenn Sie also die ursprünglich importierte Datei ändern, entfernen oder aktualisieren, hat dies keine Auswirkungen auf die Ressource in Designer.

Im Fall von [AxF-Dateien](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) ist der Prozess etwas komplizierter. Substance-Graf und Bitmap-Ressourcen werden aus dem AxF-Paket erstellt. Alle diese können jedoch weiterhin in ihren jeweiligen Editoren bearbeitet werden: Graphansicht oder 2D-Ansicht.

>[!WARNING]
>
> Bei neuen Paketen werden importierte und neue Ressourcen erst auf der Festplatte gespeichert, wenn Sie das Paket speichern.

## Verknüpfte Ressourcen

Das Verknüpfen einer Ressource bedeutet, dass Designer auf die Quelldatei an ihrem ursprünglichen Speicherort auf der Festplatte verweist, diese aber dennoch im Explorer anzeigt, als wäre sie Teil Ihres Pakets. Sie können die Ressource nicht direkt in Designer bearbeiten, sondern nur als Komponente in Ihrem Graf oder als Quelle für das Baking von Maps verwenden.

Das Verknüpfen ist ideal, wenn Sie wissen, dass Sie einen externen Editor verwenden müssen, um Ihre Ressource zu aktualisieren, während Sie gleichzeitig in Designer arbeiten. Baking Maps ist ein Paradebeispiel: Sie können Designer Referenz-Bitmaps aus einer externen Baking-Anwendung verwenden, die Ihren Graf automatisch neu laden und aktualisieren, sobald diese Dateien geändert werden. Entsprechend können 3D-Szenen nur verknüpft werden, sodass Designer jedes Mal, wenn Sie eine neue FBX-Datei aus Ihrer 3D-Anwendung exportieren, automatisch den in der 3D-Ansicht verwendeten Mesh aktualisiert. Wenn Sie Maps von diesem Mesh aus Baking geführt haben, müssen Sie den Baking manuell starten, idealerweise, indem Sie auf RMB klicken und &#39;Alle durch Baking erzeugte Map aktualisieren&#39; wählen.

## Ressourcen werden gelöscht

Beim Löschen einer Ressource aus einem Paket wird das Dialogfeld <b>Entfernen des Elements bestätigen</b> angezeigt. Wenn Elemente, die gerade entfernt werden, von anderen Ressourcen *referenziert werden (z. B. [Grapheninstanzen](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) und [Bitmapressourcen](../../resources/bitmap-resource/bitmap-resource.md), die in [Substance-Grafen](../../compositing-graphs/substance-compositing-graphs.md) verwendet werden), enthält das Dialogfeld eine* Warnung und eine Liste *dieser Elemente.*

>[!NOTE]
>
> Wir empfehlen, diese Elemente zu berücksichtigen und die erforderlichen Maßnahmen zu ergreifen, um *beschädigte Abhängigkeiten zu antizipieren*, die sich aus dem Löschen von Elementen aus einem Paket ergeben würden.\
> Diese Aktionen können *das Entfernen aller Benutzer* dieser Ressourcen vor dem Löschen umfassen.

![&#x200B; &#39;Gelöschte verwendete Ressource&#39; Warnung](../../assets/confirm-item-removal.png " &#39;Gelöschte verwendete Ressource&#39; Warnung"){width="512px"}

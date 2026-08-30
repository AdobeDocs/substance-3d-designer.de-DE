---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill", um verbundene Bereiche mit ähnlicher Farbe zu füllen, um Masken und Texturverarbeitungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill.resources/floodfill.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Flood Fill ist Teil eines erweiterten Set an Effekten, mit denen du einer einfachen, binären Kachelstruktur viel mehr Variation hinzufügen kannst. Es ist nicht für sich selbst bestimmt: sondern eher als Ausgangspunkt für andere Flood Fill-Effekte. Diese getrennten Daten ermöglichen einen dynamischeren, optimierteren und weniger destruktiven Arbeitsablauf.

Die anderen Flood Fill-Effekte sind [Flood Fill zu Verlauf](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [Flood Fill zu Farbe/Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [Flood Fill zu zufälligem Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [Flood Fill zu zufälliger Farbe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [Flood Fill zu Box-Größe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [Flood Fill zu Position](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Flood Fill-Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) und [Flood Fill zu &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> Die Eingabemap muss für den Flood Fill geeignet sein, damit sie funktioniert. Idealerweise ist es eine binäre Karte (nur Schwarz/Weiß, keine Graustufen), bei der jede Kachel von den anderen Zeilen durch einen Rand getrennt ist, der für jedes Pixel vollständig schwarz (0,0,0) ist. Ein Beispiel für einen geeigneten Bewerber ist der [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).
> 
> Probleme treten auf, wenn Kacheln nicht durch schwarze Pixel getrennt sind, in der Regel bei Verwendung von Graustufen mit schrägen Werten. Sie können dies an einem allgemeinen Mangel an roten Werten im Ergebnis und möglicherweise seltsamen Artefaktlinien erkennen. Passen Sie in solchen Fällen den Kontrast auf der Eingangskarte an oder schalten Sie die Eingangskarte aus. Stellen Sie sicher, dass Sie die Einstellung Sicherheit/Geschwindigkeit ändern, um zu sehen, ob sich etwas verbessert.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Zielkonflikt Sicherheit/Geschwindigkeit</b> <i>Einfache oder kleine Formen, komplexe oder große Formen, kein Fehlermodus.</i> | Stellen Sie den Berechnungsmodus so ein, dass er am besten zu den Eingabeformen passt. Ermöglicht deutlich genauere Ergebnisse, wenn der richtige Modus ausgewählt wird. |
| <b>Erweiterte Optionen</b> <i>Erweiterte Parameter anzeigen und erweiterte Parameter und die Ausgabe ausblenden/ausblenden</i> |  |
| <b>Überschreiben Sie den Kompromiss zwischen Sicherheit und Geschwindigkeit</b> <i>-1 - 100</i> | Nur bei aktivierten erweiterten Optionen sichtbar. Ermöglicht das Überschreiben interner Funktionen. Sehr fortgeschritten, dient zum Erstellen eigener Effekte oder zum Debuggen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-ex1.png" />
        </td>
    </tr>
</table>

Gute und schlechte Beispiele für Ergebnisse aus dem Flood Fill.

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie FXMaps in Substance 3D Designer verwenden, um Funktions-Graf auf Texturen anzuwenden und prozedurale Mustergenerierung zu ermöglichen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---


# FXMaps

**Der FX-Map-Knoten ermöglicht die Erstellung prozeduraler Images**. Es ist eine der leistungsfähigsten Funktionen der Substance-Technologie.

Eine FX-Map stellt einen speziellen Diagrammtyp dar, der als Markov-Kette bekannt ist. Markov Ketten stellen einen einfachen Kernprozess dar: wiederholt replizieren und unterteilen eines Bildes immer wieder. Bei jedem Schritt kann ein Bild gedreht, übersetzt und nach Bedarf angeglichen werden. Die Ergebnisse können alles Mögliche sein, von einfachen Mustern bis hin zu komplexen Rauschen. FX-Maps sind die Grundlage für viele der Beispiel-Substance, die mit Substance 3D Designer installiert werden.

## Erstellen von FX-Map-Grafen

Wenn Sie einen FX-Map-Graf anzeigen möchten, fügen Sie einem [Substance-Knoten](../../compositing-graphs/substance-compositing-graphs.md) einfach einen [FX-Map-Graf](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) hinzu. Klicken Sie dann mit der rechten Maustaste auf den Knoten, und drücken Sie Cmd + E (OS X) bzw. Strg + E (Windows), um den Graf zu öffnen. Dieses FX-Map-Diagramm wird auf einer neuen Registerkarte im Bedienfeld &quot;Diagramme&quot; angezeigt. Sie können zwischen diesem Graf und dem Substance-Graf wechseln, indem Sie auf die Registerkarte klicken.

## Was sind FX-Maps?

Die gebräuchlichsten Anwendungsfälle von FX-Maps sind die Erstellung sich wiederholender Muster, wie Streifen und Ziegel, und Rauschen, wie Perlin, Brownsche und Gaußsche Rauschen. Lärm ist besonders nützlich bei der Erstellung von organischen, natürlich aussehenden Texturen wie Dirt, Dust, Beton, Steinoberflächen, Flüssigspritzer und so weiter.

FX-Map-Grafen funktionieren nicht auf die gleiche Weise wie Substance-Grafen: Bei Substance-Grafen ist jeder Node unabhängig und hat keine Ahnung von seiner Position im gesamten Graf. Ebenso wenig ist es ihm wichtig, woher seine Bilddaten kommen oder wohin sie sich bewegen.

Im nächsten Kapitel werden die drei Graf-Knoten von FX-Map näher erläutert. Kurz gesagt: Jeder Knoten von FX-Map bietet einen von drei Vorgängen:

### Quadrant

Dadurch wird das Bild an dieser Stelle im Graf in vier Quadranten aufgeteilt. Dies ist der häufigste Knotentyp. Eine Kette von Quadrant-Knoten kann sehr komplex aussehende Bilder sowie komplexe Muster erzeugen.

Tatsächlich stellen Quadrantenknoten eine Ebene - oder **Oktave** - in einem Quad-Tree-Diagramm dar. FX-Map-Graf blenden diese Baumstruktur aus, indem sie jede Ebene in der Baumstruktur mit einem einzelnen Quadranten darstellen: Jedes Mal, wenn Sie einen Quadranten-Knoten mit einem anderen verbinden, erstellen Sie tatsächlich eine vollständige Baumstruktur.

Der Grund für diese &quot;Cheat&quot;-Technik ist, die Notwendigkeit zu entfernen, jeden Knoten auf jeder Ebene eines Baums einzeln darzustellen: Nach nur vier Ebenen Tiefe müssten Sie 4 x 4 x 4 x 4 Nodes verwenden, das sind 256 Einzelknoten! Stattdessen &quot;weiß&quot; jeder Quadrant-Knoten, auf welcher Ebene er sich im Baum befindet, und generiert seine Bilder entsprechend.

Für viele Leser wird das wahrscheinlich keinen Sinn ergeben, aber wir werden das in Kürze noch detaillierter beleuchten.

### Iterieren

Wiederholt das Bild, das in die rechte Verbindung übergeben wird, über das Bild, das in die linke Verbindung übergeben wird, um die festgelegte Anzahl von Iterationen.

Dieser Knoten wird am häufigsten mit einem oder mehreren Dynamic Functions-Graf verwendet, um das Eingabebild in jeder Iteration in irgendeiner Weise zu verschieben oder zu drehen.

### Wechseln

Dies nimmt zwei Eingänge und schaltet einfach zwischen den einen oder anderen, wie durch seine Selektor-Einstellung definiert. Wie beim Knoten Iterieren wird die Selektoreinstellung häufig durch eine dynamische Funktion ausgewählt.

## FX-Maps-Systemvariablen

FX-Maps unterstützen Systemvariablen. Diese Variablen beginnen immer mit einem Dollarsymbol (&quot;$&quot;) und lauten wie folgt:

| Name | Besonderheit | Datentyp | Zweck |
| --- | --- | --- | --- |
| $time | - | float1 | Diese Variable gibt die Zeit in Sekunden zurück, seit das Substance-Render-Engine gestartet wurde.Es ist ideal für Substance, die nach der Zeit animieren müssen. (E.g. In einigen Anwendungen, einschließlich Substance Player, wird eine Substance, die $time verwendet, dazu führen, dass eine Zeitleiste in der Benutzeroberfläche angezeigt wird. |
| $Tiefe | - | float1 | Gibt die Oktavzahl (Stufe) des FX-Map-Knotens zurück. Dadurch kann ein Knoten sein Verhalten ändern, je nachdem, welche Ebene in der Quad-Tree er repräsentiert. |
| $depthpow2 | - | float1 | Wie oben, aber gibt 2 erhöht, um die Macht der Oktave (Level) Zahl. Dies ist ein Hilfswert, der für einige gängige Berechnungen nützlich ist. |
| $number | Nur Knoten wiederholen | float1 | Gibt die Nummer des gezeichneten Musters zurück. Darauf können dynamische Funktionsdiagramme zugreifen, die einen Iterate-Knoten steuern, um dessen Verhalten bei jedem Iterationsschritt zu ändern. (Beachten Sie, dass $number ab 0 zählt, nicht ab 1.) |
| $size | - | float2 | Gibt die Größe des aktuellen Knotens (in Pixeln) zurück. |
| $sizelog2 | - | float2 | Wie oben, gibt aber die Größe als Power-of-2-Werte zurück (z. B.: für 2048\*2048 Bild, $sizelog2 ergibt 11). |
| $pos | Nur Quadrantenknoten | float2 | Gibt die Geburtsstellung des Musters zurück. Das Ergebnis ist immer ein Wert zwischen 0 und 1. |

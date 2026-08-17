---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Quadrant in FXMaps, um Texturen in vier Abschnitte zu unterteilen, um gekachelte Muster und Variationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Der Quadrantenknoten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# Der Quadrantenknoten

Viele FX-Maps bestehen vollständig aus Ketten von Quadrant-Knoten. Quadrantenknoten sind der leistungsstärkste und flexibelste Knoten in der FX-Map-Gruppe. Daher lohnt es sich, zu verstehen, wie dieser Knoten funktioniert.

Das Wichtigste an Quadrantenknoten ist, dass sie der einzige Knoten sind, der die Tiefe oder *Oktave* des FX-Map-Graphen erhöhen kann. Jeder Quadrant-Knoten wird dem zugrunde liegenden Quad-Tree-Graphen hinzugefügt. keiner der anderen Knoten tut dies.

Der Quadrant-Knoten verfügt über eine Reihe von Parametern:

## Farbe/Luminanz

Wenn der Knoten ein Bild zur FX-Map hinzufügt, definieren diese Einstellungen, wie die Kanäle mit anderen Bildern in der Kette vermischt werden. Die Parameter *Farbe / Luminanz* gelten für alle Bilder, die von diesem bestimmten Knoten gerendert werden.

### Zweigversatz

Verschiebt das Bild des Knotens. Der Versatz wird auf alle anderen Bilder angewendet, die von nachfolgenden Knoten im Diagramm gerendert werden. Der Verzweigungsversatz wendet die Übersetzung auf den aktuellen Quadrantenknoten und alle darunter liegenden Knoten im selben Zweig des Diagramms an.

Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Muster

Definiert das Bild (falls vorhanden), das von diesem Knoten zur FX-Map hinzugefügt werden soll.

Quadrantenknoten unterstützen eine lange Liste von Mustern, die weiter unten in diesem Thema beschrieben werden.

>[!WARNING]
>
> Dieser Parameter kann nicht von einer dynamischen Funktion in einer SBSAR-Datei gesteuert werden.

### Muster-Versatz

Verschiebt das Abbild des Knotens um den angegebenen Betrag, wirkt sich jedoch nicht auf nachfolgende Knoten aus. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Mustergröße

Definiert die Größe des Bildes (falls zutreffend), das der FX-Map hinzugefügt werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Musterrotation

Definiert die Drehung des Bildes (falls zutreffend), das der FX-Map hinzugefügt werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Mustervariation

Einige Muster haben Varianten. Mit dieser Einstellung können Sie auswählen, welche Variante verwendet werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Überblendmodus

Gibt den Mischvorgang an, der beim Mischen des Knotenbilds (falls zutreffend) mit dem FX-Map-Bild verwendet werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Zufällige Verteilung

Seed für den Zufallszahlengenerator.

Der Generator verwendet dieses Seed als Ausgangspunkt, um eine Sequenz von scheinbar zufälligen Zahlen zu erstellen. Der Vorteil dieses Ansatzes besteht darin, dass Sie im Gegensatz zur realen Welt sicherstellen können, dass jedes Mal die exakt gleiche Folge von Zufallszahlen generiert wird, was vorhersehbare, wiederholbare, aber zufällig aussehende Ergebnisse liefert.

Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Zufällig erben

Wenn &quot;Ja&quot; eingestellt ist, wird der Zufallszahlengenerator-Seed vom vorherigen Knoten im Diagramm geerbt (d. h. vom Knoten über diesem im Quad-Tree). Wenn es sich um den ersten Knoten handelt, wird sein zufälliges Seed aus dem [Substance-Diagramm](../../../compositing-graphs/substance-compositing-graphs.md) entnommen.

## Muster

Jeder Quadrant-Knoten kann optional ein Bild zur endgültigen FX-Map hinzufügen.

Standardmäßig ist &quot;Kein Muster&quot; ausgewählt, sodass kein Bild gerendert wird. Der Quadrant-Knoten unterteilt das FX-Map-Bild lediglich und teilt es für den nächsten Knoten in der Kette in vier.

Die nächste Option, *Eingabebild*, besteht darin, ein dem FX-Map-Knoten bereitgestelltes Bild zu verwenden. Der FX-Map-Knoten akzeptiert Farb- oder Graustufenbilder zur Verwendung als Hintergrund oder als Ersatz für eines der integrierten Muster. Bitte beachten Sie, dass der Quadrant-Knoten nur ein Graustufen-Eingabebild in einer Graustufen-Fx-Map rendern kann und umgekehrt nur ein Farbeingabebild in einer Farb-FX-Map rendern kann. Wenn du Farbtypen mischen willst, musst du die Eingaben vorher in das Diagramm konvertieren.

Zum Schluss kannst du zwischen den verfügbaren Mustern wählen: Square, Disc, Paraboloid, Bell, Gaussian, Thorn, Pyramid, Brick, Gradation, Waves, Half Bell, Ridge Bell, Crescent und Kapsel.

Zusätzlicher Hinweis: Sie haben die Möglichkeit, eine dynamische Funktion in diesem Parameter zu erstellen, diese funktioniert jedoch nur in Substance 3D Designer. Um Zugriff auf die Bildeingabe durch eine dynamische Funktion zu haben, müssen Sie Werte von 256 (Bildeintrag 1) bis zu höheren Werten (257 für Bildeintrag 2 usw.) verwenden.

### Mustertypen.

Muster sind Graustufen. Einige können mit dem Parameter *Mustervariation* ein wenig geändert werden.

Viele der integrierten Muster weisen eine Form von radialer Verlaufsfüllung oder Ähnliches auf. Dadurch sind sie sehr nützlich für viele Arten von Geräuschen und Mustern. Andere Muster wie &quot;Ziegel&quot;, &quot;Scheibe&quot; und &quot;Quadrat&quot; sind einfache, flache Formen.

Der Parameter &quot;Mustervariation&quot; passt ein definiertes Merkmal des Musters an.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/fxmap-quadrants.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](../../../assets/quadrant-parameters.jpg)

</td>
</tr>
</table>

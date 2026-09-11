---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Quadrant in FXMaps, um Texturen in vier Abschnitte zu unterteilen, um Kachelmuster und -variationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Der Quadrantenknoten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# Der Quadrantenknoten

Viele FX-Maps bestehen vollständig aus Ketten von Quadrant-Knoten. Quadrantenknoten sind der leistungsstärkste und flexibelste Knoten in der FX-Map-Gruppe. Daher lohnt es sich, zu verstehen, wie dieser Knoten funktioniert.

Das Wichtigste an Quadrantenknoten ist, dass sie der einzige Knoten sind, der die Tiefe oder *Oktave* des FX-Map-Grafen erhöhen kann. Jeder Quadrantenknoten wird dem zugrunde liegenden Quad-Tree-Graf hinzugefügt. keiner der anderen Knoten tut dies.

Der Quadrant-Knoten verfügt über eine Reihe von Parametern:

## Farbe/Luminanz

Wenn der Knoten dem FX-Map ein Bild hinzufügt, legen diese Einstellungen fest, wie die Kanäle mit anderen Bildern in der Kette vermischt werden. Die Parameter *Farbe / Luminanz* gelten für alle Bilder, die von diesem bestimmten Knoten gerendert werden.

### Zweigversatz

Verschiebt das Bild des Knotens. Der Versatz wird auf alle anderen Bilder angewendet, die von nachfolgenden Knoten im Graf gerendert werden. Der Verzweigungsversatz wendet die Übersetzung auf den aktuellen Quadrantenknoten und alle darunter liegenden Knoten in derselben Verzweigung des Grafen an.

Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Muster

Definiert das Bild (falls vorhanden), das von diesem Knoten zur FX-Map hinzugefügt werden soll.

Quadrantenknoten unterstützen eine lange Liste von Mustern, die weiter unten in diesem Thema beschrieben werden.

>[!WARNING]
>
> Dieser Parameter kann nicht von einer Dynamikfunktion in einer sbsar-Datei gesteuert werden.

### Muster-Versatz

Verschiebt das Abbild des Knotens um den angegebenen Betrag, wirkt sich jedoch nicht auf nachfolgende Knoten aus. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Mustergröße

Definiert die Bildgröße (falls zutreffend), die der FX-Map hinzugefügt werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Musterrotation

Definiert die Drehung des Bildes (falls zutreffend), das dem FX-Map hinzugefügt werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Mustervariation

Einige Muster haben Varianten. Mit dieser Einstellung können Sie auswählen, welche Variante verwendet werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Überblendmodus

Gibt den Mischvorgang an, der beim Mischen des Knotenbilds (falls zutreffend) mit dem FX-Map-Bild verwendet werden soll. Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Zufällige Verteilung

Seed für den Zufallszahlengenerator.

Der Generator verwendet dieses Seed als Ausgangspunkt, um eine Sequenz von scheinbar zufälligen Zahlen zu erstellen. Der Vorteil dieses Ansatzes besteht darin, dass Sie im Gegensatz zur realen Welt sicherstellen können, dass jedes Mal die exakt gleiche Folge von Zufallszahlen generiert wird, was vorhersehbare, wiederholbare, aber zufällig aussehende Ergebnisse liefert.

Dieser Parameter kann mit einer dynamischen Funktion gesteuert werden.

### Zufällig erben

Wenn &quot;Yes&quot; festgelegt ist, wird der Zufallszahlengeneratorsamen vom vorherigen Graf im Knoten (d. h. dem Knoten über diesem in der Quad-Tree) geerbt. Wenn es sich um den ersten Knoten handelt, wird sein zufälliges Seed aus dem [Substance-Graf](../../../compositing-graphs/substance-compositing-graphs.md) entnommen.

## Muster

Jeder Quadrant-Knoten kann optional ein Image zur endgültigen FX-Map hinzufügen.

Standardmäßig ist &quot;Kein Muster&quot; ausgewählt, sodass kein Bild gerendert wird. Der Quadrant-Knoten unterteilt das FX-Map-Bild lediglich und teilt es für den nächsten Knoten in vier Teile auf.

Die nächste Option, *Eingabebild*, besteht darin, ein Image zu verwenden, das dem FX-Map-Knoten bereitgestellt wird. Der FX-Map-Knoten akzeptiert Farben oder Graustufenbilder, die als Hintergrund oder als Ersatz für eines der integrierten Muster verwendet werden können. Bitte beachten Sie, dass der Quadrant-Knoten ein Graustufen-Eingabebild nur in einer Graustufen-Fx-Map rendern kann und umgekehrt ein Farb-Eingabebild nur in einer Farb-FX-Map rendern kann. Wenn Sie Farbtypen mischen möchten, müssen Sie Ihre Eingaben vorher im Graf konvertieren.

Zum Schluss kannst du zwischen den verfügbaren Mustern wählen: Square, Disc, Paraboloid, Bell, Gaussian, Dorn, Pyramide, Ziegel, Abstufung, Waves, Halbglocke, Rändelglocke, Mondsichel und Kapsel.

Zusätzlicher Hinweis: Sie haben die Möglichkeit, eine dynamische Funktion in diesem Parameter zu erstellen, diese funktioniert jedoch nur in Substance 3D Designer. Um Zugriff auf die Bildeingabe durch eine dynamische Funktion zu haben, müssen Sie Werte von 256 (Bildeintrag 1) bis zu höheren Werten (257 für Bildeintrag 2 usw.) verwenden.

### Mustertypen.

Muster sind Graustufen. Einige können mit dem Parameter *Mustervariation* ein wenig geändert werden.

Viele der integrierten Muster weisen eine Form von radialer Verlaufsfüllung oder Ähnliches auf. Das macht sie sehr nützlich für viele Rauschen und Muster. Andere Muster wie &quot;Ziegel&quot;, &quot;Disc&quot; und &quot;Quadrat&quot; sind einfache, flache Formen.

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

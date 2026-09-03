---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Iterieren in FXMaps, um sich wiederholende Muster und prozedurale Variationen in Ihren Materialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Der Knoten "Iterieren"
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# Der Knoten &quot;Iterieren&quot;

Mit dem Knoten &quot;Iterieren&quot; können Sie die Bilder eines Quadrant-Knotens multiplizieren und ist im Grunde ein &quot;Repeater&quot;-Knoten. Ein Quadrantenknoten mit einer Tiefe von 1 würde normalerweise 4 Quadranten ausgeben. Mit dem Knoten &quot;Iterieren&quot; können Sie die Ausgabebilder beliebig oft wiederholen, wobei jeder Satz von Wiederholungen separat behandelt wird.

Der Knoten &quot;Iterieren&quot; hat keine anderen Eigenschaften als &quot;Wie Wiederholungen möchten Sie?&quot;. -Parameter. Das Ergebnis ist, dass die neuen Bilder standardmäßig einfach überlagert und mit den Bildern vermischt werden, die vom Quadrant-Knoten erzeugt werden.

Der Knoten Iterieren wiederholt das empfangene Eingabebild. Die Anzahl der Wiederholungen wird durch die Eigenschaft Iterationen definiert:

Der Schlüssel zur Verwendung des Iterate-Knotens besteht darin, dass alle dynamischen Funktionen, die mit jedem wiederholten Bild verknüpft sind, ebenfalls verarbeitet werden. Das bedeutet, dass jede Wiederholung ihre eigenen einzigartigen Einstellungen haben kann. Sie können die Funktionsweise des Knotens &quot;Iterieren&quot; mithilfe der Eigenschaft &quot;Zufallsverteilung&quot; ändern. Sie können auch auf die Systemvariable *$number* in Ihren dynamischen Funktionen zugreifen, um zu bestimmen, welche Wiederholung gerade gerendert wird, und das Ergebnis der Funktion entsprechend ändern.

Beispiel: Wenn Sie auf jedes Bild in einem Quadrantenknoten eine zufällige Drehung anwenden und dann die Ausgabe dieses Quadrantenknotens an die aktive Eingabe eines Iterationsknotens weiterleiten, hat jedes der wiederholten Bilder ebenfalls seine eigene zufällige Drehung.

Alle im Quadrant-Knoten verfügbaren dynamischen Merkmale gelten auch für wiederholte Bilder, die vom Iterate-Knoten erzeugt werden. Der Knoten dupliziert den Quadrant-Knoten auf derselben Ebene, statt eine weitere Tiefe hinzuzufügen.

## Der Pass-Through-Connector

Jeder Iterate-Knoten verfügt über zwei Connectors entlang seiner Basis. Der linke Anschluss ist ein Pass-Through-Anschluss. Das Bild, das er erhält, wird direkt an den Ausgangsanschluss des Knotens weitergeleitet, wo es mit allen wiederholten Bildern überblendet wird:

Beachten Sie, dass das Pass-Through-Bild immer unberührt bleibt, unabhängig von der Einstellung des Parameters &quot;Iteration&quot;.

![](the-iterate-node.resources/the-iterate-node-01.jpg)

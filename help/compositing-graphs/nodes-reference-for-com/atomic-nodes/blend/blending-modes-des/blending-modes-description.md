---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über die in Substance 3D Designer verfügbaren Füllmethoden zum Kombinieren von Texturen mit verschiedenen Compositing-Effekten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Füllmethoden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 989234054615406114d2f7664ebee6f8c86f4bf2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# Füllmethoden

Der Knoten &quot;[Blend](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)&quot; bietet die folgenden Füllmethoden:

## Kopieren

Der Mischmodus &quot;*Kopieren*&quot; platziert den Vordergrund einfach über den Hintergrund.

![Füllmethode: Kopieren](blending-modes-description.resources/image2015-8-20-9-38-0.png "Füllmethode: Kopieren"){zoomable="yes"}

Bei Farbbildern wird der Alphakanal standardmäßig bei der Deckkraft berücksichtigt.

Dies kann mit dem Parameter &quot;Alpha-Überblendung&quot; geändert werden.

![Füllmethode: Kopieren (2)](blending-modes-description.resources/image2015-8-20-14-15-29.png "Füllmethode: Kopieren (2)"){zoomable="yes"}

## Hinzufügen (Linear abwedeln)

Der Mischmodus &quot;*Hinzufügen*&quot; fügt den Vordergrundeingabewert zu jedem entsprechenden Pixel im Hintergrund hinzu.

![Füllmethode: Hinzufügen (Linear abwedeln)](blending-modes-description.resources/image2015-8-20-9-38-19.png "Füllmethode: Hinzufügen (Linearer Abwedler)"){zoomable="yes"}

## Subtrahieren

Der Mischmodus &quot;*Substance*&quot; zieht den Vordergrundeingabewert von jedem entsprechenden Pixel im Hintergrund ab.

Wenn das Ergebnis der Subtraktion kleiner als 0 ist, wird der Wert auf 0 begrenzt, wodurch reines Schwarz entsteht.

![Füllmethode: Substrakt](blending-modes-description.resources/image2015-8-20-9-38-35.png "Füllmethode: Substrakt"){zoomable="yes"}

## Multiplizieren

Der Mischmodus *Multiplizieren* multipliziert den Hintergrundeingabewert mit jedem entsprechenden Pixel im Vordergrund.

Da der Wert jedes Pixels zwischen 0 und 1 liegt, ist das Ergebnis im Vergleich zum Original immer gleich oder kleiner (dunkler).

![Füllmethode: Multiplizieren](blending-modes-description.resources/image2015-8-20-9-38-53.png "Füllmethode: Multiply"){zoomable="yes"}

## Addieren/Subtrahieren

Der Mischmodus &quot;*Sub* hinzufügen&quot; funktioniert wie folgt:

* Vordergrundpixel, deren Wert größer als 0,5 ist, werden zu ihren jeweiligen Hintergrundpixeln hinzugefügt.
* Vordergrundpixel, deren Wert kleiner als 0,5 ist, werden von ihren jeweiligen Hintergrundpixeln subtrahiert.

![Füllmethode: Sub](blending-modes-description.resources/image2015-8-20-9-39-11.png "Füllmethode hinzufügen: Sub"){zoomable="yes"} hinzufügen

## Maximal (Aufhellen)

Der Mischmodus *Max* wählt den höheren Wert zwischen Hintergrund und Vordergrund aus.

![Füllmethode: Max. (Aufhellen)](blending-modes-description.resources/image2015-8-20-9-40-12.png "Füllmethode: Max. (Aufhellen)"){zoomable="yes"}

## Min. (Abdunkeln)

Im Mischmodus &quot;*Min*&quot; wird der niedrigere Wert zwischen Hintergrund und Vordergrund ausgewählt.

![Füllmethode: Min (Abdunkeln)](blending-modes-description.resources/image2015-8-20-9-40-31.png "Füllmethode: Min (Abdunkeln)"){zoomable="yes"}

## Wechseln

Der Mischmodus &quot;*Switch*&quot; ähnelt dem Kopiermodus, mit einem *entscheidenden* Unterschied:

* &#39;Deckkraft&#39; auf 0 eingestellt: Der Datenstrom der Knoten, die mit dem Vordergrundeingang *verbunden sind, wird nicht berechnet*.
* &#39;Deckkraft&#39; auf 1 eingestellt: Der Datenstrom der Knoten, die mit dem &#39;Background&#39;-Eingang *verbunden sind, wird nicht berechnet*.

Daher kann dieser Modus verwendet werden, um die Leistung Ihres Diagramms zu verbessern.

Die Knoten [Switch](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) und [Switch grayscale](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) sind so eingerichtet, dass sie die Mischknoten in diesen spezifischen Konfigurationen verwenden.

![Füllmethode: Switch](blending-modes-description.resources/image2015-8-20-9-38-0.png "Füllmethode: Switch"){zoomable="yes"}

## Dividieren

Der Mischmodus &quot;*Divide*&quot; teilt den Wert der Hintergrundeingabepixel durch jedes entsprechende Pixel im Vordergrund.

![Füllmethode: Dividieren](blending-modes-description.resources/image2015-8-20-9-41-32.png "Füllmethode: Dividieren"){zoomable="yes"}

## Überlagerung

Der Mischmodus &quot;*Overlay*&quot; kombiniert die Füllmethoden &quot;Multiplizieren&quot; und &quot;Negativ multiplizieren&quot;:

* &#x200B;
  * Wenn der Wert des Pixels der unteren Ebene unter 0,5 liegt, wird eine Füllmethode vom Typ *Multiplizieren* angewendet.
  * Wenn der Wert der unteren Pixelebene über 0,5 liegt, wird eine Überblendung vom Typ *Bildschirm* angewendet.

![Füllmethode: Überlagerung](blending-modes-description.resources/image2015-8-20-9-41-50.png "Füllmethode: Overlay"){zoomable="yes"}

## Negativ multiplizieren

Mit dem Mischmodus &quot;Negativ multiplizieren&quot; werden die Werte der Pixel in den beiden Eingängen invertiert und dann wieder invertiert.

Das Ergebnis ist der entgegengesetzte Effekt zu multiplizieren und ist immer gleich oder höher (heller) im Vergleich zum Original.

![Füllmethode: Negativ multiplizieren](blending-modes-description.resources/image2015-8-20-9-42-11.png "Füllmethode: Bildschirm "){zoomable="yes"}

## Weiches Licht

Der Mischmodus &quot;Weiches Licht&quot; erzeugt je nach Helligkeit der Vordergrundfarbe ein subtiles helleres oder dunkleres Ergebnis.

Beim Mischen von Farben mit einer Helligkeit von mehr als 50 % werden die Hintergrundpixel aufgehellt, während Farben mit einer Helligkeit von weniger als 50 % die Hintergrundpixel abdunkeln.

![Füllmethode: Weiches Licht](blending-modes-description.resources/image2015-8-20-9-42-32.png "Füllmethode: Weiches Licht"){zoomable="yes"}

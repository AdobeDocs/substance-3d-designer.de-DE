---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: Verwenden Sie die Knotenausrichtungswerkzeuge, um Knoten in der Diagrammansicht für sauberere, besser lesbare Diagramme zu organisieren und auszurichten.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Werkzeuge zur Knotenausrichtung
user-guide-description: ''
user-guide-title: ''
source-git-commit: a43ec663c271976e3f472d62026083a04333a401
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# Werkzeuge zur Knotenausrichtung

![Knotenausrichtungssymbolleiste](node-alignment-tools.resources/node-alignment-toolbar.png "Knotenausrichtungssymbolleiste"){zoomable="yes"}

Mit den Knotenausrichtungs-Tools können Sie Knoten in Diagrammen anordnen, um deren Lesbarkeit und Authoring-Erfahrung zu verbessern. Sie bieten Aktionen zum Ausrichten von Knoten, zum gleichmäßigen Verteilen und zum Ausrichten am Raster.

Sie wirken auf die <b> Knoten, die derzeit nur </b> ausgewählt sind.

>[!NOTE]
>
> Tastaturbefehle
> 
> Einige Aktionen verfügen über Tastaturbefehle für den schnellen Zugriff: H, V und S. Sie werden in der folgenden Aktionsliste zwischen Klammern angezeigt.
> 
> Beachten Sie, dass diese alle [-Tastaturbefehle überschreiben, die Knoten &#x200B;](../../../interface/preferences-window/preferences-window.md) zugewiesen sind.

## Ausrichtung

Die Knoten können horizontal und vertikal ausgerichtet werden, wobei für jede Achse drei Modi zur Verfügung stehen:

### Horizontale Ausrichtung

<b>![](node-alignment-tools.resources/node-alignment-h-left.png) Links:</b> Richten Sie die linke Seite der ausgewählten Knoten an der linken Seite des am weitesten links liegenden Knotens aus.

<b>![](node-alignment-tools.resources/node-alignment-h-center.png) Mitte (H):</b> Richten Sie die horizontale Mitte der ausgewählten Knoten an der horizontalen Mitte des sie umschließenden Begrenzungsrahmens aus.

<b>![](node-alignment-tools.resources/node-alignment-h-right.png) Rechts:</b> Richten Sie die rechte Seite der ausgewählten Knoten an der rechten Seite des ganz rechts befindlichen Knotens aus.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: left](node-alignment-tools.resources/node-alignment-left.gif "Knotenausrichtungstools: left"){zoomable="yes"}

*Links*

</td>
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: Mitte](node-alignment-tools.resources/node-alignment-center.gif "Knotenausrichtungswerkzeuge: center"){zoomable="yes"}

*Center*

</td>
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: right](node-alignment-tools.resources/node-alignment-right.gif "Node-Alignment-Tools: right"){zoomable="yes"}

*Rechts*

</td>
</tr>
</table>

### Vertikale Ausrichtung

<b>![](node-alignment-tools.resources/node-alignment-v-top.png) Oben:</b> Richten Sie die obere Seite der ausgewählten Knoten an der oberen Seite des obersten Knotens aus.

<b>![](node-alignment-tools.resources/node-alignment-v-middle.png) Mitte (V):</b> Richten Sie die vertikale Mitte der ausgewählten Knoten an der vertikalen Mitte des sie umschließenden Begrenzungsrahmens aus.

<b>![](node-alignment-tools.resources/node-alignment-v-bottom.png) Unten:</b> Richten Sie die untere Seite der ausgewählten Knoten an der unteren Seite des untersten Knotens aus.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: top](node-alignment-tools.resources/node-alignment-top.gif "Knotenausrichtungswerkzeuge: top"){zoomable="yes"}

*Oben*

</td>
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: Mitte](node-alignment-tools.resources/node-alignment-middle.gif "Knoten-Ausrichtungswerkzeuge: Mitte"){zoomable="yes"}

*Mitte*

</td>
<td style="border: 0;" valign="top">

![Knotenausrichtungstools: unten](node-alignment-tools.resources/node-alignment-bottom.gif "Knoten-Ausrichtungswerkzeuge: bottom"){zoomable="yes"}

*Unten*

</td>
</tr>
</table>

### Stapeln

Mit der <b>Option </b>Stapel ![](node-alignment-tools.resources/node-alignment-stack.png) können Sie <b>Überlappungen </b> bei der Verwendung von Ausrichtungen vermeiden. Diese Option ist standardmäßig aktiviert.

Wenn diese Option aktiviert ist, werden Knoten so weit wie möglich an die Referenzposition verschoben, bis sie mit einem anderen Knoten in der Auswahl kollidieren würden. Dadurch werden sie effektiv in der ausgewählten Achse mit einem Rand von einer mittleren Gitterzelle zwischen jedem Knoten gestapelt.

![Knotenausrichtungstools: Stacking](node-alignment-tools.resources/node-alignment-stacking.gif "Node-Alignment-Tools: Stacking"){zoomable="yes"}

## Distributionen

Knoten können gleichmäßig zwischen den Knoten an jedem Ende der aktuellen Auswahl auf der gewünschten Achse verteilt werden.

<b>![](node-alignment-tools.resources/node-alignment-distribute-h.png) Horizontal:</b> Knoten werden gleichmäßig zwischen dem am weitesten links und dem am weitesten rechts befindlichen Knoten in der Auswahl verteilt.

<b>![](node-alignment-tools.resources/node-alignment-distribute-v.png) Vertikal:</b> Knoten werden gleichmäßig zwischen dem obersten und dem untersten Knoten in der Auswahl verteilt.

Die Distributionen zielen auf <b>gleichmäßige Abstände</b> zwischen den Knoten ab, unabhängig von ihrer Größe.

Wenn die Mittelpunkte mehrerer Knoten perfekt auf der ausgewählten Achse ausgerichtet sind, bleiben sie erhalten und werden <b>als eins</b> in der Verteilung behandelt. Der *größte* der ausgerichteten Knoten wird für die Berechnung des geraden Abstands verwendet.

Wenn die Gesamtgröße der ausgewählten Knoten größer ist als der auf der ausgewählten Achse verfügbare Platz, kann es zu Überschneidungen kommen.

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![Knotenausrichtungstools: Horizontale Verteilung](node-alignment-tools.resources/node-alignment-distribute-h.gif "Knoten-Ausrichtungswerkzeuge: horizontale Verteilung"){zoomable="yes"}

*Horizontal*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Knotenausrichtungstools: Vertikale Verteilung](node-alignment-tools.resources/node-alignment-distribute-v.gif "Knoten-Ausrichtungswerkzeuge: vertikale Verteilung"){zoomable="yes"}

*Vertikal*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## Rasterausrichtung

Mit der Aktion <b>Ausrichten (S) ![](node-alignment-tools.resources/node-alignment-snap.png)</b> wird jeder ausgewählte Knoten so verschoben, dass seine obere linke Ecke auf dem nächstgelegenen Punkt auf dem mittleren Raster liegt.

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Knotenausrichtungstools: Rasterausrichtung](node-alignment-tools.resources/node-alignment-snapping.gif "Knotenausrichtungswerkzeuge: Rasterausrichtung "){zoomable="yes"}

</td>
</tr>
</table>

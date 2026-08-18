---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Erfahre, wie du in Substance 3D Designer Compositing-Grafiken erstellst, um prozedurale Texturen und Material-Workflows zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance-Graphen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Substance-Graphen

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../assets/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[Substance-Diagramme](https://substance3d.adobe.com/) sind der Haupttyp des in Substance 3D Designer erstellten Diagramms. Ihr Zweck ist es, <b>2D-Bilddaten</b> zu generieren und zu verarbeiten, die nicht auf eine festgelegte Auflösung, Farbe oder Form beschränkt sind. Sie sind als äußerst vielseitige Bildverarbeitungs- und Generierungswerkzeuge gedacht und nicht nur als statische, voreingestellte Ergebnisse.

Die Ergebnisse können in Form eines einfachen Schwarz-Weiß-Musters vorliegen, eines Filters, der nur auf anderen Bildern ausgeführt wird und keinen Inhalt für sich selbst generiert, oder sogar in Form eines vollwertigen prozeduralen Materials mit mehreren Kanälen.

Substance-Graphen sind [&#x200B; der am weitesten unterstützte Diagrammtyp &#x200B;](../getting-started/overview/overview.md) und können exportiert und in einer Vielzahl von verschiedenen Workflows verwendet werden.

</td>
</tr>
</table>

## Beispiele

Im Folgenden finden Sie einige typische Beispiele für häufige Anwendungsfälle.

+++Einfache Form
![Einfache Form im Substance-Diagramm](../assets/simpleshape.png "Einfache Form im Substance-Diagramm"){width="512px"}



Eine einfache Maskenform für einen Aufkleber wird erstellt, indem [ein Textstück](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) und ein [Datenträgerform](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md) generiert werden, [die Kante](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) von der Festplatte extrahiert wird und diese schließlich [zusammengemischt werden](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), bevor sie als endgültige [Ausgabe](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt werden.

Der Text mit der Nummer oder die Thickness der Kante kann extern belichtet werden, um das Diagramm dynamischer zu gestalten.

+++

+++Einstellungsfilter
![Korrekturfilter im Substance-Diagramm](../assets/simplefilter.png "Korrekturfilter im Substance-Diagramm"){width="512px"}



Ein Filterdiagramm nimmt eine normale Karte als [Eingabe](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) (mit einer benutzerdefinierten Vorschau), [konvertiert sie in Krümmung](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) und [passt den Kontrast](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) an, um eine Maske mit konvexen Kanten als endgültige [Ausgabe](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) zu erstellen.

Die im Histogramm eingestellten Kontrastwerte können belichtet werden, was dies zu einem einfachen, aber nützlichen Filter in Kombination mit dem dynamischen Eingangs-Slot macht.

+++

+++Vollständiges Material
![Vollständiges Material im Substance-Diagramm](../assets/simplematerial.png "Vollständiges Material im Substance-Diagramm"){width="512px"}



Ein komplizierteres Diagramm[fügt zwei Basismaterialien zusammen](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Eins[Basismaterial](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) ist einfach gehalten, das andere verwendet einige benutzerdefinierte Eingaben, um Interesse hinzuzufügen. Eine Maske wird verwendet, um zu bestimmen, welches der beiden Materialien an welcher Stelle angezeigt wird, bevor es als endgültige [Ausgaben](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) festgelegt wird.

In diesem Beispiel werden [Verknüpfungserstellungsmodi](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) zur Vereinfachung der Verwendung mehrerer Verknüpfungen verwendet.

+++

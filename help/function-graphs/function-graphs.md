---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie in Designer Substance-Funktionsdiagramme erstellen und verwenden, um benutzerdefinierte Funktionen und wiederverwendbare Knotennetzwerke zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance-Funktionsdiagramme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Substance-Funktionsdiagramme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](function-graphs.resources/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[Substance-Funktionsdiagramme](https://substance3d.adobe.com/) <b>verarbeiten Einzelwerte</b> (Ganzzahlen, Gleitkommawerte, Vektoren) anstelle von Bilddaten (ganze Pixelsätze). Funktionen sind auch Diagramme mit Knotennetzwerken, aber die [Nodes verwendet](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) und die Schnittstelle unterscheidet sich von [normalen Substance-Diagrammen](../compositing-graphs/substance-compositing-graphs.md). Der Workflow basiert vollständig auf <b>mathematischen Vorgängen</b> und zeigt keine Bildvorschau-Miniaturansichten an. Dadurch wird die <b>Arbeit mit Substance 3D Designer </b> um einiges weiter entwickelt.

Funktionen können in vielen verschiedenen Kontexten verwendet werden, wobei die wichtigsten darin bestehen, das Verhalten von [einem verfügbar gemachten Parameter](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) zu ändern, das Verhalten von [Pixelprozessoren](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) oder [FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) zu verfassen und [Werte in Substance-Graphen](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md) zu verwenden.

</td>
</tr>
</table>

## Beispiele

Im Folgenden finden Sie einige Beispiele aus häufig verwendeten Anwendungsfällen für Funktionen.

### Einfache Funktion

![](function-graphs.resources/lerpfunction_1.png)

Eine einfache Funktion im Kontext eines exponierten Parameters. Es erhält einen Eingangs-Gleitkommawert namens &quot;Intensität&quot;, der von 0 bis 1 geht (ein Bereich, der leicht zu verstehen ist) und weist ihn einem festgelegten Bereich von 0,1 bis 0,8 neu zu. Wenn der Benutzer die Intensität auf 0 setzt, wird intern 0,1 verwendet, wenn die Benutzeroberfläche auf 1 gesetzt ist, 0,8 wird verwendet und jeder Wert dazwischen wird linear interpoliert. Dieser Funktionstyp wird häufig verwendet, wenn [&#x200B; Parameter &#x200B;](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) verfügbar macht, aber benutzerdefinierte Funktionen verwendet werden.

Diese Funktion könnte auch als *lerp(0.1, 0.8, Intensity)* in einem Pseudocode ähnlich wie HLSL oder GLSL geschrieben werden.

### erweiterte Funktion

![](function-graphs.resources/pixel-function_1.png){width="545px"}

Diese erweiterte Funktion zeigt die inneren Funktionen eines [Pixelprozessors](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), der zum Anpassen des Farbtons einer Farbmapeingabe basierend auf der Intensität einer zweiten Graustufenmaskeneingabe vorgesehen ist.

Es erfasst beide Eingaben mit der Variablen &quot;$pos&quot; des Systems, entfernt dann das Alpha, konvertiert den Farbwert in HSL und ändert die Farbtonkomponente, indem es mit dem aufgenommenen Graustufenwert multipliziert wird. Anschließend wird der Vektor neu zusammengestellt, der HSL-Farbton wird wieder in RGB konvertiert und das Alpha für die endgültige Ausgabe wieder hinzugefügt.

im Pseudo-Code wäre dies eine viel kompliziertere Funktion, die nicht auf eine einzelne Zeile passen würde.

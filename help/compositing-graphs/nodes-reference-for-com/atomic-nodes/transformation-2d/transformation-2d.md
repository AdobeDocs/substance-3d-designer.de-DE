---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "2D-Transformation", um 2D-Transformationen auf Texturen anzuwenden, einschließlich Translation, Drehung und Skalierung.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 2D-Transformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# 2D-Transformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Transformation 2D](transformation-2d.resources/transformation-2d-01.png "Atomknoten: Transformation 2D"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Wendet eine 2D-Transformationsmatrix auf ein Bild an: Übersetzung, Drehung, Skalierung, Symmetrie und Verformung.

Sie ähnelt der Funktion &quot;Transformieren&quot; (Strg-T) in Photoshop oder der Verwendung des 2D-Zuordnungsmanipulators in Substance 3D Painter.

</td>
</tr>
</table>

Dies ist ein äußerst nützlicher und weit verbreiteter Knoten, der es ermöglicht, die Kachelung zu erhöhen, die Kachelung zu entfernen, ein Bild an einer bestimmten Position zu platzieren, einen Eingang zu dehnen oder zu quetschen, usw.

Es kann jedoch für bestimmte Anwendungen nicht perfekt geeignet sein, sodass die folgenden Knoten von Interesse sein können: [Safe Transformieren](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md), [Non-Square Transformieren](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md), [Quad Transformieren](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) und [Trapezoid Transformieren](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Deaktivieren der Unterteilung
> 
> Legen Sie die [Vererbung-Methode](../../../../glossary/glossary.md) des [Basisparameters &#x200B;](../../../../glossary/glossary.md) für den &#39;Kachelung-Modus&#39; auf &#39;Absolut&#39; fest. Dann können Sie den Parameterwert auf &#39;Keine Kachelung&#39; festlegen:
> 
> ![](transformation-2d.resources/transformation-2d-02.png)

>[!NOTE]
>
> Die Werte für Skalierung und Drehung in den Eigenschaften des Knotens sind *relativ zur aktuellen Transformation* und werden erst auf die 2D-Ansicht angewendet, wenn Sie auf die Schaltfläche &quot;Anwenden&quot; klicken.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Transformationsmatrix</b> *Float4* | Öffne die zugrunde liegende Transformationsmatrix zur direkten Bearbeitung. Ermöglicht es Ihnen, die Drehung und Skalierung zu ändern. Kann auch durch das Gizmo in der 2D-Ansicht angepasst werden.   Warnung: Sie korrelieren nicht direkt mit der Ansicht und sind relative Anpassungen, die in Schritten angewendet werden können. |
| <b>Offset</b> *Float2* | Definiert den 2D-Versatz des Bilds. Ermöglicht das Ändern der Position oder des Versatzes. Kann auch durch das Gizmo in der 2D-Ansicht angepasst werden.   Bezieht sich direkt auf die Ausgabe der 2D-Ansicht. |
| <b>MIPMAP-Modus</b> *Integer* | Ermöglicht den Wechsel zu einer manuellen [Mipmap](../../../../glossary/glossary.md)-Ebene, die Artefakte in einem Bild mithilfe von Filterungen zur Textur reduziert. |
| <b>Mipmap-Stufe</b> *Integer* | Legt die zu verwendende [mipmap](../../../../glossary/glossary.md)-Ebene fest.     *Verfügbar, wenn &#39;MIPMAP-Modus&#39; auf &#39;Manuell&#39; festgelegt ist* |
| <b>Matte Farbe</b> *Float4* | Die Farbe, die beim Anordnen der Transformation als Hintergrund verwendet wird, ist deaktiviert. Legt die Farbe fest, die verwendet wird, wenn die transformierte Eingabe einen Bereich der Ausgabe nicht abdeckt.   Kann transparent gemacht werden, wenn mit RGBA-Farbe gearbeitet wird. |
| <b>Filtern</b> *Integer* | Legt die verwendete Neuberechnungsmethode fest. Funktioniert nicht besonders gut, wenn die Mipmap-Stufe reduziert wird. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Das Bild, das transformiert werden soll. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

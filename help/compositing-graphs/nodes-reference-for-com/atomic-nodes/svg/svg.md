---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ''
description: Verwenden Sie den SVG -Knoten, um SVG-Vektorgrafiken als Texturen zu importieren und zu rendern, um skalierbare Grafikelemente zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# SVG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: SVG](svg.resources/comp_svg_1.png "Atomknoten: SVG"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Rendert ein [SVG-Image](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) als Bitmap. Mit anderen Worten, ordnet Vektorformen Pixeln zu.

Es gibt verschiedene Möglichkeiten, diesen Knoten zu erstellen. Für alle diese Möglichkeiten müssen Sie [den Unterschied zwischen dem Verknüpfen und dem Importieren von Ressourcen](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) verstehen.

</td>
</tr>
</table>

Sie können den Knoten entweder von Grund auf neu erstellen oder eine SVG-Datei in der Diagrammansicht ablegen.

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
> Generierte oder importierte SVG können mit den [Vektorbearbeitungswerkzeugen](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) im Dock [2D view](../../../../interface/2d-view/2d-view.md) bearbeitet werden.

>[!IMPORTANT]
>
> Dieser Knoten ist von einer externen Ressource abhängig. Daher müssen bei der Arbeit mit diesen Knoten einige Punkte beachtet werden:
> 
> * SVG-Knoten können entweder Farbe oder Graustufen zurückgeben, aber standardmäßig Farbe, selbst wenn die Ressource ein Graustufenvektor ist. Dies kann sich auf die Leistung und Komplexität des Diagramms auswirken. Stellen Sie daher immer sicher, dass Sie bei Bedarf zum [Graustufen-Farbmodus](#parameters) wechseln.
> * Durch das Löschen eines SVG-Knotens wird die [SVG-Ressource](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) in Ihrem [Paket](../../../../glossary/glossary.md) nicht gelöscht. Sie müssen dies manuell im [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) tun.
> * SVG-Formen werden [in Geometrie/Polygone tesseliert](../../../../glossary/glossary.md), dann *gerastert*, um in Substance-Graphen als Bitmaps verwendet zu werden. Die für diese Vorgänge verwendete Technologie unterstützt nicht mehrere Vektoreigenschaften wie Konturen. Weitere Informationen zu diesen Einschränkungen [finden Sie hier](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> SVG-Formen werden [in Geometrie/Polygone tesseliert](../../../../glossary/glossary.md), dann *gerastert*, um in Substance-Graphen als Bitmaps verwendet zu werden.
> 
> Die für diese Vorgänge verwendete Technologie unterstützt nicht mehrere Vektoreigenschaften wie Konturen.
> 
> Weitere Informationen zu diesen Einschränkungen [finden Sie hier](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Beispiele

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Bestimmt den Ausgabetyp des Knotens, der entweder in Farbe oder in Graustufen zurückgegeben wird. |
| <b>Hintergrundfarbe</b> *Farbe/Graustufen* | Legt die Hintergrundfarbe des Ausgabebilds fest, die für Bereiche verwendet werden soll, die nicht von einer Vektorform abgedeckt sind.   *Wird von der Eingabe &quot;[Hintergrund](#inputs)&quot; überschrieben, wenn diese Eingabe verbunden ist.* |
| <b>PKG-Ressourcenpfad</b> *Zeichenfolge* | Pfad zur [SVG-Ressource](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), auf die vom Knoten verwiesen wird.   Es wird empfohlen, eine Ressource nicht manuell einzugeben, sondern entweder aus dem Explorer zu kopieren und in das Parametertextfeld einzufügen, oder eine Bitmapressource direkt aus dem [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) auf den SVG-Knoten im Diagramm zu ziehen. |

## Werkzeuge zur Vektorbearbeitung.

Vektorformen können in Designer bearbeitet werden. Weitere Informationen zu den Bearbeitungswerkzeugen in [diesem Abschnitt](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Hintergrund</b> *Graustufen/Farbe* PRIMÄR | Legt die Hintergrundfarbe des Ausgabebilds fest, die für Bereiche verwendet werden soll, die nicht von einer Vektorform abgedeckt sind.   *Überschreibt den Parameter &quot;[Hintergrundfarbe](#parameters)&quot;, wenn eine Verbindung besteht.* |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

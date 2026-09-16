---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ""
description: Verwenden Sie den SVG -Knoten, um SVG-Vektorgrafiken als Texturen zum Erstellen skalierbarer Grafikelemente zu importieren und zu rendern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---

# SVG

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Elementare Knoten: SVG](svg.resources/comp_svg_1.png "Elementare Knoten: SVG"){width="100%"}

<b>In:</b> Elementare Knoten

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Rendert ein [SVG-Image](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) als Bitmap. Mit anderen Worten, ordnet Vektorformen Pixeln zu.

Es gibt verschiedene Möglichkeiten, diesen Knoten zu erstellen. Für alle diese Möglichkeiten müssen Sie [den Unterschied zwischen dem Verknüpfen und dem Importieren von Ressourcen](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) verstehen.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="svg.resources/svg-tooltip.gif" alt="SVG-QuickInfo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Sie können den Knoten entweder von Grund auf neu erstellen oder indem Sie eine SVG-Datei in die Graphansicht ablegen.


>[!TIP]
>
> Generierte oder importierte SVG können mit den [Vektorbearbeitungswerkzeugen](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) im [2D-Ansicht](../../../../interface/2d-view/2d-view.md)-Dock bearbeitet werden.

>[!IMPORTANT]
>
> Dieser Knoten ist von einer externen Ressource abhängig. Daher müssen bei der Arbeit mit diesen Knoten einige Punkte beachtet werden:
> 
> * SVG-Knoten können entweder Farbe oder Graustufen zurückgeben, aber standardmäßig Farbe, selbst wenn die Ressource ein Graustufenvektor ist. Dies kann sich auf die Leistung und Komplexität des Grafen auswirken. Stellen Sie daher immer sicher, dass Sie bei Bedarf zum [Graustufen-Farbmodus](#parameters) wechseln.
> * Durch das Löschen eines SVG-Knotens wird die [SVG-Ressource](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) in Ihrem [Paket](../../../../glossary/glossary.md) nicht gelöscht. Sie müssen dies manuell im [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) tun.
> * SVG-Formen werden [in Geometrie/Polygone tesseliert](../../../../glossary/glossary.md) und anschließend *gerastert*, um in Substance-Grafen als Bitmaps verwendet zu werden. Die für diese Vorgänge verwendete Technologie unterstützt nicht mehrere Vektoreigenschaften wie Konturen. Weitere Informationen zu diesen Einschränkungen [finden Sie hier](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> SVG-Formen werden [in Geometrie/Polygone tesseliert](../../../../glossary/glossary.md) und anschließend *gerastert*, um in Substance-Grafen als Bitmaps verwendet zu werden.
> 
> Die für diese Vorgänge verwendete Technologie unterstützt nicht mehrere Vektoreigenschaften wie Konturen.
> 
> Weitere Informationen zu diesen Einschränkungen [finden Sie hier](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).


## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolesche Wert* | Bestimmt den Ausgabetyp des Knotens, der entweder in Farbe oder in Graustufen zurückgegeben wird. |
| <b>Hintergrundfarbe</b> *Farbe/Graustufen* | Legt die Hintergrundfarbe des Ausgabebilds fest, die für Bereiche verwendet werden soll, die nicht von einer Vektorform abgedeckt sind.   *Wird von der Eingabe &quot;[Hintergrund](#inputs)&quot; überschrieben, wenn diese Eingabe verbunden ist.* |
| <b>PKG-Ressourcenpfad</b> *Zeichenfolge* | Pfad zur [SVG-Ressource](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), auf die vom Knoten verwiesen wird.   Es wird empfohlen, eine Ressource nicht manuell einzugeben, sondern entweder aus dem Explorer zu kopieren und in das Parametertextfeld einzufügen, oder eine Bitmapressource direkt aus dem [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) auf den SVG-Knoten im Diagramm zu ziehen. |

## Werkzeuge zur Vektorbearbeitung.

Vektorformen können in Designer bearbeitet werden. Weitere Informationen zu den Bearbeitungswerkzeugen in [diesem Abschnitt](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Hintergrund</b> *Graustufen/Farbe* PRIMÄR | Legt die Hintergrundfarbe des Ausgabebilds fest, die für Bereiche verwendet werden soll, die nicht von einer Vektorform abgedeckt sind.   *Überschreibt den Parameter &quot;[Hintergrundfarbe](#parameters)&quot;, wenn eine Verbindung besteht.* |


## Beispiele

*Demnächst verfügbar.*

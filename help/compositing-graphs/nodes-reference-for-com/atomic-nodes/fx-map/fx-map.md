---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: Verwenden Sie den FX-Map-Knoten, um Funktionsdiagramme auf Texturen anzuwenden, um prozedurale Muster und Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: FX-Map](fx-map.resources/fxmap.png "Atomknoten: FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Die FX-Map kann eine Bild- oder Mustereingabe immer wieder replizieren und unterteilen und die Verteilung jedes Musters über Parameter und logische Funktionen steuern.

Es ist einer der mächtigsten atomaren Knoten, sowie der komplexeste Knoten in der Anwendung.

</td>
</tr>
</table>

Ähnlich wie beim [Pixelprozessor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) liegt es an Ihnen, die Funktionen zu definieren und zu erstellen, die das Verhalten und die Ausgabe dieses Knotens bestimmen.

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
> Sehen Sie sich den [dedizierten Leitfaden](../../../../function-graphs/fxmaps/fxmaps.md) an, um mehr über den FX-Map-Prozess zu erfahren.

>[!IMPORTANT]
>
> Es wird empfohlen, sich mit allen Aspekten der Software vertraut zu machen und keine Probleme beim Erstellen von [mathematischen Funktionen](../../../../function-graphs/function-graphs.md) für Parameter zu haben, bevor Sie versuchen, den FX-Map-Knoten zu verwenden.

## Beispiele

## Parameter

Beachten Sie, dass im Gegensatz zu anderen Knoten der größte Teil des Verhaltens einer FX-Map nicht durch die Parameter bestimmt wird, sondern [ durch Bearbeiten der FX-Map-Funktionen](../../../../function-graphs/fxmaps/fxmaps.md) innerhalb der FX-Map.

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. Die Farbe ist viel langsamer als in Graustufen. |
| <b>Hintergrund</b> *Gleitend/Gleitend4* | Legt die Anfangsfarbe des Hintergrunds fest, mit der die Ergebnisse zusammengefügt werden. |
| <b>Renderregion</b> *Float4* | Ermöglicht es Ihnen, den ersten Pixelbereich für jede Seite der FX-Map festzulegen, was zu einem Dehnungseffekt führt. |
| <b>Kachelbereich</b> *Float4* | Ermöglicht das Versetzen des Kachelabstands der FX-Map. |
| <b>Außerhalb abrufen</b> *Boolescher Wert* | Führt eine Optimierung durch [Auslesen von ](../../../../glossary/glossary.md) Mustern durch, die außerhalb des normalen Bereichs liegen. |
| <b>Raueit</b> *Gleitend* | Funktioniert als Tiefe- und Deckkraftmultiplikator. Es wendet eine Voreinstellung auf den FX-Map-Mischprozess an. |
| <b>Globale Deckkraft</b> *Gleitend* | Legt die globale Deckkraft der Ausgabe der FX-Map fest. |

## FX-Map-Handbuch

*Demnächst verfügbar.*

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Hintergrund</b> *Graustufen/Farbe* PRIMÄR | Die Hintergrundfarbe des Ausgabebilds. |
| <b>Eingabebild #</b> *Graustufen/Farbe* |  |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

![](fx-map.resources/image2015-9-10-17-28-32.png)

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "FX-Map", um Funktions-Grafen auf Texturen anzuwenden, die prozedurale Muster und Effekte erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: FX-Map](fx-map.resources/fxmap.png "Elementare Knoten: FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Der FX-Map kann eine Bild- oder Mustereingabe immer wieder replizieren und unterteilen und die Verteilung jedes Musters über Parameter und Logikfunktionen steuern.

Er ist einer der leistungsstärksten elementare Knoten und der komplexeste in der Anwendung.

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
> Sehen Sie sich das [dedizierte Handbuch](../../../../function-graphs/fxmaps/fxmaps.md) an, um mehr über den FX-Map-Prozess zu erfahren.

>[!IMPORTANT]
>
> Es wird empfohlen, sich mit allen Aspekten der Software vertraut zu machen und keine Probleme beim Erstellen von [mathematischen Funktionen](../../../../function-graphs/function-graphs.md) für Parameter zu haben, bevor Sie versuchen, den FX-Map-Knoten zu verwenden.

## Beispiele

## Parameter

Beachten Sie, dass im Gegensatz zu anderen Knoten der größte Teil des Verhaltens eines FX-Map nicht durch die Parameter bestimmt wird, sondern [&#x200B; durch Bearbeiten der FX-Map-Funktionen](../../../../function-graphs/fxmaps/fxmaps.md), die sich darin befinden.

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolesche Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. Die Farbe ist viel langsamer als in Graustufen. |
| <b>Hintergrund</b> *Fließkommazahl/Fließkommazahl4* | Legt die Anfangsfarbe des Hintergrunds fest, mit der die Ergebnisse zusammengefügt werden. |
| <b>Renderregion</b> *Fließkommazahl4* | Ermöglicht es Ihnen, den ersten Pixelbereich für jede Seite des FX-Map festzulegen, was zu einem dehnend Effekt führt. |
| <b>Region der Kachelung</b> *Fließkommazahl4* | Ermöglicht das Versetzen der Kachelung des FX-Map. |
| <b>Außerhalb abrufen</b> *Boolesche Wert* | Führt eine Optimierung durch [Auslesen von &#x200B;](../../../../glossary/glossary.md) Mustern durch, die außerhalb des normalen Bereichs liegen. |
| <b>Rauheit</b> *Gleitend* | Funktioniert als Tiefe- und Deckkraftmultiplikator. Es wendet eine Voreinstellung auf den FX-Map-Mischprozess an. |
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

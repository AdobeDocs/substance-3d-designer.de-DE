---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Relief , um Reliefeffekte auf Texturen zu erzeugen, mit denen Sie Oberflächendetails Tiefe und Relief hinzufügen können.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Relief
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 9%

---


# Relief

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Relief](../../../../assets/comp_emboss_1.png "Elementare Knoten: Relief"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Wendet einen Prägeeffekt an, indem die Seiten der Formen in einem Bild aus einer angegebenen Lichtquellenrichtung beleuchtet werden.

Das heißt, der Node führt eine einfache 2D-Schattierung auf der Basis von 2 Eingängen durch und simuliert so Lichtreflexionen, die auf eine Fläche fallen, mit Height und Tiefe.

</td>
</tr>
</table>

Dieser Knoten wird nicht oft für PBR-ähnliche Projekte verwendet, kann aber in bestimmten Fällen verwendet werden, wenn Sie eine einfache, Baking geführt Beleuchtung in Ihrer Textur wünschen. Alternativ bieten [Relief With Gloss](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) und [Uber Relief](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) eine ähnliche, aber umfassendere Funktionalität.

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

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Fließkommazahl* | Passt die globale Intensität des Beleuchtungseffekts an.   Legt die Intensität des Bildes des Heights und damit die Stärke des Beleuchtungseffekts fest. |
| <b>Lichtwinkel</b> *Fließkommazahl* | Legt den Winkel fest, in dem das Licht simuliert wird.   Definiert den Beleuchtungswinkel der Markierung des geprägten Bildes. |
| <b>Markierungsfarbe</b> *Fließkommazahl/Fließkommazahl4* | Legt die Farbe der Bereiche fest, die zum Lichtwinkel zeigen.   Legt die Hervorhebungsfarbe fest, wenn das Eingabebild eine Farbe ist. |
| <b>Schattenfarbe</b> *Fließkommazahl/Fließkommazahl4* | Legt die Farbe der Bereiche fest, die vom Lichtwinkel weg zeigen.   Legt die Farbe der schattierten Bereiche des geprägten Bildes fest. |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* PRIMÄR | Stellt die unschattierten Grundfarben bereit. Betrachte es als eine Art diffuse oder Grundfarben-Textur. |
| <b>Intensitätseingabe</b> *Graustufen* | Stellt die Höhenkarte dar, mit der die Beleuchtung der Oberfläche berechnet wird. Schwarz ist niedrig und Weiß ist hoch. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen/Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

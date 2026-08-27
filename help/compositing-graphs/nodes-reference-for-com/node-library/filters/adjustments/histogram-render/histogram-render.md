---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Histogramm rendern , um Histogrammdaten als Textur für die Analyse und das Debuggen zu visualisieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendern von Histogrammen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# Rendern von Histogrammen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Anisotropes Kuwahara-Graustufen-Symbol](../../../../../../assets/histogram_render.png "Anisotropes Kuwahara-Graustufen-Symbol"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet das Histogramm für ein Graustufenbild.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen* PRIMÄR | Das Bild, für das das Histogramm gezeichnet werden soll. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Die Histogrammvisualisierung, die aus dem Eingangsbild berechnet wurde. |

## Parameter

|  |  |
| --- | --- |
| <b>Histogrammauflösung</b> *Integer* | Die Breite des Histogramms. Ein höherer Wert ermöglicht eine feinere Wertverteilung.   Verfügbare Auflösungen sind in Pixeln:  256, 512, 1024, 2048, 4096 |
| <b>Automatische Skalierung</b> *Boolescher Wert* | Wenn &quot;True&quot; festgelegt ist, wird das Histogramm neu zugeordnet, damit das gesamte Height des Bildes verwendet werden kann.   Wenn &quot;False&quot; festgelegt ist, verwendet jede Spalte so viele Pixel im Height, wie ein Wert im Eingabebild vorkommt. |
| <b>Skalierung</b> *Gleitend* | Skaliert das Histogramm vertikal, wobei der Wert 1 das gesamte Height des Histogramms ist. |
| <b>Sampling</b> *Integer* | Die Methode zum Filtern des Histogrammbilds, die sich auf das Ergebnis auswirkt, wenn die Histogrammauflösung und die Renderauflösung nicht übereinstimmen:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilinear:</b> wendet die bilineare Filterung auf das Histogramm an, was zu interpolierten Punkten führt</li> <li data-preserve-html="true"><b>Nächster Wert:</b> berechnet das nächste Pixel ohne Filterung, was zu flachen Schritten führt</li> </ul> |
| <b>Y-Achse spiegeln</b> *Boolescher Wert* | Wenn &quot;True&quot;, spiegelt das Histogramm vertikal. |

## Beispiele

![Histogramm-Rendering: Beispiel 1](../../../../../../assets/histogram_render_example_1.png "Histogramm-Rendering: Beispiel 1"){zoomable="yes"}

![Histogramm-Rendering: Beispiel 2](../../../../../../assets/histogram_render_example_2.png "Histogramm-Rendering: Beispiel 2"){zoomable="yes"}

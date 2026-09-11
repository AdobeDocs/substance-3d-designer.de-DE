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
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Rendern von Histogrammen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Anisotropes Kuwahara-Graustufen-Symbol](histogram-render.resources/histogram_render.png "Anisotropes Kuwahara-Graustufen-Symbol"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet das Histogramm für ein Graustufenbild.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> PRIMÄR | Das Bild, für das das Histogramm gezeichnet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Die Histogrammvisualisierung, die aus dem Eingangsbild berechnet wurde. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Histogrammauflösung</b> *Integer* | Die Breite des Histogramms. Ein höherer Wert ermöglicht eine feinere Wertverteilung.   Verfügbare Auflösungen sind in Pixeln:  256, 512, 1024, 2048, 4096 |
| <b>Automatische Skalierung</b> *Boolescher Wert* | Wenn &quot;True&quot; festgelegt ist, wird das Histogramm neu zugeordnet, damit das gesamte Height des Bildes verwendet werden kann.   Wenn &quot;False&quot; festgelegt ist, verwendet jede Spalte so viele Pixel im Height, wie ein Wert im Eingabebild vorkommt. |
| <b>Skalierung</b> *Gleitend* | Skaliert das Histogramm vertikal, wobei der Wert 1 das gesamte Height des Histogramms ist. |
| <b>Sampling</b> *Ganzzahl* | Die Methode zur Filterung des Histogrammbildes, die sich auf das Ergebnis auswirkt, wenn die Histogrammauflösung und die Renderauflösung nicht übereinstimmen:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilinear:</b> wendet bilineare Filterungen auf das Histogramm an, was zu interpolierten Punkten führt.</li> <li data-preserve-html="true"><b>Nächster Wert:</b> tastet das nächstgelegene Pixel ohne Filterung ab, was zu flachen Schritten führt</li> </ul> |
| <b>Y-Achse spiegeln</b> *Boolesche Wert* | Wenn &quot;True&quot;, spiegelt das Histogramm vertikal. |

## Beispiele

![Histogramm-Rendering: Beispiel 1](histogram-render.resources/histogram_render_example_1.png "Histogramm-Rendering: Beispiel 1"){zoomable="yes"}

![Histogramm-Rendering: Beispiel 2](histogram-render.resources/histogram_render_example_2.png "Histogramm-Rendering: Beispiel 2"){zoomable="yes"}

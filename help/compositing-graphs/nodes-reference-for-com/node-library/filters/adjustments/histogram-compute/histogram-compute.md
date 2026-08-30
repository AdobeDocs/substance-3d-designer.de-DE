---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Histogramm berechnen , um Histogrammdaten aus Texturen für die Analyse und Verarbeitung zu berechnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramm berechnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# Histogramm berechnen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Histogrammberechnung: Symbol](histogram-compute.resources/histogram_compute.png "Histogrammberechner: Symbol "){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet das Histogramm für ein Graustufenbild.

Das Histogramm wird als Pixelzeile in einem Bild kodiert, wobei jeder Pixelwert die *Grundgesamtheit* des Farbwerts ist, der der Pixelposition auf der X-Achse entspricht.\
Beispielsweise bedeutet ein Pixelwert von 75 bei (0,25, 0), dass 75 Pixel vorhanden sind, die den Farbwert 0,25 im Bild aufweisen.

</td>
</tr>
</table>

Der Knoten gibt außerdem die *kumulative Verteilungsfunktion* (CDF) aus, die für das Bild berechnet wurde.

Benutzerdefinierte Tools können mithilfe der vom Knoten berechneten Daten erstellt werden, z. B. benutzerdefinierte Masken, wie unten im Abschnitt &quot;Beispiele&quot; gezeigt.

>[!IMPORTANT]
>
> Alle Werte außerhalb des Bereichs [0,1] sind festgeklemmt, sodass das Histogramm für HDR möglicherweise nicht genau ist.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> PRIMÄR | Das Bild, für das das Histogramm berechnet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Histogramm</b> <i>Graustufen</i> | Das für das Eingabebild berechnete Histogramm, das als Pixelzeile codiert ist, wobei jeder Pixelwert die *Grundgesamtheit* des Farbwerts ist, der der Pixelposition auf der X-Achse entspricht.   Beispielsweise bedeutet ein Pixelwert von 75 bei (0,25, 0), dass 75 Pixel vorhanden sind, die den Farbwert 0,25 im Bild aufweisen. |
| <b>CDF</b> <i>Graustufen</i> | Das Ergebnis der *kumulativen Verteilungsfunktion* (CDF), die für das Bild berechnet wurde und in einer Pixelzeile codiert ist, wobei jedes Pixel die Summe aller Pixelwerte auf der linken Seite ist.   Diese Summe wird dann *normalisiert*, bezogen auf die Gesamtzahl der Pixel im Bild. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Histogrammauflösung</b> *Integer* | Die Breite des Histogramms. Ein höherer Wert ermöglicht eine feinere Wertverteilung.   Verfügbare Auflösungen sind in Pixeln:  256, 512, 1024, 2048, 4096 |

## Beispiele

![Histogrammberechnung: Beispiel 1](histogram-compute.resources/histogram_compute_example_1.jpg "Histogramm berechnen: Beispiel 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

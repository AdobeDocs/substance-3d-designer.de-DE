---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Histogramm ausgleichen", um die Pixelintensitäten für mehr Kontrast und Helligkeit neu zu verteilen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramm entzerren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# Histogramm entzerren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Histogrammausgleich: icon](../../../../../../assets/histogram_equalize.png "Histogramm equalize: Symbol "){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Entzerrt das Histogramm für ein Graustufenbild und passt die Graustufenwerte effektiv an, um eine gleichmäßige Verteilung zu erreichen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> PRIMÄR | Das Bild, für das das Histogramm ausgeglichen werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Ergebnisbild mit angewendeter Histogrammentzerrung. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Histogrammauflösung</b> *Integer* | Die Breite des Histogramms. Ein höherer Wert ermöglicht eine feinere Wertverteilung.   Verfügbare Auflösungen sind in Pixeln:  256, 512, 1024, 2048, 4096 |
| <b>Glättung des Histogramms</b> *Gleitend* | Das Histogramm kann geglättet werden, indem die Graustufenwerte im Bild neu verteilt werden, um die *Differenz* zwischen jedem Wert zu entzerren.   Dieser Parameter passt die Intensität der Glättung an. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Histogrammausgleich: Beispiel 1](../../../../../../assets/histogram_equalize_example_3.png "Histogramm equalize: Beispiel 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Histogrammausgleich: Beispiel 2](../../../../../../assets/histogram_equalize_example_5.png "Histogramm equalize: Beispiel 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Histogrammausgleich: Beispiel 3](../../../../../../assets/histogram_equalize_example_6.png "Histogramm equalize: Beispiel 3"){zoomable="yes"}

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Medianfilter - Graustufen , um Rauschen zu reduzieren und Kanten in Graustufenstrukturen zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graustufen des Medianfilters
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# Graustufen des Medianfilters

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Graustufen des Medianfilters: Symbol &#x200B;](median-filter-grayscale.resources/MedianFilter_Icon_Grayscale.png "Graustufen des Medianfilters: Symbol ")

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Filter glättet Rauschen in einem Bild und behält dabei die Kanten bei.

Für jedes Pixel berechnet der Knoten einen Graustufenwert entsprechend dem Medianwert der Nachbarpixel.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [Mediane Filterfarbe](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> | Das Graustufenbild, auf das der Filter angewendet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Graustufenbild, das durch Anwenden des Filters auf das Eingabe-Graustufenbild berechnet wird. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kernelgröße</b> *Integer* | Ein Kernel ist eine bestimmte Gruppe von Werten, die in den Berechnungen eines Filters verwendet werden. Dabei handelt es sich um die Werte der benachbarten Pixel.<br><br>Für jedes Pixel nimmt der Filter alle Nachbarn um dieses Pixel in einem quadratischen Kernel und berechnet den Mittelwert aller Nachbarn.<br><br>Dieser Parameter steuert die Größe des quadratischen Kernels in Pixel. Ein größerer Kernel führt zu einem stärkeren, weiter reichenden Glättungseffekt auf Kosten einiger Details.<br><br>*- 3x3:* ein Kernel, der 3 Pixel breit und 3 Pixel hoch ist und insgesamt 8 Nachbarpixel umfasst.<br>*- 5x5:* ein Kernel, der 5 Pixel breit und 5 Pixel hoch ist und insgesamt 24 Nachbarpixel umfasst. |
| <b>Filtertyp </b> *Integer* | Die Berechnung, die auf die Nachbarn angewendet wird, die im Kernel getestet wurden.<br><br>*- Median:* Verwenden Sie den Medianwert aller Nachbarn direkt.<br>*- MLMAD:* steht für &quot;Median der niedrigsten absoluten Medianabweichung&quot;. Die Abweichung gibt an, wie unterschiedlich ein Wert vom Median ist. Anstatt den Medianwert direkt zu verwenden, der von einem Ausreißer-Pixel mit hoher Abweichung geneigt werden kann, verwendet das MLMAD-Verfahren den Median aller Abweichungen. Diese Methode führt zu einem stärkeren Glättungseffekt, der Bereiche entsprechend der Kernelgröße abflachen kann. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4A.png" alt="MedianFilter_Variant4A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4B.png" alt="MedianFilter_Variant4B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1A.png" alt="MedianFilter_Variant1A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1B.png" alt="MedianFilter_Variant1B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

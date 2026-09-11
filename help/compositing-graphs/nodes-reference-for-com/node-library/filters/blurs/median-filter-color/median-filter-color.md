---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Filterfarbe Median", um das Rauschen zu reduzieren und Kanten in Farb-Texturen beizubehalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mittlere Filterfarbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Mittlere Filterfarbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Mittlere Filterfarbe: Symbol &#x200B;](median-filter-color.resources/MedianFilter_Icon_Color.png "Mittlere Filterfarbe: Symbol ")

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Filter glättet das Rauschen in einem Bild und behält dabei die Kanten bei.

Für jedes Pixel berechnet der Knoten einen Farbwert entsprechend dem Mittelwert der Nachbarn des Pixels.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [Graustufen des Medianfilters](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbe</i> | Das Farbbild, auf das der Filter angewendet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Farbe</i> | Das durch Anwenden des Filters auf das Eingabefarbbild berechnete Farbbild. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kernelgröße</b> *Ganzzahl* | Ein Kernel ist eine bestimmte Gruppe von Werten, die in den Berechnungen eines Filters verwendet werden. Dabei handelt es sich um die Werte der benachbarten Pixel.<br><br>Für jedes Pixel nimmt der Filter alle Nachbarn um dieses Pixel in einem quadratischen Kernel und berechnet den Mittelwert aller Nachbarn.<br><br>Dieser Parameter steuert die Größe des quadratischen Kernels in Pixel. Ein größerer Kernel führt zu einem stärkeren, weiter reichenden Glättungseffekt auf Kosten einiger Details.<br><br>*- 3x3:* ein Kernel, der 3 Pixel breit und 3 Pixel hoch ist und insgesamt 8 Nachbarpixel umfasst.<br>*- 5x5:* ein Kernel, der 5 Pixel breit und 5 Pixel hoch ist und insgesamt 24 Nachbarpixel umfasst. |
| <b>Filtertyp </b> *Ganzzahl* | Die Berechnung, die auf die Nachbarn angewendet wird, die im Kernel getestet wurden.<br><br>*- Median:* Verwenden Sie den Medianwert aller Nachbarn direkt.<br>*- MLMAD:* steht für &quot;Median der niedrigsten absoluten Medianabweichung&quot;. Die Abweichung gibt an, wie unterschiedlich ein Wert vom Median ist. Anstatt den Medianwert direkt zu verwenden, der von einem Ausreißer-Pixel mit hoher Abweichung geneigt werden kann, verwendet das MLMAD-Verfahren den Median aller Abweichungen. Diese Methode führt zu einem stärkeren Glättungseffekt, der Bereiche entsprechend der Kernelgröße abflachen kann. |
| <b>Alpha betreffen</b> *Boolesche Wert* | Steuert, ob der Filter auf den Alphakanal des Bildes angewendet werden soll. Wenn *True*, bleibt der Alphakanal unverändert. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Filterfarbe Median", um Rauschen zu reduzieren und Kanten in Farbstrukturen zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mittlere Filterfarbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---


# Mittlere Filterfarbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Mittlere Filterfarbe: Symbol ](../../../../../../assets/MedianFilter_Icon_Color.png "Mittlere Filterfarbe: Symbol ")

<b>In:</b> Filters > Blurs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Filter glättet Rauschen in einem Bild und behält dabei die Kanten bei.

Für jedes Pixel berechnet der Knoten einen Farbwert entsprechend dem Mittelwert der Nachbarn des Pixels.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [Graustufen des Medianfilters](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

## Eingangsanschlüsse

<b>Eingabe </b>*Farbe* Das Farbbild, auf das der Filter angewendet werden soll.

## Ausgangsanschlüsse

<b>Ausgabe</b> *Farbe* Das Farbbild, das durch Anwenden des Filters auf das Eingabefarbbild berechnet wurde.

## Parameter

<b>Kernelgröße</b> *Integer* Ein Kernel ist eine bestimmte Gruppe von Werten, die in den Berechnungen eines Filters verwendet werden. Dabei handelt es sich um die Werte der benachbarten Pixel.\
Für jedes Pixel nimmt der Filter alle Nachbarn um dieses Pixel in einem quadratischen Kernel und berechnet den Medianwert aller Nachbarn.\
Dieser Parameter steuert die Größe des quadratischen Kernels in Pixeln. Ein größerer Kernel führt zu einem stärkeren, weiter reichenden Glättungseffekt auf Kosten einiger Details.\
*- 3x3:* ein Kernel, der 3 Pixel breit und 3 Pixel hoch ist und insgesamt 8 Nachbarpixel umfasst.\
*- 5x5:* ein Kernel, der 5 Pixel breit und 5 Pixel hoch ist und insgesamt 24 Nachbarpixel umfasst.

<b>Filtertyp</b> *Integer* Die Berechnung, die auf die Nachbarn angewendet wurde, die im Kernel getestet wurden.\
*- Median:* Verwenden Sie den Medianwert aller Nachbarn direkt.\
*- MLMAD:* steht für &quot;Median der niedrigsten mittleren absoluten Abweichung&quot;. Die Abweichung gibt an, wie unterschiedlich ein Wert vom Median ist. Anstatt den Medianwert direkt zu verwenden, der von einem Ausreißer-Pixel mit hoher Abweichung geneigt werden kann, verwendet das MLMAD-Verfahren den Median aller Abweichungen. Diese Methode führt zu einem stärkeren Glättungseffekt, der Bereiche entsprechend der Kernelgröße abflachen kann.

<b>Alpha beeinflussen</b> *Boolesch* Steuert, ob der Filter auf den Alphakanal des Bildes angewendet werden soll. Wenn *True*, bleibt der Alphakanal unverändert.

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

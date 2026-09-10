---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten RT-Schatten, um Schatteninformationen aus der Geometrie in Echtzeit zu berechnen, um dynamische Beleuchtungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT-Schatten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# RT-Schatten

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RT Shadows-Knotensymbol](rt-shadow.resources/rt-shadow.png "RT Shadows-Knotensymbol")

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert Raytraced Shadows aus einer Height-Map-Eingabe.

Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Beispiele</b> <i>Integer</i> | Die Anzahl der Strahlen, die zur Berechnung der Schatten verwendet werden.<br>Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis, und das auf Kosten der Leistung. |
| <b>Modus</b> <i>Integer</i> | Die Methode zum Zeichnen der Schatten auf der Oberfläche. |
| <b>Height-Skalierung</b> <i>Gleitend</i> | Ein Multiplikator für die Intensität der Eingabe-Height-Map. |
| <b>Lichtposition</b> <i>Float2</i> | Die Position der Lichtquelle auf einer Kugel, die die Oberfläche umschließt: <br><br>- <b>X</b>: Horizontale Position in Windungszahl;<br>- <b>Y</b>: vertikale Position, wobei 0,5 der Zenit und 0/1 der Horizont sind. |
| <b>Lichtintensität</b> <i>Gleitend</i> | Die Intensität der Lichtquelle. |
| <b>Lichtgröße</b> <i>Float2</i> | (Verfügbar, wenn <b>Modus</b> auf <i>Schattiert</i> festgelegt ist) Die Größe der Lichtquelle als Rechteck. |
| <b>Lichtskala (weiche Schatten)</b> <i>Gleitend</i> | Ein Multiplikator für den Beitrag der <b>Lichtgröße</b> zur Richtung der Strahlen.<br>Ein höherer Wert führt zu weicheren Schatten. |
| <b>Licht über Horizont halten</b> <i>Boolescher Wert</i> | Wenn <b>Lichtposition</b> so eingestellt ist, dass das Licht unter dem Horizont platziert wird, verhindert dieser Parameter, dass das Licht diesen Schwellenwert überschreitet, was bedeutet, dass die Y-Werte auf den Bereich [0;1] geklemmt werden. |
| <b>Schattendeckkraft</b> <i>Gleitend</i> | Ein Multiplikator für die Deckkraft von Schatten, die auf der Oberfläche gezeichnet werden. |
| <b>Schattendämpfung</b> <i>Gleitend</i> | Ein Multiplikator für die Dämpfung der Schatten, je weiter sie von ihrem Zauberer entfernt sind.<br>Ein Wert von 0 führt zu einheitlichen Schatten (weiche Schatten werden noch angewendet). |
| <b>Max. Schattenlänge</b> <i>Gleitend</i> | Die maximale Entfernung, die ein Schatten von seinem Zauberer gezeichnet werden kann.<br>Ein Wert von 0 führt zu keinen sichtbaren Schatten. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-01.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-03.jpg" />
        </td>
    </tr>
</table>

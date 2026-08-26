---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# RT-Schatten

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RT Shadows-Knotensymbol](../../../../../../assets/rt-shadow.png "RT Shadows-Knotensymbol")

<b>In:</b> *Filter/Effekte*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Generiert Raytraced Shadows aus einer Height-Map-Eingabe.

Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden.

</td>
</tr>
</table>

## Parameter

<b>Beispiele</b> *Integer*\
Die Anzahl der Strahlen, die zur Berechnung der Schatten verwendet werden.\
Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis, was wiederum die Kosten für die Leistung verursacht.

<b>Modus</b> *Integer*\
Die Methode zum Zeichnen der Schatten auf der Oberfläche.

<b>Height-Skalierung</b> *Gleitend*\
Ein Multiplikator für die Intensität der Eingabe-Height-Map.

<b>Lichtposition </b>*Float2*\
Die Position der Lichtquelle auf einer Kugel, die die Oberfläche umschließt:
* <b>X</b>: horizontale Lage in Windungszahl;
* <b>J</b>: vertikale Position, wobei 0,5 der Zenit und 0/1 der Horizont sind.

<b>Lichtintensität</b> *Gleitend*\
Die Intensität der Lichtquelle.

<b>Lichtgröße</b> *Float2* (verfügbar, wenn <b>Modus</b> auf *Schattiert* festgelegt ist)\
Die Größe der Lichtquelle als Rechteck.

<b>Lichtskala (weiche Schatten)</b> *Gleitend*\
Ein Multiplikator für den Beitrag der <b>Lichtgröße</b> zur Strahlrichtung.\
Ein höherer Wert sorgt für weichere Schatten.

<b>Licht über Horizont halten</b> *Boolescher Wert*\
Wenn <b>Lichtposition</b> so eingestellt ist, dass das Licht unter dem Horizont platziert wird, verhindert dieser Parameter, dass das Licht diesen Schwellenwert überschreitet, was bedeutet, dass die Y-Werte auf den Bereich [0;1] geklemmt werden.

<b>Schattendeckkraft</b> *Gleitend*\
Ein Multiplikator für die Deckkraft von Schatten, die auf der Oberfläche gezeichnet werden.

<b>Schattendämpfung</b> *Gleitend*\
Ein Multiplikator für die Dämpfung der Schatten, je weiter sie von ihrem Zauberer entfernt sind.\
Ein Wert von 0 führt zu einheitlichen Schatten (weiche Schatten werden weiterhin angewendet).

<b>Max. Schattenlänge</b> *Gleitend*\
Die maximale Entfernung, die ein Schatten von seiner Rolle gezeichnet werden kann.\
Ein Wert von 0 führt zu keinen sichtbaren Schatten.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knoten &quot;RT Shadows&quot; - Beispiel 1](../../../../../../assets/RTShadows-01.jpg "Knoten &quot;RT Shadows&quot; - Beispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knoten &quot;RT Shadows&quot; - Beispiel 2](../../../../../../assets/RTShadows-02.jpg "Knoten &quot;RT Shadows&quot; - Beispiel 2")

</td>
<td style="border: 0;" valign="top">

![Knoten &quot;RT Shadows&quot; - Beispiel 3](../../../../../../assets/RTShadows-03.jpg "Knoten &quot;RT Shadows&quot; - Beispiel 3")

</td>
</tr>
</table>

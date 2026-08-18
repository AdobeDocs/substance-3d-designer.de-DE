---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Punktliste", um Punktlisten für die Spline- und Pfadgenerierung zu erstellen und zu verwalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Punktliste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Punktliste

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/point-list-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Liste von Punkten, die von einem Spline durchlaufen werden sollen.

Wenn eine vorhandene Punktliste an die <b>Point</b>-Eingaben übergeben wird, wird die generierte Liste an die Eingabeliste angehängt.

</td>
</tr>
</table>

>[!TIP]
>
> Dieser Knoten kann verwendet werden, um dem Knoten [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) Punkte zuzuweisen, um Splines zu erstellen.

>[!IMPORTANT]
>
> Die Connectors <b>Punktliste</b> und <b>Punktnummer</b> sind *nicht kompatibel* mit den Connectors <b>Spline-Code</b>, <b>Spline-Daten</b> und <b>Spline-Betrag</b>, da sie auf unterschiedlichen Daten basieren.

## Eingangsanschlüsse

<b>Vorschau </b>*Graustufen* Die Vorschau der Punkte als Graustufenbild.

<b>Punktlisteneingabe</b> *Farbe*\
Eine Liste von Eingangspunkten, die in den RGBA-Kanälen eines Farbbildes codiert sind:\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
            * Ganzzahlteil: Smoothness;\
            * Bruchteil: Thickness.

<b>Eingabe von Punktzahlen</b> *Integer*\
Die Anzahl der Eingabepunkte.

## Ausgangsanschlüsse

<b>Vorschau </b>*Graustufen* Die Vorschau der Punkte als Graustufenbild.

<b>Punkteliste </b>*Farbe*\
Die Ausgabeliste der Punkte, die in den RGBA-Kanälen eines Farbbildes codiert sind:\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
            * Ganzzahlteil: Smoothness;\
            * Bruchteil: Thickness.

<b>Punktzahl </b>*Ganzzahl*\
Die Ausgabenanzahl von Punkten.

## Parameter

<b>Punktzahl</b> *Integer* Die Anzahl der generierten Punkte.

<b>Anpassung der globalen Smoothness</b> *Gleitend* Wendet einen gleichmäßigen Versatz auf den Wert der Smoothness aller Punkte an.\
Die resultierende Smoothness wird auf den Bereich [0;1] geklemmt.

+++Punkteigenschaften
<b>p# Eigenschaften</b> *Float3* Legt die Eigenschaften des p#-Punkts fest.\
*- Height:* Passt das Height des Punktes an, an dem ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet;\
*- Smoothness:* Verschiebt den Beginn der Glättung des Splines bei p#, wobei ein Wert von 0 zu einer harten Kurve und 1 zu einer völlig glatten Kurve führt;\
*- Thickness:* Passt die Thickness des Splines bei p# an. Thickness wird von bestimmten Spline-Knoten verwendet.

+++

+++Punktkoordinaten
<b>p#</b> *Float2* Legt die Position des p#-Punkts im Texturraum fest.

+++

+++Vorschau
<b>Beschriftungen anzeigen</b> *Boolesch*\
Zeigt für jeden Punkt den Namen des Punkts daneben in der Vorschau an.

<b>Labelgröße</b> *Gleitkomma* (verfügbar, wenn &quot;Labels anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist)\
Die Größe des Labels für jeden Punkt im Texturraum, wobei 0,1 ein Zehntel der Texturbreite ist.

<b>Punkte anzeigen</b> *Boolescher Wert*\
Zeigt die Punkte in der Vorschau an.

<b>Punktgröße</b> *Gleitend* (verfügbar, wenn &quot;Punkte anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist)\
Der Radius der Punkte im Texturraum, wobei 0,1 ein Zehntel der Texturbreite beträgt.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/PointList-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/PointList-Demo1.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

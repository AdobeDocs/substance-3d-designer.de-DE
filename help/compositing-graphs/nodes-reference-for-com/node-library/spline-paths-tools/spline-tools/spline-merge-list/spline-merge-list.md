---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline-Zusammenführungsliste , um mehrere Splines in einer einzigen Spline-Liste für kombinierte Operationen zusammenzuführen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Zusammenführungsliste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---


# Spline-Zusammenführungsliste

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-merge-list-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Fügt alle Splines in der Eingabeliste zu einem einzigen Spline zusammen.

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:\
<b> R</b> - X-Position\
<b> G</b> - Y-Position\
<b> B</b> - Height\
<b>A</b> - Paketdaten:\
* Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
* Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b> R</b> - Tangenten X\
<b> G</b> - Tangenten Y\
<b> B</b> - Nicht verwendet\
<b> A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Eingabe-Splines.

## Ausgangsanschlüsse

<b>Vorschau</b> *Graustufen* Die Vorschau der zusammengeführten Splines als Graustufenbild.

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der Punkte der zusammengeführten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b>R</b> - X-Position\
<b>G</b> - Y-Position\
<b>B</b> - Height\
<b>A</b> - Paketdaten:\
* Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
* Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der zusammengeführten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b>R</b> - Tangenten X\
<b>G</b> - Tangenten Y\
<b>B</b> - Nicht verwendet\
<b>A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der zusammengeführten Splines.

## Parameter

<b>Schwellenwert für geschlossene Spline-Distanz</b> *Gleitend* Der Abstand im Texturraum, unter dem zwei Enden desselben Splines als ein einzelner Punkt verarbeitet werden, der diesen Spline schließt.\
Dadurch werden Überlappungen beim Streuen von Formen oder beim Zuordnen von Bildern entlang der Splines verhindert.

+++Vorschau
<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Umschlag der Thickness anzeigen</b> *Boolescher Wert*\
Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschauausgabe an.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant2-Before.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant2-After.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-Before.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-After.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Knotendemo](../../../../../../assets/SplineMergeList-Demo.gif "Knotendemo")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

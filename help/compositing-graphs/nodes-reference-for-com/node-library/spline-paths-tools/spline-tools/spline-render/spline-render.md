---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline-Render, um Splines als Texturen mit anpassbaren Breiten-, Farb- und Füllmethoden zu rendern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Render
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---


# Spline-Render

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-render-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet Zeichenfolgen von Segmenten entlang der Eingabe <b>Splines</b> über der Eingabe <b>Background</b>.

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Hintergrund </b>*Graustufen* Das Graustufenbild, über das Splines gezeichnet werden sollen.

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

<b>Ausgabe</b> *Graustufen*\
Das Ergebnisbild des Zeichnens der Eingabe-Splines über dem Hintergrund.

## Parameter

<b>Modus</b> *Integer* Die Methode zum Auswählen, welche Splines gezeichnet werden sollen:
* *Spline-Liste zeichnen*: Zeichnen aller Splines in der Eingabeliste
* *Spline zeichnen*: Zeichnen Sie nur den angegebenen Spline aus der Eingabeliste.
* *Spline-Bereich zeichnen*: Zeichnen Sie nur die Splines im angegebenen Bereich aus der Eingabeliste.

<b>Spline-Index zeichnen</b> *Integer* (Verfügbar, wenn &quot;Modus&quot; auf &quot;Einzelne Spline zeichnen&quot; festgelegt ist)Der Index des Splines, der gezeichnet werden soll.

<b>Spline-Bereich zeichnen</b> *Integer2* (Verfügbar, wenn &quot;Modus&quot; auf &quot;Spline-Bereich zeichnen&quot; festgelegt ist)Der Indexbereich für die Splines, die gezeichnet werden sollen.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeichnet für jeden Spline einen Punkt am Anfang des Splines und eine Pfeilspitze am Ende.

<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der entlang der Splines gezeichneten Segmente an.\
Je höher der Wert, desto glatter die Linien.

<b>Spline-Betrag für Umschlag</b> *Integer*\
Die Anzahl der doppelten Segmente, die entlang der Thickness jedes Splines gezeichnet werden sollen.

<b>Start</b> *Gleitend* Verschiebt den Anfang des Bereichs des Splines, der gezeichnet werden soll.\
Der Wert stellt die normalisierte Länge des Splines dar.

<b>Ende</b> *Gleitend* Verschiebt das Ende des Bereichs des Splines, der gezeichnet werden soll.\
Der Wert stellt die normalisierte Länge des Splines dar.

<b>Thickness-Größenmodus</b> *Integer* Die Methode zum Berechnen der Thickness der gezeichneten Segmente:
* *Image*: Der Wert wird im Texturraum normalisiert, wobei 1 die volle Breite des Bildes ist. die Thickness ist relativ zur Texturauflösung;
* *Pixel*: Der Wert ist eine absolute Anzahl von Pixeln in der Textur, wobei 1 ein ganzes Pixel ist. Die Thickness ist von der Texturauflösung getrennt.

<b>Thickness (Bild)</b> *Gleitkommawert* (verfügbar, wenn &quot;Bildgrößenmodus&quot; auf &quot;Thickness&quot; festgelegt ist)Die Thickness der gezeichneten Segmente, die im Texturraum normalisiert wurde, wobei 1 die volle Bildbreite ist.

<b>Thickness (px)</b> *Gleitkommawert* (verfügbar, wenn &quot;Pixelgrößenmodus&quot; auf &quot;Thickness&quot; festgelegt ist)Die Thickness der gezeichneten Segmente als absolute Pixelanzahl in der Textur, wobei 1 ein Vollpixel ist.

<b>Verbindungen aktivieren</b> *Boolean* Füllt die Lücken zwischen den einzelnen Segmenten, die entlang der Splines gezeichnet werden, mithilfe von Datenträgern.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

+++Color
<b>Hintergrundintensität</b> *Gleitend* Der Wert multipliziert mit dem Hintergrundeingabebild.

<b>Spline-Stil</b> *Integer* Die zum Einfärben der Splines verwendete Methode:
* *Farbfläche*: Die Segmente werden mit einem einheitlichen Graustufenwert gezeichnet.
* *Verlauf*: Ein Farbverlauf von Schwarz zu Weiß wird auf jede Zeichenfolge von Segmenten von Anfang bis Ende angewendet.
* *Height*: Das Height der Splines wird als Graustufenwert zum Zeichnen der Segmente verwendet.

<b>Spline-Farbe</b> *Gleitend* Der einheitliche Graustufenwert, der zum Zeichnen der Segmente verwendet wird.\
Wenn ein anderer Spline-Stil als &quot;Farbfläche&quot; ausgewählt ist, wird diese Farbe mit der formatierten Farbe multipliziert.

<b>Zufällige Luminanz</b> *Gleitend* Wendet für jede Zeichenfolge ungeschnittener Segmente in einem Spline einen zufälligen Offset im angegebenen Bereich auf den Graustufenwert an, der zum Zeichnen dieser Zeichenfolge verwendet wird.

<b>Füllmethode</b> *Integer* Die Methode zum Mischen der Farben des Hintergrunds und der überlappenden Segmente, die entlang der Splines gezeichnet werden:
* *Max*: Der hellste Wert wird verwendet.
* *Hinzufügen*: Die Werte werden addiert.

+++

+++Zufällige Segmente
<b>Zufallssegmente beginnen</b> *Gleitend* Passt die Wahrscheinlichkeit an, dass die Zeichenfolge der Segmente, die näher am Anfang des Splines liegt, abgeschnitten wird.

<b>Ende zufälliger Segmente</b> *Gleitend* Passt die Wahrscheinlichkeit an, dass die Zeichenfolge der Segmente, die näher am Ende des Splines liegt, abgeschnitten wird.

<b>Zufallsversatz</b> *Gleitend* Legt den maximalen Versatz fest, der auf jedes Schnittsegment entlang seiner Normalen angewendet wird.\
Dieser Parameter hat keine Auswirkungen, wenn Start und Ende beide auf 0 gesetzt sind.

<b>Zentrum für zufällige Verschiebung</b> *Gleitend* Verschiebt den Mittelpunkt des zufälligen Versatzes, der auf jedes Schnittsegment angewendet wird, entlang seiner Normalen.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineRender-Demo.gif "Knotenbeispiel 1")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

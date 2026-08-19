---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Spline-Beispiel-Thickness", um Spline-Werte entlang von Thicknessen für prozedurale Effekte aufzunehmen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Beispiel-Thickness
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---


# Spline-Beispiel-Thickness

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-sample-thickness-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ändert die Thickness der Eingabe-Splines, indem ihnen eine Eingabe-Thickness Map zugeordnet wird.

Der Effekt der zugeordneten Height-Map kann angepasst werden, indem die Füllmethode und die Deckkraft dieses Effekts geändert werden.

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Vorschau</b> *Graustufen* Die Vorschau der Eingabe-Splines als Graustufenbild.

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

<b>Thicknessen-Map</b> *Graustufen* Das Graustufenbild, das zum Ändern der Thickness des Eingabesplines verwendet wurde.

## Ausgangsanschlüsse

<b>Vorschau</b> *Graustufen* Die Vorschau der Ausgabe-Splines als Graustufenbild.

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der Punkte der Ausgabesplines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
        * Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
        * Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Ausgabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - Tangenten X\
    <b>G</b> - Tangenten Y\
    <b>B</b> - Nicht verwendet\
    <b>A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Ausgabe-Splines.

## Parameter

<b>Sampling-Modus</b> *Integer* Die Methode zum Zuordnen der Werte in der Thickness Map zu den Splines:\
*- Texturraum*: Die Werte werden auf die Splines angewendet, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;an Ort und Stelle&quot; angewendet.\
*- Horizontal entlang Spline*: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Koordinaten-Eingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird.\
*- Stunde. entlang der Spline (Rand). Versatz X)*: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Koordinaten).\
*- Stunde. entlang der Spline (Rand). Offset Y)*: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird.

<b>Deckkraft</b> *Gleitkommawert* Ein Multiplikator für die Intensität des Beitrags der Thickness-Map-Eingabe zur Thickness des Splines.<b></b>

<b>Füllmethode</b> *Integer* Die Methode zum Mischen der Daten der Thickness Map mit der <span id="_Hlk135820484"></span>-Thickness des Eingabesplines:\
*- Kopie*: Überschreiben der Thickness des Splines mit den Height-Map-Werten\
*-* hinzufügen: Fügen Sie der Thickness des Splines die Werte für &quot;Thickness zuordnen&quot; hinzu.\
*-* subtrahieren: Subtrahieren Sie die Werte für die Thicknessen-Map von der Thickness des Splines.\
*- Multiplizieren*: Multiplizieren Sie die Thickness-Map-Werte mit der Thickness des Splines.

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
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
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

![Knotenbeispiel 1](../../../../../../assets/SplineSampleThickness-Variant1-After1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineSampleThickness-Demo.gif "Knotenbeispiel 2")

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

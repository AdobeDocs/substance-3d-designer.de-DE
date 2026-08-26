---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Verwenden Sie den Spline Warp -Knoten, um Texturen entlang von Spline-Pfaden zu verkrümmen, um gekrümmte und organische Muster zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Verkrümmung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# Spline-Verkrümmung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-warp-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verschiebt die Eingabe-Splines basierend auf der Eingabe-Intensitätskarte oder Vektorkarte.

Die Intensität des Verkrümmungseffekts kann mithilfe von Dämpfungssteuerelementen entlang des Splines angepasst werden.

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

<b>Intensitätskarte</b> *Graustufen* (verfügbar, wenn &quot;Vektorzuordnung verwenden&quot; auf &quot;Falsch&quot; festgelegt ist)\
Das Graustufenbild für die Eingabe, das zum Steuern der Richtung und Intensität des Verkrümmungseffekts auf den Eingabesplines verwendet wird.\
Die Farbe jedes Pixels im Bild gibt einen Multiplikator an, mit dem die Punkte des Splines entlang ihrer Normalen (d. h. der Richtung senkrecht zum Spline) bis zur vollen Bildspanne verschoben werden.\
Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1] Bereich, wenn er als Multiplikator gelesen wird: 0 und 1 verschieben den Spline um denselben Abstand, jedoch in entgegengesetzte Richtungen. 0,5 belässt den Spline an Ort und Stelle.

<b>Vektorzuordnung</b> *Graustufen* (verfügbar, wenn &quot;Vektorkarte verwenden&quot; auf &quot;Wahr&quot; gesetzt ist): Das Eingabefarbbild, das zum Steuern der Richtung und Intensität des Verkrümmungseffekts auf den Eingabesplines verwendet wird.\
Die Farbe jedes Pixels im Bild gibt den Vektor (X, Y) an, dessen Koordinaten in den roten (X) und grünen (Y) Kanälen codiert sind. +X ist rechts und +Y ist unten.\
Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1]-Bereich, wenn er als Vektorkoordinaten gelesen wird: 0 rot verschiebt Punkte nach links und 0 grün verschiebt Punkte nach oben. 0,5 rot und grün hinterlässt den Spline an Ort und Stelle.

<b>Dämpfungskurve</b> *Graustufen* Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.\
Wenn der Parameter Dämpfungskurve verwenden auf Wahr gesetzt ist, wird diese Eingabe verwendet, um die Dämpfung des Verkrümmungseffekts in der Nähe des Anfangs und des Endes des Splines zu steuern.\
Die Kurve bietet ein Profil für die Dämpfung, wobei das erste Pixel in der Zeile die Intensität des Verkrümmungseffekts am Anfang des Spline-Effekts und das letzte die Intensität am Ende ist. Der Graustufenwert ist die Intensität.\
Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden.

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

<b>Verkrümmungsintensität</b> *Gleitend* Die Intensität, um die die Splines verschoben werden.

<b>Verkrümmungszentrum</b> *Float* Gibt den Intensitätszuordnungswert an, der dem Verbleiben der Splines entspricht.\
Ein Wert von 0 oder 1 bedeutet, dass die Splines nur einseitig verschoben werden können.

<b>Sampling-Modus</b> *Integer* Die Methode zum Zuordnen der Werte in der Intensitätszuordnung oder der Vektorzuordnung zu den Splines:\
*- Texturraum*: Die Werte werden auf die Splines angewendet, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;an Ort und Stelle&quot; angewendet.\
*- Horizontal entlang Spline*: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Koordinaten-Eingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird.\
*- Stunde. entlang der Spline (Rand). Versatz X)*: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Koordinaten).\
*- Stunde. entlang der Spline (Rand). Offset Y)*: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird.

<b>Vektorzuordnung verwenden</b> *Boolesch* Schaltet die Methode zum Verschieben der Splines auf die Verwendung einer Vektorzuordnungs-Eingabe um, um die Richtung des Versatzes anzugeben.\
Die Farbe jedes Pixels im Bild gibt den Vektor (X, Y) an, dessen Koordinaten in den roten (X) und grünen (Y) Kanälen codiert sind. +X ist rechts und +Y ist unten.\
Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1]-Bereich, wenn er als Vektorkoordinaten gelesen wird: 0 rot verschiebt Punkte nach links und 0 grün verschiebt Punkte nach oben. 0,5 rot und grün hinterlässt den Spline an Ort und Stelle.

<b>Dämpfungskurve verwenden</b> *Boolescher Wert* Ermöglicht die Steuerung der Intensität des Verkrümmungseffekts entlang eines Splines mithilfe einer Kurve, die im Eingabebild der Dämpfungskurve codiert ist.<b></b>

<b>Intensitätszuordnungs-Kachel</b> *Float* (verfügbar, wenn &quot;Sampling-Modus&quot; nicht auf &quot;Texturraum&quot; festgelegt ist): Passt die Unterteilung der Intensitätskarte an, wenn sie den Spline-Koordinaten direkt zugeordnet wird (siehe Spline-Koordinateneingabe).<b></b>

<b>Dämpfung starten</b> *Gleitkommawert* (verfügbar, wenn &quot;Dämpfungskurve verwenden&quot; auf &quot;Falsch&quot; gesetzt ist)Ein Multiplikator für die Dämpfung des Verkrümmungseffekts am Anfang des Splines.\
Ein Wert von 1 bedeutet, dass keine Verkrümmung auf den Anfang des Splines angewendet wird.

<b>Enddämpfung</b> *Gleitkommawert* (verfügbar, wenn &quot;Dämpfungskurve verwenden&quot; auf &quot;Falsch&quot; gesetzt ist)Ein Multiplikator für die Dämpfung des Verkrümmungseffekts am Ende des Splines.\
Ein Wert von 1 bedeutet, dass keine Verkrümmung auf das Ende des Splines angewendet wird.<b></b>

<b>Tangenten neu berechnen</b> *Boolescher Wert* Wenn dieser Wert auf &quot;Wahr&quot; gesetzt ist, werden die Tangenten eines Splines neu berechnet, nachdem der Verkrümmungseffekt angewendet wurde.\
Dies stellt sicher, dass die Tangenten des Spline-Effekts mit seiner Trajektorie konsistent bleiben, wenn sie in Knoten wie &quot;Streuung&quot; in Spline oder &quot;Spline Flow Mapper&quot; verwendet werden.

+++Vorschau
<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Umschlag der Thickness anzeigen</b> *Boolescher Wert*\
Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschauausgabe an.

<b>Intensität der Hintergrundvorschau</b> *Gleitend*\
Der Wert multipliziert mit dem Hintergrundbild für die Vorschau.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Knotenbeispiel 1](../../../../../../assets/SplineWarp-Demo.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">



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

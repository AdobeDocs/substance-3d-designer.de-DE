---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
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
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# Spline-Verkrümmung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-warp.resources/spline-warp-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verschiebt die Eingabe-Splines basierend auf der Eingabe-Intensitätskarte oder Vektorkarte.

Die Intensität des Verkrümmungseffekts kann mithilfe von Dämpfungssteuerelementen entlang des Splines angepasst werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |
| <b>Intensitätskarte</b> <i>Graustufen</i> | (Verfügbar, wenn &quot;Vektorkarte verwenden&quot; auf &quot;Falsch&quot; gesetzt ist) Das Graustufenbild, mit dem die Richtung und Intensität des Verkrümmungseffekts auf den Eingangs-Splines gesteuert wird.<br>Die Farbe jedes Pixels im Bild gibt einen Multiplikator an, mit dem die Punkte des Splines entlang ihrer Normalen (d. h. der Richtung senkrecht zum Spline) bis zur vollen Bildspanne verschoben werden.<br>Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1] Bereich, wenn er als Multiplikator gelesen wird: 0 und 1 verschieben den Spline um denselben Abstand, jedoch in entgegengesetzte Richtungen. 0,5 belässt den Spline an Ort und Stelle. |
| <b>Vektorzuordnung</b> <i>Graustufen</i> | (Verfügbar, wenn &quot;Vektorkarte verwenden&quot; auf &quot;Wahr&quot; gesetzt ist) Das Eingabefarbbild, das zur Steuerung der Richtung und Intensität des Verkrümmungseffekts auf den Eingabesplines verwendet wird.<br>Die Farbe jedes Pixels im Bild gibt den Vektor (X, Y) an, dessen Koordinaten in den roten (X) und grünen (Y) Kanälen codiert sind. +X ist rechts und +Y ist unten.<br>Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1]-Bereich, wenn er als Vektorkoordinaten gelesen wird: 0 rot verschiebt Punkte nach links und 0 grün verschiebt Punkte nach oben. 0,5 rot und grün hinterlässt den Spline an Ort und Stelle. |
| <b>Dämpfungskurve</b> <i>Graustufen</i> | Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.<br>Wenn der Parameter &quot;Dämpfungskurve verwenden&quot; auf &quot;Wahr&quot; gesetzt ist, wird diese Eingabe verwendet, um die Dämpfung des Verkrümmungseffekts am Anfang und Ende des Splines zu steuern.<br>Die Kurve bietet ein Profil für die Dämpfung, wobei das erste Pixel in der Zeile die Intensität des Verkrümmungseffekts am Anfang des Spline-Effekts und das letzte die Intensität am Ende ist. Der Graustufenwert ist die Intensität.<br>Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Ausgabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Ausgabesplines.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der in den RGBA-Kanälen eines Farbbilds codierten Ausgabe-Splines.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Ausgabe-Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Verkrümmungsintensität</b> <i>Gleitend</i> | Die Intensität, um die die Splines verschoben werden. |
| <b>Verkrümmungszentrum</b> <i>Gleitend</i> | Gibt den Intensitätszuordnungswert an, der dem Belassen der Splines entspricht.<br>Ein Wert von 0 oder 1 bedeutet, dass die Splines nur auf einer Seite verschoben werden können. |
| <b>Sampling-Modus</b> <i>Integer</i> | Die Methode zum Zuordnen der Werte in der Intensitätszuordnung oder der Vektorzuordnung zu den Splines:<br>- <i>Texturen-Raum</i>: Die Werte werden auf die Splines angewendet, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;in place&quot;;<br>- <i>Horizontal entlang Spline</i> angewendet: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Koordinateneingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird;<br>- <i>Hor. entlang der Spline (Rand). Versatz X)</i>: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Coords);<br>- <i>Hor. entlang der Spline (Rand). Offset Y)</i>: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird. |
| <b>Vektorzuordnung verwenden</b> <i>Boolescher Wert</i> | Schaltet die Methode zum Verschieben der Splines auf die Verwendung einer Vektorzuordnungs-Eingabe um, um die Richtung des Versatzes anzugeben.<br>Die Farbe jedes Pixels im Bild gibt den Vektor (X, Y) an, dessen Koordinaten in den roten (X) und grünen (Y) Kanälen codiert sind. +X ist rechts und +Y ist unten.<br>Die [0; 1] Werte im Bild werden neu zugeordnet zu [-1; 1]-Bereich, wenn er als Vektorkoordinaten gelesen wird: 0 rot verschiebt Punkte nach links und 0 grün verschiebt Punkte nach oben. 0,5 rot und grün hinterlässt den Spline an Ort und Stelle. |
| <b>Dämpfungskurve verwenden</b> <i>Boolescher Wert</i> | Aktiviert die Steuerung der Intensität des Verkrümmungseffekts entlang eines Splines mithilfe einer im Eingabebild &quot;Dämpfungskurve&quot; codierten Kurve. |
| <b>Intensitätszuordnungs-Kachel</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Sampling Mode&quot; nicht auf &quot;Textur Space&quot; festgelegt ist) Passt die Kachelung der Intensitätskarte an, wenn sie den Spline-Koordinaten direkt zugeordnet wird (siehe Spline-Koordinateneingabe). |
| <b>Dämpfung starten</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Dämpfungskurve verwenden&quot; auf &quot;Falsch&quot; gesetzt ist) Ein Multiplikator für die Dämpfung des Verkrümmungseffekts am Anfang des Splines.<br>Ein Wert von 1 bedeutet, dass keine Verkrümmung auf den Anfang des Splines angewendet wird. |
| <b>Enddämpfung</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Dämpfungskurve verwenden&quot; auf &quot;Falsch&quot; gesetzt ist) Ein Multiplikator für die Dämpfung des Verkrümmungseffekts am Ende des Splines.<br>Ein Wert von 1 bedeutet, dass keine Verkrümmung auf das Ende des Splines angewendet wird. |
| <b>Tangenten neu berechnen</b> <i>Boolescher Wert</i> | Wenn dieser Wert wahr ist, werden die Tangenten eines Splines neu berechnet, nachdem der Verkrümmungseffekt angewendet wurde.<br>Dadurch wird sichergestellt, dass die Tangenten des Splines mit seiner Trajektorie konsistent bleiben, wenn sie in Knoten wie &quot;Streuung&quot; in Spline oder &quot;Spline Flow Mapper&quot; verwendet werden. |
| <b>Vorschau</b> |  |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.<br>Ein höherer Wert führt zu einer glatteren Linie. |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschau an. |
| <b>Intensität der Hintergrundvorschau</b> <i>Gleitend</i> | Der Wert multipliziert mit dem Hintergrundbild für die Vorschau. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Knotenbeispiel 1](spline-warp.resources/SplineWarp-Demo.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

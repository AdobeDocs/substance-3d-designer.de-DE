---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Verwenden Sie den Spline Circle-Knoten, um runde Splines zum Erzeugen runder Muster und Formen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Circle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Spline Circle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-circle-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt einen einzelnen Spline-Effekt in Form eines Kreises.

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

<b>Kreisradius</b> *Gleitend*\
Passt den Radius des Kreises im Texturraum an.

<b>Kreisvordrehung</b> *Gleitend*\
Wendet eine Drehung auf den Grundkreis an, bevor Größe angewendet wird.

<b>Kreisgröße</b> *Float2*\
Passt die horizontale Größe (X) und vertikale Größe (Y) des Kreises an.

<b>Kreis nach Drehung</b> *Gleitend*\
Wendet eine Drehung auf den Grundkreis an, nachdem die Größe angewendet wurde.

<b>Kreisposition</b> *Float2*\
Legt die Position des Mittelpunkts des Kreises im Texturraum fest.

<b>Thickness starten</b> *Gleitend* Passt die Thickness des Anfangspunkts des Kreises an.\
Diese Thickness wird entlang der Spline bis zur Thickness &quot;Ende&quot; interpoliert.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>Thickness beenden</b> *Gleitend* Passt die Thickness des Kreisendpunkts an.\
Diese Thickness wird entlang der Spline zur Start-Thickness interpoliert.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>Height starten</b> *Gleitend* Passt das Height des Anfangspunkts des Kreises an, wobei ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dieses Height wird entlang der Spline zum Height Ende interpoliert.

<b>Height beenden</b> *Gleitend* Passt das Height des Kreisendpunkts an, wobei ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dieses Height wird entlang des Spline vom Height Start interpoliert.

<b>Zuschneiden</b> *Gleitkomma2* Verschiebt den Start- und Endpunkt des Splines entlang des Kreises.\
Diese Werte werden normalisiert.

<b>Spirale</b> *Gleitend* Verschiebt den Anfangspunkt des Kreises von seinem Radius zu seinem Mittelpunkt.\
Der Abstand vom Mittelpunkt wird dann entlang der Spline bis zum Ende der Spline interpoliert.\
Dieser Wert wird normalisiert.

<b>Spiraldrehungen</b> *Gleitend* Definiert die Anzahl der Windungen, die von der Spirale um ihren Mittelpunkt gemacht werden.

<b>Spiralleistung</b> *Gleitend* Wendet eine Leistungskurve auf den Abstand vom Mittelpunkt an, der zum Zeichnen der Spirale verwendet wird.\
Ein Wert, der größer als Eins ist, bedeutet, dass ein größerer Teil der Spirale in der Nähe der Mitte verbleibt.

<b>Richtung spiegeln</b> *Boolescher Wert*\
Kehrt die Richtung des Spline um.

<b>Einheitliche Verteilung</b> *Boolescher Wert*\
Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden die Punkte des Splines in gleichmäßigen Abständen vom Anfang bis zum Ende ausgerichtet.

<b>Spline anfügen</b> *Boolescher Wert*\
Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

+++Vorschau
<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Umschlag der Thickness anzeigen</b> *Boolescher Wert*\
Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an.

<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in der Vorschauausgabe in Pixel an.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineCircle-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineCircle-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Beispiel 3](../../../../../../assets/SplineCircle-Variant2.jpg "Beispiel 3")

</td>
<td style="border: 0;" valign="top">

![Beispiel 4](../../../../../../assets/SplineCircle-Variant3.jpg "Beispiel 4")

</td>
</tr>
</table>

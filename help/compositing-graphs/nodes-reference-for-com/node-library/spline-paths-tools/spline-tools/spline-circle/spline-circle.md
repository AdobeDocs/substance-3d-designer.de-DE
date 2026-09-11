---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
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
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# Spline Circle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-circle.resources/spline-circle-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt einen einzelnen Spline-Effekt in Form eines Kreises.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Ausgabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Ausgabesplines.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der in den RGBA-Kanälen eines Farbbilds codierten Ausgabe-Splines.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Ausgabe-Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kreisradius</b> <i>Gleitend</i> | Passt den Radius des Kreises im Texturraum an. |
| <b>Kreisvordrehung</b> <i>Gleitend</i> | Wendet eine Drehung auf den Grundkreis an, bevor Größe angewendet wird. |
| <b>Kreisgröße</b> <i>Float2</i> | Passt die horizontale Größe (X) und vertikale Größe (Y) des Kreises an. |
| <b>Kreis nach Drehung</b> <i>Gleitend</i> | Wendet eine Drehung auf den Grundkreis an, nachdem die Größe angewendet wurde. |
| <b>Kreisposition</b> <i>Float2</i> | Legt die Position des Kreismittelpunkts in der Textur fest. |
| <b>Thickness starten</b> <i>Gleitend</i> | Passt die Thickness des Anfangspunkts des Kreises an. Diese Thickness wird entlang des Splines zur End-Thickness interpoliert.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Thickness beenden</b> <i>Gleitend</i> | Passt die Thickness des Kreisendpunkts an. Diese Thickness wird entlang der Spline zur Start-Thickness interpoliert.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Height starten</b> <i>Gleitend</i> | Passt das Height des Anfangspunkts des Kreises an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Stelle bedeutet. Dieses Height wird entlang der Spline zum Height Ende interpoliert. |
| <b>Height beenden</b> <i>Gleitend</i> | Passt das Height des Kreisendpunkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Stelle bedeutet. Dieses Height wird entlang des Spline vom Height Start interpoliert. |
| <b>Zuschneiden</b> <i>Float2</i> | Verschiebt den Start- und Endpunkt der Spline entlang des Kreises. Diese Werte werden normalisiert. |
| <b>Spirale</b> <i>Gleitend</i> | Verschiebt den Anfangspunkt des Kreises von seinem Radius zu seinem Mittelpunkt. Der Abstand vom Mittelpunkt wird dann entlang der Spline bis zum Ende der Spline interpoliert. Dieser Wert wird normalisiert. |
| <b>Spiraldrehungen</b> <i>Gleitend</i> | Definiert die Anzahl der Windungen, die die Spirale um ihren Mittelpunkt herum erzeugt. |
| <b>Spiralleistung</b> <i>Gleitend</i> | Wendet eine Leistungskurve auf den Abstand vom Mittelpunkt an, der zum Zeichnen der Spirale verwendet wird. Ein Wert, der größer als Eins ist, bedeutet, dass ein größerer Teil der Spirale in der Nähe der Mitte verbleibt. |
| <b>Richtung spiegeln</b> <i>Boolescher Wert</i> | Kehrt die Richtung des Spline um. |
| <b>Einheitliche Verteilung</b> <i>Boolescher Wert</i> | Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden die Punkte des Splines in gleichmäßigen Abständen vom Anfang bis zum Ende ausgerichtet. |
| <b>Spline anfügen</b> <i>Boolescher Wert</i> | Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Vorschau</b> |  |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden. Je höher der Wert, desto glatter die Linie. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in der Vorschauausgabe in Pixel an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](spline-circle.resources/SplineCircle-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-circle.resources/SplineCircle-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Beispiel 3](spline-circle.resources/SplineCircle-Variant2.jpg "Beispiel 3")

</td>
<td style="border: 0;" valign="top">

![Beispiel 4](spline-circle.resources/SplineCircle-Variant3.jpg "Beispiel 4")

</td>
</tr>
</table>

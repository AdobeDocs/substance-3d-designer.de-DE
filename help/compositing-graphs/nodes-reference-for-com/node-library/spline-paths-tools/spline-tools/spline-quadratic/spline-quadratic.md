---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline Quadratic , um glatte quadratische Splines mit drei Kontrollpunkten zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (quadratisch)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# Spline (quadratisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (quadratisch): Symbol ](spline-quadratic.resources/spline-quadratic-icon.png "Spline (Quadratisch): Symbol ")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert einen einzelnen Spline zwischen zwei Punkten <b>p1</b> und <b>p3</b> an beliebigen Positionen.

Die Trajektorie des Splines wird durch die &quot;out&quot;-Tangente von <b>p1</b> und die &quot;in&quot;-Tangente von <b>p3</b>, *both*, gesteuert durch einen einzigen Punkt <b>p3</b>.

Die Spannweite des durch die Spline gebildeten Bogens ist *einstellbar*, sodass ein Teil der Trajektorie von den Enden aus gerade bleiben kann.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Tangenten Z<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Ausgabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Ausgabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der in den RGBA-Kanälen eines Farbbildes codierten Ausgabe-Splines:<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Tangenten Z<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Ausgabe-Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Richtung spiegeln</b> <i>Boolescher Wert</i> | Kehrt die Richtung des Spline um. |
| <b>Einheitliche Verteilung</b> <i>Boolescher Wert</i> | Wenn <i>True</i>, werden die Spline-Punkte gleichmäßig vom Anfang bis zum Ende verteilt. |
| <b>Eingabe-Spline anfügen</b> <i>Boolescher Wert</i> | Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Smoothness</b> <i>Gleitend</i> | Passt die <i>Spanne des Bogens </i> an, der durch den Spline gebildet wird. 1 bedeutet, dass der Spline gewölbt ist und 0 bedeutet, dass der Spline vollständig gerade ist. Der Bogen verläuft von Punkt <b>p3</b> entlang des Splines bis zu seinen Extremitäten. |
| <b>Height</b> |  |
| <b>Height starten</b> <i>Gleitend</i> | Passt das Height des <b>p1</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.<br>Dies wirkt sich auf das Height des Splines bei <b>p1</b> aus. |
| <b>Height beenden</b> <i>Gleitend</i> | Passt das Height des <b>p3</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.<br>Dies wirkt sich auf die Thickness des Splines bei <b>p3</b> aus. |
| <b>Automatisches Tangenten-Height</b> <i>Boolescher Wert</i> | Passt das Height des <b>p3</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.<br>Dies wirkt sich auf die Thickness des Splines bei <b>p3</b> aus. |
| <b>Tangent-Height</b> <i>Gleitend</i> | Passt das Height an, das von den Tangenten gesteuert wird, die vom <b>p2</b>-Punkt gesteuert werden.<br>Dies wirkt sich auf das Height entlang des Splines aus, wenn es von <b>p1</b> abgezogen wird, und geht in <b>p3</b>.<br><i>Hinweis:</i> Dieser Parameter ist nur verfügbar, wenn <b>Height für automatische Tangente</b> auf &quot;Falsch&quot; festgelegt ist. |
| <b>Thickness</b> |  |
| <b>Thickness starten</b> <i>Gleitend</i> | Passt die Thickness des <b>p1</b>-Punkts an. Dies wirkt sich auf die Thickness des Splines bei <b>p1</b>.<br><i>Hinweis:</i> Die Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Thickness beenden</b> <i>Gleitend</i> | Passt die Thickness des <b>p3</b>-Punkts an. Dies wirkt sich auf die Thickness des Splines bei <b>p3</b>.<br><i>Hinweis:</i> Die Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Automatische Tangenten-Thickness</b> <i>Boolescher Wert</i> | Setzt die Thickness der Spline-Tangenten automatisch so, dass sie linear von der <b>Start-Thickness</b> zur <b>End-Thickness</b> interpoliert werden.<br><i>Hinweis:</i> Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Tangent-Thickness</b> <i>Gleitend</i> | Passt die Thickness an, die von den Tangenten gesteuert wird, die vom <b>p2</b>-Punkt gesteuert werden.<br>Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie von <b>p1</b> abgezogen wird und in <b>p3</b> übergeht.<br><i>Hinweis:</i> Die Thickness wird von bestimmten Spline-Knoten verwendet.<br><i>Hinweis 2:</i> Dieser Parameter ist nur verfügbar, wenn <b>die automatische Tangente Thickness</b> auf &quot;Falsch&quot; festgelegt ist. |
| <b>Punktkoordinaten</b> |  |
| <b>p1</b> <i>Float2</i> | Legt die Position des <b>p1</b>-Punkts im Texturraum fest. |
| <b>p2</b> <i>Float2</i> | Legt die Position des <b>p2</b>-Punkts im Texturraum fest.<br>Der <b>p2</b>-Punkt steuert die <i>Tangenten</i> von <b>p1</b> und <b>p3</b>-Punkten. |
| <b>p3</b> <i>Float2</i> | Legt die Position des <b>p3</b>-Punkts im Texturraum fest. |
| <b>Vorschau</b> |  |
| <b>Tangenten anzeigen</b> <i>Boolescher Wert</i> | Zeigt die <b>p1</b>-Point-Out-Tangente und die <b>p3</b>-Point-In-Tangente in der <b>Vorschau</b>-Ausgabe an. Kehrt die Richtung des Spline um. |
| <b>Richtungs-Helfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze am Ende in der <b>Vorschau</b>-Ausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe verwendet werden.<br>Ein höherer Wert führt zu einer glatteren Linie. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe in Pixel an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (quadratisch): Beispiel 1](spline-quadratic.resources/spline-quadratic-example-1.png "Spline (quadratisch): Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (quadratisch): Beispiel 2](spline-quadratic.resources/spline-quadratic-example-2.png "Spline (quadratisch): Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (quadratisch): Demo](spline-quadratic.resources/spline-quadratic-demo.gif "Spline (quadratisch): Demo "){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

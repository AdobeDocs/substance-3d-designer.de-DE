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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# Spline (quadratisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (quadratisch): Symbol &#x200B;](../../../../../../assets/spline-quadratic-icon.png "Spline (Quadratisch): Symbol ")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert einen einzelnen Spline zwischen zwei Punkten <b>p1</b> und <b>p3</b> an beliebigen Positionen.

Die Trajektorie der Spline wird durch die &quot;out&quot;-Tangente von <b>p1</b> und die &quot;in&quot;-Tangente von <b>p3</b>, *beide* gesteuert durch einen einzigen Punkt <b>p3</b>.

Die Spannweite des durch die Spline gebildeten Bogens ist *einstellbar*, sodass ein Teil der Trajektorie von den Enden aus gerade bleiben kann.

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Vorschau</b> *Graustufen* | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> *Farbe* | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines: <b>R</b> - X-Position <b>G</b> - Y-Position <b>B</b> - Height <b>A</b> - Packed data:          - Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).          - Absoluter Wert: Thickness + 1. |
| <b>Spline-Daten</b> *Farbe* | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - Tangenten X <b>G</b> - Tangenten Y <b>B</b> - Tangenten Z <b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> *Integer* | Die Anzahl der Eingabe-Splines. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Vorschau</b> *Graustufen* | Die Vorschau der Ausgabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> *Farbe* | Die Koordinaten der Punkte der Ausgabesplines, die in den RGBA-Kanälen eines Farbbildes codiert sind:  <b>R</b> - X-Position <b>G</b> - Y-Position <b>B</b> - Height <b>A</b> - Packed data:          - Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).          - Absoluter Wert: Thickness + 1. |
| <b>Spline-Daten</b> *Farbe* | Zusätzliche Daten zu den in den RGBA-Kanälen eines Farbbildes codierten Ausgabe-Splines:  <b>R</b> - Tangenten X <b>G</b> - Tangenten Y <b>B</b> - Tangenten Z <b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> *Integer* | Die Anzahl der Ausgabe-Splines. |

## Parameter

|  |  |
| --- | --- |
| <b>Richtung spiegeln</b> *Boolescher Wert* | Kehrt die Richtung des Spline um. |
| <b>Einheitliche Verteilung</b> *Boolescher Wert* | Wenn *True*, werden die Spline-Punkte gleichmäßig vom Anfang bis zum Ende verteilt. |
| <b>Eingabe-Spline anfügen</b> *Boolescher Wert* | Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind. |
| <b>Nicht-quadratische Korrektur</b> *Boolescher Wert* | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Smoothness</b> *Gleitend* | Passt die *Spanne des Bogens* an, der durch den Spline gebildet wird. 1 bedeutet, dass der Spline gewölbt ist und 0 bedeutet, dass der Spline vollständig gerade ist. Der Bogen verläuft von Punkt <b>p3</b> entlang des Splines bis zu seinen Extremitäten. |

+++Höhe

|  |  |
| --- | --- |
| <b>Height starten</b> *Gleitend* | Passt das Height des <b>p1</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.  Dies wirkt sich auf das Height des Splines bei <b>p1</b> aus. |
| <b>Height beenden</b> *Gleitend* | Passt das Height des <b>p3</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.  Dies wirkt sich auf die Thickness des Splines bei <b>p3</b> aus. |
| <b>Automatisches Tangenten-Height</b> *Boolescher Wert* | Passt das Height des <b>p3</b>-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.  Dies wirkt sich auf die Thickness des Splines bei <b>p3</b> aus. |
| <b>Tangent-Height</b> *Gleitend* | Passt das Height an, das von den Tangenten gesteuert wird, die vom <b>p2</b>-Punkt gesteuert werden.  Dies wirkt sich auf das Height entlang des Splines aus, wenn es von <b>p1</b> weggezogen wird und in <b>p3</b> übergeht.   *Hinweis:* Dieser Parameter ist nur verfügbar, wenn <b>das automatische Tangenten-Height</b> auf &quot;False&quot; festgelegt ist. |


+++

+++Stärke

|  |  |
| --- | --- |
| <b>Thickness starten</b> *Gleitend* | Passt die Thickness des <b>p1</b>-Punkts an. Dies wirkt sich auf die Thickness des Splines bei <b>p1</b> aus.   *Hinweis: Die*-Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Thickness beenden</b> *Gleitend* | Passt die Thickness des <b>p3</b>-Punkts an. Dies wirkt sich auf die Thickness des Splines bei <b>p3</b> aus.   *Hinweis: Die*-Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Automatische Tangenten-Thickness</b> *Boolescher Wert* | Setzt die Thickness der Spline-Tangenten automatisch so, dass sie linear von der <b>Start-Thickness</b> zur <b>End-Thickness</b> interpoliert wird.   *Hinweis: Die*-Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Tangent-Thickness</b> *Gleitend* | Passt die Thickness an, die von den Tangenten gesteuert wird, die vom <b>p2</b>-Punkt gesteuert werden.  Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie sich von <b>p1</b> entfernt und in <b>p3</b> übergeht.   *Hinweis: Die*-Thickness wird von bestimmten Spline-Knoten verwendet.  *Hinweis 2:* Dieser Parameter ist nur verfügbar, wenn <b>die automatische Tangente Thickness</b> auf &quot;Falsch&quot; festgelegt ist. |


+++

+++Punktkoordinaten

|  |  |
| --- | --- |
| <b>p1</b> *Float2* | Legt die Position des <b>p1</b>-Punkts im Texturraum fest. |
| <b>p2</b> *Float2* | Legt die Position des <b>p2</b>-Punkts im Texturraum fest.  Der <b>p2</b>-Punkt steuert die *Tangenten* von <b>p1</b> und <b>p3</b>-Punkten. |
| <b>p3</b> *Float2* | Legt die Position des <b>p3</b>-Punkts im Texturraum fest. |


+++

+++Vorschau

|  |  |
| --- | --- |
| <b>Tangenten anzeigen</b> *Boolescher Wert* | Zeigt die Tangente <b>p1</b> Punkt &quot;out&quot; und <b>p3</b> Punkt &quot;in&quot; in der Ausgabe <b>Vorschau</b> an.Kehrt die Richtung des Spline um. |
| <b>Richtungshelfer anzeigen</b> *Boolescher Wert* | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze am Ende in der <b>Vorschau</b>-Ausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> *Boolescher Wert* | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Segmentierungsbetrag</b> *Integer* | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe verwendet werden.  Je höher der Wert, desto glatter die Linie. |
| <b>Thickness (px)</b> *Gleitend* | Passt die Thickness der Spline-Visualisierung in der <b>Vorschau</b>-Ausgabe in Pixel an. |


+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (quadratisch): Beispiel 1](../../../../../../assets/spline-quadratic-example-1.png "Spline (quadratisch): Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (quadratisch): Beispiel 2](../../../../../../assets/spline-quadratic-example-2.png "Spline (quadratisch): Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (quadratisch): Demo](../../../../../../assets/spline-quadratic-demo.gif "Spline (quadratisch): Demo "){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

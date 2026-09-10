---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Verwenden Sie den kubischen Spline-Knoten, um glatte kubische Splines mit vier Steuerpunkten für gekrümmte Pfade zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Kubisch)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---


# Spline (Kubisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-cubic.resources/spline-cubic-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert einen einzelnen Spline zwischen zwei Punkten <b>p1 </b> und <b>p2</b> an beliebigen Positionen.

Die Trajektorie des Splines wird durch die &quot;out&quot;-Tangente von <b>p1</b> und die &quot;in&quot;-Tangente von <b>p2</b> gesteuert.

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
| <b>Spline-Betrag</b> <i>Ganzzahl</i> | Die Anzahl der Eingabe-Splines. |

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
| <b>Richtung spiegeln</b> <i>Boolescher Wert</i> | Kehrt die Richtung des Spline um. |
| <b>Spline anfügen</b> <i>Boolescher Wert</i> | Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Height</b> |  |
| <b>Height starten</b> <i>Gleitend</i> | Passt das Height des p1-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet. Dies wirkt sich auf das Height des Splines bei p1 aus. |
| <b>Height beenden</b> <i>Gleitend</i> | Passt das Height des p2-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet. Dies wirkt sich auf die Thickness des Splines bei p2 aus. |
| <b>Height für automatische Tangente</b> <i>Boolesche Wert</i> | Setzt das Height der Spline-Tangenten automatisch so, dass es linear vom Height &quot;Anfang&quot; zum Height &quot;Ende&quot; interpoliert wird. |
| <b>p1 Tangente Height</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Height der automatischen Tangente&quot; &quot;True&quot; ist) | Passt das Height der &quot;Out&quot;-Tangente des p1-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet. Dies wirkt sich auf das Height entlang des Splines aus, wenn es von p1 weggezogen wird. |
| <b>p2 Tangente Height</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Height der automatischen Tangente&quot; &quot;True&quot; ist) | Passt das Height der Tangente &quot;in&quot; des p2-Punkts an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet. Dies wirkt sich auf das Height entlang des Splines aus, wenn es von p2 weggezogen wird. |
| <b>Thickness</b> |  |
| <b>Thickness starten</b> <i>Fließkommazahl</i> | Passt die Thickness des p1-Punkts an. Dies wirkt sich auf die Thickness des Splines bei p1 aus.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Thickness beenden</b> <i>Fließkommazahl</i> | Passt die Thickness des p2-Punkts an. Dies wirkt sich auf die Thickness des Splines bei p2 aus.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Thickness der automatischen Tangente</b> <i>Boolesche Wert</i> | Setzt die Thickness der Spline-Tangenten automatisch so, dass sie linear von der Start-Thickness zur End-Thickness interpoliert werden.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>p1 Tangente Thickness</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Thickness der automatischen Tangente&quot; &quot;True&quot; ist) | Passt die Thickness der &quot;out&quot;-Tangente des p1-Punkts an. Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie von p1 weggezogen wird.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>p2 Tangente Thickness</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Thickness der automatischen Tangente&quot; &quot;True&quot; ist) | Passt die Thickness der &quot;in&quot;-Tangente des p2-Punkts an. Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie von p2 weggezogen wird.<br>Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Punktkoordinaten</b> |  |
| <b>p1</b> <i>Fließkommazahl2</i> | Legt die Position des p1-Punkts im Texturen-Leerzeichen fest. |
| <b>p1 Tangente</b> <i>Fließkommazahl2</i> | Legt die Position des Griffs der Tangente &quot;out&quot; des p1-Punkts in der Textur fest. |
| <b>p2</b> <i>Fließkommazahl2</i> | Legt die Position des p2-Punkts im Textur-Raum fest. |
| <b>p2 Tangente</b> <i>Fließkommazahl2</i> | Legt die Position des Handles mit der Tangente &quot;in&quot; des p2-Punkts im Textur-Bereich fest. |
| <b>Vorschau</b> |  |
| <b>Tangenten anzeigen</b> <i>Boolesche Wert</i> | Zeigt die &quot;out&quot;-Tangente des p1-Punkts und die &quot;in&quot;-Tangente des p2-Punkts in der Vorschauausgabe an. |
| <b>Richtungs-Helfer anzeigen</b> <i>Boolesche Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden. Je höher der Wert, desto glatter die Linie. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in der Vorschauausgabe in Pixel an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](spline-cubic.resources/SplineCubic-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-cubic.resources/SplineCubic-Variant2.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 3](spline-cubic.resources/SplineCubic-Demo.gif "Knotenbeispiel 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

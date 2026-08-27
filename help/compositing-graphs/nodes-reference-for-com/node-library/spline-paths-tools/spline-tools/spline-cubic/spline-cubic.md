---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# Spline (Kubisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-cubic-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert einen einzelnen Spline zwischen zwei Punkten <b>p1 </b> und <b>p2</b> an beliebigen Positionen.

Die Trajektorie der Spline wird durch die &quot;out&quot;-Tangente von <b>p1</b> und die &quot;in&quot;-Tangente von <b>p2</b> gesteuert.

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

<b>Richtung spiegeln</b> *Boolescher Wert*\
Kehrt die Richtung des Spline um.

<b>Spline anfügen</b> *Boolescher Wert*\
Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

+++Höhe
<b>Height starten</b> *Gleitend* Passt das Height des p1-Punktes an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dies wirkt sich auf das Height des Splines bei p1 aus.

<b>Height beenden</b> *Gleitend* Passt das Height des p2-Punktes an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dies wirkt sich auf die Thickness des Splines bei p2 aus.

<b>Automatisches Tangenten-Height</b> *Boolean* Legt automatisch das Height der Spline-Tangenten fest, das linear vom Height &quot;Anfang&quot; zum Height &quot;Ende&quot; interpoliert wird.

<b>p1 Tangent-Height</b> *Float* (verfügbar, wenn &quot;Auto Tangent Height&quot; &quot;True&quot; ist)\
Passt das Height der Tangente des p1-Punkts &quot;out&quot; an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dies wirkt sich auf das Height entlang des Splines aus, wenn es von p1 weggezogen wird.

<b>p2 Tangent-Height</b> *Float* (verfügbar, wenn &quot;Auto Tangent Height&quot; &quot;True&quot; ist)\
Passt das Height der Tangente des p2-Punkts &quot;in&quot; an, wenn ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet.\
Dies wirkt sich auf das Height entlang des Splines aus, wenn es von p2 weggezogen wird.

+++

+++Stärke
<b>Thickness starten</b> *Gleitend* Passt die Thickness des p1-Punkts an.\
Dies wirkt sich auf die Thickness des Splines bei p1 aus.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>Thickness beenden</b> *Gleitend* Passt die Thickness des p2-Punkts an.\
Dies wirkt sich auf die Thickness des Splines bei p2 aus.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>Automatische Tangent-Thickness</b> *Boolean* Setzt die Thickness der Spline-Tangenten automatisch so, dass sie linear von der Start-Thickness zur End-Thickness interpoliert werden.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>p1 Tangent-Thickness</b> *Float* (verfügbar, wenn &quot;Automatische Tangente-Thickness&quot; &quot;True&quot; ist)\
Passt die Thickness der Tangente des p1-Punkts an.\
Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie von p1 weggezogen wird.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

<b>p2 Tangent-Thickness</b> *Float* (verfügbar, wenn &quot;Automatische Tangente-Thickness&quot; &quot;True&quot; ist)\
Passt die Thickness der Tangente des p2-Punktes &quot;in&quot; an.\
Dies wirkt sich auf die Thickness entlang des Splines aus, wenn sie von p2 weggezogen wird.\
Hinweis: Thickness wird von bestimmten Spline-Knoten verwendet.

+++

+++Punktkoordinaten
<b>p1</b> *Float2* Legt die Position des p1-Punkts im Texturraum fest.

<b>p1 Tangente</b> *Float2* Legt die Position des Tangentengriffs &quot;out&quot; des p1-Punkts im Texturraum fest.

<b>p2</b> *Float2* Legt die Position des p2-Punkts im Texturraum fest.

<b>p2 Tangente</b> *Float2* Legt die Position des Tangentengriffs &quot;in&quot; des p2-Punkts im Texturraum fest.

+++

+++Vorschau
<b>Tangenten anzeigen</b> *Boolesch* Zeigt die Tangente &quot;out&quot; für den p1-Punkt und die Tangente &quot;in&quot; für den p2-Punkt in der Vorschauausgabe an.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in der Vorschauausgabe in Pixel an.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineCubic-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineCubic-Variant2.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 3](../../../../../../assets/SplineCubic-Demo.gif "Knotenbeispiel 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

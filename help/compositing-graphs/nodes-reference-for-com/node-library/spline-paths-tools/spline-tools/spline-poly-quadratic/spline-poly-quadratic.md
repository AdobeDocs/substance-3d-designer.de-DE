---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: Verwenden Sie den Spline Poly Quadratic-Knoten, um komplexe quadratische Splines mit mehreren Kontrollpunkten zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Poly Quadratic)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---


# Spline (Poly Quadratic)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-poly-quadratic-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt einen Spline-Effekt entlang mehrerer Punkte. Die Anzahl und die Positionen dieser Punkte können willkürlich sein oder von einem [Punktlisten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md)-Knoten gesammelt werden.

</td>
</tr>
</table>

Die Bahn der Spline kann von ihren Zwischenpunkten weg geglättet werden, indem jeder Zwischenpunkt der Treffpunkt der &quot;Aus&quot;- und &quot;In&quot;-Tangenten seiner Nachbarn ist.

## Eingangsanschlüsse

<b>Vorschau</b> *Graustufen* Die Vorschau der Eingabe-Splines als Graustufenbild.

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:\
<b> R</b> - X-Position\
<b> G</b> - Y-Position\
<b> B</b> - Height\
<b> A</b> - Paketdaten:\
        * Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
        * Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b> R</b> - Tangenten X\
<b> G</b> - Tangenten Y\
<b> B</b> - Nicht verwendet\
<b> A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Eingabe-Splines.

<b>Punktvorschau </b>*Graustufen* Die Vorschau der Punkte als Graustufenbild.

<b>Eingabepunktliste</b> *Color* (verfügbar, wenn &quot;Eingabepunktliste verwenden&quot; &quot;True&quot; ist)\
Eine Liste von Punkten, die in den RGBA-Kanälen eines Farbbildes codiert sind:\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
        * Ganzzahlteil: Smoothness;\
        * Bruchteil: Thickness.

<b>Punktzahl</b> *Integer* (verfügbar, wenn &quot;Eingabepunktliste verwenden&quot; &quot;True&quot; ist)\
Die Anzahl der Punkte.

>[!IMPORTANT]
>
> Die Connectors <b>Punktliste</b> und <b>Punktnummer</b> sind *nicht kompatibel* mit den Connectors <b>Spline-Code</b>, <b>Spline-Daten</b> und <b>Spline-Betrag</b>, da sie auf unterschiedlichen Daten basieren.

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

<b>Anzahl der Punkte</b> *Integer* Die willkürliche Anzahl von Punkten, die zum Erstellen des Splines verwendet wurden.

<b>Spline-Eingangsverbindungsmodus</b> *Integer* Die zum Verbinden der Eingabe-Splines verwendete Methode:\
*- Auto:* Das Ende des letzten Eingangs-Splines ist mit dem Anfang des generierten Splines verbunden, und das Ende des generierten Splines ist mit dem Anfang des ersten Eingangs-Splines verbunden;\
*- Manuell:* Sie können angeben, welcher der Eingangs-Splines mit den Enden des generierten Splines verbunden werden soll und wo diese Verbindungen auf den Eingangs-Splines landen sollen.

<b>Spline schließen</b> *Boolean* Steuert, ob der Endpunkt des Splines mit seinem Startpunkt verbunden werden soll.\
Die Glättung, die auf den Spline am Start- und Endpunkt angewendet wird, wird durch die Werte dieser Smoothnessen festgelegt.

<b>Richtung spiegeln</b> *Boolescher Wert*\
Kehrt die Richtung des Spline um.

<b>Eingabepunktliste verwenden</b> *Boolesch* Verwenden Sie die Liste der Punkte, die den Eingabesteckern &quot;Eingabepunktliste&quot; und &quot;Punktnummer&quot; bereitgestellt werden, anstelle einer beliebigen Punktliste.\
Die Punktliste kann von einem [Punktliste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md)-Knoten bereitgestellt werden.

<b>Start mit Eingabe-Spline verbinden</b> *Boolean* Wenn dieser Wert auf &quot;True&quot; gesetzt ist, ist der Start des generierten Splines mit dem letzten Punkt des letzten Splines in den Eingangs-Splines verbunden.

<b>Spline-Index für Verbindung starten</b> *Integer* (Verfügbar, wenn &quot;Spline-Eingabemodus&quot; auf &quot;Manuell&quot; und &quot;Start mit Eingabespline verbinden&quot; auf &quot;Wahr&quot; festgelegt ist)Der Index des Eingangssplines, der mit dem Start des generierten Splines verbunden werden soll.

<b>Verbindungsposition starten</b> *Gleitkommawert* (verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Start mit Eingangsabschnitt verbinden&quot; auf &quot;Wahr&quot; gesetzt ist): Die Position auf dem ausgewählten Eingangs-Spline, an der die Verbindung mit dem Start des generierten Splines erfolgen soll.\
Dieser Wert ist die normalisierte Länge des ausgewählten Eingangs-Splines.

<b>Ende mit Eingabe-Spline verbinden</b> *Boolean* Wenn dieser Wert auf &quot;True&quot; gesetzt ist, ist das Ende des generierten Splines mit dem ersten Punkt des ersten Splines in den Eingangs-Splines verbunden.

<b>Spline-Index für Verbindung beenden</b> *Integer* (Verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Ende mit Eingangsabschnitt verbinden&quot; auf &quot;Wahr&quot; festgelegt ist)Der Index des Eingangsabschnitts, der mit dem Ende des generierten Abschnitts verbunden werden soll.

<b>Verbindungsposition beenden</b> *Gleitkommawert* (verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Spline-Ende an Eingang anschließen&quot; auf &quot;Wahr&quot; gesetzt ist)Die Position auf dem ausgewählten Eingangs-Spline, an der die Verbindung zum Ende des generierten Splines enden soll.\
Dieser Wert ist die normalisierte Länge des ausgewählten Eingangs-Splines.

<b>Einheitliche Verteilung</b> *Boolescher Wert*\
Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden die Punkte des Splines in gleichmäßigen Abständen vom Anfang bis zum Ende ausgerichtet.

<b>Spline anfügen</b> *Boolescher Wert*\
Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

<b>Anpassung der globalen Smoothness</b> *Gleitend* Wendet einen gleichmäßigen Versatz auf den Wert der Smoothness aller Punkte an.\
Die resultierende Smoothness wird auf den Bereich [0;1] geklemmt.

+++Punkteigenschaften
<b>p# Eigenschaften</b> *Float3* Legt die Eigenschaften des p#-Punkts fest.\
*- Height:* Passt das Height des Punktes an, an dem ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet;\
*- Smoothness:* Verschiebt den Beginn der Glättung des Splines bei p#, wobei ein Wert von 0 zu einer harten Kurve und 1 zu einer völlig glatten Kurve führt;\
*- Thickness:* Passt die Thickness des Splines bei p# an. Thickness wird von bestimmten Spline-Knoten verwendet.

+++

+++Punktkoordinaten
<b>p#</b> *Float2* Legt die Position des p#-Punkts im Texturraum fest.

+++

+++Vorschau
<b>Tangenten anzeigen</b> *Boolean* Zeigt die Tangenten von p1 und p3 auf p2 in der Vorschauausgabe an.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Umschlag der Thickness anzeigen</b> *Boolescher Wert*\
Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an.

<b>Punktebezeichnung anzeigen</b> *Boolescher Wert*\
Zeigt für jeden Punkt den Namen des Punkts daneben in der Vorschau an.

<b>Labelgröße für Punkte</b> *Float* (Verfügbar, wenn &quot;Punktebezeichnung anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist)\
Die Größe des Labels für jeden Punkt im Texturraum, wobei 0,1 ein Zehntel der Texturbreite ist.

<b>Punkte anzeigen</b> *Boolescher Wert*\
Zeigt die Steuerpunkte für den Spline an.

<b>Punktgröße</b> *Float* (verfügbar, wenn &quot;Punkte anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist)\
Der Radius der Punkte im Texturraum, wobei 0,1 ein Zehntel der Texturbreite beträgt.

<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschauausgabe an.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "Knotenbeispiel 2")

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

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
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Spline (Poly Quadratic)

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

Die Bahn der Spline kann von ihren Zwischenpunkten weg geglättet werden, indem jeder Zwischenpunkt der Treffpunkt der &quot;Out&quot;- und &quot;In&quot;-Tangenten der Nachbarn ist.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |
| <b>Punktevorschau</b> <i>Graustufen</i> | Die Vorschau der Punkte als Graustufenbild. |
| <b>Eingabepunktliste</b> <i>Farbe</i> | (verfügbar, wenn &quot;Eingabepunktliste verwenden&quot; auf &quot;True&quot; gesetzt ist) Eine Punktliste, die in den RGBA-Kanälen eines Farbbildes codiert ist:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Ganzzahl part: Smoothness;<br> - Bruchteil: Thickness. |
| <b>Punktzahl</b> <i>Integer</i> | (verfügbar, wenn &quot;Eingabepunktliste verwenden&quot; auf &quot;True&quot; gesetzt ist) Die Anzahl der Punkte. |

>[!IMPORTANT]
>
> Die Connectors <b>Punktliste</b> und <b>Punktnummer</b> sind *nicht kompatibel* mit den Connectors <b>Spline-Code</b>, <b>Spline-Daten</b> und <b>Spline-Betrag</b>, da sie auf unterschiedlichen Daten basieren.

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
| <b>Anzahl der Punkte</b> <i>Integer</i> | Die beliebige Anzahl der Punkte, die zum Erstellen des Splines verwendet werden. |
| <b>Spline-Eingangsverbindungsmodus</b> <i>Integer</i> | Die Methode, die zum Verbinden der Splines für die Eingabe verwendet wird:<br>- <i>Auto:</i> Das Ende des letzten Splines für die Eingabe ist mit dem Anfang des generierten Splines verbunden, und das Ende des generierten Splines ist mit dem Anfang des ersten Splines für die Eingabe verbunden;<br>- <i>Manuell:</i> Sie können angeben, welcher der Splines für die Eingabe mit den Enden des generierten Splines verbunden werden soll und wo diese Verbindungen auf den Splines für die Eingabe platziert werden sollen. |
| <b>Spline schließen</b> <i>Boolescher Wert</i> | Steuert, ob der Endpunkt des Splines mit seinem Startpunkt verbunden werden soll.<br>Die Glättung, die auf den Spline am Start- und Endpunkt angewendet wird, wird durch die Werte für die Smoothness dieser Punkte angegeben. |
| <b>Richtung spiegeln</b> <i>Boolescher Wert</i> | Kehrt die Richtung des Spline um. |
| <b>Eingabepunktliste verwenden</b> <i>Boolescher Wert</i> | Verwenden Sie statt einer beliebigen Punktliste die Punktliste, die in den Verbindungen &quot;Eingabepunktliste&quot; und &quot;Punktnummer&quot; angegeben ist.<br>Die Punktliste kann von einem [Punktliste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md)-Knoten bereitgestellt werden. |
| <b>Start mit Eingabe-Spline verbinden</b> <i>Boolescher Wert</i> | Wenn dieser Wert auf &quot;True&quot; gesetzt ist, ist der Start des generierten Splines mit dem letzten Punkt des letzten Splines in den Eingabe-Splines verbunden. |
| <b>Spline-Index für Verbindung starten</b> <i>Integer</i> | (Verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Start an Eingangsleitung anschließen&quot; auf &quot;Wahr&quot; gesetzt ist) Der Index des Eingangs-Splines, der mit dem Start des generierten Splines verbunden werden soll. |
| <b>Verbindungsposition starten</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Start mit Eingangsverbindung verbinden&quot; auf &quot;Wahr&quot; gesetzt ist) Die Position auf dem ausgewählten Eingangs-Spline, an der die Verbindung mit dem Start des erzeugten Spline enden soll.<br>Dieser Wert ist die normalisierte Länge des ausgewählten Eingangs-Splines. |
| <b>Ende mit Eingabe-Spline verbinden</b> <i>Boolescher Wert</i> | Wenn dieser Wert auf &quot;True&quot; gesetzt ist, wird das Ende des generierten Splines mit dem ersten Punkt des ersten Splines in den Eingangs-Splines verbunden. |
| <b>Spline-Index für Verbindung beenden</b> <i>Integer</i> | (Verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Spline-Ende an Eingang anschließen&quot; auf &quot;Wahr&quot; eingestellt ist) Der Index des Eingangs-Splines, der mit dem Ende des generierten Splines verbunden werden soll. |
| <b>Verbindungsposition beenden</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Spline-Eingangsverbindungsmodus&quot; auf &quot;Manuell&quot; und &quot;Spline-Ende an Eingang anschließen&quot; auf &quot;Wahr&quot; gesetzt ist) Die Position auf dem ausgewählten Eingangs-Spline, an der die Verbindung zum Ende des erzeugten Spline enden soll.<br>Dieser Wert ist die normalisierte Länge des ausgewählten Eingangs-Splines. |
| <b>Einheitliche Verteilung</b> <i>Boolescher Wert</i> | Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden die Punkte des Splines in gleichmäßigen Abständen vom Anfang bis zum Ende ausgerichtet. |
| <b>Spline anfügen</b> <i>Boolescher Wert</i> | Fügt den generierten Spline am Ende der Liste der Splines hinzu, die mit den <b>Spline</b>-Eingängen verbunden sind. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten.<br>Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Anpassung der globalen Smoothness</b> <i>Gleitend</i> | Wendet einen gleichmäßigen Versatz auf den Wert der Smoothness aller Punkte an.<br>Der resultierende Wert für die Smoothness wird auf den Bereich [0;1] geklemmt. |
| <b>Punkteigenschaften</b> |  |
| <b>p# Eigenschaften</b> <i>Float3</i> | Legt die Eigenschaften des p#-Punkts fest.<br>- <i>Height:</i> Passt das Height des Punkts an, an dem ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet;<br>- <i>Smoothness:</i> Verschiebt den Beginn der Glättung des Splines bei p#, wobei ein Wert von 0 zu einer harten Trajektorie und 1 zu einer völlig glatten führt;<br>- <i>Thickness:</i> Passt die Thickness des Splines bei p# an. Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Punktkoordinaten</b> |  |
| <b>p#</b> <i>Float2</i> | Legt die Position des p#-Punkts im Texturen-Leerzeichen fest. |
| <b>Vorschau</b> |  |
| <b>Tangenten anzeigen</b> <i>Boolescher Wert</i> | Zeigt die Tangenten von p1 und p3 auf p2 in der Vorschauausgabe an. |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Punktebezeichnung anzeigen</b> <i>Boolescher Wert</i> | Zeigt für jeden Punkt den Namen des Punkts daneben in der Vorschau an. |
| <b>Labelgröße für Punkte</b> <i>Gleitend</i> | (Diese Option ist verfügbar, wenn &quot;Punktebeschriftung anzeigen&quot; auf &quot;Wahr&quot; gesetzt ist.) Die Beschriftungsgröße für jeden Punkt im Breitenbereich, wobei 0,1 ein Zehntel der Textur der Textur ist. |
| <b>Punkte anzeigen</b> <i>Boolescher Wert</i> | Zeigt die Steuerpunkte für den Spline an. |
| <b>Punktgröße</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Punkte anzeigen&quot; auf &quot;Wahr&quot; gesetzt ist) Der Radius der Punkte im Breitenbereich, wobei 0,1 ein Zehntel der Textur der Textur ist. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.<br>Ein höherer Wert führt zu einer glatteren Linie. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschau an. |

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

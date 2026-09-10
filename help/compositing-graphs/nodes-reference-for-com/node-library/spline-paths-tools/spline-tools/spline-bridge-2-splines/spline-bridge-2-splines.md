---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Verwenden Sie den Spline Bridge -Knoten, um Texturen zwischen zwei Splines zu überbrücken, um nahtlose Verbindungen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge (2 Splines)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---


# Spline Bridge (2 Splines)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-bridge-2-splines.resources/spline-bridge-2splines-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert Splines von <b>Spline #1</b> bis <b>Spline #2</b> entlang dieser Splines. Die generierten Splines können linear (gerade) oder kubisch (Bézier) (gekrümmt) sein.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Wenn die an die <b>Spline #1</b>- und <b>Spline #2</b>-Eingaben übergebenen Daten mehr als einen Spline enthalten, wird nur der letzte Spline in jeder Liste verwendet.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau #1</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines #1 als Graustufenbild. |
| <b>Spline-#1</b> <i>Farbe</i> | Die Koordinaten der Splines-Punkte #1 in den RGBA-Kanälen eines Farbbildes codiert.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-#1</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines #1 in den RGBA-Kanälen eines Farbbildes codiert.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag #1</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines, die #1 werden. |
| <b>Vorschau #2</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines #2 als Graustufenbild. |
| <b>Spline-#2</b> <i>Farbe</i> | Die Koordinaten der #2 der Eingabesplines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-#2</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines #2 in den RGBA-Kanälen eines Farbbildes codiert.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag #2</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines, die #2 werden. |
| <b>Tangentenlängenkurve starten</b> <i>Graustufen</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.<br>Diese Eingabe wird verwendet, um die Länge der &#39;out&#39;-Tangenten für den Startpunkt jedes generierten Splines entlang der Spline-#1 zu steuern.<br>Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden. |
| <b>Tangentendrehungskurve starten</b> <i>Graustufen</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.<br>Diese Eingabe wird verwendet, um die Drehung der Out-Tangenten für den Startpunkt jeder generierten Spline entlang der Spline-#1 zu steuern.<br>Der Graustufenwert des Bildes stellt eine Anzahl von Windungen dar.<br>Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden. |
| <b>Tangenten-Endlängenkurve</b> <i>Graustufen</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.<br>Diese Eingabe wird verwendet, um die Länge der &quot;in&quot;-Tangenten für den Endpunkt jedes generierten Splines entlang der Spline-#2 zu steuern.<br>Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden. |
| <b>Tangentendrehkurve beenden</b> <i>Graustufen</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.<br>Diese Eingabe wird verwendet, um die Drehung der &quot;in&quot;-Tangenten für den Endpunkt jedes generierten Splines entlang der Spline-#2 zu steuern.<br>Der Graustufenwert des Bildes stellt eine Anzahl von Windungen dar.<br>Sie können einen Kurvenknoten zum Erstellen der Kurve verwenden. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Ausgabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Ausgabesplines.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der in den RGBA-Kanälen eines Farbbilds codierten Ausgabe-Splines.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Ganzzahl</i> | Die Anzahl der Ausgabe-Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Splines-Betrag für Bridge</b> <i>Ganzzahl</i> | Die Anzahl der Splines, die entlang der Spline-#1 zu Spline-#2 generiert werden. |
| <b>Bridge-Splines-Typ</b> <i>Ganzzahl</i> | Der generierte Spline-Typ:<br><br>- Linear: eine gerade Spline von Anfang bis Ende;<br>- Kubische Bézier: eine gekrümmte Spline von Anfang bis Ende, wobei die Kurve durch die Länge und den Winkel der Start- und Endpunkte gesteuert wird. |
| <b>Spline starten #1</b> <i>Fließkommazahl</i> | Verschiebt die Position entlang der Spline-#1 von der Stelle, an der Splines generiert werden. Der Wert ist die normalisierte Länge der Spline-#1.<br>Ein höherer Wert führt dazu, dass die gleiche Anzahl von Splines enger zusammengepackt wird. |
| <b>Spline starten #2</b> <i>Fließkommazahl</i> | Verschiebt die Position entlang der Spline-#2 von der Stelle, an der Splines generiert werden. Der Wert ist die normalisierte Länge der Spline-#2.<br>Ein höherer Wert führt dazu, dass die gleiche Anzahl von Splines enger zusammengepackt wird. |
| <b>Spline-#1 beenden</b> <i>Gleitend</i> | Verschiebt die Position entlang der Spline-#1 bis zu der Stelle, an der Splines generiert werden. Der Wert ist die normalisierte Länge der Spline-#1.<br>Ein niedrigerer Wert führt dazu, dass die gleiche Anzahl von Splines enger zusammengepackt wird. |
| <b>Spline-#1 beenden</b> <i>Gleitend</i> | Verschiebt die Position entlang der Spline-#2 bis zu der Stelle, an der Splines generiert werden. Der Wert ist die normalisierte Länge der Spline-#2.<br>Ein niedrigerer Wert führt dazu, dass die gleiche Anzahl von Splines enger zusammengepackt wird. |
| <b>Spline-Versatz #1</b> <i>Gleitend</i> | Wendet einen Versatz auf den Anfangspunkt aller Splines entlang der Spline-#1 an. Der Wert ist die normalisierte Länge der Spline-#1.<br>Splines, die den Anfang oder das Ende der Spline-Kurve erreichen, werden dort belassen. |
| <b>Spline-Versatz #2</b> <i>Gleitend</i> | Wendet einen Versatz auf den Anfangspunkt aller Splines entlang der Spline-#2 an. Der Wert ist die normalisierte Länge der Spline-#2.<br>Splines, die den Anfang oder das Ende der Spline-Kurve erreichen, werden dort belassen. |
| <b>Zufallsstart versetzen</b> <i>Gleitend</i> | Wendet einen zufälligen Versatz auf den Anfangspunkt jedes Spline entlang der Spline-#1 an. Der Wert ist der normalisierte Abstand zwischen den Splines in der Spline-#1.<br>Wenn dieser Wert auf 0 belassen wird, sind die Splines in gleichmäßigen Abständen zwischen dem Spline-#1 &quot;Anfang&quot; und dem Spline-#1 &quot;Ende&quot; angeordnet. |
| <b>Versatz zufälliges Ende</b> <i>Gleitend</i> | Wendet einen zufälligen Versatz auf den Endpunkt jedes Spline entlang der Spline-#2 an. Der Wert ist der normalisierte Abstand zwischen den Splines in der Spline-#2.<br>Wenn dieser Wert auf 0 belassen wird, sind die Splines in gleichmäßigen Abständen zwischen dem Spline-#2 &quot;Anfang&quot; und dem Spline-#2 &quot;Ende&quot; angeordnet. |
| <b>Tangente Length Start</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Die Länge der Out-Tangente für den Startpunkt auf der Spline-#1 aller generierten Splines. |
| <b>Ende der Tangente</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Die Länge der In-Tangente für den Endpunkt auf der Spline-#2 aller generierten Splines. |
| <b>Drehung der Tangente </b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Die Drehung der Out-Tangente für den Startpunkt auf der Spline-#1 aller generierten Splines.<br>Der Wert ist eine Anzahl von Umdrehungen. |
| <b>Tangente Drehende</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Bridge Splines Type&quot; auf &quot;Cubic Bézier&quot; festgelegt ist) | Die Drehung der In-Tangente für den Endpunkt auf der Spline-#2 aller generierten Splines.<br>Der Wert ist eine Anzahl von Umdrehungen. |
| <b>Vorschau</b> |  |
| <b>Segmentierungsbetrag</b> <i>Ganzzahl</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden. Je höher der Wert, desto glatter die Linie. |
| <b>Richtungs-Helfer anzeigen</b> <i>Boolesche Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolesche Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Thickness (px)</b> <i>Fließkommazahl</i> | Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschau an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-bridge-2-splines.resources/SplineBridge-2Splines_Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

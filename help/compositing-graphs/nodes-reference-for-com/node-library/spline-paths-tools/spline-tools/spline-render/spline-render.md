---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline-Render, um Splines als Texturen mit anpassbaren Breiten-, Farb- und Füllmethoden zu rendern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Render
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Spline-Render

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-render-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet Zeichenfolgen von Segmenten entlang der Eingabe <b>Splines</b> über der Eingabe <b>Background</b>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrund</b> <i>Graustufen</i> | Das Graustufenbild, über das Splines gezeichnet werden sollen. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Ergebnisbild des Zeichnens der Eingabe-Splines über dem Hintergrund. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Modus</b> <i>Integer</i> | Die Methode zum Auswählen der zu zeichnenden Splines:<br>- <i>Spline-Liste zeichnen</i>: Alle Splines in der Eingabeliste zeichnen;<br>- <i>Einzelne Spline zeichnen</i>: Zeichnen Sie nur den angegebenen Spline aus der Eingabeliste;<br>- <i>Spline-Bereich zeichnen</i>: Zeichnen Sie nur die Splines im angegebenen Bereich aus der Eingabeliste. |
| <b>Spline-Index zeichnen</b> <i>Integer</i> | (Verfügbar, wenn &quot;Modus&quot; auf &quot;Einzelne Spline zeichnen&quot; eingestellt ist) Der Index des Splines, der gezeichnet werden soll. |
| <b>Spline-Bereich zeichnen</b> <i>Integer2</i> | (Verfügbar, wenn &quot;Modus&quot; auf &quot;Spline-Bereich zeichnen&quot; eingestellt ist) Der Indexbereich für die Splines, die gezeichnet werden sollen. |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeichnet für jeden Spline-Effekt einen Punkt am Anfang und eine Pfeilspitze an ihrem Ende. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der entlang der Splines gezeichneten Segmente an.<br>Ein höherer Wert führt zu glatteren Linien. |
| <b>Spline-Betrag für Umschlag</b> <i>Integer</i> | Die Anzahl der doppelten Segmente, die entlang der Thickness jedes Splines gezeichnet werden sollen. |
| <b>Start</b> <i>Gleitend</i> | Versetzt den Anfang des Abschnitts des Spline-Effekts, der gezeichnet werden soll.<br>Der Wert stellt die normalisierte Länge des Splines dar. |
| <b>Ende</b> <i>Gleitend</i> | Versetzt das Ende des Abschnitts des Spline-Effekts, der gezeichnet werden soll.<br>Der Wert stellt die normalisierte Länge des Splines dar. |
| <b>Thickness-Größenmodus</b> <i>Integer</i> | Die Methode zum Berechnen der Thickness der gezeichneten Segmente:<br>- <i>Image</i>: Der Wert wird im Texturraum normalisiert, wobei 1 die volle Breite des Bildes ist. Die Thickness ist relativ zur Auflösung der Textur;<br>- <i>Pixel</i>: Der Wert ist eine absolute Anzahl von Pixeln in der Textur, wobei 1 ein ganzes Pixel ist. Die Thickness ist von der Texturauflösung getrennt. |
| <b>Thickness (Bild)</b> <i>Gleitend</i> | (verfügbar, wenn &quot;Bildgrößenmodus&quot; auf &quot;Thickness&quot; eingestellt ist) Die Thickness der gezeichneten Texturen, die im Bildbereich normalisiert wurden, wobei 1 die volle Bildbreite ist. |
| <b>Thickness (px)</b> <i>Gleitend</i> | (verfügbar, wenn &quot;Pixelgrößenmodus&quot; auf &quot;Thickness&quot; gesetzt ist) Die Thickness der gezeichneten Segmente als absolute Pixelanzahl in der Textur, wobei 1 ein Vollpixel ist. |
| <b>Verbindungen aktivieren</b> <i>Boolescher Wert</i> | Füllt die Lücken zwischen den einzelnen Segmenten, die entlang der Splines gezeichnet werden, mithilfe von Discs. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten.<br>Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Farbe</b> |  |
| <b>Hintergrundintensität</b> <i>Gleitend</i> | Der Wert, der mit dem Eingabebild Hintergrund multipliziert wird. |
| <b>Spline-Stil</b> <i>Integer</i> | Die zum Einfärben der Splines verwendete Methode:<br>- <i>Solid</i>: Die Segmente werden mit einem einheitlichen Graustufenwert gezeichnet;<br>- <i>Verlauf</i>: Ein Farbverlauf von Schwarz zu Weiß wird entlang jeder Segmentzeichenfolge von Anfang bis Ende angewendet;<br>- <i>Height</i>: Das Height der Splines wird als Graustufenwert zum Zeichnen der Segmente verwendet. |
| <b>Spline-Farbe</b> <i>Gleitend</i> | Der einheitliche Graustufenwert, der zum Zeichnen der Segmente verwendet wird.<br>Wenn ein anderer Spline-Stil als &quot;Farbfläche&quot; ausgewählt ist, wird diese Farbe mit der formatierten Farbe multipliziert. |
| <b>Zufällige Luminanz</b> <i>Gleitend</i> | Wendet für jede Zeichenfolge aus ungeschnittenen Segmenten in einem Spline einen zufälligen Offset im angegebenen Bereich auf den Graustufenwert an, der zum Zeichnen dieser Zeichenfolge verwendet wird. |
| <b>Füllmethode</b> <i>Integer</i> | Die Methode zum Mischen der Farben des Hintergrunds und der überlappenden Segmente, die entlang der Splines gezeichnet werden: <br>- <i>Max</i>: Der hellste Wert wird verwendet;<br>- <i>Hinzufügen</i>: Die Werte werden addiert. |
| <b>Zufällige Segmente</b> |  |
| <b>Zufallssegmente beginnen</b> <i>Gleitend</i> | Passt die Wahrscheinlichkeit an, dass die Zeichenfolge aus Segmenten, die näher am Anfang des Splines liegt, abgeschnitten wird. |
| <b>Ende zufälliger Segmente</b> <i>Gleitend</i> | Passt die Wahrscheinlichkeit an, dass die Segmentfolge näher am Ende des Spline-Effekts abgeschnitten wird. |
| <b>Zufallsversatz</b> <i>Gleitend</i> | Legt den maximalen Versatz fest, der auf jedes Schnittsegment entlang seiner Normalen angewendet wird.<br>Dieser Parameter hat keine Auswirkungen, wenn Start und Ende beide auf 0 festgelegt sind. |
| <b>Zentrum für zufällige Verschiebung</b> <i>Gleitend</i> | Verschiebt den Mittelpunkt des zufälligen Versatzes, der auf jedes Schnittsegment angewendet wird, entlang seiner Normalen. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
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

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineRender-Demo.gif "Knotenbeispiel 1")

</td>
</tr>
</table>

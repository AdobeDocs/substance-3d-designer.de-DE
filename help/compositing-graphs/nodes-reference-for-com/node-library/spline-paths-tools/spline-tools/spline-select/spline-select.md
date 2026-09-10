---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: Verwenden Sie den Spline-Auswahlknoten, um bestimmte Bereiche basierend auf den Spline-Pfaden in Ihren Graf auszuwählen und zu maskieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Auswahl
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Spline-Auswahl

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-select.resources/spline-select-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wählt Splines in der Eingabeliste entsprechend den angegebenen Kriterien aus und gibt eine neue Liste aus, die nur die ausgewählten Splines enthält.

Ausgewählte Splines können auch zugeschnitten werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

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
| <b>Auswahlmodus</b> <i>Integer</i> | Die Methode zum Auswählen der Splines in der Eingabeliste:<br>- <i>First</i>: Wählt den ersten Spline in der Liste aus;<br>- <i>Last</i>: Wählt den letzten Spline in der Liste aus;<br>- <i>Index</i>: Wählt den Spline mit dem angegebenen Index aus;<br>- <i>Bereich</i>: Wählt die Splines aus, die Indizes im angegebenen Bereich enthalten sind. |
| <b>Spline-Index</b> <i>Integer</i> | (Verfügbar, wenn &quot;Auswahlmodus&quot; auf &quot;Index&quot; eingestellt ist) Der Index des Splines, der ausgewählt werden soll. |
| <b>Bereichsstart</b> <i>Integer</i> | (Verfügbar, wenn &quot;Auswahlmodus&quot; auf &quot;Bereich&quot; eingestellt ist) Der niedrigste Index im Bereich der ausgewählten Splines. |
| <b>Bereichsende</b> <i>Integer</i> | (Verfügbar, wenn &quot;Auswahlmodus&quot; auf &quot;Bereich&quot; eingestellt ist) Der höchste Index im Bereich der ausgewählten Splines. |
| <b>Start</b> <i>Gleitend</i> | Versetzt den Anfang des Abschnitts des Spline-Effekts, der ausgewählt werden soll. Dies schneidet den Spline effektiv zu.<br>Der Wert stellt die normalisierte Länge des Splines dar. |
| <b>Ende</b> <i>Gleitend</i> | Versetzt das Ende des Abschnitts des Spline-Effekts, der ausgewählt werden soll. Dies schneidet den Spline effektiv zu.<br>Der Wert stellt die normalisierte Länge des Splines dar. |
| <b>Vorschau</b> |  |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.<br>Ein höherer Wert führt zu einer glatteren Linie. |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschau an. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Knotenbeispiel 1](spline-select.resources/SplineSelect-Demo.gif "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

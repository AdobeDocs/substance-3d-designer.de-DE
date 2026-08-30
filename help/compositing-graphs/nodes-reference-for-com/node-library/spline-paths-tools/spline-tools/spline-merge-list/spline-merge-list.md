---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline-Zusammenführungsliste , um mehrere Splines in einer einzigen Spline-Liste für kombinierte Operationen zusammenzuführen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Zusammenführungsliste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Spline-Zusammenführungsliste

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-merge-list.resources/spline-merge-list-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Fügt alle Splines in der Eingabeliste zu einem einzigen Spline zusammen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der zusammengeführten Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der Punkte der zusammengeführten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - X-Position<br><b>G</b> - Y-Position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> - Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br> - Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der zusammengeführten Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der zusammengeführten Splines. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Schwellenwert für geschlossene Spline-Distanz</b> <i>Gleitend</i> | Der Abstand im Textur-Raum, unterhalb dessen zwei Enden eines Splines als ein Punkt verarbeitet werden, der diesen Spline schließt.<br>Dies verhindert Überlappungen beim Streuen von Formen oder beim Zuordnen von Bildern entlang der Splines. |
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
      <img src="spline-merge-list.resources/SplineMergeList-Variant2-Before.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant2-After.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant1-Before.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/SplineMergeList-Variant1-After.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Knotendemo](spline-merge-list.resources/SplineMergeList-Demo.gif "Knotendemo")

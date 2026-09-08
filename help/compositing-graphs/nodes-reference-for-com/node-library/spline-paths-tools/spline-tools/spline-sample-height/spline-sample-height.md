---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-height.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline-Beispiel-Height , um Spline-Height-Werte entlang von Splines für prozedurale Versatz-Effekte aufzunehmen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Beispiel-Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Spline-Beispiel-Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-sample-height-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ändert das Height der Eingabe-Splines, indem ihnen ein Eingabe-Height Map zugeordnet wird.

Der Effekt der zugeordneten Height-Map kann angepasst werden, indem die Füllmethode und die Deckkraft dieses Effekts geändert werden.

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
| <b>Height-Map</b> <i>Graustufen</i> | Das zum Ändern des Heights des Eingabe-Splines verwendete Graustufenbild. |

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
| <b>Sampling-Modus</b> <i>Integer</i> | Die Methode zum Zuordnen der Werte auf der Höhen-Map zu den Splines:<br>- <i>Texturen-Leerzeichen</i>: Die Werte werden auf die Splines angewendet, wenn sie in einer Textur unter Verwendung der UV-Koordinaten der Textur platziert würden. Dadurch wird der Wert effektiv auf die Splines &quot;in place&quot;;<br>- <i>Horizontal entlang Spline</i> angewendet: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Koordinateneingabe), wobei jede Zeile auf einen anderen Spline von oben nach unten angewendet wird;<br>- <i>Hor. entlang der Spline (Rand). Versatz X)</i>: Die Werte werden direkt auf die Koordinaten der codierten Splines angewendet (siehe Spline-Coords-Eingabe), mit einem zufälligen horizontalen Versatz in der Skalierungszuordnung für jeden Spline (d. h. jede Zeile in Spline-Coords);<br>- <i>Hor. entlang der Spline (Rand). Offset Y)</i>: Die Werte werden direkt auf die Koordinaten der codierten Spline-Linien angewendet (siehe Spline-Koordinateneingabe), wobei für jeden Spline (d. h. jede Zeile in Spline-Koordinaten) ein zufälliger vertikaler Versatz in der Skalierungszuordnung angezeigt wird. |
| <b>Deckkraft</b> <i>Gleitend</i> | Ein Multiplikator für die Intensität des Beitrags des Höhen-Map-Eingangs zum Height des Splines. |
| <b>Füllmethode</b> <i>Integer</i> | Die Methode zum Mischen der Daten der Höhen-Map mit dem Height des Eingabe-Splines:<br>- <i>Kopieren</i>: Das Height des Splines mit den Höhen-Map-Werten überschreiben;<br>- <i>Hinzufügen</i>: Fügen Sie die Höhen-Map-Werte zum Height des Splines hinzu;<br>- <i>Subtrahieren</i>: Subtrahieren der Höhen-Map-Werte auf das Height des Splines;<br>- <i>Multiplizieren</i>: Multiplizieren Sie die Height-Map-Werte mit dem Height des Splines. |
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
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-After.jpg" alt="SplineSampleHeight-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-After3.jpg" alt="SplineSampleHeight-Variant1-After3">
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

![Knotenbeispiel 1](../../../../../../assets/SplineSampleHeight-Variant1-After4.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineSampleHeight-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

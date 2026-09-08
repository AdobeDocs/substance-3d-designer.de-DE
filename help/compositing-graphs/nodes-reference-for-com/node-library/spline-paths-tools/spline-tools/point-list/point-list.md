---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Punktliste", um Punktlisten für die Spline- und Pfadgenerierung zu erstellen und zu verwalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Punktliste
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Punktliste

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/point-list-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Liste von Punkten, die von einem Spline durchlaufen werden sollen.

Wenn eine vorhandene Punktliste an die <b>Point</b>-Eingaben übergeben wird, wird die generierte Liste an die Eingabeliste angehängt.

</td>
</tr>
</table>

>[!TIP]
>
> Dieser Knoten kann verwendet werden, um dem Knoten [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) Punkte zuzuweisen, um Splines zu erstellen.

>[!IMPORTANT]
>
> Die Connectors <b>Punktliste</b> und <b>Punktnummer</b> sind *nicht kompatibel* mit den Connectors <b>Spline-Code</b>, <b>Spline-Daten</b> und <b>Spline-Betrag</b>, da sie auf unterschiedlichen Daten basieren.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Punkte als Graustufenbild. |
| <b>Punktlisteneingabe</b> <i>Farbe</i> | Eine Liste von Eingangspunkten, die in den RGBA-Kanälen eines Farbbildes codiert sind:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> * Ganzzahl part: Smoothness;<br> * Bruchteil: Thickness. |
| <b>Eingabe von Punktzahlen</b> <i>Integer</i> | Die Anzahl der Eingabepunkte. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Punkte als Graustufenbild. |
| <b>Punkteliste</b> <i>Farbe</i> | Die Ausgabeliste mit Punkten, die in den RGBA-Kanälen eines Farbbildes codiert sind:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br> * Ganzzahl part: Smoothness;<br> * Bruchteil: Thickness. |
| <b>Punktzahl</b> <i>Integer</i> | Die Ausgabenanzahl von Punkten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Punktzahl</b> <i>Integer</i> | Die Anzahl der generierten Punkte. |
| <b>Anpassung der globalen Smoothness</b> <i>Gleitend</i> | Wendet einen gleichmäßigen Versatz auf den Wert der Smoothness aller Punkte an.<br>Der resultierende Wert für die Smoothness wird auf den Bereich [0;1] geklemmt. |
| <b>Punkteigenschaften</b> |  |
| <b>p# Eigenschaften</b> <i>Float3</i> | Legt die Eigenschaften des p#-Punkts fest.<br>*- Height:* Passt das Height des Punkts an, an dem ein niedrigerer Wert eine niedrigere oder tiefere Position bedeutet;<br>*- Smoothness:* Verschiebt den Beginn der Glättung des Splines bei p#, wobei ein Wert von 0 zu einer harten Trajektorie und 1 zu einer völlig glatten führt;<br>*- Thickness:* Passt die Thickness des Splines bei p# an. Thickness wird von bestimmten Spline-Knoten verwendet. |
| <b>Punktkoordinaten</b> |  |
| <b>p#</b> <i>Float2</i> | Legt die Position des p#-Punkts im Texturen-Leerzeichen fest. |
| <b>Vorschau</b> |  |
| <b>Beschriftungen anzeigen</b> <i>Boolescher Wert</i> | Zeigt für jeden Punkt den Namen des Punkts daneben in der Vorschau an. |
| <b>Labelgröße</b> <i>Fließkommazahl</i> (verfügbar, wenn &quot;Beschriftungen anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist) | Die Größe des Labels für jeden Punkt im Texturraum, wobei 0,1 ein Zehntel der Texturbreite ist. |
| <b>Punkte anzeigen</b> <i>Boolescher Wert</i> | Zeigt die Punkte in der Vorschau an. |
| <b>Punktgröße</b> <i>Float</i> (verfügbar, wenn &quot;Punkte anzeigen&quot; auf &quot;Wahr&quot; festgelegt ist) | Der Radius der Punkte im Texturraum, wobei 0,1 ein Zehntel der Texturbreite beträgt. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/PointList-Variant1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/PointList-Demo1.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

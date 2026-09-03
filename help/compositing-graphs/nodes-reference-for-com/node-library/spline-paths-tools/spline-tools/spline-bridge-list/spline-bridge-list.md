---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline Bridge-Liste , um Texturen zwischen mehreren Splines in einer Liste für komplexe Muster zu überbrücken.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge (Liste)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Spline Bridge (Liste)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-bridge-list.resources/spline-bridge-list-01.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert Splines, die alle Splines in der Eingabeliste entlang dieser Splines durchlaufen.

Die generierten Splines können linear (gerade) oder quadratisch (gekrümmt) sein.

</td>
</tr>
</table>

>[!TIP]
>
> Die generierten Splines wechseln vom ersten Spline in der Liste zum letzten und durchlaufen die mittleren Splines, indem sie der Reihenfolge dieser Splines in der Liste genau folgen.
> 
> Daher sollten Sie die Reihenfolge beachten, in der Sie vorher Splines anfügen.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vorschau</b> <i>Graustufen</i> | Die Vorschau der Eingabe-Splines als Graustufenbild. |
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |

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
| <b>Spline-Betrag für Bridge</b> <i>Integer</i> | Die Anzahl der Splines, die über die Eingabe-Splines generiert wurden. |
| <b>Bridge-Splines-Typ</b> <i>Integer</i> | Der generierte Spline-Typ:<br><br>- Linear: eine scharfe Spline, die mittlere Splines mit geraden Trajektorien von Anfang bis Ende verbindet;<br>- Quadratische Bézier: eine gekrümmte Spline, die zwischengeschaltete Splines mit glatten Trajektorien von Anfang bis Ende verbindet.<br><br>Hinweis: Für die Berechnung eines quadratischen Bézier-Splines sind mindestens 3 Splines für den Eingang erforderlich. |
| <b>Eingabe-Splines sind geschlossen</b> <i>Boolescher Wert</i> | Steuert, ob der erste und der letzte Punkt der Eingabe-Splines als ein einzelner Punkt verarbeitet werden sollen. Dadurch wird verhindert, dass der erste und der letzte Spline-Verlauf dupliziert werden. |
| <b>Richtung spiegeln</b> <i>Boolescher Wert</i> | Kehrt die Richtung des Spline um. |
| <b>Bridge-Spline schließen</b> <i>Boolescher Wert</i> | Erweitert die durchlaufenden Splines, um zum ersten Spline in der Eingabeliste zurückzukehren. |
| <b>Spline-Versatz der ersten Brücke</b> <i>Fließkommazahl2</i> | Wendet einen Versatz auf den Anfang aller durchlaufenen Splines an. Der Wert ist die normalisierte Länge der Eingabe-Splines.<br>Generierte Splines, die den Anfangs- oder Endpunkt der durchlaufenen Splines erfüllen, werden dort belassen. |
| <b>Letzter Spline-Versatz für Bridge</b> <i>Float2</i> | Wendet einen Versatz auf das Ende aller durchlaufenen Splines an. Der Wert ist die normalisierte Länge der Eingabe-Splines.<br>Generierte Splines, die den Anfangs- oder Endpunkt der durchlaufenen Splines erfüllen, werden dort belassen. |
| <b>Bereich für zufällige Verschiebung</b> <i>Ganzzahl</i> | Der maximale Abstand, der für den zufälligen Versatz verwendet wird, der auf Splines angewendet wird.<br><br>- <i>Übergeordneter Spline:</i> Die gesamte Länge der übergeordneten Splines wird verwendet. Kann Überschneidungen verursachen.<br>- <i>Intervall:</i> Das Intervall zwischen den Brückenzwickeln wird verwendet. Dadurch werden Überschneidungen vermieden. Dieser Abstand nimmt mit zunehmender Anzahl der Brückenverzahnungen ab. |
| <b>Zufallsversatz starten</b> <i>Gleitend</i> | Ein Multiplikator für den zufälligen Versatz, der auf die Startposition von Brückenzahnkeilen angewendet wird, wobei der maximale Abstand durch den Parameter <b>Bereich für zufällige Versätze</b> angegeben wird. |
| <b>Zufallsverschiebung beenden</b> <i>Gleitend</i> | Ein Multiplikator für den zufälligen Versatz, der auf die Endposition von Brückenzahnkeilen angewendet wird, wobei der maximale Abstand durch den Parameter <b>Zufälliger Versatzbereich</b> angegeben wird. |
| <b>Globaler zufälliger Versatz</b> <i>Fließkommazahl</i> | Ein Multiplikator für den *gleichen Betrag* des zufälligen Versatzes, der auf die *beiden* Anfangs- und Endposition von Brückenzahnkeilen angewendet wird, wobei der maximale Abstand durch den <b>Parameter für den Bereich des zufälligen Versatzes</b> angegeben wird. |
| <b>Einheitliche Verteilung</b> <i>Boolescher Wert</i> | Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden die Punkte der generierten Splines in gleichmäßigen Abständen von Anfang bis Ende angeordnet. |
| <b>Thickness</b> |  |
| <b>Thickness-Modus</b> <i>Integer</i> | Die Methode zum Erfassen des Thickness-Werts für die Bridge-Splines.<br><br>- <i>Von übergeordneten Splines erben:</i> Die Thickness der übergeordneten Splines an den Start- und Endpositionen der Bridge-Splines wird verwendet<br>- <i>Überschreiben:</i> Der beliebige Wert, den Sie im Parameter <b>Thickness</b> angeben, wird verwendet |
| <b>Thickness</b> <i>Gleitend</i> | Der Wert für die absolute Thickness, der auf die Splines der Brücke angewendet wird. |
| <b>Thickness zufällig</b> <i>Gleitend</i> | Ein zufälliger Multiplikator für die Thickness der Brückenzweige, wobei die anfängliche Thickness, auf die dieser Multiplikator angewendet wird, durch den Parameter <b>Thickness mode</b> angegeben wird. |
| <b>Height</b> |  |
| <b>Height-Modus</b> <i>Integer</i> | Die Methode zum Erfassen des Height-Werts für die Bridge-Splines.<br><br>- <i>Von übergeordneten Splines erben:</i> Das Height der übergeordneten Splines an der Start- und Endposition der Bridge-Splines wird verwendet<br>- <i>Überschreiben:</i> Der beliebige Wert, den Sie im Parameter <b>Height</b> angeben, wird verwendet |
| <b>Height-Offset</b> <i>Gleitend</i> | Der Versatzbetrag, der auf das von den übergeordneten Splines geerbte Height angewendet wird, bevor dieses Height auf die Brückensplines angewendet wird. |
| <b>Height</b> <i>Gleitend</i> | Der absolute Height-Wert, der auf die Brückenzweige angewendet wird. |
| <b>Height zufällig</b> <i>Gleitend</i> | Ein zufälliger Anpassungsbetrag für das Height der Bridge-Splines, wobei diese Anpassung von dem ausgewählten <b>Height mode</b>-Parameter abhängt:<br><br>- <i>Von übergeordneten Splines erben:</i> Der Wert ist ein Multiplikator für das geerbte Height.<br>- <i>Überschreiben:</i> Der Wert ist ein Versatz, der dem Height hinzugefügt wird. |
| <b>Nicht-quadratische Korrektur</b> <i>Boolescher Wert</i> | Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht quadratischen Auflösungen beizubehalten. Dies wirkt sich auch auf die einheitliche Verteilung aus. |
| <b>Vorschau</b> |  |
| <b>Richtungshelfer anzeigen</b> <i>Boolescher Wert</i> | Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an. |
| <b>Umschlag der Thickness anzeigen</b> <i>Boolescher Wert</i> | Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an. |
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden. Je höher der Wert, desto glatter die Linie. |
| <b>Thickness (px)</b> <i>Gleitend</i> | Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschau an. |
| <b>Intensität der Hintergrundvorschau</b> <i>Gleitend</i> | Die Intensität der Vorschauvisualisierung. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-bridge-list.resources/spline-bridge-list-04.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

![Knoten im Diagramm](spline-bridge-list.resources/spline-bridge-list-05.jpg "Knoten im Diagramm")

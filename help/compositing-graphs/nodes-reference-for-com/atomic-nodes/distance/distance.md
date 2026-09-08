---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Abstand", um Abstands-Map aus Formen zum Erstellen von Masken und prozeduralen Effekten zu berechnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Abstand
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 8%

---


# Abstand

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Entfernung](../../../../assets/comp_distance_1.png "Atomknoten: Entfernung"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Sucht die Position des nächstgelegenen weißen Pixels in einer Maske und gibt einen Verlauf von dieser Position aus bzw. die Farbe an dieser Position in einem Quellbild aus.

Dieser Knoten erstellt eine lineare Überblendung (Farbverlauf) nach außen von allen Pixeln im Eingangsmaximum über 0,5 Graustufenwert.

</td>
</tr>
</table>

Die nach außen gerichtete Überblendung endet sich, sobald sie auf eine andere Zelle trifft: sie werden sich nie überschneiden. Intern ist dies eigentlich die Berechnung und Anzeige der Entfernung zum nächsten Pixel > 0,5, mit dem Abstand Knoten als Klemme / Maximum gesetzt.

Eine optionale Quell-Map ermöglicht das Kombinieren der Zellen mit der Textur aus einer sekundären Eingangs-Map.

Der Distanzknoten ist kein einfacher Knoten, den man beherrschen kann, aber seine Hauptanwendungsfälle sind die zuverlässige Erweiterung vorhandener Masken (im Vergleich zum Weichzeichnen und Anpassen des Kontrasts), die Erzeugung von Störzellen vom Voronoi-Typ und das Abschrägen vorhandener Formen mit einem scharfen, linearen Profil (das später neu zugeordnet werden kann).

Weitere Informationen finden Sie in den folgenden [Beispielen](#examples).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. Ändert auch den Eingabetyp &quot;Quelleingabe&quot;. |
| <b>Maximale Entfernung</b> *Gleitend* | Passt den maximalen Abstand für die Erkennung des nächsten Rahmens in der Maske in Pixel an. |
| <b>Quelle/Entfernung kombinieren</b> *Boolescher Wert* | Legen Sie fest, wie die optionale &quot;Quelleingabe&quot; mit den endgültigen Zellen kombiniert wird.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Kombinieren:</i> Kombiniert den Wert &quot;Quelleingabe&quot; mit der verblassenden linearen Maske. Wenn der Eingang &quot;Quelleingang&quot; angeschlossen ist, wird sein Wert mit dem berechneten Abstand kombiniert.</li> <li data-preserve-html="true"><i>Nur Quelle:</i> Ergibt nur Volltonfarbe aus der Quelleingabe.</li> </ul> |
| <b>Abstandsmodus</b> *Integer* | Wählt die Methode aus, mit der der Abstand zum nächsten Rand in der extrahierten Maske berechnet wird:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Euklidisch:</i> Summe der quadratischen X/Y-Unterschiede.</li> <li data-preserve-html="true"><i>Manhattan:</i> Summe der X/Y-absolute Werte.</li> <li data-preserve-html="true"><i>Chebyshev:</i> Maximale Anzahl von absoluten Werten von X/Y-Unterschieden.</li> </ul>  <div><img alt="Beispiele für Abstandsmodi" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="../../../../assets/distance-comparison.jpg" title="Beispiele für Abstandsmodi"/></div> |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Maskeneingabe</b> *Graustufen* PRIMÄR | Eine Graustufenmaske, deren Rahmen mit einem Abstandswert berechnet werden soll.   Aus dem Bild wird eine binäre Maske mit einem Schwellenwert von 0,5 extrahiert. Dabei sind alle Werte oberhalb dieses Schwellenwerts weiß und alle darunter liegenden Werte schwarz. |
| <b>Quelleingabe</b> *Farbe/Graustufen* | Optionales Graustufenbild, aus dem der Pixelwert am nächsten Rand der &quot;Maskeneingabe&quot; kopiert werden soll. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe/Graustufen* |  |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex01.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex02.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex03.gif){width="250px"}

</td>
</tr>
</table>

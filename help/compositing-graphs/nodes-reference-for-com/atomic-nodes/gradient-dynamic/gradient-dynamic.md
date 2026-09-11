---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: Verwenden Sie den Verlaufsknoten (Dynamisch), um dynamische Verläufe zu erstellen, die durch Eingabeparameter und Werte gesteuert werden können.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verlauf (dynamisch)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# Verlauf (dynamisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elementare Knoten: Dynamischer Verlauf](gradient-dynamic.resources/comp_dyngradient_1.png "Elementare Knoten: Dynamischer Farbverlauf"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ordnet die Graustufenwerte in einem Bild mithilfe eines von einer Pixelzeile oder -spalte in einem anderen Bild bereitgestellten Verlaufs neu zu.

Sie dient als geringfügige Alternative zum Verlaufsknoten. Im Gegensatz zum Verlaufsknoten werden die Farbtasten für Verläufe jedoch nicht intern definiert, sondern stammen von einer externen Eingabe.

</td>
</tr>
</table>

Dadurch kann vor allem das Problem vermieden werden, dass Parameter nicht gelegt werden können, da die Farbparameter außerhalb des Knotens verschoben werden. Das macht es &quot;dynamisch&quot;.

Der Knoten &quot;Verlauf (Dynamisch)&quot; ist zwar nicht schwer zu verwenden, aber die Anwendungsfälle sind etwas komplexer: Die meisten Standardnutzungen können vom regulären Verlaufsknoten abgedeckt werden.

Dieser Knoten kommt zum Einsatz, wenn Sie durch das Schlüsselsystem des Verlaufseditors zu eingeschränkt sind und möchten, dass Farben und Rampenpositionen von anderen Eingaben, Parametern und Teilen Ihres Grafen gesteuert werden.

Alternativ kann der Schieberegler für die Verlaufseingabeposition verwendet werden, um zwischen mehreren Verläufen zu wechseln, die in einem einzelnen Rampeneingang gespeichert sind.

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

## Parameter

</td>
<td style="border: 0;" valign="top">

### Eingabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Ausgabe-Verbindungen

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Verlaufsadressierung</b> *Boolesche Wert* | Legt fest, ob sich der Verlauf wiederholt (Musterelemente) oder geklemmt wird.   Dieser Parameter bestimmt, wie HDR außerhalb des Bereichs [0, 1] behandelt werden. Pixel der Graustufeneingabe werden verarbeitet: eingeklemmt oder gefaltet bis [0, 1]. |
| <b>Verlaufsausrichtung</b> *Ganzzahl* | Legt die Achse fest, entlang der die &quot;Verlaufseingabe&quot; gesampelt werden soll:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal:</i> Aufnehmen einer Pixelzeile auf der X-Achse.</li> <li data-preserve-html="true"><i>Vertikal:</i> Nehmen Sie eine Pixelspalte auf der Y-Achse auf.</li> </ul> |
| <b>Verlaufseingabeposition</b> *Fließkommazahl* | Die normierte Position der Zeile oder Spalte mit Pixeln, die in der &quot;Verlaufseingabe&quot; abgetastet werden soll. |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Graustufeneingabe</b> *Graustufen* PRIMÄR | Das neu zuzuordnende Graustufenbild. |
| <b>Verlaufseingabe</b> *Farbe/Graustufen* | Der Verlauf wird aus diesem Bild aufgenommen. |

## Ausgabe-Verbindungen

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe/Graustufen* |  |

## Beispiele

*Demnächst verfügbar.*

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Verlauf (Dynamisch), um dynamische Farbverläufe zu erstellen, die über Eingabeparameter und Werte gesteuert werden können.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verlauf (dynamisch)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# Verlauf (dynamisch)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Dynamischer Verlauf](gradient-dynamic.resources/gradient-dynamic-01.png "Atomic Node: Dynamischer Farbverlauf"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ordnet die Graustufenwerte in einem Bild mithilfe eines von einer Pixelzeile oder -spalte in einem anderen Bild bereitgestellten Verlaufs neu zu.

Sie dient als geringfügige Alternative zum Verlaufsknoten. Im Gegensatz zum Verlaufsknoten werden die Farbtasten für Verläufe jedoch nicht intern definiert, sondern stammen von einer externen Eingabe.

</td>
</tr>
</table>

Dadurch lässt sich hauptsächlich das Problem vermeiden, dass Parameter nicht verfügbar gemacht werden können, da die Parameter für Farbe außerhalb des Knotens verschoben werden. Das macht es &quot;dynamisch&quot;.

Der Knoten &quot;Verlauf (Dynamisch)&quot; ist zwar nicht schwer zu verwenden, aber die Anwendungsfälle sind etwas komplexer: Die meisten Standardnutzungen können vom regulären Verlaufsknoten abgedeckt werden.

Dieser Knoten kommt zum Einsatz, wenn du zu eingeschränkt durch das Schlüsselsystem des Verlaufseditors bist und möchtest, dass Farben und Rampenpositionen von anderen Eingaben, Parametern und Teilen deines Diagramms gesteuert werden.

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

### Eingangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Verlaufsadressierung</b> *Boolescher Wert* | Legt fest, ob sich der Verlauf wiederholt (Musterelemente) oder geklemmt wird.   Dieser Parameter bestimmt, wie HDR-Pixel außerhalb des [0, 1]-Bereichs der Graustufeneingabe behandelt werden: eingeklemmt oder gefaltet bis [0, 1]. |
| <b>Verlaufsausrichtung</b> *Integer* | Legt die Achse fest, entlang der die &quot;Verlaufseingabe&quot; abgetastet werden soll:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal:</i> Aufnehmen einer Pixelzeile auf der X-Achse.</li> <li data-preserve-html="true"><i>Vertikal:</i> Nehmen Sie eine Pixelspalte auf der Y-Achse auf.</li> </ul> |
| <b>Verlaufseingabeposition</b> *Gleitend* | Die normierte Position der Zeile oder Spalte mit Pixeln, die in der &quot;Verlaufseingabe&quot; abgetastet werden soll. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Graustufeneingabe</b> *Graustufen* PRIMÄR | Das neu zuzuordnende Graustufenbild. |
| <b>Verlaufseingabe</b> *Farbe/Graustufen* | Der Verlauf wird aus diesem Bild aufgenommen. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe/Graustufen* |  |

## Beispiele

*Demnächst verfügbar.*

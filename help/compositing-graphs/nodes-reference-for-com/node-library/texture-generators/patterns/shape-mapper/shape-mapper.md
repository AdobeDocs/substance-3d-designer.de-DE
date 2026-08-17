---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: Verwenden Sie den Formenzuordnungs-Knoten, um Formen mit anpassbaren Transformationen und Positionierungen Texturen zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Formenzuordnung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Formenzuordnung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Formenzuordnung - Symbol](../../../../../../assets/shape_mapper.png "Formenzuordnung - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Projiziert ein Eingabebild entlang eines Kreises oder Polygons.

Durch die Projektion wird das Bild so verformt, dass es der Umrisslinie der Form folgt, und es wird exakt auf eine bestimmte Anzahl von Wiederholungen ohne Lücken angepasst.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Eingaben

</td>
<td style="border: 0;" valign="top">

### Ausgaben

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Eingaben

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen* | Das Muster, das entlang der Form platziert werden soll. |

## Ausgaben

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Das Ergebnis der Projektion des Musters entlang der Form als Graustufen-Bitmap. |

## Parameter

|  |  |
| --- | --- |
| <b>Shape</b> Integer | Legt den Typ der Form fest, entlang der Muster platziert werden sollen:<ul data-preserve-html="true"> <li data-preserve-html="true">Kreis</li> <li data-preserve-html="true">Polygon</li> </ul> |
| <b>Musterbetrag</b> Ganzzahl | Die Anzahl der Muster, die entlang der ausgewählten Form platziert werden. |
| <b>Verknüpfungssegmente mit Mustermenge</b> Boolescher Wert *Verfügbar, wenn &quot;Form&quot; auf &quot;Polygon&quot; festgelegt ist* | Verwenden Sie den <b>Musterbetrag</b> als Anzahl von <b>Segmenten</b>.   Dadurch verhinderst du, dass Muster um Ecken fließen. Du erhältst ein gerades, einheitliches Aussehen. |
| <b>Segmente</b> Ganzzahl *Verfügbar, wenn &quot;Form&quot; auf &quot;Polygon&quot; und &quot;Segmente mit Musterbetrag verknüpfen&quot; auf &quot;Falsch&quot; festgelegt sind* | Die Anzahl der Segmente für das Polygon, entlang denen Muster platziert werden.   Segmente haben eine *gleichmäßige Größe*, und alle Scheitelpunkte sind *äquidistant von der Mitte*, sodass durch Erhöhen der Anzahl der Segmente das Polygon zu einem Kreis zusammenläuft. |
| <b>Radius</b> Gleitend | Ein Multiplikator für den Radius der Form, wobei 1,0 die halbe Länge der kürzesten Seite des Bildes ist. |
| <b>Breite</b> Gleitend | Ein Multiplikator für die Breite der Muster entlang der Form, wobei 1,0 die halbe Länge der kürzesten Seite des Bildes ist. |
| <b>Drehung</b> Gleitend | Der Wert, um den die Drehung auf die Form angewendet wird, in der Anzahl der Windungen im Uhrzeigersinn von der horizontalen rechten Seite. |
| <b>Einen auf zwei spiegeln</b> Boolescher Wert | Spiegeln Sie jede zweite Form vertikal. |
| <b>Filtermodus</b> Ganze Zahl | Die Filtermethode, die auf die entlang der Form platzierten Muster angewendet wird:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Nächster Wert:</i> Wendet den Wert des nächstgelegenen projizierten Pixels unverändert an, was zu einem schärferen, aber geglätteten Aussehen führt.</li> <li data-preserve-html="true"><i>Bilinear:</i> Wendet einen bilinearen Filter an, um das projizierte Pixel mit seinen Nachbarn zu interpolieren, um einen glatteren, aber unschärferen Look zu erzielen.</li> </ul> |
| <b>Nicht quadratische Erweiterung</b> Boolescher Wert | Bei nicht quadratischen Bildern bleibt die erzeugte Form quadratisch und erweitert die Bilderzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

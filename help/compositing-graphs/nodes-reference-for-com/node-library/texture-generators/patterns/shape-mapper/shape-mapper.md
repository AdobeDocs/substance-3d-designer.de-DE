---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Formenzuordnung

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

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> | Das Muster, das entlang der Form platziert werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Ergebnis der Projektion des Musters entlang der Form als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Form</b> <i>Integer</i> | Legt den Typ der Form fest, entlang der Muster platziert werden sollen:<ul data-preserve-html="true"> <li data-preserve-html="true">Kreis</li> <li data-preserve-html="true">Polygon</li> </ul> |
| <b>Mustermenge</b> <i>Integer</i> | Die Anzahl der Muster, die entlang der ausgewählten Form platziert werden. |
| <b>Segmente mit Musterbetrag verknüpfen</b> <i>Boolescher Wert</i>   *Verfügbar, wenn &#39;Shape&#39; auf &#39;Polygon&#39; festgelegt ist* | Verwenden Sie den <b>Musterbetrag</b> als Anzahl von <b>Segmenten</b>.   Dadurch verhinderst du, dass Muster um Ecken fließen. Du erhältst ein gerades, einheitliches Aussehen. |
| <b>Segmente</b> <i>Integer</i>   *Verfügbar, wenn &quot;Shape&quot; auf &quot;Polygon&quot; und &quot;Segmente mit Musterumfang verknüpfen&quot; auf &quot;False&quot; festgelegt ist* | Die Anzahl der Segmente für das Polygon, entlang denen Muster platziert werden.   Segmente haben eine *gleichmäßige Größe*, und alle Scheitelpunkte sind *äquidistant von der Mitte*, sodass durch Erhöhen der Anzahl der Segmente das Polygon zu einem Kreis zusammenläuft. |
| <b>Radius</b> <i>Gleitend</i> | Ein Multiplikator für den Radius der Form, wobei 1,0 die halbe Länge der kürzesten Seite des Bildes ist. |
| <b>Breite</b> <i>Gleitend</i> | Ein Multiplikator für die Breite der Muster entlang der Form, wobei 1,0 die halbe Länge der kürzesten Seite des Bildes ist. |
| <b>Drehung</b> <i>Gleitend</i> | Der Wert, um den die Drehung auf die Form angewendet wird, in der Anzahl der Windungen im Uhrzeigersinn von der horizontalen rechten Seite. |
| <b>Einen auf zwei spiegeln</b> <i>Boolescher Wert</i> | Spiegeln Sie jede zweite Form vertikal. |
| <b>Filtermethode</b> <i>Integer</i> | Die Filtermethode, die auf die entlang der Form platzierten Muster angewendet wird:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Nächster Wert:</i> Wendet den Wert des nächstgelegenen projizierten Pixels unverändert an, was zu einem schärferen, aber geglätteten Aussehen führt.</li> <li data-preserve-html="true"><i>Bilinear:</i> Wendet einen bilinearen Filter an, um das projizierte Pixel mit seinen Nachbarn zu interpolieren, um einen glatteren, aber unschärferen Look zu erzielen.</li> </ul> |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt die erzeugte Form quadratisch und erweitert die Bilderzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

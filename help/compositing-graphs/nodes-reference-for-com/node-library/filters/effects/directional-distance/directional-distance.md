---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/directional-distance.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Richtungsabstand", um Abstandsfelder in bestimmten Richtungen für prozedurale Effekte zu berechnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Directional distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsabstand
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Richtungsabstand

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Anisotropes Kuwahara-Graustufen-Symbol](directional-distance.resources/directional_distance.png "Anisotropes Kuwahara-Graustufen-Symbol"){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet einen Abstandsverlauf von den Rändern einer Maske in eine bestimmte Richtung.

Überlappende Farbverläufe werden nach invertierten normalisierten Abständen sortiert, sodass der Abstand zum nächsten Rand gezeichnet wird.

Der Abstand des Verlaufs kann mithilfe eines Abstands-Map dynamisch entlang des Rands angepasst werden.

</td>
</tr>
</table>

>[!TIP]
>
> Der Knoten &quot;[Weiche Abschrägung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md)&quot; bietet ähnliche Funktionen, bei denen die Erweiterung in alle Richtungen ausgeführt wird.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> PRIMÄR | Das Bild, aus dem die Maske entnommen werden soll.   Alle Werte über 0,5 sind in dieser Maske weiß. |
| <b>Abstands-Map</b> <i>Graustufen</i> | Eine optionale Eingabe, die verwendet wird, wenn der Wert des Parameters &quot;Abstands-Map-Multiplikator&quot; größer als 0 ist.   Er wird verwendet, um den Abschrägungs-/Dilatationsabstand entlang der Ränder der Maske einzustellen, wobei ein dunklerer Wert zu einem kürzeren Abstand führt. |
| <b>Winkelzuordnung</b> <i>Graustufen</i> | Eine optionale Eingabe, die verwendet wird, wenn der Wert des Parameters &quot;Winkelzuordnungsvervielfacher&quot; größer als 0 ist.   Er wird verwendet, um die Richtung des Abstandsverlaufs anzupassen, indem sein Wert dem Richtungswinkel in der Anzahl der Windungen hinzugefügt wird.   Mit dem Parameter &quot;Winkel-Map-Versatz&quot; können Sie die Werte neu zuordnen, indem Sie angeben, welcher Wert 0 ist. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das Ergebnisbild entsprechend dem ausgewählten &#39;Ausgabemodus&#39;. |
| <b>UV</b> <i>Farbe</i> | Eine UV-Map, in der die UVs von den Maskenrändern entlang der angegebenen Richtung erweitert werden.   Dieser kann mit einem [UV Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)-Knoten verbunden werden, um ein anderes Bild mithilfe dieser erweiterten UVs zuzuordnen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabemodus</b> *Integer* | Die Methode zum Zeichnen des Abstandsverlaufs von den Maskenrändern:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Invertierte normalisierte Entfernung:</b> Ein Farbverlauf von 1 bis 0, wobei 0 bei der &#39;Maximalen Entfernung&#39; erreicht wird, multipliziert mit der &#39;Abstands-Map&#39;, falls verbunden</li> <li data-preserve-html="true"><b>Abstand:</b> Ein Farbverlauf mit unformatierten Abstandswerten von der Maskenbegrenzung, wobei 1 die Länge der Schmalseite des Eingabebilds ist</li> </ul> |
| <b>Maximale Entfernung</b> *Gleitend* | Die Entfernung, die der Abstandsverlauf zurücklegt, in einem normierten Bildraum, wobei 1 die Länge der Schmalseite des Eingabebilds ist. |
| <b>Winkel</b> *Gleitend* | Die Richtung des Abstandsgradienten in mehreren Windungen, wobei 0 horizontal und nach rechts - d. h. ein (1,0) Vektor - verläuft. |
| <b>Abstands-Map-Multiplikator</b> *Gleitend* | Passt die Auswirkung des Abstands-Map auf die &quot;Maximale Entfernung&quot; an.   Hinweis: Dieser Parameter hat keine Auswirkungen, wenn der Abstands-Map-Eingang nicht angeschlossen ist. |
| <b>Winkelzuordnungsmultiplikator</b> *Gleitend* | Passt die Auswirkung der &quot;Winkelkarte&quot; auf den &quot;Winkel&quot; an. |
| <b>Winkelzuordnungs-Offset</b> *Gleitend* | Ordnet die Werte in der &#39;Angle Map&#39; neu zu, indem angegeben wird, welcher Wert in dieser Karte 0 sein soll.   Beispielsweise bedeutet ein Versatz von 0,5, dass ein Wert von 0,75 0,25 Windungen und ein Wert von 0,3 -0,2 Windungen beträgt. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_before.jpg" alt="direction_distance_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_after.jpg" alt="direction_distance_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_before.jpg" alt="direction_distance_example_3_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_after.jpg" alt="direction_distance_example_3_after">
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

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_before.jpg" alt="direction_distance_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_after.jpg" alt="direction_distance_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_before.jpg" alt="direction_distance_example_5_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_after.jpg" alt="direction_distance_example_5_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_before.jpg" alt="direction_distance_example_4_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_after.jpg" alt="direction_distance_example_4_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

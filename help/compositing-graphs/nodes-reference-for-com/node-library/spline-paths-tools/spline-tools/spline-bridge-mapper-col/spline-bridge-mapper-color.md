---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Spline Bridge Mapper Color , um Texturen mit einer Farbzuordnung zwischen zwei Splines zu überbrücken.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Bridge-Zuordnungsfarbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Spline-Bridge-Zuordnungsfarbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ordnet ein Farbbild einer Liste von Eingabe-Splines zu, sodass das Bild die Splines in der richtigen Reihenfolge durchläuft.

</td>
</tr>
</table>

>[!TIP]
>
> Die Zuordnung geht vom ersten Spline in der Liste zum letzten und durchläuft die mittleren Splines, indem die Reihenfolge dieser Splines in der Liste strikt eingehalten wird.
> 
> Daher sollten Sie die Reihenfolge beachten, in der Sie vorher Splines anfügen.

>[!NOTE]
>
> Siehe auch [Spline Bridge Mapper Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Spline-Kabel</b> <i>Farbe</i> | Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Packed data:<br>- Sign: Spline ist geschlossen (negativ) oder offen (positiv);<br>- Absolute Wert: Thickness + 1. |
| <b>Spline-Daten</b> <i>Farbe</i> | Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.<br><b>R</b> - Tangenten X<br><b>G</b> - Tangenten Y<br><b>B</b> - Nicht verwendet<br><b>A</b> - Nicht verwendet |
| <b>Spline-Betrag</b> <i>Integer</i> | Die Anzahl der Eingabe-Splines. |
| <b>Farbzuordnung</b> <i>Farbe</i> | Das Eingabefarbbild, das den Eingabesplines zugeordnet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Farbe</b> <i>Graustufen</i> | Das Ergebnis der Zuordnung des Eingabefarbbilds über die Splines über dem Hintergrund als Farbbild. |
| <b>Height</b> <i>Graustufen</i> | Das Height der Splines, die den Splines als Graustufenbild zugeordnet sind. |
| <b>UV</b> <i>Farbe</i> | Die UVs (d. h. Koordinaten) des abgebildeten Bildes, codiert in den roten (U) und grünen (V) Kanälen eines Farbbildes. |
| <b>Maske</b> <i>Graustufen</i> | Eine Maske der Zuordnung über die Splines hinweg. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Segmentierungsbetrag</b> <i>Integer</i> | Splines werden zu Segmenten vereinfacht, bevor Bildkoordinaten sie durchlaufen. Eine größere Anzahl von Segmenten führt zu einer glatteren Zuordnung entlang von Kurven. |
| <b>UVs dehnen</b> <i>Boolescher Wert</i> | Passt die Methode zur Interpolation der Bildkoordinaten von einem Spline zum nächsten an, um den dehn zu minimieren, wenn der Abstand zwischen den Splines ungleichmäßig ist. |
| <b>UV-Skalierung</b> <i>Float2</i> | Passt die Skalierung der Bildkoordinaten an. Höhere Werte führen zu einem dichter gefliesten Bild. |
| <b>UV-Drehung</b> <i>Gleitend</i> | Dreht die Bildkoordinaten um ihren Mittelpunkt. |
| <b>Hintergrundfarbe</b> <i>Float4</i> | Die Hintergrundfarbe im Ausgabebild. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Graph.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

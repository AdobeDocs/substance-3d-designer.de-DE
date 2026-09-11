---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten UV Mapper Graustufen , um Graustufen-Texturen entlang von Splines für die prozedurale Generierung von Texturen zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV Mapper Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# UV Mapper Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](uv-mapper-grayscale.resources/uv-mapper-grayscale-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ordnet das eingegebene Graustufenbild anhand der Koordinaten zu, die in der UV-Eingabe angegeben sind.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [UV Mapper Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>UV</b> <i>Farbe</i> | Bildkoordinaten, die in den roten (U) und grünen (V) Kanälen eines Farbbildes codiert sind. |
| <b>Eingabe</b> <i>Farbe</i> | Das Graustufenbild, das den Koordinaten in der UV-Eingabe zugeordnet werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Farbe</i> | Das Ergebnis der Zuordnung des Eingabebilds mithilfe der eingegebenen UV-Koordinaten als Graustufenbild. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/UVMapper-Variant2-After.jpg" alt="UVMapper-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Knotenbeispiel 1](uv-mapper-grayscale.resources/UVMapper-Graph.jpg "Knotenbeispiel 1")

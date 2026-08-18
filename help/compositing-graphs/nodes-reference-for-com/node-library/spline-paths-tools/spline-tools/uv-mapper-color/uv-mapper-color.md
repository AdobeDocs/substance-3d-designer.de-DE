---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "UV-Mapper-Farbe", um Farbstrukturen entlang von Splines für die prozedurale Texturgenerierung zuzuordnen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV-Mapper-Farbe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# UV-Mapper-Farbe

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/uv-mapper-color-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ordnet das Eingabefarbbild anhand der Koordinaten zu, die in der UV-Eingabe angegeben sind.

</td>
</tr>
</table>

>[!NOTE]
>
> Siehe auch [UV Mapper Graustufen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

## Eingangsanschlüsse

<b>UV</b> *Farbe* Bildkoordinaten, die in den roten (U) und grünen (V) Kanälen eines Farbbildes codiert sind.

<b>Eingabe</b> *Farbe* Das Farbbild, das den Koordinaten in der UV-Eingabe zugeordnet werden soll.

## Ausgangsanschlüsse

<b>Ausgabe</b> *Farbe* Das Ergebnis der Zuordnung des Eingabebilds unter Verwendung der Eingabe-UV-Koordinaten als Farbbild.

## Parameter

<b>Hintergrundfarbe</b> *Float4* Die Hintergrundfarbe des Ausgabebildes.\
Der Hintergrund ist in den Bereichen des Bildes sichtbar, in denen keine UVs definiert sind (d. h. der Wert ist (0, 0, 0, 0)).

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Knoten im Diagramm](../../../../../../assets/UVMapperColor-Graph.jpg "Knoten im Diagramm")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

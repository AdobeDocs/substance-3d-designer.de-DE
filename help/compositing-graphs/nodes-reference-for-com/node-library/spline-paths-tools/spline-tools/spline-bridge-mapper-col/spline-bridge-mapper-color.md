---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Spline-Bridge-Zuordnungsfarbe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-bridge-mapper-color-icon.png "Knotensymbol")

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

## Eingangsanschlüsse

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der in den RGBA-Kanälen eines Farbbildes codierten Punkte der Eingabesplines:\
<b> R</b> - X-Position\
<b> G</b> - Y-Position\
<b> B</b> - Height\
<b>A</b> - Paketdaten:\
* Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
* Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Eingabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
<b> R</b> - Tangenten X\
<b> G</b> - Tangenten Y\
<b> B</b> - Nicht verwendet\
<b> A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Eingabe-Splines.

<b>Farbzuordnung </b>*Farbe* Das Eingabefarbbild, das den Eingabesplines zugeordnet werden soll.

## Ausgangsanschlüsse

<b>Farbe</b> *Graustufen* Das Ergebnis der Zuordnung des Eingabefarbbilds über die Splines über dem Hintergrund als Farbbild.

<b>Height</b> *Graustufen* Das Height der Splines, die den Splines als Graustufenbild zugeordnet sind.

<b>UV</b> *Farbe* Die UVs (d. h. Koordinaten) des zugeordneten Bildes, codiert in den roten (U) und grünen (V) Kanälen eines Farbbildes.

<b>Maske</b> *Graustufen* Eine Maske der Zuordnung über die Splines hinweg.

## Parameter

<b>Segmentierungsbetrag</b> *Integer* Splines werden in Segmente vereinfacht, bevor Bildkoordinaten sie durchlaufen.\
Eine größere Anzahl von Segmenten führt zu einer glatteren Zuordnung entlang von Kurven.

<b>UVs dehnen</b> *Boolean* Passt die Methode an, die zum Interpolieren der Bildkoordinaten von einem Spline zum nächsten verwendet wird, um die Dehnung zu minimieren, wenn der Abstand zwischen den Splines ungleichmäßig ist.

<b>UV-Skalierung</b> *Gleitkomma2* Passt die Skalierung der Bildkoordinaten an. Höhere Werte führen zu einem dichter gefliesten Bild.

<b>UV-Drehung</b> *Gleitend* Dreht die Bildkoordinaten um ihren Mittelpunkt.

<b>Hintergrundfarbe</b> *Float4* Die Hintergrundfarbe im Ausgabebild.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

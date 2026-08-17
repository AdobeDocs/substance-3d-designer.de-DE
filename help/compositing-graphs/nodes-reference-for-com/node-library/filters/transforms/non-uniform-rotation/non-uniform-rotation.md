---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Uneinheitliche Drehung", um uneinheitliche Drehtransformationen anzuwenden, um Spiral- und Wirbeleffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ungleichmäßige Drehung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# ungleichmäßige Drehung

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**In:** Filter*/Transformationen*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Nicht-gleichförmige Drehung** dreht die **Eingabe** mithilfe der **Rotation Map**-Eingabe.

Die Werte des Bildes stellen eine *Anzahl von Windungen* dar. Die Drehung wird um die Position ausgeführt, die durch den Wert **Pivot-Position** oder die Eingabe **Pivot-Positionen-Map** angegeben wird.\
Positive Werte in der **Rotation Map**-Eingabe führen zu einer *Drehung im Uhrzeigersinn*.

</td>
</tr>
</table>

## Parameter

### Eingaben

* **Eingabe** *Graustufen/Farbe*\
  Das Graustufenbild, das gedreht werden soll.
* **Rotation Map** *Graustufen* Die Karte, die verwendet wurde, um den Umfang der Drehung zu steuern, in *Anzahl der Windungen*. Die aufgenommenen Werte werden mit dem **Drehwinkelmultiplikator** multipliziert. Negative Werte führen zu einer Drehung von *gegen den Uhrzeigersinn*.
* **Drehfarbenzuordnung** *Pivot-Position*\
  Das Bild, das zum Angeben der Position der Drehung *Pivot* verwendet wird. Die Position **X/Y** ist den **R/G** Kanälen des Bildes zugeordnet.

### Parameter

* **Drehwinkelmultiplikator** *Gleitend*\
  Passt die Intensität der **Rotation Map**-Eingabe an.
* **Versatz des Drehwinkels** *Gleitend*\
  Wendet die angegebene zusätzliche Drehung an.
* **Pivot-Positionen-Map verwenden** *Boolesch*\
  Verwenden Sie eine *Bitmapeingabe*, um die Position des Drehzapfens anzugeben. Die Position **X/Y** ist den Kanälen **R/G** der Eingabe **Positionszuordnung** zugeordnet.
* **Pivot-Position** *Gleitkomma2*\
  Die Position des Drehpunkts, um den das Bild gedreht wird.
* **Hintergrundfarbe** *Unverankert/Unverankert4*\
  Hintergrundfarbe, die *außerhalb der Bildbegrenzungen* anzeigt, falls die Unterteilung nicht auf **H und V Unterteilung** festgelegt ist.
* **Filtermodus** *Ganzzahl*\
  Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn ** zwischen Pixeln interpoliert wird:
  * *Nächste*: nimmt genau den *gleichen* Wert auf (schneller)
  * *Bilinear*: wendet einen bilinearen Filter auf das Ergebnis für einen *glatteren*-Look an.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>

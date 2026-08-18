---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Extend Shape", um Formen über ihre Begrenzungen hinaus zu erweitern und so erweiterte Masken- und Mustereffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**In:** Filters*/Effects*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Extend Shape** erweitert einen *Abschnitt* der **Eingabe** um eine festgelegte Richtung und Entfernung.

Mit dem Parameter **Show helper** können Sie den erweiterten Abschnitt und die Erweiterungsrichtung anzeigen.

</td>
</tr>
</table>

## Parameter

* **Modus** *Integer* Definiert die *Parameter*, die zum Anwenden der Erweiterung verwendet werden:
  * *Bidirektional*: Der Abschnitt der **Eingabe**, der durch die **Erweiterungsposition** und den **Erweiterungswinkel** angegeben wird, wird über die **Erweiterungsentfernung** in *entgegengesetzte Richtungen erweitert*
  * *Unidirektional*: Der Abschnitt der **Eingabe**, der durch die **Erweiterungsposition** und den **Erweiterungswinkel** angegeben wird, wird über die **Erweiterungsentfernung** in einer *einfachen Richtung* erweitert.
  * *Start-/Endpositionen*: Eine Erweiterung *Vektor* wird durch **Startposition** und **Endposition** definiert. Der Abschnitt *Senkrecht* der **Eingabe** an der **Startposition** wird *über diesen Vektor* bis zur **Endposition** erweitert.
* **Erweiterungsentfernung** *Gleitkommawert* Die Entfernung, über die der durch die **Erweiterungsposition** und **Erweiterungswinkel** angegebene Abschnitt erweitert werden soll. Der Abstand wird als *Proportion* der Bildspanne ausgedrückt.
* **Erweiterungsposition** *Unverankert* Die Position im Bild des Abschnitts, der erweitert werden soll. Der Wert wird als *-Versatz vom Mittelpunkt* ausgedrückt.
* **Ausdehnungswinkel** *Gleitend* Der Winkel des Abschnitts, der erweitert werden soll, wobei der Ausgangspunkt ein *vertikaler Abschnitt* ist.
* **Startposition** *Gleitkomma2* Die Startposition des *Erweiterungsvektors*.
* **Endposition** *Gleitkomma2* Endposition des *Erweiterungsvektors*.
* **Luminanzversatz starten** *Unverankert* Wendet einen Luminanzversatz auf den Bereich des Bildes an, der *dem erweiterten Abschnitt vorausgeht*. Dieser Luminanzversatz wird *entlang des Abschnitts* auf die Luminanz des Bildbereichs nach dem Abschnitt interpoliert.\
  *Hinweis*: Dieser Parameter ist nur in der **Grayscale**-Version des Knotens verfügbar.
* **Luminanzversatz beenden** *Unverankert* Wendet einen Luminanzversatz auf den Bereich des Bildes an, der *auf den erweiterten Abschnitt folgt*. Dieser Luminanzversatz wird *entlang des Abschnitts* auf die Luminanz des Bereichs des Bildes vor dem Abschnitt interpoliert.\
  *Hinweis*: Dieser Parameter ist nur in der **Grayscale**-Version des Knotens verfügbar.
* **Lum. Offset ignoriert schwarze Pixel** *Boolean* Wenn auf *True* festgelegt, werden die in *beiden* **Luminanzversatz starten** und **Luminanzversatz beenden** angegebenen Luminanzversätze nur auf *nicht schwarze* Pixel angewendet, d. h. Pixel, deren Wert größer als 0 ist.\
  *Hinweis*: Dieser Parameter ist nur in der **Grayscale**-Version des Knotens verfügbar.
* **Filtermodus** *Integer* Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn *zwischen Pixeln interpoliert wird*:
  * *Nächste*: nimmt genau den *gleichen* Wert auf (schneller)
  * *Bilinear*: wendet einen bilinearen Filter auf das Ergebnis für einen *glatteren*-Look an.
* **Helper anzeigen** *Boolesch* Den erweiterten *Abschnitt anzeigen* als Überlagerung mit Pfeilen, die die *Richtung* der Erweiterung anzeigen.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>

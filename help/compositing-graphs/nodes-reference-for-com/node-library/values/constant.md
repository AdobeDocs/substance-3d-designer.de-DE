---
helpx_url: ""
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer auf Konstantenknoten zu, um Konstantenwerte in Substance-Graf zu definieren.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Konstanten
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Konstanten

Konstantenknoten sind eine Möglichkeit, einen statischen Wert für die Verwendung innerhalb von Substance-Grafen zu erstellen.

Sie finden diese Knoten im Abschnitt **Werte > Konstanten** der Bibliothek.\
Sie alle enthalten einen einfachen [Wertprozessor](../../atomic-nodes/value-processor/value-processor.md)-Knoten, der den Wert generiert.

+++ Konstante Knoten in der Bibliothek

![constants-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="Knoten mit konstanter Fließkommazahl" /></p>

## Ganzzahlen

Konstante Ganzzahlen generieren ganze Zahlen und haben eine Stufe von 1.

[Sie können in eine Fließkommazahl konvertiert werden, &#x200B;](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md). Dies wird empfohlen, wenn ein Vorgang ausgeführt wird, der komplexer ist als Additionen, Subtraktionen und einfache Vergleiche.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Ganzzahl](constant.resources/fn-constant-integer.png "Symbol für Ganzzahl")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Ganzzahl</b>

Eine Ganzzahl besteht aus einer einzigen Komponente. Er ist nützlich als Index für Auswahlen, z. B.:

* Auswahl einer Option, die dem Benutzer als Dropdown-Menü angezeigt wird (siehe &quot;Dropdown-Liste&quot; in [dieser Seite](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* Auswählen der Eingabe eines [Multiswitch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)-Knotens.<b></b>

>[!IMPORTANT]
>
> <b>Negative Ganzzahlen</b> in Parameterfunktionen werden *nicht unterstützt*. Eine Problemumgehung finden Sie unter [dieser Seite](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) im Abschnitt &quot;Technische Probleme&quot;.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Typsymbol für Ganzzahl2](constant.resources/fn-constant-integer2.png "Typsymbol für Ganzzahl2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Ganzzahl2</b>

Ein Ganzzahl2-Knoten generiert einen statischen 2-Komponenten-Komponentenvektor mit (X, Y) Ganzzahlen.

Ein häufiger Anwendungsfall von Ganzzahl2 ist das Festlegen von X- und Y-Knotengrößen, wie im Raster [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Typsymbol für Ganzzahl3](constant.resources/fn-constant-integer3.png "Typsymbol für Ganzzahl3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Ganzzahl3</b>

Ein Ganzzahl3-Knoten erzeugt einen statischen 3-Komponenten-Komponentenvektor mit (X, Y, Z) Ganzzahlen.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Integer4-Typ](constant.resources/fn-constant-integer4.png "Symbol für Integer4-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer4</b>

Ein Integer4-Knoten generiert einen statischen ganzzahligen 4-Komponenten-Vektor mit (X, Y, Z, W) Komponenten.

</td>
</tr>
</table>

## Floats

Konstante Gleitkommawerte erzeugen Bruchzahlen, d.h. sie unterstützen Werte nach dem Dezimalzeichen und können in Schritten kleiner als 1 angepasst werden. (Standard: 0,01)

[Floats können in Integers](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) konvertiert werden, werden jedoch auf die nächste Integer-Zahl aufgerundet oder abgerundet, was bedeutet, dass Daten und Genauigkeit verloren gehen.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Gleitkommatyp](constant.resources/fn-constant-float.png "Symbol für Gleitkommatyp")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Gleitend</b>

Ein Gleitkommawert hat eine einzelne Komponente und wird sehr häufig für jeden einzelnen Wert verwendet, der Präzision erfordert.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Float2-Typ](constant.resources/fn-constant-float2.png "Symbol für Float2-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Ein Float2-Knoten generiert einen 2-Komponenten-Vektor mit (X, Y) Komponenten.

Float2 wird häufig für [Sampling-Koordinaten](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), [Offset-Transformationen](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) und allgemeine 2D-Vektorbearbeitung verwendet.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Float3-Typ](constant.resources/fn-constant-float3.png "Symbol für Float3-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Ein Float3-Knoten generiert einen 3-Komponenten-Vektor (X, Y, Z).

Float3 wird hauptsächlich bei der Arbeit mit 3D-Objekten und [3D-Skalierungskoordinaten](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) verwendet, z. B. in [3D-SDF-Knoten](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), und als einfachere Möglichkeit, RGB-Farben zu speichern - d. h. ohne Alpha.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Float4-Typ](constant.resources/fn-constant-float4.png "Symbol für Float4-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Ein Float4 erzeugt einen 4-Komponenten-Vektor (X, Y, Z, W).

&quot;Float4&quot; ist die bevorzugte Methode zum Speichern und Festlegen von Farbinformationen, wobei XYZW-Werte RGBA zugeordnet werden, wie z. B. im [Uniform Color Node](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md).

</td>
</tr>
</table>

## Nicht numerisch

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für booleschen Typ](constant.resources/fn-constant-boolean.png "Symbol für booleschen Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Boolescher Wert</b>

Ein Boolean -Wert ist der einfachste Datentyp, der vorhanden ist, da er nur zwei Status kennt: <code>true</code> oder <code>false</code>.

Dieser Typ ist recht häufig bei der Arbeit mit Umschaltparametern und [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md)-Bedingungen.<br>Booleans sind eine einfache und effiziente Methode zur Steuerung des Ablaufs einer Funktion oder eines Grafen, z. B. mithilfe eines [Wechselknotens](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md).

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer-Funktionsdiagrammen auf Konstantenknoten zu, um Konstantenwerte und -parameter zu definieren.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Konstanten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4e61f5588fb279e139240ac5939d6b7e58e1027a
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# Konstanten

Konstante Knoten sind eine Möglichkeit, einen statischen Wert für die Verwendung innerhalb von Substance-Funktionsdiagrammen zu erstellen. Im Gegensatz zu [Variablen](../../../../function-graphs/variables/variables.md) können sie nicht extern geändert werden.

Darüber hinaus enthält diese Seite einige zusätzliche Informationen zu jedem Datentyp und zu häufigen Anwendungsfällen.

## Ganzzahlen

Konstante Ganzzahlen generieren ganze Zahlen und haben einen Schritt von 1.

[Sie können in &quot;Float&quot;,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) konvertiert werden. Dies wird empfohlen, wenn ein Vorgang ausgeführt wird, der komplexer ist als Additionen, Subtraktionen und einfache Vergleiche.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Ganzzahltyp](constant-nodes.resources/fn-constant-integer.png "Symbol für Ganzzahltyp")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer</b>

Eine Ganzzahl hat eine einzelne Komponente. Er ist nützlich als Index für Auswahlen, z. B.:

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

![Symbol für Integer2-Typ](constant-nodes.resources/fn-constant-integer2.png "Symbol für Integer2-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer2</b>

Ein Integer2-Knoten generiert einen statischen Ganzzahlvektor mit 2 Komponenten und (X, Y) Komponenten.

Integer2 ist nicht üblich, wird aber beispielsweise verwendet, um die X- und Y 2D-Unterteilung in einem [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) festzulegen.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Integer3-Typ](constant-nodes.resources/fn-constant-integer3.png "Symbol für Integer3-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer3</b>

Ein Integer3-Knoten generiert einen statischen ganzzahligen 3-Komponenten-Vektor mit (X, Y, Z) Komponenten.

Integer 3 ist nicht häufig und wird wahrscheinlich nicht häufig vorkommen.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Integer4-Typ](constant-nodes.resources/fn-constant-integer4.png "Symbol für Integer4-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer4</b>

Ein Ganzzahl4-Knoten erzeugt einen statischen 4-Komponenten-Komponentenvektor mit (X, Y, Z, W) Ganzzahlen.

Ganzzahl 4 ist nicht häufig und wird wahrscheinlich nicht häufig vorkommen.<b>\
</b>

</td>
</tr>
</table>

## Fließkommazahlen

Konstante Fließkommazahlen erzeugen nicht ganzzahlige, sondern Bruchzahlen, d. h., sie haben immer Werte nach dem Dezimalzeichen und können in- oder abgenommen werden, wenn sie kleiner als 1 sind (Standardwert 0,01).

[Fließkommazahlen können in Ganzzahlen konvertiert werden](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), sie werden jedoch auf die nächstgelegene Ganzzahl aufgerundet oder abgerundet, was bedeutet, dass Daten verloren gehen und die Genauigkeit verloren geht.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Fließkommazahl](constant-nodes.resources/fn-constant-float.png "Symbol für Fließkommazahl")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Fließkommazahl</b>

Eine Fließkommazahl, die eine Einzelkomponente hat, wird aus Kurzgründen in der Bezeichnung (1) weggelassen. Fließkommazahl ist sehr gebräuchlich und wird für jeden Wert verwendet, der eine präzise Steuerung in Form eines Schiebereglers oder eines Winkels erfordert. Sie finden sie in fast allen Knotenparametern. Es ist auch der bevorzugte Datentyp für einen Graustufenwert!<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Typsymbol für Fließkommazahl2](constant-nodes.resources/fn-constant-float2.png "Typsymbol für Fließkommazahl2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Fließkommazahl2</b>

Ein Fließkommazahl2-Knoten generiert einen statischen 2-Komponenten-Fließkommazahl-Vektor. Die Komponenten haben den Namen X, Y. Fließkommazahl2 ist recht häufig und wird für [Sampling-Koordinaten](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) und für [Transformations-Offsets](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) verwendet.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Typsymbol für Fließkommazahl3](constant-nodes.resources/fn-constant-float3.png "Typsymbol für Fließkommazahl3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Fließkommazahl3</b>

Ein Fließkommazahl3-Knoten generiert einen statischen 3-Komponenten-Fließkommazahl-Vektor. Die Komponenten haben den Namen X,Y,Z. Fließkommazahl3 ist ungewöhnlich, wird hauptsächlich zur Darstellung von [3D-Skalierungskoordinaten](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) verwendet und ermöglicht eine einfachere Speicherung von Alphas ohne Farbdaten.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Typsymbol für Fließkommazahl4](constant-nodes.resources/fn-constant-float4.png "Typsymbol für Fließkommazahl4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Fließkommazahl4</b>

Eine Fließkommazahl4 generiert einen statischen 4-Komponenten-Komponentenvektor.Die Fließkommazahlen werden X,Y,Z,W genannt. Fließkommazahl4 ist sehr gebräuchlich, da dies die bevorzugte Methode zum Speichern und Festlegen von [Farbinformationen ist, wobei XYZW-Daten RGBA-Werte darstellen.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## Sonstige

Zwei zusätzliche Datentypen sind in Substance-Funktions-Grafen vorhanden: booleans und strings. Zeichenfolgen wurden neben dem Knoten [Text](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) in Designer Version 6 hinzugefügt.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Boolesche Wert-Typ](constant-nodes.resources/fn-constant-boolean.png "Symbol für Boolesche Wert-Typ")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Boolescher Wert</b>

Ein Boolean -Wert ist der einfachste Datentyp, der vorhanden ist, da er nur zwei Status kennt: True oder False, 1 oder 0. Sie wird durch die Farbe Weiß dargestellt. Es ist nicht möglich, zwischen Boolean und Integer ohne [Umwandlung](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) oder mithilfe von [logischen Knoten zu wechseln.](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) Ein Boolescher Wert ist recht häufig und stellt eine hervorragende Möglichkeit dar, den Fluss einer Funktion oder eines Diagramms zu steuern. Ein typischer Anwendungsfall wäre ein [Wechselknoten.](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Symbol für Zeichenfolgentyp](constant-nodes.resources/fn-constant-string.png "Symbol für Zeichenfolgentyp")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Zeichenfolge</b>

Ein String-Knoten generiert einen statischen String, einen Textausschnitt. Es ist der exotischste Datentyp, der in Funktionen verfügbar ist, und kann im Allgemeinen nicht viel in Verbindung mit anderen Funktionsknoten verwendet werden. Hauptziel ist es, als endgültige Ausgabe für den [Textknoten zu fungieren.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Mit dem Spline-Append-Knoten können Sie mehrere Splines anfügen, um längere kontinuierliche Pfade zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Append
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Spline Append

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-append-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Splines werden als Liste verpackt. Dieser Knoten fügt eine Liste von Eingabe-Splines (set #2) an eine vorhandene Liste (set #1) an.

Die Reihenfolge der Listen bleibt erhalten, d. h. das Anhängen einer Liste D-E-F an eine Liste A-B-C führt zu einer Liste A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Achten Sie auf die Reihenfolge, in der Sie Splines anhängen, da diese Reihenfolge in anderen Knoten berücksichtigt wird, z. B. [Streuung auf Splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), [Spline Bridge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) usw.

## Eingangsanschlüsse

<b>Vorschau #1</b> *Graustufen* Die Vorschau des ersten Satzes von Eingabe-Splines als Graustufenbild.

<b>Spline-#1</b> *Farbe* Die Koordinaten des ersten Satzes von Eingangs-Splines’-Punkten, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
        * Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
        * Absoluter Wert: Thickness + 1.

<b>Spline #1 Data</b> *Farbe* Zusätzliche Daten des ersten Satzes von Eingangs-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - Tangenten X\
    <b>G</b> - Tangenten Y\
    <b>B</b> - Nicht verwendet\
    <b>A</b> - Nicht verwendet

<b>Spline-#1</b> *Integer* Die Anzahl der Eingabe-Splines in der ersten Gruppe.

<b>Vorschau #2</b> *Graustufen* Die Vorschau des zweiten Satzes von Eingabe-Splines als Graustufenbild.

<b>Spline-#2</b> *Farbe* Die Koordinaten des zweiten Satzes von Eingangs-Splines’-Punkten, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
        * Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
        * Absoluter Wert: Thickness + 1.

<b>Spline #2 Data</b> *Farbe* Zusätzliche Daten des zweiten Satzes von Eingangs-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - Tangenten X\
    <b>G</b> - Tangenten Y\
    <b>B</b> - Nicht verwendet\
    <b>A</b> - Nicht verwendet

<b>Spline-#2</b> *Integer* Die Anzahl der Eingabe-Splines in der zweiten Gruppe.

## Ausgangsanschlüsse

<b>Vorschau</b> *Graustufen* Die Vorschau der Ausgabe-Splines als Graustufenbild.

<b>Spline-Kabel</b> *Farbe* Die Koordinaten der Punkte der Ausgabesplines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - X-Position\
    <b>G</b> - Y-Position\
    <b>B</b> - Height\
    <b>A</b> - Paketdaten:\
        * Signieren: Die Spline ist geschlossen (negativ) oder offen (positiv).\
        * Absoluter Wert: Thickness + 1.

<b>Spline-Daten</b> *Farbe* Zusätzliche Daten der Ausgabe-Splines, die in den RGBA-Kanälen eines Farbbildes codiert sind.\
    <b>R</b> - Tangenten X\
    <b>G</b> - Tangenten Y\
    <b>B</b> - Nicht verwendet\
    <b>A</b> - Nicht verwendet

<b>Spline-Betrag</b> *Integer* Die Anzahl der Ausgabe-Splines.

## Parameter

<b>Spline-#1 spiegeln </b>*Boolesch* Kehrt die Richtung der Splines im ersten Satz um.

<b>Spline-#2 spiegeln </b>*Boolesch* Kehrt die Richtung der Splines im zweiten Satz um.

+++Vorschau
<b>Segmentierungsbetrag</b> *Integer* Passt die Anzahl der Segmente an, die zum Zeichnen der Spline-Visualisierung in der Vorschauausgabe verwendet werden.\
Je höher der Wert, desto glatter die Linie.

<b>Richtungshelfer anzeigen</b> *Boolescher Wert* Zeigt einen Punkt am Anfang des Splines und eine Pfeilspitze an seinem Ende in der Vorschauausgabe an.

<b>Umschlag der Thickness anzeigen</b> *Boolescher Wert*\
Zeigt an den Kanten der Spline-Thickness zusätzliche Linien an.

<b>Thickness (px)</b> *Gleitend* Passt die Thickness der Spline-Visualisierung in Pixel in der Vorschauausgabe an.

+++

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 1](../../../../../../assets/SplineAppend-Demo.jpg "Knotenbeispiel 1")

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineAppend-Graph.jpg "Knotenbeispiel 2")

</td>
</tr>
</table>

![Knotendemo](../../../../../../assets/SplineAppend-Demo2.gif "Knotendemo")

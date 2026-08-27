---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Spline Flow Mapper", um fließende Texturmuster entlang von Spline-Pfaden für organische Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline-Flow-Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Spline-Flow-Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/spline-flow-mapper-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Spline-Werkzeuge

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Zeichnet eine Flow Map, in der Flussvektordaten entlang der Eingabe-Splines gezeichnet werden.

Mit Splines kannst du die Richtung, die Trajektorie, die Intensität und die Thickness des Flows steuern. Außerdem kannst du die Verlaufsrampe verwenden, mit der die gezeichneten Daten in den neutralen Hintergrund überblendet werden.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Das Ergebnis kann unerwünschte Artefakte außerhalb der Hülle des Spline-Effekts sein, wenn sehr niedrige Werte für die Thickness verwendet werden. Dies ist ein bekanntes Problem.

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

<b>Dämpfungsprofilkurve</b> *Graustufen*<span id="_Hlk135812146"></span> Das Bild, das eine Kurve anhand der Werte der ersten Pixelzeile beschreibt.\
Wenn der Parameter &quot;Dämpfungsprofil&quot; auf &quot;Eingangsprofilkurve&quot; eingestellt ist, wird mit dieser Eingabe die Verlaufsrampe für die Dämpfung der Flussvektordaten gesteuert, die entlang des Splines gezeichnet werden.\
Sie können einen Knoten [Kurve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) verwenden, um die Kurve zu erstellen.

## Ausgangsanschlüsse

<b>Ausgabe</b> *Farbe* Die in einem Farbbild codierte Ausgabestromzuordnung.

## Parameter

<b>Segmentierungsbetrag</b> *Integer* Splines werden in Segmente vereinfacht, bevor sie von Vektordatendaten durchlaufen werden.\
Eine größere Anzahl von Segmenten führt zu einer glatteren Flusszuordnung entlang von Kurven.

<b>Modus</b> *Integer* Die Methode zum Auswählen der Splines, entlang derer Vektor-Flussdaten gezeichnet werden sollen:\
*- Spline-Liste zeichnen*: Alle Splines in der Eingabeliste werden verwendet.\
*- Einzelne Spline zeichnen*: Es wird nur der Spline-Code mit dem angegebenen Index verwendet.\
*- Spline-Bereich zeichnen*: Es werden nur die Splines verwendet, deren Index im angegebenen Bereich enthalten ist.

<b>Spline-Index zeichnen</b> *Integer* (Verfügbar, wenn &quot;Modus&quot; auf &quot;Einzelne Spline zeichnen&quot; festgelegt ist)Der Index der Spline, entlang der Vektor-Flussdaten gezeichnet werden sollen.

<b>Spline-Bereich zeichnen</b> *Integer2* (Verfügbar, wenn &quot;Modus&quot; auf &quot;Spline-Bereich zeichnen&quot; festgelegt ist)Der Indexbereich für die Splines, entlang derer Vektor-Flussdaten gezeichnet werden sollen.

<b>Thickness-Modus</b> *Integer* Die Methode zum Festlegen der Thickness der gezeichneten Vektor-Flussdaten\
*- Manuell*: Legen Sie die Thickness explizit mit einem beliebigen Wert fest.\
*- Aus Spline*: Verwenden Sie die Thickness des Splines.

<b>Thickness</b> *Gleitkommawert* (verfügbar, wenn &quot;Thickness-Modus&quot; auf &quot;Manuell&quot; festgelegt ist)Der willkürliche Wert für die Thickness der Vektor-Flussdaten, die entlang der Splines gezeichnet werden.<b></b>

<b>Thicknessen-Multiplikator</b> *Gleitkommawert* (verfügbar, wenn &quot;Thickness-Modus&quot; auf &quot;Von Spline&quot; festgelegt ist)Ein globaler Multiplikator für die Thickness der entlang den Splines gezeichneten Vektor-Flussdaten, wenn diese Thickness von der Splines gesteuert wird.

<b>Richtung</b> *Integer* Die Richtung des Vektorflusses in Bezug auf den Spline.\
*- Tangente*: Tangentenvektor des Splines verwenden\
*- Normal*: Verwenden Sie den normalen Vektor des Splines.\
*- Normal gespiegelt*: Verwenden Sie die gespiegelte Version des normalen Vektors des Splines.

<b>Richtung spiegeln</b> *Boolean* Kehrt die Richtung der Splines um, was sich auch auf die Richtung des Flussvektors auswirkt.

<b>Dämpfungsprofil</b> *Integer* Die Verlaufsrampe, die zum Zeichnen der Dämpfung der Flussvektordaten verwendet wird, die entlang der Spline gezeichnet werden:\
*- Linear*: Verwenden einer linearen Verlaufsrampe\
*- Gaußscher*: Gaußschen Verlauf verwenden\
*- Eingabeprofilkurve*: Verwenden Sie die Kurve für den Eingang der Dämpfungsprofilkurve als Verlaufsrampe.

<b>Dämpfung starten</b> *Boolescher Wert*<span id="_Hlk135769398"></span> Fügt einen Halbkreis am Anfang des Splines hinzu. Der Halbkreis verwendet die gleiche Dämpfung wie der Spline.

<b>Enddämpfung</b> *Boolescher Wert* Fügt am Ende des Splines einen Halbkreis hinzu. Der Halbkreis verwendet die gleiche Dämpfung wie der Spline.

<b>Spline-Height-Dämpfung</b> *Gleitkommawert* Die Intensität der Flussvektordaten, die entlang der Spline gezeichnet werden, wird mit dem Height der Spline multipliziert, wobei die gezeichneten Daten an die neutrale Hintergrundfarbe (0,5, 0,5, 0) übergehen, wenn das Height näher an 0 kommt.

<b>Nicht-quadratische Korrektur </b>*Boolesch* Passen Sie die Punktpositionen und die Thickness an, um die Spline-Form in nicht-quadratischen Auflösungen beizubehalten.\
Dies wirkt sich auch auf die einheitliche Verteilung aus.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/SplineFlowMapper-Demo.gif "Knotenbeispiel 2")

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Pfade auswählen", um bestimmte Pfade aus einer Pfadliste anhand von Kriterien auszuwählen und zu filtern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfade auswählen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# Pfade auswählen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/paths-select-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Isolieren Sie einen Pfad unter mehreren Pfaden, die in Pfaden enthalten sind.

</td>
</tr>
</table>

## Eingangsanschlüsse

<b>Bezeichnung</b> *Typ*\
Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten.

## Ausgangsanschlüsse

<b>Pfade</b> *Farbe*\
Die Pfade werden mit nur einem Pfad eingegeben. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten.

## Parameter

<b>Auswahlmodus</b> *Integer* Die zum Auswählen der Pfade verwendete Methode:\
*- Nach ID:* Wählt den Pfad aus der Liste aus, deren Index mit dem in <b>Pfad-ID</b> angegebenen Index übereinstimmt.\
*- Nach Länge:* Wählt die Pfade aus, deren Länge über oder unter dem in <b>Ziellänge</b> angegebenen Schwellenwert liegt.

<b>Pfad-ID</b> *Integer* (verfügbar, wenn <b>Auswahlmodus</b> auf *Von ID* festgelegt ist)\
Der Index des ausgewählten Pfads.\
Ein Wert, der größer als die Anzahl der Pfade in <b>Pfaden *ist, führt zu einer leeren Ausgabe von*</b>.

<b>Länge größer oder kleiner?</b> *Boolescher Wert* (verfügbar, wenn der <b>Auswahlmodus</b> auf *Länge* festgelegt ist)\
Steuert, ob die Auswahl eine größere oder geringere Länge als die <b>Ziellänge</b> enthalten soll.

<b>Ziellänge</b> *Float*(Verfügbar, wenn <b>Auswahlmodus</b> auf *Länge* festgelegt ist)\
Der Längenschwellenwert, der zum Auswählen von Splines verwendet wird.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant2.jpg" alt="PfadeSelect-Variant2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

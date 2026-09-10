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
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# Pfade auswählen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](paths-select.resources/paths-select-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Isolieren Sie einen Pfad unter mehreren Pfaden, die in Pfaden enthalten sind.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Bezeichnung</b> <i>Typ</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Die Pfade werden mit nur einem Pfad eingegeben. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Auswahlmodus</b> <i>Integer</i> | Die zum Auswählen der Pfade verwendete Methode:<br>*- Nach ID:* Wählt den Pfad aus der Liste aus, dessen Index mit dem in <b>Pfad-ID</b>;<br>*- Nach Länge:* angegebenen Index übereinstimmt. Wählt die Pfade aus, deren Länge über oder unter dem in <b>Ziellänge</b> angegebenen Schwellenwert liegt. |
| <b>Pfad-ID</b> <i>Integer</i> (verfügbar, wenn <b>Auswahlmodus</b> auf *Von ID* festgelegt ist) | Der Index des ausgewählten Pfads.<br>Ein Wert, der größer als die Anzahl der Pfade in <b>Pfaden *ist, führt zu einer leeren Ausgabe von*</b>. |
| <b>Länge größer oder kleiner?</b> <i>Boolescher Wert</i> (verfügbar, wenn der <b>Auswahlmodus</b> auf *Länge* festgelegt ist) | Steuert, ob die Auswahl eine größere oder geringere Länge als die <b>Ziellänge</b> enthalten soll. |
| <b>Ziellänge</b> <i>Fließkommazahl</i> (verfügbar, wenn <b>Auswahlmodus</b> auf *Länge* festgelegt ist) | Der Längenschwellenwert, der zum Auswählen von Splines verwendet wird. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PfadeSelect-Variant2">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

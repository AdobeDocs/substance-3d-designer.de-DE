---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
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
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

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

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten <b>Extend Shape</b> erweitert einen <i>Abschnitt</i> der <b>Eingabe</b> um eine festgelegte Richtung und Entfernung.

Mit dem Parameter &quot;<b>Helfer anzeigen</b>&quot; können Sie den erweiterten Abschnitt und die Erweiterungsrichtung anzeigen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Modus</b> <i>Integer</i> | Definiert die <i>Parameter</i>, die zum Anwenden der Erweiterung verwendet werden:<br><br>- <i>Bidirektional</i>: Der Abschnitt der <b>Eingabe</b>, der durch die <b>Erweiterungsposition</b> und den <b>Erweiterungswinkel</b> angegeben wird, wird über die <b>Erweiterungsentfernung</b> in <i>entgegengesetzte Richtungen</i><br>- <i>unidirektional</i> erweitert: Der Abschnitt der <b>Eingabe</b>, der durch die <b>Erweiterungsposition</b> und <b>Erweiterungswinkel</b> angegeben wird, wird über die <b>Erweiterungsentfernung</b> in einer <i>einfachen Richtung</i><br>- <i>Start-/Endpositionen</i> erweitert: Eine Erweiterung <i>vektor</i> wird durch <b>Startposition</b> und <b>Endposition</b> definiert. Der Abschnitt <i>Senkrecht</i> der <b>Eingabe</b> an der <b>Startposition</b> wird <i> über diesen Vektor</i> bis zur <b>Endposition</b> erweitert. |
| <b>Erweiterungsabstand</b> <i>Gleitend</i> | Die Entfernung, über die der durch die <b>Erweiterungsposition</b> und <b>Erweiterungswinkel</b> angegebene Abschnitt erweitert werden soll. Der Abstand wird als <i>Proportion</i> der Bildspanne ausgedrückt. |
| <b>Erweiterungsposition</b> <i>Gleitend</i> | Die Position im Bild des Abschnitts, der erweitert werden soll. Der Wert wird als <i>-Versatz vom Mittelpunkt </i> ausgedrückt. |
| <b>Erweiterungswinkel</b> <i>Gleitend</i> | Der Winkel des Abschnitts, der erweitert werden sollte, da der Ausgangspunkt ein <i>vertikaler Abschnitt</i> ist. |
| <b>Startposition</b> <i>Float2</i> | Die Startposition des <i>Erweiterungsvektors</i>. |
| <b>Endposition</b> <i>Float2</i> | Die Endposition des <i>Erweiterungsvektors</i>. |
| <b>Offset der Luminanz starten</b> <i>Gleitend</i> | Wendet einen Luminanz-Offset auf den Bereich des Bildes <i> an, der dem erweiterten Abschnitt </i> vorausgeht. Dieser Luminanzen-Offset wird <i>entlang des Abschnitts </i> auf die Luminanz des Bildbereichs nach dem Abschnitt interpoliert.<br><br><i>Hinweis</i>: Dieser Parameter ist nur in der <b>Grayscale</b>-Version des Knotens verfügbar. |
| <b>Offset der Luminanz beenden</b> <i>Gleitend</i> | Wendet einen Luminanz-Offset auf den Bereich des Bildes <i> an, der dem erweiterten Abschnitt folgt</i>. Dieser Luminanzen-Offset wird <i>entlang des Abschnitts </i> auf die Luminanz des Bildbereichs vor dem Abschnitt interpoliert.<br><br><i>Hinweis</i>: Dieser Parameter ist nur in der <b>Grayscale</b>-Version des Knotens verfügbar. |
| <b>Lum. Offset ignoriert schwarze Pixel</b> <i>Boolescher Wert</i> | Wenn auf <i>True</i> festgelegt, werden die in <i>both</i> angegebenen Luminanzen-Offsets angegeben. <b>Start-Luminanz-Offset</b> und <b>End-Luminanz-Offset</b> werden nur auf <i>nicht schwarze</i> Pixel angewendet, d. h. Pixel, deren Wert größer als 0 ist.<br><br><i>Hinweis</i>: Dieser Parameter ist nur in der <b>Grayscale</b>-Version des Knotens verfügbar. |
| <b>Filtermodus</b> <i>Integer</i> | Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn <i>zwischen den Pixeln <br><br>- <i>Nächste</i> interpoliert wird: nimmt genau den <i>gleichen</i> Wert (schneller)<br>- <i>Bilinear</i> auf: wendet einen bilinearen Filter auf das Ergebnis für einen <i>glatteren</i>-Look an.</i> |
| <b>Helfer anzeigen</b> <i>Boolescher Wert</i> | Visualisieren Sie den <i>erweiterten Abschnitt</i> als Überlagerung mit Pfeilen, die die <i>Richtung</i> der Erweiterung anzeigen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-node.png" />
        </td>
    </tr>
</table>

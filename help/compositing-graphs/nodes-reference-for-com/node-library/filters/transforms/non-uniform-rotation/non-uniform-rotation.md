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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# ungleichmäßige Drehung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/non-uniform-rotation-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/non-uniform-rotation-02.png){width="200px"}

</td>
</tr>
</table>

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Nicht-gleichförmige Drehung** dreht die **Eingabe** mithilfe der **Rotation Map**-Eingabe.

Die Werte des Bildes stellen eine *Anzahl von Windungen* dar. Die Drehung wird um die Position ausgeführt, die durch den Wert **Pivot-Position** oder die Eingabe **Pivot-Positionen-Map** angegeben wird.\
Positive Werte in der **Rotation Map**-Eingabe führen zu einer *Drehung im Uhrzeigersinn*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen/Farbe</i> | Das Graustufenbild, das gedreht werden soll. |
| <b>Rotation Map</b> <i>Graustufen</i> | Die Karte, die verwendet wird, um den Umfang der Drehung in *Anzahl der Windungen* zu steuern. Die aufgenommenen Werte werden mit dem **Drehwinkelmultiplikator** multipliziert. Negative Werte führen zu einer Drehung von *gegen den Uhrzeigersinn*. |
| <b>Drehungszuordnung für die Pivot-Position</b> <i>Farbe</i> | Das Bild, das zum Angeben der Position der Drehung *Pivot* verwendet wird. Die Position **X/Y** ist den **R/G** Kanälen des Bildes zugeordnet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Drehwinkelmultiplikator</b> <i>Gleitend</i> | Passt die Intensität der **Rotation Map**-Eingabe an. |
| <b>Versatz des Drehwinkels</b> <i>Gleitend</i> | Wendet die angegebene zusätzliche Drehung an. |
| <b>Pivot-Positionen-Map verwenden</b> <i>Boolescher Wert</i> | Verwenden Sie eine *Bitmapeingabe*, um die Position des Drehzapfens anzugeben. Die Position **X/Y** ist den Kanälen **R/G** der Eingabe **Positionszuordnung** zugeordnet. |
| <b>Pivot-Position</b> <i>Float2</i> | Die Position des Drehpunkts, um den das Bild gedreht wird. |
| <b>Hintergrundfarbe</b> <i>Gleitend/Gleitend4</i> | Hintergrundfarbe, die *außerhalb der Bildbegrenzungen* anzeigt, falls die Unterteilung nicht auf **H und V Unterteilung** festgelegt ist. |
| <b>Filtermodus</b> <i>Integer</i> | Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn *zwischen den Pixeln <br><br>-* Nächste *interpoliert wird: nimmt genau den* gleichen *Wert (schneller)<br>-* Bilinear *auf: wendet einen bilinearen Filter auf das Ergebnis für einen* glatteren *-Look an.* |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/non-uniform-rotation-05.png" />
        </td>
    </tr>
</table>

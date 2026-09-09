---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Automatisches Freistellen , um Texturen automatisch zuzuschneiden, um leere Rahmen zu entfernen und die Texturabmessungen zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Automatisches Freistellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Automatisches Freistellen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Automatisches Freistellen** passt die **Eingabe** so an, dass der Inhalt entweder in der *Mitte* des Bildes platziert wird, ohne dass die Größe geändert wird, oder *die Größe auf den Bereich* des Bildes angepasst wird.

Der Inhalt des Bildes wird durch ein Feld definiert, das an die *ersten und letzten Pixel* auf **X** und **Y** angepasst ist, deren Werte *höher als 0* sind (d. h. nicht schwarz). Mit der **Color**-Version können Sie aus den RGB- und Alpha-Kanälen auswählen, um dieses Feld zu definieren.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Modus</b> <i>Integer</i> | Legen Sie die Zuschneidemethode fest, die angewendet werden soll: <br><br>- <i>Zuschneidequadrat</i>: Das Bild wird so beschnitten, dass sich die Form in der Mitte des kleinsten <i>quadratischen</i> Bildes befindet, das es vollständig enthalten kann<br>- <i>Automatisches Freistellen</i>: Das Bild wird so beschnitten, dass sich die Form in der Mitte des kleinsten <i>quadratischen oder nicht quadratischen</i> Bildes befindet, das es vollständig enthalten kann<br>- <i>Einpassen (Verhältnis beibehalten)</i>: Die Größe des Bilds wird auf den <i>vollen Bereich</i> des Bilds skaliert, wobei die <i>Proportionen</i> (d. h. das Verhältnis von Breite zu Länge)<br>- <i>Füllung (Gedehnt)</i> beibehalten werden: Die Größe des Bildes wird auf die <i>volle Bildspanne</i> geändert. |
| <b>Alpha verwenden</b> <i>Boolescher Wert</i> | Verwenden Sie den Alphakanal der <b>Eingabe</b>, um die <i>Grenzen</i> des Bildinhalts für das Zuschneiden zu bestimmen. Wenn die Option auf <i>False</i> festgelegt ist, werden stattdessen schwarze Pixel verwendet.<br><br><i>Hinweis:</i> Dieser Parameter ist nur in der <b>Color</b>-Version des Knotens verfügbar. |
| <b>Filtermodus</b> <i>Integer</i> | Definiert, wie die aufgenommenen Ergebnisse behandelt werden, wenn <i>zwischen den Pixeln <br><br>- <i>Nächste</i> interpoliert wird: nimmt genau den <i>gleichen</i> Wert (schneller)<br>- <i>Bilinear</i> auf: wendet einen bilinearen Filter auf das Ergebnis für einen <i>glatteren</i>-Look an<br>- <i>Auto</i>: Verwendet je nach ausgewähltem <b>Modus</b> zum Zuschneiden den am besten geeigneten der beiden oben genannten Modi</i> |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-node.png" />
        </td>
    </tr>
</table>

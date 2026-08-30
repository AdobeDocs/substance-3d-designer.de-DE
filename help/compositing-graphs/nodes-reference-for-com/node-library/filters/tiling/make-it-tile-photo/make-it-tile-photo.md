---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Make It Tile Foto , um Fotos in nahtlose Kachelung-Texturen für die Erstellung von Materials zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Foto unterteilen.
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Foto unterteilen.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>In:</b> Filters > Kachelung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten bietet Kantenkorrekturfunktionen für alle Bilder, die aufgrund nicht kontinuierlicher Kanten nicht kacheln können. Sie wirkt sich nur auf die Kanten des Eingabebilds aus. Wenn Sie die Skalierung oder Kachel auf verschiedene Weise anpassen möchten, sehen Sie sich [Make It Tile Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md) an.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Maskenkrümmung H</b> <i>-100.0 - 100.0</i> | Führt Verkrümmungen auf der horizontalen Achse ein, um undefinierte Übergänge zu vermeiden. |
| <b>Maskenkrümmung V</b> <i>-100.0 - 100.0</i> | Führt Verkrümmungen auf der senkrechten Achse ein, um undefinierte Übergänge zu vermeiden. |
| <b>Maskengröße H</b> <i>0.0 - 1.0</i> | Legt fest, wie weit die Übergangskante horizontal reicht. |
| <b>Maskengröße V</b> <i>0.0 - 1.0</i> | Legt fest, wie weit die Übergangskante vertikal reicht. |
| <b>Maskengenauigkeit H</b> <i>0.0 - 1.0</i> | Legt fest, wie weich der Übergang horizontal ist. |
| <b>Maskengenauigkeit V</b> <i>0.0 - 1.0</i> | Legt fest, wie weich der Übergang vertikal verläuft. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>

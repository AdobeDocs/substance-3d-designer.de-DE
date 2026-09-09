---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Make It Tile Patch zum Ausbessern und Erstellen nahtloser Kacheltexturen aus Eingabebildern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kachelüberlagerung erstellen
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# Kachelüberlagerung erstellen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>In:</b> Filters > Kachelung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist ein gitterbasierter halbzufälliger Kachel. Es wird ein Eingabefeld verwendet und mit einem Stempel versehen, um zu versuchen, es in ein gekacheltes Bild zu verwandeln, ohne dass es zu viele Wiederholungen gibt, je nach Ihren Einstellungen.

Das ist nützlich, wenn du eine kleine Struktur hast und daraus eine größere, kachelbare Struktur erstellen möchtest.

Beachten Sie, dass dies ein Unterschied zu [Make-It-Tile Foto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md) ist, bei dem hauptsächlich Kanten korrigiert werden.

Informationen zum Verwenden des gesamten Materials finden Sie unter [Smart Auto Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Maskengröße</b> <i>0.0 - 1.0</i> | Größe der runden Maske, die beim Prägen des Pflasters verwendet wird. |
| <b>Maskengenauigkeit</b> <i>0.0 - 1.0</i> | Abfall-/Maskengenauigkeit der Smoothness. |
| <b>Maskenverkrümmung</b> <i>-100.0 - 100.0</i> | Führt eine Verkrümmung an Maskenkanten ein. Gut zum Vermeiden glatter, undefinierter Übergänge zwischen Patches. |
| <b>Breite der Mustergröße</b> <i>0.0 - 1000.0</i> | Ändert die Breite des Pflasters ungleichmäßig. |
| <b>Height der Mustergröße</b> <i>0.0 - 1000.0</i> | Ändert das Height des Pflasters ungleichmäßig. |
| <b>Störung</b> <i>0.0 - 1.0</i> | Führt translationale Zufälligkeit ein, leicht verschiebbare Flecken. |
| <b>Größenänderung</b> <i>0.0 - 100.0</i> | Führt die Größenvariation für die Maske ein. |
| <b>Oktave</b> <i>0 - 6</i> | Dies ist das Hauptsteuerelement, das die Gesamtgröße bestimmt. |
| <b>Drehung</b> <i>-360.0 - 360.0</i> | Dreht den Patch vorab. |
| <b>Drehungsvariation</b> <i>0.0 - 360.0</i> | Führt eine zufällige Drehung für jeden Ausbesserungsstempel ein. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Legt die Hintergrundfarbe für Bereiche fest, in denen kein Patch auftritt. |
| <b>Farbvariation</b> <i>0.0 - 1.0 (Nur Farbversion)</i> | Führt Farbvariationen pro Patch ein. |
| <b>Variation der Luminanz</b> <i>(nur Graustufenversion)</i> | Führt die Luminanzvariation pro Patch ein. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>

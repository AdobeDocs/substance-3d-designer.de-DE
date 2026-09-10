---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Verwenden Sie den Smart Auto Tile-Knoten, um mithilfe der intelligenten Mustererkennung aus gescannten Materialien automatisch nahtlose Kacheln zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Smart Auto Tile
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# Smart Auto Tile

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Node verwandelt eine Nicht-Kachelung-Menge von Basecolor-, Normal- und Heightmaps in eine Kachelung-Version entsprechend der Smart-Analyse der Eingänge. Es ähnelt [Make It Tile Foto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), ist aber viel komplexer, da es Informationen aus allen Kanälen nutzt, um Dinge auf intelligente Weise miteinander zu vermischen (ähnlich wie [Klon Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Sie verfügt außerdem über eine interne [Zuschneidefunktion](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md), um zu bestimmen, welcher Bereich bei der Kachelung verwendet werden soll. Lesen Sie [mehr über den Zuschneideknoten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md), um diese Funktion richtig zu verstehen.

Um diesen Knoten zu verwenden, definiere zunächst den Bereich &quot;Beschnitten&quot;. Lege dann mit den Einstellungen unter &quot;Kante&quot; fest, wie die gekachelten Kanten in der Mitte vermischt werden. Die Treshold-Parameter sind dabei von zentraler Bedeutung! Beachten Sie, dass große, einheitliche Bereiche mit diesem Effekt nicht besonders gut funktionieren. Je mehr Details und Formen es gibt, desto besser funktioniert es.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske verwenden&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Zuschneiden</b> |  |
| <b>Eingabegröße</b> <i>0 - 8192</i> | Auflösung und Proportionen von Eingabebilds. Sehr wichtig für nicht quadratische Bilder. |
| <b>Transformieren</b> <i>(Transformationsmatrix)</i> | Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Edge</b> |  |
| <b>Kanten erkennen</b> <i>False/True</i> | Schaltet die Überblendung mit erkannten Spezialkanten ein bzw. aus. |
| <b>Schwellenwert pro Kanal verwenden</b> <i>False/True</i> | Wechselt zwischen einem globalen Schwellenwert oder einem für jeden Kanal. |
| <b>Schwellenwert</b> <i>0.0 - 1.0</i> |  |
| <b>Grundfarbe des Schwellenwerts</b> <i>0.0 - 1.0</i> |  |
| <b>Schwellenwert Normal</b> <i>0.0 - 1.0</i> |  |
| <b>Schwellenwert-Height</b> <i>0.0 - 1.0</i> |  |
| <b>Offset beschneiden</b> <i>0.0 - 0.5</i> | Hauptsteuerung zum Bewegen des Schnitts, X- und Y-Achsen sind voneinander getrennt. |
| <b>Weichzeichnen</b> <i>0.0 - 2.0</i> | Lässt die Überblendung verschwimmen. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Steuert die Zackenbildung bei Kantenanalyseergebnissen. |
| <b>Auflösung des Rasters</b> <i>1 - 11</i> | Hochwertige Auflösung der Kantenanalyse. |
| <b>Grundfarbe verwenden</b> <i>False/True</i> | Schaltet die Verarbeitung von Grundfarben (ein- und ausblenden) um. |
| <b>Normal verwenden</b> <i>False/True</i> | Schaltet die normale Verarbeitung (ein und aus) um. |
| <b>Height verwenden</b> <i>False/True</i> | Schaltet die normale Verarbeitung (ein und aus) um. |
| <b>Maske verwenden</b> <i>False/True</i> | Schaltet die Verwendung der Maskenzuordnung für benutzerdefinierte Stempelmaskenformen ein oder aus. |

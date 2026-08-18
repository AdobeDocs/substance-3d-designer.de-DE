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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Kachelüberlagerung erstellen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## Musterelement anordnen (Graustufen)

**In:** *Filters/Tiling*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist ein gitterbasierter halbzufälliger Kachel. Es wird ein Eingabefeld verwendet und mit einem Stempel versehen, um zu versuchen, es in ein gekacheltes Bild zu verwandeln, ohne dass es zu viele Wiederholungen gibt, je nach Ihren Einstellungen.

Das ist nützlich, wenn du eine kleine Struktur hast und daraus eine größere, kachelbare Struktur erstellen möchtest.

Beachten Sie, dass dies ein Unterschied zu [Make-It-Tile Foto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md) ist, bei dem hauptsächlich Kanten korrigiert werden.

Informationen zum Verwenden des gesamten Materials finden Sie unter [Smart Auto Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

## Parameter

* **Maskengröße**: *0.0 - 1.0* Größe der runden Maske, die beim Stempeln des Pflasters verwendet wird.
* **Maskengenauigkeit**: *0.0 - 1.0* Abfall-/Maskengenauigkeit der Smoothness.
* **Maskenverkrümmung**: *-100.0 - 100.0* Führt Verkrümmung an Maskenkanten ein. Gut zum Vermeiden glatter, undefinierter Übergänge zwischen Patches.
* **Breite der Mustergröße**: *0.0 - 1000.0*&#x200B;Ändert die Breite des Patches ungleichmäßig.
* **Height der Mustergröße**: *0.0 - 1000.0*&#x200B;Ändert das Height des Patches ungleichmäßig.
* **Störung**: *0.0 - 1.0*\
  Führt translationale Zufälligkeit ein, leicht verschiebbare Flecken.
* **Größenänderung**: *0.0 - 100.0* Führt die Größenvariation für die Maske ein.
* **Oktave**: *0 - 6* Dies ist das Hauptsteuerelement, das die Gesamtgröße bestimmt.
* **Drehung**: *-360.0 - 360.0* Vordrehen des Patches.
* **Drehungsvariation**: *0.0 - 360.0* Führt eine zufällige Rotation für jeden Patch-Stempel ein.
* **Hintergrundfarbe**: *(Farbwert)*Legt die Hintergrundfarbe für Bereiche fest, in denen keine Ausbesserung auftritt.
* **Farbvariation**: *0.0 - 1.0 (Nur Farbversion)*Führt Farbvariationen pro Patch ein.
* **Luminanzvariation** *(nur Graustufenversion)*Führt Luminanzvariation pro Patch ein.

## Beispielbilder

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>

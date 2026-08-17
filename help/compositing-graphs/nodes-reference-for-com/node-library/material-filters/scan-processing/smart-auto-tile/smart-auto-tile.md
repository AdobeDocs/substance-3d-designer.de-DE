---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Smart Auto Tile

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## Smart Auto Tile

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten verwandelt einen nicht kachelbaren Satz von Grundfarben-, Normal- und Höhenkarten in eine kachelbare Version gemäß intelligenter Analyse der Eingaben. Es ähnelt [Make It Tile Foto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), ist aber viel komplexer, da es Informationen aus allen Kanälen nutzt, um Dinge auf intelligente Weise miteinander zu vermischen (ähnlich wie [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Es verfügt außerdem über eine interne [Zuschneiden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)-Funktion, mit der ermittelt wird, welcher Bereich beim Kacheln verwendet werden soll. Lesen Sie [mehr über den Zuschneiden-Knoten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md), um diese Funktion richtig zu verstehen.

Um diesen Knoten zu verwenden, definiere zunächst den Bereich &quot;Beschnitten&quot;. Lege dann mit den Einstellungen unter &quot;Kante&quot; fest, wie die gekachelten Kanten in der Mitte vermischt werden. Die Treshold-Parameter sind dabei von zentraler Bedeutung! Beachten Sie, dass große, einheitliche Bereiche mit diesem Effekt nicht besonders gut funktionieren. Je mehr Details und Formen es gibt, desto besser funktioniert es.

## Parameter

### Eingaben

* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske verwenden&quot; umschaltbar.

### Parameter

* **Zuschneiden**
  * **Eingabegröße**: *0 - 8192* Auflösung und Proportionen der Eingabebilder. Sehr wichtig für nicht quadratische Bilder.
  * **Transformieren**: *(Transformationsmatrix)*\
    Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
  * **Offset**: *0.0 - 1.0*\
    Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Edge**
  * **Kanten erkennen**: *Falsch/Wahr* Aktiviert oder deaktiviert die Überblendung mit der erkannten Spezialkante.
  * **Schwellenwert pro Kanal verwenden**: *Falsch/Wahr* Wechselt zwischen einem globalen Schwellenwert oder einem für jeden Kanal.
  * **Schwellenwert**: *0.0 - 1.0*
  * **Schwellenwert-Basisfarbe**: *0.0 - 1.0*
  * **Schwellenwert Normal**: *0.0 - 1.0*
  * **Schwellenwert-Height**: *0.0 - 1.0*
  * **Offset abschneiden**: *0.0 - 0.5* Hauptsteuerung zum Bewegen des Schnitts, X- und Y-Achsen werden getrennt.
  * **Weichzeichnen**: *0.0 - 2.0* Blendet den Mischübergang ein.
  * **Smoothness**: *0.0 - 2.0* Steuert die Zackenbildung der Ergebnisse der Kantenanalyse.
  * **Rasterauflösung**: *1 - 11* Qualitätsauflösung der Kantenanalyse.
  * **Grundfarbe verwenden**: *Falsch/Wahr* Schaltet die Verarbeitung der Grundfarbe um (ein- und ausblenden).
  * **Normal verwenden**: *Falsch/Wahr* Schaltet die normale Verarbeitung (ein- und ausgehend) um.
  * **Height verwenden**: *Falsch/Wahr* Schaltet die normale Verarbeitung (ein- und ausgehend) um.
  * **Maske verwenden**: *False/True*\
    Schaltet die Verwendung der Maskenzuordnung für benutzerdefinierte Stempelmaskenformen ein oder aus.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

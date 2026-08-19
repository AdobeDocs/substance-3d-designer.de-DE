---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Nadir Patch-Knoten, um den Nadirbereich von HDRI-Panoramen zu patchen, um Artefakte am unteren Rand in Umgebungskarten zu korrigieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir Patch

**In:** *3D-Ansicht/HDRI-Werkzeuge*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten bietet Funktionen zum Überflicken des zentralen Bodenpunkts (Nadir) eines kugelförmig abgebildeten Bildes. Es kann verwendet werden, um ein hässliches Nadir, eine sichtbare Kamera oder ein Stativ zu verbergen oder &quot;auszuklonen&quot;. Es funktioniert wie ein [Klonpatch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), jedoch mit Anpassungen für sphärisch zugeordnete Bilder. Der Benutzer wählt einen Punkt an einer anderen Stelle im Bild aus, das ist der geklonte Punkt, der am Nadir eingeblendet wird. Es sind keine weiteren externen Eingaben erforderlich, außer einer einzelnen HDRI, aber für den Patch-Effekt kann eine externe Maske als Alpha verwendet werden.

Der Effekt kann schnell mit [Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md) überprüft und validiert werden.

## Eingaben

* **Eingabe**: *Farbeingabe*
* **Maskeneingabe**: *Graustufen-Eingabe*\
  Optionaler Maskenschlitz zum Maskieren des Patches. Funktioniert wie ein Alpha.

## Parameter

* **Aktivieren**: *False/True*\
  Aktivieren oder Deaktivieren des Patching-Effekts.
* **Frame-Hilfe anzeigen**: *False/True*\
  Ein- oder Ausblenden der Hilfslinien zu Debugzwecken.
* **Frame-Thickness**: *0.0 - 1.0*\
  Thickness der Hilfslinien.
* **Patch-Skalierung**: *0.0 - 1.0*\
  Globale, einheitliche Patch-Skalierung. Wirkt sich sowohl auf Quell- als auch auf Zielebene aus.
* **Patch-Größe**: *0.0 - 1.0*\
  Uneinheitliche Größe des Pflasters.
* **Patch-Drehung**: *0.0 - 1.0*\
  Drehen des Pflasters. Betrifft Quelle und Ziel.
* **Patch-Alpha**: *Quadratisch glätten, Gaußsch, Maskeneingabe*\
  Lege fest, mit welcher Alpha-Zahl die Farbfläche mit dem Hintergrund überblendet wird.
* **Patch-Härte**: *0.0 - 1.0*\
  Legt die Härte/den Kontrast von Alpha fest.
* **Offset für Quelldrehung**: *0.0 - 1.0*\
  Drehung nur für Quelle des Pflasters.
* **Positionskoordinaten**
  * **Quellposition**:\
    Position der Quelle. Hat Handle in 2D-Ansicht.
  * **Patch-Position**:\
    Zielposition. Hat Handle in 2D-Ansicht.

## Beispielbilder

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Risse-Verwitterung -Knoten, um Rissmuster auf der Grundlage von Gitterkrümmung und Spannungspunkten zu Materialien hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risse, die wettern
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Risse, die wettern

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## Risse, die wettern

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Vollmaterial-Effekt, der auf mehreren Kanälen gleichzeitig funktioniert. Es fügt ein zufälliges Rissmuster hinzu, mit Kontrolle über Ausbreitung und Tiefe.

Vergewissern Sie sich, dass Sie die [Verknüpfungserstellungsmodi](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) richtig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Eine fertig gestellte oder generierte Karte, die für interne Effekte und Maskierung verwendet wird.
* **Height** : *Graustufen-Eingabe*\
  Eine fertig gestellte oder generierte Karte, die für interne Effekte und Maskierung verwendet wird.
* **Maske** : *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Erweitert**
  * **Normales Format**: *DirectX, OpenGL*\
    Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
  * **Maske**: *False/True*\
    Schaltet die Verwendung der Maskenkarte ein oder aus.
* **Effekt**
  * **Risse-Propagierung**: *0.0 - 1.0* Wie weit sollten sich die Risse ausbreiten? Dies ist die Hauptsteuerung für diesen Effekt.
  * **Risse Tiefe**: *0.0 - 1.0* Tiefe des Risseffekts. Dies wirkt sich hauptsächlich auf das Height und geringfügig auf die visuelle Thickness aus.
* **Überblenden**
  * Steuert, wie stark der Effekt in die einzelnen resultierenden Kanäle übergeht.

## Beispielbilder

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>

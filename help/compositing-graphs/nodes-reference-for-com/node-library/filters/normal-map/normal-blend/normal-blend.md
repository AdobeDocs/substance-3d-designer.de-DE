---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normale Überblendung , um Normalmaps miteinander zu überblenden und so glatte Übergänge zwischen Oberflächendetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# Normale Überblendung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## Normale Überblendung

**In:** *Filters/Normal Map*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Mit &quot;Normale Überblendung&quot; können Sie zwei Normalmaps mit einer optionalen Maske überblenden, während Sie gleichzeitig sicherstellen, dass alle Werte normalisiert bleiben. Er unterscheidet sich nicht sehr von einem [atomaren Mischknoten](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), hat aber interne Berechnungen für Normalmaps hinzugefügt.

&quot;Normale Überblendung&quot; ist nicht zum Kombinieren (Überlagern) von Normalmaps gedacht, wobei die obere Karte der unteren Karte Details hinzufügt. Verwenden Sie stattdessen [Normale Kombination](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

## Parameter

### Eingaben

* **NormalFG**: *Farbeingabe*\
  Vordergrund-/obere Normalmap.
* **NormalBG**: *Farbeingabe*\
  Hintergrund/untere Normalmap
* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske verwenden&quot; umschaltbar.

### Parameter

* **Deckkraft**: *0.0 - 1.0*\
  Füllmethode zwischen Vorder- und Hintergrund
* **Maske verwenden**: *False/True*\
  Schaltet die Verwendung der Maskenkarte ein oder aus.

## Beispielbilder

![](../../../../../../assets/normalblend-ex.gif)

*(.gif-Format führt Dithering im Beispiel ein, Anwendungsinterne Ergebnisse sind glatt)*

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Weichzeichnungsknoten, um Weichzeichnungseffekte auf Texturen anzuwenden, um Details zu glätten und einen weichen Fokuseffekt zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Weichzeichnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---


# Weichzeichnen

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Symbol für Weichzeichnerknoten](blur.resources/blur-01.png){width="200px"}

**In:** Atomknoten

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Weichzeichnungsknoten führt einen &quot;box-blur&quot;-Vorgang aus: Mittelung der Pixelwerte über eine festgelegte Entfernung, was zu einem verschwommenen, unscharfen Look führt. Es bietet den einfachsten, schnellsten und einfachsten Weichzeichnungsvorgang, der in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) verfügbar ist.

Der Weichzeichner eignet sich zwar gut für schnelle, einfache Vorgänge, z. B. für das leichte Weichzeichnen einiger Kanten. In jedem anspruchsvolleren Szenario ist [Weichzeichnen HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) eine bessere Wahl, wenn Sie die Leistung gegen Qualität eintauschen möchten.

</td>
</tr>
</table>

## Parameter

* **Intensität**: 0-unlimited\
  Legt die Intensität oder den Abstand für die Weichzeichnung fest. Die Zahl ist nicht begrenzt, aber bei hohen Werten wird das gesamte Bild zu einer gemittelten Farbe.

Das folgende Beispiel zeigt den Weichzeichner dieses Knotens auf der linken Seite im Vergleich zu [Weichzeichner HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) auf der rechten Seite, wenn hohe Werte verwendet werden (in diesem Fall 50). Bei Werten um 1-2 ist der Unterschied nicht spürbar.

| Weichzeichnen (atomar) | HQ-Weichzeichnen |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-02.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-03.png"/></div> |

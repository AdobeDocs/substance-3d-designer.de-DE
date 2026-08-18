---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kantenerkennung", um Kanten in Texturen zu erkennen, um Umrisse und kantenbasierte Maskeneffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kantenerkennung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Kantenerkennung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## Kantenerkennung

**In:** *Filter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erkennt den Kontrast in Schwarz-Weiß-Bildern und erstellt dann eine Schwarz-Weiß-Maske, die den Kontrast hervorhebt.

Dies ist in vielen Fällen nützlich, wenn eine Maske für Kanten benötigt wird. Beachten Sie, dass dies am besten mit kontrastreichen Inputs funktioniert. Passen Sie bei Bedarf den Kontrast an, bevor Sie etwas an diesen Knoten übergeben.

## Parameter

* **Kantenbreite**: *1.0 - 16.0* Breite der erkannten Bereiche um die Kanten.
* **Kantenrundung**: *0.0 - 16.0* Führt ein Runden, Weichzeichnen und Glätten der generierten Maske durch.
* **Umkehren**: *False/True*\
  Kehrt das Ergebnis um.
* **Toleranz**: *0.0 - 1.0* Toleranzschwellenwert für die Stelle, an der Kanten angezeigt werden sollen.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

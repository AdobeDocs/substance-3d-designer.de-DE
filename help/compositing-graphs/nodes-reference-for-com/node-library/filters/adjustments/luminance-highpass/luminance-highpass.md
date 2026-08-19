---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Luminanzhochpass , um hochfrequente Luminanzdetails aus Texturen zu extrahieren, um Oberflächendetails zu verbessern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminanzhochpass
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# Luminanzhochpass

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## Luminanzhochpass

**In:** *Filter/Korrekturen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Bricht Beleuchtungsinformationen ab, indem ein [Hochpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) für den Luminanzwert der Eingabe ausgeführt wird. Nützlich, um fotografierte Texturen mit Beleuchtungsinformationen zu korrigieren. Kann in [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) mit mehreren Durchläufen kombiniert werden, um unterschiedliche Lichtfrequenzen zu entfernen.

Erweist sich als etwas besser bei der Farberhaltung als [Beleuchtung Niederfrequenzen abbrechen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

## Parameter

* **Radius**: *0.0 - 64.0* Radius des Hochpasseffekts. Ein kleinerer Radius annulliert eine kleinere Beleuchtung und passt sie an die Eingabebilder an.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

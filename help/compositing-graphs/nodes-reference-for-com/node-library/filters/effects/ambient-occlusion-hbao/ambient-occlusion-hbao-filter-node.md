---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den HBAO-Filterknoten für die Umgebungsalgorithmen, um mithilfe horizontaler Verdeckungen Umgebungsalgorithmen für eine realistische Schattierung zu generieren. Verdeckung
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Umgebungsluft (HBAO) (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Umgebungsluft (HBAO) (Filterknoten)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Umgebungs-Verdeckung (HBAO)

**In:** *Filter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Verwendet eine Höhenkarte als Eingabe und generiert daraus eine Umgebungskarte für die Verdeckung. Es verwendet Horizon-Based Ambient Verdeckung, einen Algorithmus, der ursprünglich für die Echtzeit-AO-Generierung im Bildschirmbereich entwickelt wurde. Sehr nützlich für das Erstellen prozeduraler AO-Maps aus prozeduralen Heightmaps.

Eine alternative, komplexere, aber langsamere Version von AO finden Sie unter [Ambient Verdeckung (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## Parameter

* **Welteinheiten verwenden**: *Falsch/Wahr* Schaltet die Verwendung von Welt- oder Bildschirmraumeinheiten um. Aktiviert zusätzliche Parameter, die eine präzisere Steuerung ermöglichen.
* **Height-Tiefe**: *0.0 - 1.0* Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;False&quot; gesetzt ist. Steuert die globale Skalierung.
* **Oberflächengröße**: **0.0 - 1000.0** Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;True&quot; festgelegt ist. Steuert die globale Skalierung.
* **Height-Skalierung (cm)**: *0.0 - 1000.0* Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;True&quot; festgelegt ist. Steuert die globale Skalierung.
* **Radius**: *0.0 - 1.0* Steuert die Verteilung des AO.
* **Qualität**: *4 Samples, 8 Samples, 16 Samples*\
  Legt die Qualitätsstufe fest, indem die Anzahl der für die Berechnung verwendeten Stichproben bestimmt wird.
* **GPU-Optimierung**: *Falsch/Wahr* Aktiviert die interne GPU-Optimierung und beschleunigt die Verarbeitung.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>

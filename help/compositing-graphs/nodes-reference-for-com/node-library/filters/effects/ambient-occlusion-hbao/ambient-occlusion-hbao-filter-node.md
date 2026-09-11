---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
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
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Umgebungsluft (HBAO) (Filterknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ambient-occlusion-hbao-filter-node.resources/hbao.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Verwendet eine Höhenkarte als Eingabe und generiert daraus eine Umgebungskarte für die Verdeckung. Es verwendet Horizon-Based Ambient Verdeckung, einen Algorithmus, der ursprünglich für die Echtzeit-AO-Generierung im Bildschirmbereich entwickelt wurde. Sehr nützlich für das Erstellen prozeduraler AO-Maps aus prozeduralen Heightmaps.

Eine alternative, komplexere, aber langsamere Version von AO finden Sie unter [Ambient Verdeckung (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Welteinheiten verwenden</b> <i>False/True</i> | Schaltet die Verwendung von Welt- oder Bildschirmraumeinheiten um. Aktiviert zusätzliche Parameter, die eine präzisere Steuerung ermöglichen. |
| <b>Height-Tiefe</b> <i>0.0 - 1.0</i> | Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;False&quot; gesetzt ist. Steuert die globale Skalierung. |
| <b>Oberflächengröße</b> <i>0.0 - 1000.0</i> | Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;True&quot; gesetzt ist. Steuert die globale Skalierung. |
| <b>Height-Skalierung (cm)</b> <i>0.0 - 1000.0</i> | Wird nur verwendet, wenn &quot;World Units&quot; auf &quot;True&quot; gesetzt ist. Steuert die globale Skalierung. |
| <b>Radius</b> <i>0.0 - 1.0</i> | Steuert die Verteilung des AO. |
| <b>Qualität</b> <i>4 Samples, 8 Samples, 16 Samples</i> | Legt die Qualitätsstufe fest, indem die Anzahl der für die Berechnung verwendeten Stichproben bestimmt wird. |
| <b>GPU-Optimierung</b> <i>False/True</i> | Ermöglicht interne GPU-Optimierung und beschleunigt die Verarbeitung. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Verwenden Sie den Ambient occlusion-Knoten (RTAO), um ambient occlusion-Maps in Echtzeit aus Höhen-Map für eine realistische Schattierung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ambient occlusion (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Ambient occlusion (RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RTAO-Knotensymbol](ambient-occlusion-rtao.resources/rt-ao.png "RTAO-Knotensymbol")

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Ambient occlusion-Map basierend auf einer Höhen-Map-Eingabe.

Dieser Filter liefert präzisere Ergebnisse als der HBAO, sollte aber aufgrund der Berechnung nicht in Kombination mit dem CPU (SSE)-Engine verwendet werden.

Eine schnellere und einfachere Alternative finden Sie unter [Ambient occlusion (HBAO) (Filterknoten)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Physische Größe verwenden</b> <i>Boolesche Wert</i> | Verwenden Sie die Einstellung Physische Größe , um die Skalierung des Heights festzulegen. |
| <b>Physische Größe</b> <i>Fließkommazahl3</i> <i>(Verfügbar, wenn <b>Physische Größe </b> verwenden auf <i>Wahr</i> festgelegt ist)</i> | Passt den Maßstab des Heights an die tatsächliche Physische Größe der Fläche an. |
| <b>Beispiele</b> <i>Ganzzahl</i> | Die Anzahl der Strahlen, die zur Berechnung der ambient occlusion verwendet werden.<br>Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis auf Kosten der Leistung. |
| <b>Height-Skalierung</b> <i>Fließkommazahl</i> <i>(Verfügbar, wenn <b>Physische Größe </b> verwenden auf <i>Falsch</i> festgelegt ist)</i> | Multiplikator für die Intensität des Höhen-Map-Eingangs. |
| <b>Verteilung</b> <i>Ganzzahl</i> | Legt die Verteilungsmethode fest. Auswirkungen auf die Abnahme von Schattenbereichen, |
| <b>Maximale Entfernung</b> <i>Gleitend</i> | Legt die maximale Entfernung fest, die Strahlen zurücklegen können. |
| <b>Spread Angle</b> <i>Gleitend</i> | Legt den Ausbreitungswinkel für die Strahlen fest, auf die geschossen werden soll. Ein Wert von 1 ist eine ganze Hemisphäre. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-7-48.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-9-0-1.png" />
        </td>
    </tr>
</table>

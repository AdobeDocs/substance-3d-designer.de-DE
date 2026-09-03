---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Umgebungsunterstütze (RTAO), um aus Height-Maps Echtzeit-Umgebungsunterstützungszuordnungen für eine realistische Verdeckung zu erstellen, um eine realistische Schattierung der Verdeckung zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Umgebungs-Verdeckung (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Umgebungs-Verdeckung (RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RTAO-Knotensymbol](ambient-occlusion-rtao.resources/ambient-occlusion-rtao-01.png "RTAO-Knotensymbol")

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Umgebungszuordnung für die Verdeckung auf der Grundlage einer Height-Zuordnungseingabe.

Dieser Filter liefert präzisere Ergebnisse als der HBAO, sollte aber aufgrund der Berechnungszeit nicht in Kombination mit der CPU (SSE)-Engine verwendet werden.

Eine schnellere und einfachere Alternative finden Sie unter [Umgebungsspannung (HBAO) (Filterknoten)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Physische Größe verwenden</b> <i>Boolescher Wert</i> | Verwenden Sie die Einstellung Physische Größe , um die Skalierung des Heights festzulegen. |
| <b>Physische Größe</b> <i>Float3</i> <i>(Verfügbar, wenn <b>Physische Größe </b> verwenden auf <i>Wahr</i> festgelegt ist)</i> | Passt den Maßstab des Heights an die tatsächliche Physische Größe der Fläche an. |
| <b>Beispiele</b> <i>Integer</i> | Die Anzahl der Strahlen, die zur Berechnung der ambient occlusion verwendet werden.<br>Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis auf Kosten der Leistung. |
| <b>Height-Skalierung</b> <i>Gleitend</i> <i>(Verfügbar, wenn <b>Physische Größe </b> verwenden auf <i>Falsch</i> festgelegt ist)</i> | Multiplikator für die Intensität des Height-Map-Eingangs. |
| <b>Verteilung</b> <i>Integer</i> | Legt die Verteilungsmethode fest. Auswirkungen auf die Abnahme von Schattenbereichen, |
| <b>Maximale Entfernung</b> <i>Gleitend</i> | Legt die maximale Entfernung fest, die Strahlen zurücklegen können. |
| <b>Spread Angle</b> <i>Gleitend</i> | Legt den Ausbreitungswinkel für die Strahlen fest, auf die geschossen werden soll. Ein Wert von 1 ist eine ganze Hemisphäre. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-03.png" />
        </td>
    </tr>
</table>

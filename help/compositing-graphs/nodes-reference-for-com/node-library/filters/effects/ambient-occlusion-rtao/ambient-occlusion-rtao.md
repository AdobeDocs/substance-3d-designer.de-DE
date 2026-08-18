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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Umgebungs-Verdeckung (RTAO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RTAO-Knotensymbol](../../../../../../assets/rt-ao.png "RTAO-Knotensymbol")

<b>In:</b> *Filter/Effekte*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Umgebungszuordnung für die Verdeckung auf der Grundlage einer Height-Zuordnungseingabe.

Dieser Filter liefert präzisere Ergebnisse als der HBAO, sollte aber aufgrund der Berechnungszeit nicht in Kombination mit der CPU (SSE)-Engine verwendet werden.

Eine schnellere und einfachere Alternative finden Sie unter [Umgebungsspannung (HBAO) (Filterknoten)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md).

</td>
</tr>
</table>

## Parameter

<b>Physische Größe verwenden</b> *Boolesch*\
Verwenden Sie die Einstellung Physische Größe , um die Skalierung des Heights festzulegen.

<b>Physische Größe</b> *Float3* (verfügbar, wenn <b>Physische Größe </b> verwenden auf *Wahr* festgelegt ist)\
Passt den Maßstab des Heights an die tatsächliche Physische Größe der Fläche an.

<b>Beispiele </b>*Ganzzahl*\
Die Anzahl der Strahlen, die zur Berechnung der Umgebungs-Verdeckung verwendet werden.\
Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis auf Kosten der Leistung.

<b>Height-Skalierung</b> *Gleitkomma* (verfügbar, wenn <b>Physische Größe verwenden</b> auf *Falsch* festgelegt ist)\
Multiplikator für die Intensität des Height-Map-Eingangs.

<b>Distribution</b> *Integer* Legt die Verteilungsmethode fest. Auswirkungen auf die Abnahme von Schattenbereichen,

<b>Maximale Entfernung</b> *Gleitend*\
Legt die maximale Entfernung fest, die Strahlen zurücklegen können.

<b>Spread Angle</b> *Float*\
Legt den Ausbreitungswinkel für die Strahlen fest, auf die geschossen werden soll. Ein Wert von 1 ist eine ganze Hemisphäre.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RTAO-Knoten - Beispiel 1](../../../../../../assets/image2021-6-18-11-7-48.png "RTAO-Knoten - Beispiel 1")

</td>
<td style="border: 0;" valign="top">

![RTAO-Knoten - Beispiel 2](../../../../../../assets/image2021-6-18-11-9-0-1.png "RTAO-Knoten - Beispiel 2")

</td>
</tr>
</table>

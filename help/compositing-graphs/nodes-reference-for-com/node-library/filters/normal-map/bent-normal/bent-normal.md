---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Abgewinkelte Normale, um abgewinkelte Normalmaps zu erzeugen, die die Umgebungsbeleuchtung und die indirekte Verdeckung berücksichtigen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal gebogen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# Normal gebogen

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Symbol für gebogenen normalen Knoten](../../../../../../assets/rt-bent-normal.png "Symbol für gebogenen normalen Knoten")

<b>In:</b> *Filter/Normalmap*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine gebogene Normalmap basierend auf einer Height-Map-Eingabe. Eine gekrümmte Normalmap ist eine Sonderversion von [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) und [Umgebungskarte (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), die eine Normalmap mit eingebetteter umgebender Verdeckung erzeugt.\
Dies kann in Echtzeit-Engines verwendet werden, um Umgebungsreflexionen in die Normalmap einzubinden, z. B. für präzisere Reflexionen der Verdeckung auf Verdeckungen aus Metallen.

Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden.

</td>
</tr>
</table>

## Parameter

<b>Physische Größe verwenden</b> *Boolesch*\
Verwenden Sie die Einstellung Physische Größe , um die Skalierung des Heights festzulegen.

<b>Physische Größe</b> *Float3* (verfügbar, wenn <b>Physische Größe </b> verwenden auf *Wahr* festgelegt ist)\
Passt den Maßstab des Heights auf der Grundlage der realen Physische Größe der Fläche an.

<b>Beispiele</b> *Integer*\
Anzahl der Strahlen, die zur Berechnung der gebogenen Normalen verwendet werden.\
Ein höherer Wert sorgt für ein glatteres und präziseres Ergebnis auf Kosten der Leistung.

<b>Height-Skalierung</b> *Gleitkomma (verfügbar, wenn &quot;Physische Größe verwenden&quot; auf &quot;Falsch&quot; festgelegt ist)*\
Multiplikator für die Intensität des Height-Map-Eingangs.

<b>Verteilung</b> *Ganzzahl*\
Legt die Verteilungsmethode fest. Betrifft Falloff in Richtung Schattenbereiche.

<b>Maximale Entfernung</b> *Gleitend*\
Legt die maximale Entfernung fest, die Strahlen zurücklegen können.

<b>Spread Angle</b> *Float*\
Legt den Ausbreitungswinkel für die Strahlen fest, auf die geschossen werden soll. Ein Wert von 1 ist eine ganze Hemisphäre.

<b>Normales Format</b> *Ganzzahl*\
Kehrt den grünen Kanal der Ausgabe um.

## Beispielbilder

![Gebogener normaler Knoten - Beispiel 1](../../../../../../assets/bent-normal-ex-1.jpg "Gebogener normaler Knoten - Beispiel 1")

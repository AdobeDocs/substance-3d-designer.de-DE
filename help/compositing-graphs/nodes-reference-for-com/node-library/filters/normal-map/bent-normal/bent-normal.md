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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# Normal gebogen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol für gebogenen normalen Knoten](bent-normal.resources/rt-bent-normal.png "Symbol für gebogenen normalen Knoten")

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine gebogene Normalmap basierend auf einer Height-Map-Eingabe. Eine gekrümmte Normalmap ist eine Sonderversion von [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) und [Umgebungskarte (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), die eine Normalmap mit eingebetteter umgebender Verdeckung erzeugt.\
Dies kann in Echtzeit-Engines verwendet werden, um Umgebungsreflexionen in die Normalmap einzubinden, z. B. für präzisere Reflexionen der Verdeckung auf Verdeckungen aus Metallen.

Dieser Knoten sollte aufgrund der Berechnungszeit nicht in Kombination mit der CPU-Engine (SSE) verwendet werden.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Physische Größe verwenden</b> <i>Boolescher Wert</i> | Verwenden Sie die Einstellung Physische Größe , um die Skalierung des Heights festzulegen. |
| <b>Physische Größe</b> <i>Float3</i> | (Verfügbar, wenn <b>Physische Größe verwenden</b> auf <i>Wahr</i> festgelegt ist) Passt die Skalierung des Heights auf der Grundlage der tatsächlichen Physische Größe der Oberfläche an. |
| <b>Beispiele</b> <i>Integer</i> | Anzahl der Strahlen, die zur Berechnung der gebogenen Normalen verwendet werden.<br>Eine höhere liefert ein glatteres und präziseres Ergebnis auf Kosten der Leistung. |
| <b>Height-Skalierung</b> <i>Gleitend</i> | (Verfügbar, wenn &quot;Physische Größe verwenden&quot; auf &quot;Falsch&quot; gesetzt ist) Multiplikator für die Intensität des Höhen-Map-Eingangs. |
| <b>Verteilung</b> <i>Integer</i> | Legt die Verteilungsmethode fest. Betrifft Falloff in Richtung Schattenbereiche. |
| <b>Maximale Entfernung</b> <i>Gleitend</i> | Legt die maximale Entfernung fest, die Strahlen zurücklegen können. |
| <b>Spread Angle</b> <i>Gleitend</i> | Legt den Ausbreitungswinkel für die Strahlen fest, auf die geschossen werden soll. Ein Wert von 1 ist eine ganze Hemisphäre. |
| <b>Normales Format</b> <i>Integer</i> | Kehrt den grünen Kanal der Ausgabe um. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-ex-1.jpg" />
        </td>
    </tr>
</table>

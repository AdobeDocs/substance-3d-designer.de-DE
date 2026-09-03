---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Flood Fill zu Box-Größe", um Bereiche mit Werten für die Größe des Begrenzungsrahmens für prozedurale Skalierungseffekte zu füllen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill in Box-Größe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Flood Fill in Box-Größe

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-bbox-size.resources/flood-fill-to-bbox-size-01.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Graustufenzuordnung aus einer [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)-Basis, wobei die Werte mit der individuellen Größe jeder Kachel verknüpft sind.

Die Werte sind relativ zur Gesamtgröße der Arbeitsfläche (eine vollständig weiße Kachel würde bedeuten, dass sie die gesamte Arbeitsfläche dehnt), daher ist der Kontrast oft gering.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>max(X, Y), X, Y</i> | Legt fest, auf welcher Metrik der Wert basiert: Breite, Länge oder beides. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-bbox-size.resources/flood-fill-to-bbox-size-02.png" />
        </td>
    </tr>
</table>

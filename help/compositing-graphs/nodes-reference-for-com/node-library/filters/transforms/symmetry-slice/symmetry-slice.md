---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Symmetrie-Slice", um Strukturen entlang von Symmetrieachsen zu segmentieren und so gespiegelte Muster und Effekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Symmetrie-Slice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# Symmetrie-Slice

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/symmetry-slice-01.png){width="128px"}

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Komplexer Symmetrie-/Spiegelungs-Betriebsknoten. Ermöglicht eine Vielzahl von geometrischen Operationen mit voller Kontrolle, erfordert jedoch einige Experimente.

Im Vergleich zu [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) und [Symmetry](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md) verfügt dieser Knoten über viele weitere Optionen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Symmetrie-Modus</b> <i>0 - 6</i> | Wählen Sie Symmetrie geometrie/Spiegellinie. Folgende Optionen stehen zur Auswahl: Horizontal, Vertikal, Diagonal von links nach rechts, Diagonal von rechts nach links, Vertikal umkehren, Ecke und Diagonale Ecke. |
| <b>Übertragungsmodus</b> <i>0 - 6</i> | Füllmethode. Folgende Optionen stehen zur Verfügung: |
| <b>Überblendung</b> <i>0.0 - 1.0</i> | Überblendung das Originalbild wieder in das Ergebnis ein. |
| <b>Seite spiegeln</b> <i>False/True</i> | Spiegelt den Ursprung, d. h., die Ausgangsseite des Vorgangs wird umgekehrt. Die Symmetrie von links nach rechts wird beispielsweise von rechts nach links. |
| <b>Seite spiegeln2</b> <i>False/True</i> | Wird nur verwendet, wenn der Symmetrie-Modus 5 oder 6 ist. Ursprung der gedrehten Ecke. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symmetry-slice-02.png" />
        </td>
    </tr>
</table>

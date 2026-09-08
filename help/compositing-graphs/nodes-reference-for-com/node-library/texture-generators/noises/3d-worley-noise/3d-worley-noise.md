---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D Worley Rauschen-Knoten, um Worley Rauschen auf der Grundlage der 3D-Position zu generieren, um volumetrische Textur-Effekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Worley Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 7%

---


# 3D Worley Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Es ist eine der vielseitigsten und fortschrittlichsten Rauschen in der Library und generiert eine Worley Rauschen im 3D-Raum, basierend auf einer Eingangspositionskarte. Verfügt über eine Vielzahl von Optionen, die es viel leistungsfähiger machen als die standardmäßigen [Zellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) oder [Entfernungen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)-basierten Rauschen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>1 - 64</i> | Legen Sie die globale Skalierung für den Effekt fest. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Führen Sie eine ungleichmäßige Skalierung auf X-, Y- und Z-Achsen separat durch. |
| <b>Modus</b> <i>Euklidean, Manhattan, Chebyshev, Minkowski</i> | Ändern Sie die Abstandsmetrik. Lässt einige sehr unterschiedliche Rauschen-Typen zu. |
| <b>Minkowski-Zahl</b> <i>0.0 - 20.0</i> | Nur mit Minkowski Entfernungsmetrik. Überblendungen zwischen verschiedenen Kennzahlen. |
| <b>Stil</b> <i>F1, F2, F2-F1, Rahmen, Zufallsfarbe</i> | Legen Sie die Metrik-Kombinationsmathematik fest. Ermöglicht viele weitere Kombinationen. |
| <b>Rahmenbreite</b> <i>0.0 - 1.0</i> | Wenn die Rahmenkombination &quot;Mathematik&quot; aktiviert ist, wird die Breite des Rahmens gesteuert. |
| <b>Rundheit</b> <i>0.0 - 1.0</i> | Nur verfügbar mit den Modi F1, F2 und F2-F1. Legt die mittlere Position des Levels fest. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt das Ergebnis um. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex01.png" />
        </td>
    </tr>
</table>

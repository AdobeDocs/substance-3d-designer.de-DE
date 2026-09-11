---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Verwenden Sie den Krümmung-Filterknoten, um Krümmungs-Map aus Höhen-Map für die Erkennung konvexer und konkaver Flächen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Krümmung (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Krümmung (Filterknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-1.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt eine einfache, harte Konvertierung der Krümmung in einem Durchgang zur Eingabe von [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) durch. Die resultierende Karte enthält weiße Farbtöne für konvexe Bereiche und schwarze Farbtöne für konkave Bereiche. Krümmung erzeugt immer pixelgenaue Linien und gestochen scharfe Übergänge.

Dieser Knoten ist nützlich, um bestimmte Kanten schnell hervorzuheben oder abzudunkeln. Sie ist im Vergleich zu [Krümmung Smooth](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (das qualitativ hochwertigere Ergebnisse liefert) und [Krümmung Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (das mehr Optionen bietet) begrenzt.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 10.0</i> | Intensität des Effekts. Erhöht den Kontrast des Ergebnisses. |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-ex.png" />
        </td>
    </tr>
</table>

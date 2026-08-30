---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Krümmung Sobel, um Maskenkanten mit Sobel-Operatoren zum Erstellen von randbasierten Krümmungen zu erkennen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Krümmungssobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Krümmungssobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-sobel.resources/curvature-sobel.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt eine einfache, harte Konversion der Einmalpasskrümmung zur Eingabe von [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) durch. Die resultierende Karte enthält weiße Farbtöne für konvexe Bereiche und schwarze Farbtöne für konkave Bereiche. Mit &quot;Krümmung&quot; werden immer dickere Linien und gestochen scharfe Übergänge erzeugt.

Dieser Knoten ist nützlich, um bestimmte Kanten schnell hervorzuheben oder abzudunkeln. Sie unterscheidet sich leicht von [Krümmung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), da sie bessere Qualitätsergebnisse liefert, aber immer noch scharf und hart ist.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Intensität</b> <i>0.0 - 1.0</i> | Intensität des Effekts, passt Kontrast an. |
| <b>Normaler Typ</b> <i>DirectX, OpenGL</i> |  |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-sobel.resources/curv-sobel-ex.png" />
        </td>
    </tr>
</table>

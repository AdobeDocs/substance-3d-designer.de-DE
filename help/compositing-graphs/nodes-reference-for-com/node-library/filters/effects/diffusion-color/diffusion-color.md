---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Diffusion-Diffusion", um Farbeffekte anzuwenden und so sanfte Farbübergänge und -überblendungen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diffusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# Diffusion

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-color.resources/diffusion-color-icon.png){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wenden Sie einen Farbkorrekturprozess auf die Diffusionen in der Bildeingabe &quot;**Source**&quot; entsprechend der bereitgestellten Bildeingabe &quot;**Mask**&quot; an, um bei Verwendung von [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) glatte Farbabstufungen zwischen den Farben zu erstellen.

Nur Farben aus Pixeln, die der Maske entsprechen, werden gestreut. andere Pixel nicht am Ergebnis beteiligt sind.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Quelle</b> <i>Farbe</i> | Das zu streuende Bild. |
| <b>Maske</b> <i>Graustufen</i> | Diffusionsmaske: Weiße Pixel werden in <i>Quelle</i> aufgenommen und in schwarzen Pixeln verteilt. Das Bild sollte schwarzweiß sein. Wenn die Maske Farbverläufe enthält, ist der Cutoff-Wert 0,5. |
| <b>Intensität</b> <i>Graustufen</i> | Legt lokal fest, wie stark der Diffusionsprozess angewendet wird. Diese Zuordnung sollte <i>kontrastiert</i> sein, um einen spürbaren Effekt zu erzielen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Iterationen</b> <i>0.0 - 64.0</i> | Die Anzahl der auszuführenden Diffusion-Iterationen (höher ist besser, aber langsamer). Nützliche Werte liegen im Bereich [8, 48].<br>Bitte beachten Sie, dass niedrige Werte in Ordnung oder sogar besser sind, wenn Sie nicht nach mathematischer Korrektheit suchen. |
| <b>Entfernung</b> <i>0.0 - 1.0</i> | Passt die maximale Entfernung der Diffusion an. |
| <b>Dithering aktivieren</b> <i>Wahr/Falsch</i> | Steuert die Sampling-Methode für jeden Durchgang. Beim Dithering ist die Konvergenz in weniger Durchgängen möglich, es entsteht jedoch Rauschen.<br>Ohne diese Methode ist jeder Durchgang schneller, aber es sind mehr Durchgänge erforderlich, um ein glattes Ergebnis ohne Banding-Artefakte zu erzielen. |
| <b>Ist Normalen-Map</b> <i>Wahr/Falsch</i> | Fügt bei jedem Schritt eine Normalisierung der Werte hinzu. |
| <b>Alpha als Maske verwenden</b> <i>Wahr/Falsch</i> | Verwenden Sie anstelle der Eingabe <i>Diffusion</i> den Alphakanal der <i>Quellmaske</i> als Maske für die Maske. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01b-after-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01a-after-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal-render.jpg" />
        </td>
    </tr>
</table>

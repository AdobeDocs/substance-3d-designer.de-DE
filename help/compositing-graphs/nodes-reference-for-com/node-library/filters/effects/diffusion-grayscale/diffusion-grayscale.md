---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Diffusionsgrau", um Graustufen-Diffusionseffekte anzuwenden, um glatte Farbübergänge und Füllmethoden zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diffusions-Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# Diffusions-Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-icon.png){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wenden Sie einen Diffusionsprozess auf die Werte in der Bildeingabe **Quelle** entsprechend der bereitgestellten Bildeingabe **Maske** an, um glatte Abstufungen zwischen den Werten zu erstellen.

Nur Werte aus Pixeln, die der Maske entsprechen, werden gestreut. andere Pixel nicht am Ergebnis beteiligt sind.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Quelle</b> <i>Graustufen</i> | Das zu streuende Bild. |
| <b>Maske</b> <i>Graustufen</i> | Diffusionsmaske: Weiße Pixel werden in <i>Quelle</i> aufgenommen und in schwarzen Pixeln verteilt. Das Bild sollte schwarzweiß sein. Wenn die Maske Farbverläufe enthält, ist der Cutoff-Wert 0,5. |
| <b>Intensität</b> <i>Graustufen</i> | Legt lokal fest, wie stark der Diffusionsprozess angewendet wird. Diese Zuordnung sollte <i>kontrastiert</i> sein, um einen spürbaren Effekt zu erzielen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Iterationen</b> <i>0.0 - 64.0</i> | Die Anzahl der auszuführenden Diffusion-Iterationen (höher ist besser, aber langsamer). Nützliche Werte liegen im Bereich [8, 48].<br>Bitte beachten Sie, dass niedrige Werte in Ordnung oder sogar besser sind, wenn Sie nicht nach mathematischer Korrektheit suchen. |
| <b>Entfernung</b> <i>0.0 - 1.0</i> | Passt die maximale Entfernung der Diffusion an. |
| <b>Dithering aktivieren</b> <i>Wahr/Falsch</i> | Steuert die Sampling-Methode für jeden Durchgang. Beim Dithering ist die Konvergenz in weniger Durchgängen möglich, es entsteht jedoch Rauschen.<br>Ohne diese Methode ist jeder Durchgang schneller, aber es sind mehr Durchgänge erforderlich, um ein glattes Ergebnis ohne Banding-Artefakte zu erzielen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-render.jpg" />
        </td>
    </tr>
</table>

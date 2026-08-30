---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Diffusion UV , um Diffusionen im UV-Bereich anzuwenden, um sanfte Farbübergänge und Füllmethoden zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diffusion UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# Diffusion UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-icon.png){width="200px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wenden Sie einen Maskierungsprozess auf die UV-Koordinaten in der Bildeingabe **Diffusion** gemäß der bereitgestellten Bildeingabe **Maske** an, wobei die Koordinaten zwischen den Werten aus **Quelle** interpoliert werden.

Nur UVs von Pixeln, die der Maske entsprechen, werden gestreut. andere Pixel nicht am Ergebnis beteiligt sind.

Bitte beachten Sie, dass die Kachelung in einer besonderen Art und Weise erfolgt: Wenn die Kachelung *aktiviert ist* (was standardmäßig der Fall ist), können benachbarte Koordinaten über die 0/1-Grenze gemittelt werden.

Wenn beispielsweise der U-Koordinatenwert auf einem Pixel 0,1 und auf einem anderen Pixel 0,8 beträgt, wird der Durchschnittswert 0,95 und nicht 0,45 betragen, da *die Kachelung der Koordinaten angenommen wird*. Dies ist unabhängig von der tatsächlichen Pixelposition: Koordinatenwerte werden im ganzen Bild gleich behandelt.

Dies kann zu unerwünschten Ergebnissen führen, wenn dieser Filter für *Texturen-Deformation* verwendet wird. Stellen Sie in diesem Fall sicher, dass in der Maske nicht mehr als *eine halbe Textur im Abstand von* &quot;Steuerkurven/Punkte&quot; definiert sind.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Quelle</b> <i>Farbe</i> | Die zu diffundierenden UVs. Beachten Sie, dass die Kachelung in diesem Filter besonders behandelt wird (siehe <i>Beschreibung</i>). |
| <b>Maske</b> <i>Graustufen</i> | Diffusion: Weiße Pixel werden in <i>Quelle</i> aufgenommen und in schwarzen Pixeln verteilt. Das Bild sollte schwarzweiß sein. Wenn die Maske Farbverläufe enthält, ist der Cutoff-Wert 0,5. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Iterationen</b> <i>0.0 - 64.0</i> | Die Anzahl der auszuführenden Diffusion-Iterationen (höher ist besser, aber langsamer). Nützliche Werte liegen im Bereich [8, 48].<br>Bitte beachten Sie, dass niedrige Werte in Ordnung oder sogar besser sind, wenn Sie nicht nach mathematischer Korrektheit suchen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>

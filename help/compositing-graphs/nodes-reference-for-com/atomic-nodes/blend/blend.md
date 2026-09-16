---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Überblendung , um mithilfe verschiedener Füllmethoden zwei Texturen miteinander zu verblenden und so Kompositionseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Überblenden
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 8%
---

# Überblenden

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Elementare Knoten: Überblendung](blend.resources/comp_blend_1.png "Elementare Knoten: Überblendung"){width="100%"}

<b>In:</b> Elementare Knoten

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Kombiniert zwei Bilder mit einer angegebenen Füllmethode und einer optionalen Maske.

Es ist der nützlichste Elementare Knoten aller Graf. Dieser Knoten wird von nahezu jedem Knoten verwendet, den Sie in [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) erstellen.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="blend.resources/blend-tooltip.gif" alt="Angleichen-QuickInfo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Die Funktionalität ähnelt der von zwei Ebenen übereinander in [Substance 3D Painter](https://www.adobe.com/de/products/substance3d-painter.html) oder [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html), die durch den Mischmodus, den Sie auf der obersten Ebene festgelegt haben, miteinander vermischt werden.

>[!TIP]
>
> Erfahren Sie mehr über die im Knoten &quot;Überblendung&quot; in [dieser dedizierten Seite](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md) verfügbaren Mischmodi.



## Parameter

|  |  |
| --- | --- |
| <b>Deckkraft</b> *Fließkommazahl* | Deckkraft der Ebene &quot;Vordergrund&quot;, die mit dem Hintergrund verschmilzt. Sie arbeitet unabhängig von der Deckkrafteingabe und dient ihr als zusätzlicher Multiplikator. |
| <b>Füllmethode</b> *Ganzzahl* [Statisch](../../../../glossary/glossary.md) | Legt den zu verwendenden Mischvorgang fest.   Weitere Informationen finden Sie auf der [dedizierten Seite zu den Füllmethoden](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md). |
| <b>Alpha-Überblendung</b> *Ganzzahl* [Statisch](../../../../glossary/glossary.md) | Legt das Füllverhalten fest, wenn Farbeingaben Alphakanal aufweisen:<ul data-preserve-html="true"> <li data-preserve-html="true">Quelle Alpha verwenden</li> <li data-preserve-html="true">Alpha ignorieren</li> <li data-preserve-html="true">Gerade Alpha-Überblendung</li> <li data-preserve-html="true">Vormultiplizierte Alpha-Überblendung</li> </ul> |
| <b>Zuschneidebereich</b> *Fließkommazahl4* [Statisch](../../../../glossary/glossary.md) | Legen Sie einen benutzerdefinierten Zuschneidebereich fest, der sich wie eine zusätzliche Deckkraftmaske verhält. Jeder zugeschnittene Bereich zeigt nur den Hintergrund. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Vordergrund</b> *Graustufen/Farbe* | Obere oder Vordergrundebene des Mischvorgangs. |
| <b>Hintergrund</b> *Graustufen/Farbe* PRIMÄR | Untere oder Hintergrundebene des Mischvorgangs. |
| <b>Deckkraft</b> *Graustufen* | Optionale Alpha-Masken-Eingabe. |

>[!IMPORTANT]
>
> Mischknoten verfügen über dynamische Eingänge, die je nach Ihren Verbindungen zwischen Graustufen und Farbe wechseln.<b> Ein Überblendknoten kann nur zwei Eingaben desselben Typs überblenden</b>.
> 
> Wenn Sie eine Farb- und Graustufeneingabe mit dem Vorder- und Hintergrund verbinden, wird eine gestrichelte rote Verbindungslinie angezeigt, was einen Berechnungsfehler bedeutet.
> 
> Dies ist der wichtigste Grund, warum neue Benutzer Probleme mit Farb- und Graustufenverbindungen haben: Stellen Sie sicher, dass beide Verbindungen vom gleichen Typ sind!


## Beispiele

*Demnächst verfügbar.*

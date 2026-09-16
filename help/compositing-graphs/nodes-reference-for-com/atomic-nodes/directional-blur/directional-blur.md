---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ""
description: Verwenden Sie den Richtungsknoten, um Unschärfe-Effekt in einer bestimmten Richtungsunschärfe anzuwenden, um Bewegungsunschärfe- und Stricheffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsunschärfe
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 8%
---

# Richtungsunschärfe

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Elementare Knoten: Richtungsunschärfe](directional-blur.resources/comp_dirmotionblur_1.png "Elementare Knoten: Richtungsunschärfe"){width="100%"}

<b>In:</b> Elementare Knoten

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Wendet Unschärfe in einer bestimmten Richtung gemäß einer Intensitäts-Map an.

Dieser Knoten führt einen Vorgang aus, der einer Bewegungsunschärfe an einem Eingang ähnelt. Im Gegensatz zum regulären Knoten &quot;[Blur](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&quot;, der in allen Richtungen gleichmäßig verschwimmt, funktioniert die &quot;Richtungsunschärfe&quot; entlang eines benutzerdefinierten Winkels.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="directional-blur.resources/directional-blur-tooltip.gif" alt="Richtungsunschärfe-QuickInfo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Ähnlich wie &quot;Weichzeichnen&quot; ist es auch ein schnellerer und qualitativ schlechter Vorgang. Eine erweiterte, qualitativ hochwertigere Alternative wird in [Anisotropischer Weichzeichner](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) bereitgestellt, mit einem leistungsfähigen Kompromiss


## Richtungsunschärfe und Anisotropie

Diese Bilder unten zeigen die Richtungsunschärfe und die [Anisotrope Unschärfe](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), die für dieselbe Eingabeform mit ähnlichen Parametern wirksam sind. Der anisotrope Weichzeichner wurde auf volle Anisotropie und hohe Qualität eingestellt.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Richtungsunschärfe</b>

![Vergleich der Richtungsunschärfe](directional-blur.resources/dirblur-01.png "Vergleich der Richtungsunschärfe"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>Anisotropischer Weichzeichner</b>

![Vergleich der anisotropen Weichzeichnung](directional-blur.resources/aniso-01.png "Vergleich der anisotropen Weichzeichnung"){zoomable="yes"}

</td>
</tr>
</table>


## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Fließkommazahl* | Legt den Weichzeichnungsradius in Pixel fest. |
| <b>Winkel</b> *Fließkommazahl* | Die Richtung des Unschärfe-Effekts in der Anzahl der Windungen im Uhrzeigersinn, ausgehend von der Horizontalen - d.h. dem Richtungsvektor (1, 0). |

## Eingabe-Verbindungen

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* [PRIMÄR](../../../../glossary/glossary.md) | Das zu verarbeitende Bild. |


## Beispiele

*Demnächst verfügbar.*

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Richtungsunschärfe", um Unschärfeeffekte in einer bestimmten Richtung anzuwenden, um Bewegungsunschärfe- und Stricheffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsunschärfe
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 8%
---

# Richtungsunschärfe

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Atomknoten: Richtungsunschärfe](directional-blur.resources/comp_dirmotionblur_1.png "Atomarer Knoten: Richtungsunschärfe"){width="100%"}

<b>In:</b> Atomknoten

</td>
<td style="border: 0;" valign="top">

Wendet Unschärfe in einer bestimmten Richtung gemäß einer Intensitäts-Map an.

Dieser Knoten führt eine Operation ähnlich einer Bewegungsunschärfe an einer Eingabe aus. Im Gegensatz zum regulären Knoten &quot;[Blur](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&quot;, der in allen Richtungen gleichmäßig verschwimmt, funktioniert die &quot;Richtungsunschärfe&quot; entlang eines benutzerdefinierten Winkels.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="directional-blur.resources/directional-blur-tooltip.gif" alt="Richtungsunschärfe-QuickInfo" /></td>
<td style="border: 0; width: 15%"></td>
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
| <b>Intensität</b> *Gleitend* | Legt den Weichzeichnungsradius in Pixel fest. |
| <b>Winkel</b> *Gleitend* | Die Richtung des Weichzeichnereffekts in der Anzahl der Windungen im Uhrzeigersinn, beginnend bei der Horizontalen - d. h. dem Richtungsvektor (1, 0). |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen/Farbe* [PRIMÄR](../../../../glossary/glossary.md) | Das zu verarbeitende Bild. |


## Beispiele

*Demnächst verfügbar.*

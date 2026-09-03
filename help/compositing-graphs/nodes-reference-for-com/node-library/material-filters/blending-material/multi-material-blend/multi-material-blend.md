---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Multi-Material-Überblendung , um mehrere Materialien zusammenzuführen und so komplexe Materialkombinationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Multi-Material-Mischung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# Multi-Material-Mischung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend-01.png){width="128px"}

<b>In:</b> Materialfilter > Mischen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten kombiniert mehrere Materialien basierend auf einer Material-ID-/Farb-ID-Map, eines, das aus einem Gitter gebacken werden kann. Es kann bis zu 16 verschiedene Vollmaterialien aufnehmen, mit allen Kanälen, die Sie in der Gruppe &quot;Kanäle&quot; aktivieren.

Der Knoten ist sehr nützlich beim Texturieren voller Requisiten, da er die vollständige Parametrisierung von Materialien ermöglicht, während er sie alle dynamisch kombiniert. Ideal für die Texturierung einfacher bis komplexer Requisiten, die über korrekte ID-Backs verfügen, oder sogar für die Erstellung vollständig Pipeline-fähiger &quot;Template&quot;-Substance, die sich vollständig an Teamstandards halten.

Beachten Sie, dass bei Verwendung dieser Option Material 1, Steckplatz 1 immer das Standardmaterial ist und überall angezeigt wird, wo kein anderes Material angezeigt wird. Aus diesem Grund können Sie keine Farbe dafür festlegen. Wenn Sie diesen Tresor abspielen möchten, können Sie beispielsweise ein [Basismaterial](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md), das auf grobes Schwarz festgelegt ist, einstecken.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>1-16 Steckplätze für vollständige Material</b> | Die Anzahl der Steckplätze wird durch die Dropdown-Liste <b>Materials</b> bestimmt. |
| <b>Farb-ID</b> <i>Farbeingabe</i> | Kennungszuordnung für vorkompilierte Farben. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Materials</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | Legt die Höchstmenge der verschiedenen Material fest, die überblendet werden sollen. |
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Material 2-16</b> | Für jedes aktivierte Material wird eine Gruppe angezeigt. |
| <b>Farbe</b> <i>(Farbwert)</i> | Die Farbe, die von der ID-Map ausgewählt werden soll, die diesem Material-Steckplatz entspricht. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Anschnitt für Nachbarfarben verwenden. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Härte der Überblendungen: Maskenkontrast. |

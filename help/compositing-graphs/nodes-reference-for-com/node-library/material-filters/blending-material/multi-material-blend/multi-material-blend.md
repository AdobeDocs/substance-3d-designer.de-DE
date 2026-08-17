---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Multi-Material-Mischung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## Multi-Material-Mischung

**In:** *Materialfilter/Füllmethode*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten kombiniert mehrere Materialien basierend auf einer Material-ID-/Farb-ID-Map, eines, das aus einem Gitter gebacken werden kann. Es kann bis zu 16 verschiedene Vollmaterialien aufnehmen, mit allen Kanälen, die Sie in der Gruppe &quot;Kanäle&quot; aktivieren.

Der Knoten ist sehr nützlich beim Texturieren voller Requisiten, da er die vollständige Parametrisierung von Materialien ermöglicht, während er sie alle dynamisch kombiniert. Ideal für die Texturierung einfacher bis komplexer Requisiten, die über korrekte ID-Backs verfügen, oder sogar für die Erstellung vollständig Pipeline-fähiger &quot;Template&quot;-Substance, die sich vollständig an Teamstandards halten.

Beachten Sie, dass bei Verwendung dieser Option Material 1, Steckplatz 1 immer das Standardmaterial ist und überall angezeigt wird, wo kein anderes Material angezeigt wird. Aus diesem Grund können Sie keine Farbe dafür festlegen. Wenn Sie diesen Tresor abspielen möchten, können Sie beispielsweise ein [Basismaterial](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md), das auf grobes Schwarz festgelegt ist, einstecken.

## Parameter

### Eingaben

* **1-16 Steckplätze für gesamtes Material** Die Anzahl der Steckplätze wird durch die Dropdown-Liste **Materialien** bestimmt.
* **Farb-ID**: *Farbeingabe*\
  Kennungszuordnung für vorkompilierte Farben.

### Parameter

* **Materialien**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16* Legt die maximale Menge an verschiedenen Materialien fest, die gemischt werden sollen.
* **Kanäle**\
  Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Material 2-16** Für jedes aktivierte Material wird eine Gruppe angezeigt.
  * **Farbe**: *(Farbwert)*Farbe, die aus der ID-Karte ausgewählt werden soll, die diesem Materialschlitz entspricht.
  * **Unschärfe**: *0.01 - 1.0* Anschnitt in benachbarte Farben.
  * **Auffüllen**: *0.0 - 1.0* Härte von Überblendungen: Maskenkontrast.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

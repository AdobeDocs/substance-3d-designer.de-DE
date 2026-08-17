---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Height-Materialverblend-Knoten, um mehrere Heights auf der Grundlage von Materialzuordnungen zu überblenden und so Materialeffekte mit Ebenen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Height Mischen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Material Height Mischen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## Material Height Mischen

**In:** *Materialfilter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist eine erweiterte Version von [Materialüberblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md), bei der zwei Heights auf der Grundlage ihrer Höhenkarten überblendet werden. Es gibt keine benutzerdefinierte Maske. Sie müssen also zwei Höhenkarten haben, eine für jedes Material, von denen mindestens eine keinen einheitlichen Wert hat.

Dies kann nützlich sein, um zwei verschiedene, hochwertige Materialien ohne eine hochwertige Mischmaske zu kombinieren.

Wenn Sie Wasser oder Schnee einblenden möchten, sind die Snow [Abdeckung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) und [Wasserstand](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) verfügbar.

## Parameter

### Parameter

* **Kanäle**\
  Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Height-Offset**: *0.0 - 1.0* Verschiebt Höhenkarten so, dass der Überblendungsgrad entlang der Achse des Heights verschoben wird. Dies ist die Hauptsteuerung für die Füllmethode.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast der Füllmethode an und sorgt für schärfere Übergänge.
* **Modus**: *Ausgewogenes Height, Priorität des unteren Heights* Wechselt zwischen zwei verschiedenen Füllmethoden.
* **Deckkraft**: *0.0 - 1.0*\
  Füllmethode des Heights im Vordergrund: ein- oder ausblenden.
* **Übereinstimmung der Albedo**: *0.0 - 1.0* Die Anzahl der internen Farbabstimmungen, die zwischen den Albedo ausgeführt werden sollen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

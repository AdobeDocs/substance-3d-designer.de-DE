---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Material Height Mischen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist eine erweiterte Version von [Materialüberblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md), bei der zwei Heights auf der Grundlage ihrer Höhenkarten überblendet werden. Es gibt keine benutzerdefinierte Maske. Sie müssen also zwei Höhenkarten haben, eine für jedes Material, von denen mindestens eine keinen einheitlichen Wert hat.

Dies kann nützlich sein, um zwei verschiedene, hochwertige Materialien ohne eine hochwertige Mischmaske zu kombinieren.

Wenn Sie Wasser oder Schnee einblenden möchten, sind die Snow [Abdeckung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) und [Wasserstand](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) verfügbar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Height-Offset</b> <i>0.0 - 1.0</i> | Versetzt Höhenzuordnungen so, dass der Überblendungsgrad entlang der Achse des Heights verschoben wird. Dies ist die Hauptsteuerung für die Füllmethode. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast der Füllmethode an und sorgt für schärfere Übergänge. |
| <b>Modus</b> <i>Ausgewogenes Height, Priorität des unteren Heights</i> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode des Heights im Vordergrund: ein- oder ausblenden. |
| <b>Übereinstimmung der Albedo </b> <i>0.0 - 1.0</i> | Die Anzahl der internen Farbabstimmungen zwischen Albedo. |

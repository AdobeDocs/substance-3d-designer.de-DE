---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Material Height Überblendung , um mehrere Materialien auf der Grundlage von Höhen-Map zu überblenden, um Materialien mit mehreren Ebenen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Height Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Material Height Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Bei diesem Knoten handelt es sich um eine erweiterte Version von [Height Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md), bei der zwei Material auf der Grundlage ihrer Höhenkarten miteinander vermischt werden. Es gibt keine benutzerdefinierte Maske. Sie müssen also zwei Heightmaps haben, eine für jedes Material, von denen mindestens eine keinen einheitlichen Wert hat.

Dies kann nützlich sein, um zwei verschiedene, hochwertige Materialien ohne eine hochwertige blending mask zu kombinieren.

Wenn Sie Wasser oder Schnee einblenden möchten, sind die Snow [Abdeckung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) und [Wasserstand](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) verfügbar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Material-Kanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanz-Maps anstelle von &quot;Metallic/Rauheit&quot; verwenden. |
| <b>Height-Offset</b> <i>0.0 - 1.0</i> | Versetzt Höhenzuordnungen so, dass der Überblendungsgrad entlang der Achse des Heights verschoben wird. Dies ist die Hauptsteuerung für die Füllmethode. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast der Füllmethode an und sorgt für schärfere Übergänge. |
| <b>Modus</b> <i>Ausgewogenes Height, Priorität des unteren Heights</i> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode des Heights im Vordergrund: ein- oder ausblenden. |
| <b>Übereinstimmung der Albedo </b> <i>0.0 - 1.0</i> | Die Anzahl der internen Farbabstimmungen zwischen Albedo. |

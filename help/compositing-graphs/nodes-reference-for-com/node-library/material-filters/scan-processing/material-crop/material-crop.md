---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Material-Freistellung , um Bereiche der Textur aus gescannten Materialien zuzuschneiden und so bestimmte Interessensbereiche zu isolieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Crop
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Material Crop

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist die Vollversion des mehrkanaligen Materials von [Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Damit können Sie einen Zuschneidevorgang für alle Material-Kanäle gleichzeitig ausführen.

>[!NOTE]
>
> [Weitere Informationen finden Sie im Original ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[Zuschneiden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie Material-Kanäle in dieser Gruppe ein und aus, wenn Sie Specular-/Glanz-Maps anstelle von z. B. Metallic/Rauheit verwenden. |
| <b>Eingabegröße</b> <i>0 - 8192</i> | Eingabebilds Auflösung und Proportionen. Sehr wichtig für nicht quadratische Bilder. |
| <b>Hintergrund</b> <i>(Farbwert) / (Graustufenwert)</i> | Einheitlicher Hintergrundwert für Bereiche, die nicht von der Freistellung abgedeckt sind. |
| <b>Transformieren</b> <i>(Transformationsmatrix)</i> | Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |

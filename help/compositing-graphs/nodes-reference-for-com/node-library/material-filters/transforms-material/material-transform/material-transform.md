---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Materialtransformation", um Transformationen auf Materialausgaben anzuwenden, einschließlich Drehung, Skalierung und Versatz.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialtransformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Materialtransformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>In:</b> Materialfilter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Bei &quot;Materialtransformation&quot; handelt es sich einfach um die &quot;Multi-Channel&quot;-Materialversion von [dem atomaren 2D-Transformationsknoten](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Es transformiert alle Kanäle eines Eingabematerials gleichzeitig mit derselben Schnittstelle wie &quot;2D transformieren&quot;.

Achten Sie nur darauf, die Kanäle richtig einzurichten! Standardmäßig sind &quot;Metallisch/Raueit&quot; und &quot;Specular/Glanz&quot; aktiviert, was zu Verwirrung führen kann.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Transformation</b> <i>(Transformationsmatrix)</i> | Dreht und skaliert das Ergebnis. Das Verschieben/Schwenken erfolgt über den Parameter &quot;Versatz&quot; |
| <b>Offset</b> <i>-0.5 - 0.5</i> | Verschiebt oder verschiebt das Ergebnis. Wenn die Transformationssteuerung vorhanden ist, kann das Ergebnis durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Normales Format</b> | Wählen Sie zwischen DirectX- und OpenGL-Formaten (Grün umkehren). |
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multi Crop", um mehrere Textur-Kanäle gleichzeitig zuzuschneiden und so gescannte Materialien effizient zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrfachzuschnitt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# Mehrfachzuschnitt

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-crop.resources/crop-multi.png){width="128px"}

![](multi-crop.resources/crop-multi-grayscale.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multikanal-Version von &quot;Zuschneiden&quot;. Es schneidet einen Bereich aus einem Bild aus und ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel nach Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel nach Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie im ursprünglichen [Zuschneiden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabeanzahl</b> <i>1 - 8</i> | Legt die Anzahl der parallel zu verarbeitenden Eingaben fest. |
| <b>Eingabegröße</b> <i>0 - 8192</i> | Auflösung und Proportionen von Eingabebilds. Sehr wichtig für nicht quadratische Bilder. |
| <b>Hintergrund</b> <i>(Farbwert) / (Graustufenwert)</i> | Einheitlicher Hintergrundwert für Bereiche, die nicht von der Freistellung abgedeckt sind. |
| <b>Transformieren</b> <i>(Transformationsmatrix)</i> | Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder Kamera bewegt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden. |
| <b>Ist normal (nur für Farbversion)</b> <i>False/True</i> | Gibt an, ob die Eingabe als Normalmap behandelt werden soll. |

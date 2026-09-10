---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Mehrere Winkel zu Albedo", um Albedo-Maps aus gescannten Bildern mit mehreren Winkeln zu extrahieren, um saubere Materialfarben zu erhalten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrere Winkel zur Albedo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Mehrere Winkel zur Albedo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-albedo.resources/multi-angle-to-albedo.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten versucht, Informationen über die gesamte Beleuchtung aus einem Satz von Eingabebildern/Scans zu entfernen, die unter verschiedenen Beleuchtungswinkeln aufgenommen wurden. Es kombiniert alle Samples zu einem einzigen Bild, das so lichtneutral und damit PBR-korrekt wie möglich sein sollte.

Behalte im Hinterkopf: Je mehr Samples du hast und je größer der Unterschied im Beleuchtungswinkel ist, desto größer ist der Erfolg, den du erzielst. Ab vier Proben sollte es möglich sein, je nach Eingabebildern nahezu perfekte Ergebnisse zu erzielen. Eingabebilder sollten mit einem Stativ aufgenommen werden und minimale oder idealerweise sogar keine Unterschiede aufweisen, außer bei Beleuchtung aus einem anderen Winkel!

>[!NOTE]
>
> Weitere Informationen zur Normalmap-Version dieses Knotens finden Sie unter [Mehrwinkel zu Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md). Wenn Sie Ihre Eingaben vorverarbeiten möchten, können [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) und [Multi Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) hilfreich sein, da sie mit diesen Knoten kombiniert werden sollen.
> 
> [Der Blogpost &quot;Ihr Smartphone ist ein Materialscanner&quot; veranschaulicht diesen Prozess etwas besser.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1-8</b> <i>Farbeingabe</i> | Die Anzahl der Eingaben wird durch den Parameter Samples Amount bestimmt. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Beispielbetrag</b> <i>2 - 8</i> | Legt die Anzahl der Samples (Eingaben) fest, die bei der Verarbeitung verwendet werden sollen. |

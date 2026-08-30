---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "HDR-Zusammenfügung", um mehrere HDR-Bilder zu einem einzigen Panorama zusammenzufügen und so zusammengesetzte Umgebungszuordnungen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HDR verbinden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# HDR verbinden

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Kombiniere mehrere Belichtungen zu einer High Dynamic Range. Der erste Eingang ist das am stärksten unterbelichtete Bild.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1-16</b> <i>Farbeingabe</i> | Eingabebilder. Die verfügbare Menge hängt vom Parameter ab. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingaben</b> <i>2 - 16</i> | Legt die Menge der verfügbaren Eingaben fest. |
| <b>Belichtungsdelta (EV)</b> <i>0.0 - 4.0</i> | Legt den Belichtungsunterschied fest, der zwischen Bildern interpretiert werden soll. |
| <b>Weißpunkt</b> <i>0.0 - 13.0</i> | Mit dem Weißpunkt kannst du das Endergebnis weiter anpassen. |

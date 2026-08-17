---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Hald CLUT, um Farbtabellen mit dem Format Hald CLUT für Farbkorrektur und -abstufung anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## Hald CLUT

**In:** *Filter/Korrekturen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Wendet eine LUT auf das Eingabebild an. Die LUT muss im Hald-Format mit einer Auflösung von 4096\*4096 vorliegen. Weitere Informationen finden Sie unter <http://www.quelsolaar.com/technology/clut.html>.

### Eingaben

* **Eingabe**: *Farbeingabe*\
  Bild, auf das die LUT angewendet werden soll.
* **lut**: *Farbeingang* Lut-Eingangssteckplatz. Muss 4096x4096 sein.

## Parameter

* **LUT-Intensität nach Alpha**: *Falsch/Wahr* Definiert, ob der LUT-Effekt durch den Alphakanal gewichtet wird.

Beispiele

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>

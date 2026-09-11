---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Verlauf radial , um radiale Farbverläufe zu erstellen, die von einem Mittelpunkt für kreisförmige Farbübergänge ausstrahlen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Radialer Verlauf
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# Radialer Verlauf

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial.png){width="128px"}

<b>In:</b> Texturen > Muster generieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ähnlich wie [Verlaufskreis](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md) erstellt einen Graustufenverlaufsübergang, der durch zwei benutzerdefinierte Punkte in radialer Weise definiert wird. Die Überblendung erfolgt von a nach b, definiert durch Mittelpunkt und Radius. Denke daran, dass die Ergebnisse nicht immer kacheln.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Form</b> <i>Kegel, Hemisphäre</i> | Bestimmt das Überblendungsprofil. Kegel ist ein scharfer, gerader Übergang, Halbkugel ist weich und in der Mitte abgerundet. |
| <b>Punkt 1</b> | Mittelpunkt des Farbverlaufs. Beginnt weiß. |
| <b>Punkt 2</b> | Radiuspunkt zum Bestimmen des Verlaufsumfangs. Endet schwarz. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Aktivieren Sie die Kompensation von Squash und dehn mit nicht quadratischen Verhältnissen. |

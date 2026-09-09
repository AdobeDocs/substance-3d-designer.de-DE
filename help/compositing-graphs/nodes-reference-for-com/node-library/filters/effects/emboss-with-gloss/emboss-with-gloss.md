---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Relief mit Glanz, um Reliefeffekte mit Glanzmasken zu erstellen, um Texturen Tiefe und Glanz zu verleihen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Relief mit Glanz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# Relief mit Glanz

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Prägeeffekt mit hinzugefügtem Glanz (Specular-Reflexion) auf eine Farb- und Height-Eingabe durch. Fügt einem Height im Wesentlichen eine gefälschte, Baking geführt Beleuchtung auf der Grundlage von Bildinformationen hinzu. Nützlich für einige Texturierungsstile, bei denen die Beleuchtung in die Texturen Baking geführt werden muss.

Eine Version mit weiteren Optionen finden Sie unter [Uber Relief](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md). Es gibt auch die einfachere, atomare Version von [Relief](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Farbe</b> <i>Farbeingabe</i> |  |
| <b>Height</b> <i>Graustufen-Eingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Markierungsfarbe</b> <i>(Farbwert)</i> | Die Farbe des Specular-Lichts. |
| <b>Schattenfarbe</b> <i>(Farbwert)</i> | Farbe, die in schattierten/unbeleuchteten Bereichen verwendet wird. |
| <b>Glanz</b> <i>0.0 - 0.5</i> | Hervorhebungsgröße des Glanzes. |
| <b>Intensität</b> <i>0.0 - 10.0</i> | Intensität der Markierung. |
| <b>Lichtwinkel</b> <i>0.0 - 1.0</i> | Einfallswinkel des (gefälschten) Lichts. |

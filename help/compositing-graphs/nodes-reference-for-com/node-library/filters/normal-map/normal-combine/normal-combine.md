---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal kombinieren , um mehrere Normalmaps zu kombinieren und so Oberflächendetails und -details zu überlagern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Kombination
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Normale Kombination

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

<b>In:</b> Filters > Normal map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Normal kombinieren kombiniert die Details zweier normaler Maps auf mathematisch korrekte Weise.

Es ähnelt der bekannten &quot;Overlay&quot;-Methode anderer 2D-Bildbearbeitungssoftware, funktioniert aber intern etwas anders (drei Optionen).

</td>
</tr>
</table>

Dies ist die beste und richtige Methode, um 2D-generierte Normalmap-Details zu einer durch Baking erzeugte Map hinzuzufügen.

Wenn Sie zwei normale Maps überblenden möchten, ohne ihre Details zu kombinieren (z. B. mit einer Maske), sollten Sie [Normale Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md) verwenden.

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normal 2</b> <i>Farbe</i> | Beschreibung |
| <b>Normal 1</b> <i>Farbe</i> | Beschreibung |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Technik</b> *Integer* | Legt fest, welche interne Mischtechnik verwendet werden soll, wobei die Geschwindigkeit auf Qualität gesetzt wird.<br><br>*- Whiteout (niedrige Qualität)<br>* Kanalmixer (hohe Qualität)<br>* Detailorientiert (hohe Qualität)* |

## Beispiele

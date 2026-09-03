---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal kombinieren , um mehrere Normalen-Map zu kombinieren, um Oberflächendetails und -details zu schichten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale Kombination
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Normale Kombination

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine-01.png){width="128px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Normal kombinieren kombiniert die Details zweier Normalen-Map auf mathematisch korrekte Weise.

Es ähnelt der bekannten &quot;Overlay&quot;-Methode anderer 2D-Bildbearbeitungssoftware, funktioniert aber intern etwas anders (drei Optionen).

</td>
</tr>
</table>

Auf diese Weise lassen sich 2D-generierte Normalen-Map-Details am besten und am besten zu einer durch Baking erzeugte Map hinzufügen.

Wenn Sie zwei Normalen-Map überblenden möchten, ohne ihre Details zu kombinieren (z. B. mithilfe einer Maske), sollten Sie [Normale Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md) verwenden.

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
| <b>Technik</b> *Ganzzahl* | Legt fest, welche interne Mischtechnik verwendet werden soll, wobei die Geschwindigkeit auf Qualität gesetzt wird.<br><br>*- Whiteout (niedrige Qualität)<br>* Kanalmixer (hohe Qualität)<br>* Detailorientiert (hohe Qualität)* |

## Beispiele

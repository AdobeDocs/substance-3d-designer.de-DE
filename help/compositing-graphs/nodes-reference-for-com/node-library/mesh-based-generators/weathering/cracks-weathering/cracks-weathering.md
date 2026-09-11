---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Risse Verwitterung , um Rissmuster zu Materialien hinzuzufügen, die auf der Krümmung des Meshs und den Belastungspunkten basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risse Verwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Risse Verwitterung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Verwitterung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Effekt mit vollem Material, der auf mehreren Kanälen gleichzeitig funktioniert. Es fügt ein zufälliges Rissmuster hinzu, mit Kontrolle über Ausbreitung und Tiefe.

Vergewissern Sie sich, dass Sie die [Link Creation Modes](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) richtig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Baking geführt oder generierte Map, die für interne Effekte und Maskierung verwendet wird. |
| <b>Height</b> <i>Graustufen-Eingabe</i> | Baking geführt oder generierte Map, die für interne Effekte und Maskierung verwendet wird. |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Material-Kanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanz-Maps anstelle von &quot;Metallic/Rauheit&quot; verwenden. |
| <b>Erweitert</b> |  |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Maske</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |
| <b>Effekt</b> |  |
| <b>Risse-Propagierung</b> <i>0.0 - 1.0</i> | Wie weit sollten sich die Risse ausbreiten? Dies ist die Hauptsteuerung für diesen Effekt. |
| <b>Risse Tiefe</b> <i>0.0 - 1.0</i> | Tiefe des Risseffekts. Dies wirkt sich hauptsächlich auf das Height und geringfügig auf die visuelle Thickness aus. |
| <b>Überblenden</b> | Steuert, wie stark der Effekt in die einzelnen resultierenden Kanäle übergeht. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-ex.gif" />
        </td>
    </tr>
</table>

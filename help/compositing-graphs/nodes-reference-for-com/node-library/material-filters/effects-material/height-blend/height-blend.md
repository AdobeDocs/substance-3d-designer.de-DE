---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Height-Überblendung", um Texturen auf der Grundlage von Height-Maps zu überblenden und realistische Materialübergänge zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height-Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Height-Überblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Kombiniert zwei Höhenkarten basierend auf ihren Height-Informationen. Generiert eine überblendete Höhenkarte, aber auch eine Schwarzweiß-Maske, die an anderer Stelle verwendet werden kann.

Dies ist nützlich, wenn Sie zwei hochwertige Höhenkarten kombinieren müssen, aber nicht unbedingt ein vollständiges Height, wie es für [Materialmaterialüberblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md) erforderlich ist.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Height Top</b> <i>Graustufen-Eingabe</i> |  |
| <b>Height unten</b> <i>Graustufen-Eingabe</i> |  |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Height-Offset</b> <i>0.0 - 1.0</i> | Versetzt Höhenzuordnungen so, dass der Überblendungsgrad entlang der Achse des Heights verschoben wird. Dies ist die Hauptsteuerung für die Füllmethode. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast der Füllmethode an und sorgt für schärfere Übergänge. |
| <b>Modus</b> <i>Ausgewogenes Height, Priorität des unteren Heights</i> |  |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Füllmethode des Heights im Vordergrund: ein- oder ausblenden. |

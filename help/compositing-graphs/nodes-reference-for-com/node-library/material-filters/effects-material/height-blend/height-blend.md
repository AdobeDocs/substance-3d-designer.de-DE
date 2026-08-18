---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Height-Überblendung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Height-Überblendung

**In:** *Materialfilter/Effekte*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Kombiniert zwei Höhenkarten basierend auf ihren Height-Informationen. Generiert eine überblendete Höhenkarte, aber auch eine Schwarzweiß-Maske, die an anderer Stelle verwendet werden kann.

Dies ist nützlich, wenn Sie zwei hochwertige Höhenkarten kombinieren müssen, aber nicht unbedingt ein vollständiges Height, wie es für [Materialmaterialüberblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md) erforderlich ist.

## Parameter

### Eingaben

* **Height Top**: *Graustufen-Eingabe*
* **Height unten**: *Graustufen-Eingabe*
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Height-Offset**: *0.0 - 1.0* Verschiebt Höhenkarten so, dass der Überblendungsgrad entlang der Achse des Heights verschoben wird. Dies ist die Hauptsteuerung für die Füllmethode.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast der Füllmethode an und sorgt für schärfere Übergänge.
* **Modus**: *Ausgewogenes Height, Priorität des unteren Heights* Wechselt zwischen zwei verschiedenen Füllmethoden.
* **Deckkraft**: *0.0 - 1.0*\
  Füllmethode des Heights im Vordergrund: ein- oder ausblenden.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

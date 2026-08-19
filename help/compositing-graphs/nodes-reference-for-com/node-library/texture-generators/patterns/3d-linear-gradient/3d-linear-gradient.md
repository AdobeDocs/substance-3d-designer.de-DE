---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D Linear gradient, um lineare Farbverläufe zu erstellen, die auf der 3D-Weltposition für räumliche Effekte basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D Linear gradient

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erstellt einen volumetrischen Farbverlauf basierend auf der Eingabe-Positions-Map. Erzeugt im 3D-Raum effektiv einen Übergang von Schwarz zu Weiß zwischen 2 Punkten. Wird nur für die Verwendung mit der GPU-Engine konzipiert.

Siehe auch [3D-Volumenmaske](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) für einen ähnlichen Effekt.

## Parameter

* **Punktpositionsmodus**: *UV-Positionen, Weltraumpositionen* Wählen Sie aus, ob die Verlaufspunkte im UV-Raum (funktioniert am besten, wenn sie in der 2D-Ansicht eingestellt werden) oder in 3D-Koordinaten funktionieren, wenn Sie manuell eine exakte Position eingeben möchten.
* **Punkt 1**:\
  Startpunkt des Verlaufs. Kann 2D- oder 3D-Koordinaten basierend auf dem Positionsmodus sein.
* **Punkt 2**:\
  Endpunkt des Verlaufs. Kann 2D- oder 3D-Koordinaten basierend auf dem Positionsmodus sein.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.

## Beispielbilder

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>

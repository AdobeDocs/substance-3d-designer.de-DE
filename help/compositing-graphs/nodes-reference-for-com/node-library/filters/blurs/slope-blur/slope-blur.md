---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Steigung-Weichzeichner-Knoten, um Richtungsunschärfeeffekte anzuwenden, die auf Height-Map-Steigungen zum Erstellen von Bewegungsunschärfe basieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Steigung weichzeichnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# Steigung weichzeichnen

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## Steigung weichzeichnen (Graustufen)

**In:** *Filter/Unschärfen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt einen erweiterten, qualitativ hochwertigen Weichzeichner durch, bei dem die Anisotropie/Richtung durch eine Graustufen-&quot;Steigung Map&quot; gesteuert wird. Stellen Sie sich den Effekt &quot;Steigung-Weichzeichner&quot; nach den Steigungen Ihrer Steigung-Map als Höhenkarte vor, ähnlich wie [Richtungsverkrümmung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (auf der intern basiert).

Das ist einer der interessantesten und mächtigsten Weichzeichner in Designer. Es kann verwendet werden, um einige sehr interessante und unerwartete Effekte zu erzielen, wie z. B. Splittern und Verwittern von Kanten oder Verschmieren und Lecken von Dirt oder Rost.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Steigung-Weichzeichner&quot; für Farbeingaben bzw. &quot;Steigung-Weichzeichner-Graustufen&quot; für Graustufeneingaben.

## Parameter

### Eingaben

* **Steigung**: *GrayScale-Eingabe* Steigung-Map zum Ansteuerungswinkel der Anisotropie. sollte idealerweise geneigte Farbverläufe enthalten; harte, scharfe Übergänge werden nicht gut funktionieren!

### Parameter

* **Beispiele**: *0 - 32* Die Anzahl der Samples beeinflusst die Qualität auf Kosten der Geschwindigkeit.
* **Intensität**: *0.0 - 16.0*\
  Weichzeichnungsgrad oder -stärke.
* **Modus**: *Weichzeichnen, Min, Max*|\
  Füllmethode für nachfolgende Weichzeichnungspässe. &quot;Weichzeichnen&quot; verhält sich eher wie ein standardmäßiger [Anisotroper Weichzeichner](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), während Min vorhandene Bereiche &quot;wegfrisst&quot; und Max weiße Bereiche &quot;wegschmiert&quot;.

## Beispielbilder

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>

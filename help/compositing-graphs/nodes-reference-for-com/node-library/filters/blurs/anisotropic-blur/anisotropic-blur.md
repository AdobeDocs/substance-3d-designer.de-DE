---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Anisotropischer Weichzeichner , um Richtungsunschärfeeffekte zum Erstellen von Bewegungsunschärfe- und Stricheffekten anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anisotropischer Weichzeichner
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# Anisotropischer Weichzeichner

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## Anisotropischer Weichzeichner (Graustufen)

**In:** *Filter/Unschärfen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt eine qualitativ hochwertige [Richtungsunschärfe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) durch, mit einigen Einstellungen zum Anpassen des Erscheinungsbilds. Auch bekannt als &quot;Bewegungsunschärfe&quot;.

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Anisotropischer Weichzeichner&quot; für Farbeingaben bzw. &quot;Anisotropischer Weichzeichner, Graustufen&quot; für Graustufeneingaben.

## Parameter

* **Intensität**: *0.0 - 16.0* Stärke (Radius) der Weichzeichnung. Je höher dieser Wert ist, desto weiter reicht die Weichzeichnung.
* **Anisotropie**: *0.0 - 1.0* Richtung der Weichzeichnung. Der Wert 0,0 entspricht dem normalen Weichzeichnen.
* **Winkel**: *0.0 - 1.0* Legt den Winkel für die Weichzeichnungsrichtung fest.
* **Qualität**: *0 - 1* Wechselt intern zwischen einer [Box-Weichzeichnung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) und einer HQ-Weichzeichnung. Schneller Trading für Qualität.

## Beispielbilder

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Dust", um Dust-Akkumulationsmasken auf der Grundlage der Gittergeometrie zu generieren, um realistische Dust- und Rastereffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt die Dust dar, die sich in verdeckten, abgesenkten Bereichen angesammelt hat, sowie nur in Bereichen, die nach oben zeigen. Erfordert ordnungsgemäße gebackene AO und World Space Normale, um zu arbeiten.

## Parameter

### Eingaben

* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für die Platzierung der Dust. Erforderlich!
* **Normaler Weltraum**: *Farbeingabe*\
  Durch Baking erzeugte Map für die Platzierung der Dust. Erforderlich!
* **Rauschen**: *Graustufen-Eingabe*\
  Benutzerdefinierte Düste-Map (optional) wird nur angezeigt, wenn &quot;Rauschen überschreiben&quot; auf &quot;True&quot; festgelegt ist.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Gesamtmenge der Dust fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast der Dust an.
* **Verdeckung**: *0.0 - 1.0* Legt den Einfluss von AO fest; mehr Dust wird in verdeckten Bereichen erscheinen.
* **Rauschdeckkraft**: *0.0 - 1.0* Legt die Menge an Rauschen fest, die in staubigen Bereichen sichtbar ist.
* **Rauschen überschreiben**: *Falsch/Wahr* Einstellung zur Verwendung der benutzerdefinierten Düste-Map-Eingabe.

## Beispielbilder

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>

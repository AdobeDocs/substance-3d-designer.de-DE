---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: Verwenden Sie den Mischknoten "Farbig nachbelichten", um Texturen abzudunkeln, indem Sie den Kontrast erhöhen, um Schatten- und Nachbelichtungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbig nachbelichten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Farbig nachbelichten

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## Farbig nachbelichten

**In:** *Filters/Blending*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt einen Farbig-Nachbelichtungsübergang zwischen Vorder- und Hintergrund durch. Mathematisch ist die Formel 1 - (1-Hintergrund) / Vordergrund.

## Parameter

### Eingaben

* **Vordergrund**: *Farbeingabe*
* **Hintergrund**: *Farbeingabe*
* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Deckkraft**: *0.0 - 1.0*\
  Füllmethode Deckkraft zwischen Vorder- und Hintergrund.
* **Alpha-Überblendung**: *False/True*\
  Blendet die Alphakanäle für Vorder- und Hintergrund ein bzw. aus. Wenn der Wert auf &quot;Falsch&quot; gesetzt ist, wird der Alphakanal des Vordergrunds ignoriert.

## Beispielbilder

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Unten nach oben", um Verlaufsmasken von unten nach oben basierend auf der Gitterweltposition zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Von unten nach oben
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# Von unten nach oben

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## Von unten nach oben

**In:** *Mesh-basierte Generatoren/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/features/smart-materials-and-masks) in [Painter](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/home).

Dadurch wird ein weißer bis schwarzer Übergang vom unteren zum oberen Rand eines Modells erzeugt. Das ist nützlich, um geometriebasierte Abweichungen und Auswahlen vorzunehmen.

## Parameter

### Eingaben

* **Position**: *Farbeingabe*\
  Backed-Positions-Map. Erforderlich!
* **Raueit:** *Graustufeneingabe*\
  Dies hat nichts mit der PBR-Raueit zu tun, sondern ist eine (optionale) Variationskarte, um die Überblendung aufzubrechen. Wird nur angezeigt, wenn &quot;Raueit&quot; höher als 0 eingestellt ist.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Verschiebt die durchschnittliche Stufe des Ergebnisses zwischen Schwarz und Weiß, wie bei einer Helligkeitsanpassung.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast der Überblendung an.
* **Raueit\_Variation**: *0.0 - 1.0* Bestimmt den Umfang der Rauigkeitsabbildung, die zur Variation eingeblendet werden soll. Wenn Sie diesen Wert auf über 0 erhöhen, wird der Kartenschlitz angezeigt.

## Beispielbilder

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>

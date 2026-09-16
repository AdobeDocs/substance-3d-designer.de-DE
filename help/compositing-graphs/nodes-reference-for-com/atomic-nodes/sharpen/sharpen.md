---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: Mit dem Knoten "Scharf stellen" können Sie die Textur und Kanten verbessern, um gestochen scharfe, definierte Oberflächendetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scharfzeichnen
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# Scharfzeichnen

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Knotensymbol schärfen](sharpen.resources/sharpen-4.png "Knotensymbol schärfen")

<b>In:</b> Elementare Knoten

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Der Scharfzeichnungsknoten führt einen Scharfzeichnungsvorgang an einer Eingabe durch. Dieser Knoten ist nützlich, um einem Bild den letzten Schliff zu verleihen.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="sharpen.resources/sharpen-tooltip.gif" alt="QuickInfo schärfen" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Sie ähnelt mathematisch sehr der Unscharf-Maske von Photoshop, obwohl der Name anders lautet. Er eignet sich gut für Grundfarbenkarten, sollte aber auf Karten wie Normalen-Map und Metallic Karten vermieden werden.

## Eingaben

<b>Eingabe</b> *Farbe/Graustufen* (Primär)\
Das Bild, das geschärft werden soll.

## Parameter

<b>Intensität</b> *Fließkommazahl*\
Legt die Intensität des Scharfzeichnungseffekts fest.

<b>Punchthrough-Alpha</b> *Boolesche Wert* (verfügbar, wenn ein Farbbild mit dem <b>Eingang</b> verbunden ist)\
Legt fest, ob der Alphakanal des Bildes geschärft oder unverändert bleiben soll.

## Beispiele

![Scharfzeichnungsknoten - Beispiel 1](sharpen.resources/sharpen-ex.png "Scharfzeichnungsknoten - Beispiel 1")

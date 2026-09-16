---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Scharf stellen , um die Strukturdetails und Kanten zu verbessern und gestochen scharfe, definierte Oberflächendetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scharfzeichnen
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# Scharfzeichnen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol schärfen](sharpen.resources/sharpen-4.png "Knotensymbol schärfen"){width="20%"}

<b>In:</b> Atomknoten

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Scharfzeichnungsknoten führt einen Scharfzeichnungsvorgang an einer Eingabe durch. Dieser Knoten ist nützlich, um einem Bild den letzten Schliff zu verleihen.

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="sharpen.resources/sharpen-tooltip.gif" alt="QuickInfo schärfen" /></div>

Sie ähnelt mathematisch sehr der Unscharf-Maske von Photoshop, obwohl der Name anders lautet. Es eignet sich gut für Grundfarben-Maps, sollte aber auf Karten wie &quot;Normal&quot;-Maps und &quot;Metallic&quot;-Maps vermieden werden.

## Eingaben

<b>Eingabe</b> *Farbe/Graustufen* (Primär)\
Das Bild, das geschärft werden soll.

## Parameter

<b>Intensität</b> *Gleitend*\
Legt die Intensität des Scharfzeichnungseffekts fest.

<b>Punchthrough-Alpha</b> *Boolean* (verfügbar, wenn ein Farbbild mit der <b>Eingabe</b> verbunden ist)\
Legt fest, ob der Alphakanal des Bildes geschärft oder unverändert bleiben soll.

## Beispiele

![Scharfzeichnungsknoten - Beispiel 1](sharpen.resources/sharpen-ex.png "Scharfzeichnungsknoten - Beispiel 1")

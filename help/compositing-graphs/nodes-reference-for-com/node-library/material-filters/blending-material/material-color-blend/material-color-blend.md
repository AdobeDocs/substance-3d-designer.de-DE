---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialfarben-Überblendung , um Farbkanäle zwischen Materialien zu überblenden und so zusammengesetzte Materialeffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialfarben-Überblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Materialfarben-Überblendung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## Materialfarben-Überblendung

**In:** *Materialfilter/Füllmethode*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ermöglicht Anpassungen an einem Multi-Channel-Vollmaterial, indem Volltonfarben oben vermischt werden. Dies ist der Hauptunterschied zu [Materialanpassungsüberblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), die nur [Tonwertkorrekturen](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) an Kanälen zulässt, während dieser Knoten [Anpassungen vom Typ &quot;Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)&quot; mit einer Volltonfarbe verwendet.

Dieser Knoten ist am nützlichsten, wenn Sie entweder einen flachen Farbhinweis in die Diffuse- oder Grundfarbe einfügen möchten oder andere Kanäle mithilfe eines festgelegten Werts für die Volltonfarbe &quot;glätten&quot; möchten.

## Parameter

### Eingaben

* **ColorID**: *Farbeingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Graustufenmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, wenn Sie z. B. Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Diffus**
  * **Farbe**: *(Farbwert)*Der Farbwert, der über dem Diffuse-Kanal überblendet werden soll.
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode Deckkraft zwischen Vorder- und Hintergrund.
  * **Füllmethode**: *Normal, Addieren, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch* Füllmethode zur Verwendung im Vorgang.
* **Grundfarbe**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Normal**
  * **Quelle**: *Height, Maske*
  * **Füllmethode**: *Zusammenführen, Überblenden*
  * **Height-Intensität**: *0.0 - 1.0*
  * **Deckkraft des Heights**: *0.0 - 1.0*
  * **Format**: *DirectX, OpenGL*
* **Specular**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Ausstrahlend**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Glossarität**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Raueit**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Metallisch**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Specular level**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Umgebungs-Verdeckung**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Height**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Deckkraft**
  * Mischt eine Volltonfarbe über diesem Kanal mit Optionen wie in der Gruppe &quot;Diffus&quot;.
* **Farb-ID-Maske**: *Falsch/Wahr* Verwenden Sie Farb-ID-Maske anstelle der Graustufenmaske. Beachten Sie, dass dies nur für eine Farbe ist!\
  Aktiviert alle folgenden Optionen.
* **Farbe**: *(Farbwert)*Welche Farbe ausgewählt und in Weiß konvertiert werden soll.
* **Unschärfe**: *0.01 - 1.0* Der Umfang, in dem die von Ihnen ausgewählte Farbe in ihre Nachbarfarben übergeht.
* **Auffüllen**: *0.0 - 1.0*&#x200B;Übergangskontrast der ausgewählten Farbe.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

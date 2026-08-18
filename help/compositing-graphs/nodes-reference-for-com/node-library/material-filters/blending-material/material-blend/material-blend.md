---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialüberblendung , um ganze Materialien mithilfe von Masken zusammenzufügen und so zusammengesetzte Materialeffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialüberblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Materialüberblendung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## Materialüberblendung

**In:** *Materialfilter/Füllmethode*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Materialüberblendung ist das mehrkanalige vollständige Materialäquivalent von [dem atomaren Überblendknoten](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Es fügt sich zwischen zwei Vollmaterialien ein (alle möglichen Kanäle), basierend auf einer Graustufenmaske, oder optional basierend auf einer einzigen Farbe aus einer Farb-ID-Maske.

Dieser Knoten ist nützlich, wenn Sie zwei Materialien überblenden und eine Graustufenzuordnung haben möchten, aber keine vollständige Farb-ID eingebrannt werden soll. Wenn Sie über eine Farb-ID verfügen und mehr als zwei Materialien überblenden möchten, empfehlen wir Ihnen, [Mehrematerial-Überblendung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) zu verwenden.

## Parameter

### Eingaben

* **ColorID**: *Farbeingabe*\
  Optionale Kennungszuordnung für vordefinierte Farben.
* **Graustufenmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, wenn Sie z. B. Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Diffus**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Grundfarbe**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Normal**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
* **Specular**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Ausstrahlend**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Glossarität**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Raueit**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Metallisch**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Specular level**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Umgebungs-Verdeckung**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Height**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Deckkraft**
  * **Deckkraft**: *0.0 - 1.0*\
    Füllmethode zwischen Vorder- und Hintergrund
  * **Füllmethode**: *Normal, Hinzufügen, Subtrahieren, Multiplizieren, Addieren/Sub, Max, Min, Switch*
* **Farb-ID-Maske**: *Falsch/Wahr* Verwenden Sie Farb-ID-Maske anstelle der Graustufenmaske. Beachten Sie, dass dies nur für eine Farbe ist!
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

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Mehrere Winkel zu Normal", um aus gescannten Bildern mit mehreren Winkeln Normalzuordnungen für präzise Oberflächendetails zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrere Winkel zu Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# Mehrere Winkel zu Normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-normal.png){width="128px"}

## Mehrere Winkel zu Normal

**In:** *Materialfilter/Scanverarbeitung*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten erstellt eine Normalmap aus einer Reihe von Fotos/Scans, die unter verschiedenen Lichtverhältnissen erstellt wurden. Es ermöglicht eine viel präzisere Normmap-Konvertierung als beim Versuch, Normale aus einer einzigen Albedo zu extrahieren.

Es ist komplizierter als [Mehrwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), da Sie für Ihre Eingaben festgelegte, präzise Lichtwinkel verwenden müssen. Der Beleuchtungswinkel jedes Musters sollte gleichmäßig verteilt sein, und die Muster müssen nacheinander eingegeben werden. Bei drei Proben sollte der Lichtwinkel wie folgt gewählt werden: 0, 120, 240 - oder ein beliebiger gleichmäßiger Versatz davon (z. B. 90, 210, 330).

>[!NOTE]
>
> Weitere Informationen zur Albedo dieses Knotens finden Sie unter [Mehrwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md). Wenn Sie Ihre Eingaben vorverarbeiten möchten, können [Multi-Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi-Zuschnitt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) und [Multi-Clone-Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) von Nutzen sein, da sie mit diesen Knoten kombiniert werden sollen.

## Parameter

### Eingaben

* **Eingabe 1-8**: *Farbeingabe*

### Parameter

* **Normales Format**: *DirectX, OpenGL*\
  Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
* **Beispielbetrag**: *2 - 8* Legt die Anzahl der zu verarbeitenden Samples (Eingaben) fest.
* **Intensität**: *0.0 - 1.0* Legt die Intensität der Normalmap fest.
* **Lichtwinkel der ersten Probe**: *0.0 - 360.0* Legt die Beleuchtungswinkelrichtung der ersten Eingabe fest.
* **Nächster Beispiellichtwinkel**: *Gegen den Uhrzeigersinn, gegen den Uhrzeigersinn* Legt fest, in welche Richtung sich die Beleuchtung im nächsten Sample bewegt.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

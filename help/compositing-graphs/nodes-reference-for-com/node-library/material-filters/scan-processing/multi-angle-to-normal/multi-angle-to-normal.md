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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# Mehrere Winkel zu Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal-01.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten erstellt eine Normalmap aus einer Reihe von Fotos/Scans, die unter verschiedenen Lichtverhältnissen erstellt wurden. Es ermöglicht eine viel präzisere Normmap-Konvertierung als beim Versuch, Normale aus einer einzigen Albedo zu extrahieren.

Es ist komplizierter als [Mehrwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), da Sie für Ihre Eingaben festgelegte, präzise Lichtwinkel verwenden müssen. Der Beleuchtungswinkel jedes Musters sollte gleichmäßig verteilt sein, und die Muster müssen nacheinander eingegeben werden. Bei drei Proben sollte der Lichtwinkel wie folgt gewählt werden: 0, 120, 240 - oder ein beliebiger gleichmäßiger Versatz davon (z. B. 90, 210, 330).

>[!NOTE]
>
> Weitere Informationen zur Albedo dieses Knotens finden Sie unter [Mehrwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md). Wenn Sie Ihre Eingaben vorverarbeiten möchten, können [Multi-Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi-Zuschnitt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) und [Multi-Clone-Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) von Nutzen sein, da sie mit diesen Knoten kombiniert werden sollen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1-8</b> <i>Farbeingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Beispielbetrag</b> <i>2 - 8</i> | Legt die Anzahl der zu verarbeitenden Samples (Eingaben) fest. |
| <b>Intensität</b> <i>0.0 - 1.0</i> | Legt die normale Intensität der Karte fest. |
| <b>Lichtwinkel der ersten Probe</b> <i>0.0 - 360.0</i> | Legt die Beleuchtungswinkelrichtung der ersten Eingabe fest. |
| <b>Nächster Beispiellichtwinkel</b> <i>Gegen den Uhrzeigersinn, im Uhrzeigersinn</i> | Legt fest, in welche Richtung sich die Beleuchtung im nächsten Sample bewegt. |

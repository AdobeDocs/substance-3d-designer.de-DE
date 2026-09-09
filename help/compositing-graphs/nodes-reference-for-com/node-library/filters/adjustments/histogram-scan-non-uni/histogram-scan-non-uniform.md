---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Histogramm Scan Non-Uniform (Histogramm scannen ohne Uniform), um ein ungleichmäßiges Histogramm zur erweiterten Farbkorrektur zu scannen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramm Scan ungleichmäßig
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Histogramm Scan ungleichmäßig

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erweiterte Version von [Histogramm-Scan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) mit zusätzlichen Steuerelementen und Eingabemechanismen, um den Effekt auf Pixelebene zu steuern, anstatt einheitlich über das gesamte Bild hinweg. Kann verwendet werden, um noch komplexere Kontrast- und Überblendungen in Masken zu erzielen.

Die Verwendung ist wesentlich komplexer als die normale [Histogrammprüfung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md). Stellen Sie daher sicher, dass Sie mit dieser Methode vertraut sind, bevor Sie versuchen, die nicht einheitliche Version zu verwenden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen-Eingabe</i> | Quellergebnis, das geändert werden soll. |
| <b>Positionszuordnung</b> <i>Graustufen-Eingabe</i> | Eingangssteckplatz zum Ansteuern des Positionsparameters. Aktiviert, wenn &quot;Positionseingabe verwenden&quot; auf &quot;True&quot; gesetzt ist. Der effektive Wertebereich ist klein und hängt von der Kontrastkarte und den Einstellungen ab. |
| <b>Kontrastkarte</b> <i>Graustufen-Eingabe</i> | Eingangssteckplatz zur Steuerung des Kontrastparameters. Aktiviert, wenn &quot;Kontrasteingabe verwenden&quot; auf &quot;True&quot; gesetzt ist. Der effektive Wertebereich ist klein. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Positionseingabe verwenden</b> <i>False/True</i> | Umschalten der Verwendung des Positionszuordnungs-Eingangssteckplatzes. |
| <b>Position</b> <i>0.0 - 1.0</i> | Steuert oder ändert die Kartenergebnisse, um die Positionseinstellung zu steuern. |
| <b>Kontrasteingabe verwenden</b> <i>False/True</i> | Umschalten der Verwendung des Kontrastzuordnungs-Eingangssteckplatzes. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Steuert oder ändert die Kartenergebnisse, um die Kontrasteinstellung zu steuern. |

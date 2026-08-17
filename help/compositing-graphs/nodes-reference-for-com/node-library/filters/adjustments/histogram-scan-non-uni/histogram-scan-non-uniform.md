---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# Histogramm Scan ungleichmäßig

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## Histogramm Scan ungleichmäßig

**In:** *Filter/Korrekturen*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erweiterte Version von [Histogramm-Scan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) mit zusätzlichen Steuerelementen und Eingabemechanismen, um den Effekt auf Pixelebene zu steuern, anstatt einheitlich über das gesamte Bild hinweg. Kann verwendet werden, um noch komplexere Kontrast- und Überblendungen in Masken zu erzielen.

Die Verwendung ist wesentlich komplexer als die normale [Histogrammprüfung](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md). Stellen Sie daher sicher, dass Sie mit dieser Methode vertraut sind, bevor Sie versuchen, die nicht einheitliche Version zu verwenden.

## Parameter

### Eingaben

* **Eingabe**: *Graustufeneingabe* Quellergebnis zum Ändern.
* **Positionszuordnung**: *Graustufen-Eingang* Eingangssteckplatz zum Steuern des Positionsparameters. Aktiviert, wenn &quot;Positionseingabe verwenden&quot; auf &quot;True&quot; gesetzt ist. Der effektive Wertebereich ist klein und hängt von der Kontrastkarte und den Einstellungen ab.
* **Kontrastkarte**: *Graustufen-Eingang* Eingangssteckplatz zur Steuerung des Kontrastparameters. Aktiviert, wenn &quot;Kontrasteingabe verwenden&quot; auf &quot;True&quot; gesetzt ist. Der effektive Wertebereich ist klein.

### Parameter

* **Positionseingabe verwenden**: *Falsch/Wahr* Verwendung des Positionszuordnungs-Eingabefelds umschalten.
* **Position**: *0.0 - 1.0* Steuert oder ändert die Kartenergebnisse, um die Positionseinstellung zu steuern.
* **Kontrasteingabe verwenden**: *Falsch/Wahr* Verwendung des Kontrastzuordnungs-Eingabeslots umschalten.
* **Kontrast**: *0.0 - 1.0* Steuert oder ändert die Kartenergebnisse, um die Kontrasteinstellung zu steuern.

## Beispielbilder

</td>
</tr>
</table>

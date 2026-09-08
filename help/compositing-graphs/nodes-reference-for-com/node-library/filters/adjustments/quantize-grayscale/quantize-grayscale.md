---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Graustufen quantisieren", um die Anzahl der Graustufen für Posterisierungseffekte zu reduzieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graustufen quantisieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Graustufen quantisieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Graustufen quantisieren&quot;](../../../../../../assets/quantize-grayscale.png "Symbol &quot;Graustufen quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt einen einzelnen Spline-Effekt in Form eines Kreises.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Schritte</b> *Integer* | Die Anzahl der separaten Werte, denen der Eingabebereich angenähert werden soll. |
| <b>Offset</b> *Gleitend* | Wendet einen Offset auf den Eingabebereich an, wodurch *die Ergebnisse entlang des Bereichs verschiebt*. |
| <b>Steigung</b> *Gleitend* | Wendet einen Überblendungsverlauf auf die *Steigungen* zwischen ungefähren Werten an, bis zur *vollen Spanne eines Schritts*. |
| <b>Kurve der Steigung</b> *Integer* | Legt die Methode zum Erfassen der Kurve für die Steigung fest, die durch den Parameter <b>Steigung</b> festgelegt wird:<ul data-preserve-html="true"> <li data-preserve-html="true">*Linear*: Wendet eine Gerade an, was zu einer geraden Steigung führt</li> <li data-preserve-html="true">*Smoothstep*: Wendet eine Glättungskurve an, die zu einer glatten Steigung führt.</li> <li data-preserve-html="true">*Kurveneingabe*: Wendet die durch die Eingabezuordnung <b>Kurveneingabe</b> beschriebene Kurve an. Sie können einen Knoten [Kurve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) verwenden, um diese Kurve mit viel Kontrolle zu beschreiben.</li> </ul> |

## Beispiele

![Beispiel 1](../../../../../../assets/quantizegrayscale.gif "Beispiel 1")

![Beispiel 2](../../../../../../assets/quantizegrayscale.png "Beispiel 2")

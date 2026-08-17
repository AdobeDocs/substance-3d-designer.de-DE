---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Uneinheitlicher Weichzeichner", um einen Weichzeichner mit unterschiedlichen Intensitäten in X- und Y-Richtungen anzuwenden und so anisotrope Effekte zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uneinheitlicher Weichzeichner
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Uneinheitlicher Weichzeichner

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## Uneinheitlicher Weichzeichner (Graustufen)

**In:** *Filter/Unschärfen*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Führt einen Weichzeichner mit hoher Qualität durch, bei dem die Intensität durch eine Eingabemaske gesteuert wird. Mit den Optionen können Anisotropie und Asymetrie hinzugefügt werden.

## Parameter

### Eingaben

* **Weichzeichnungszuordnung**: *Graustufen-Eingabe* Maskenzuordnung zur Steigerung der Effektstärke.

### Parameter

* **Intensität**: *0.0 - 50.0* Maximale Stärke zum Anwenden der Weichzeichnung. Maskiert durch die Weichzeichnermatrix, sodass diese Einstellung keine Auswirkungen auf schwarze Bereiche der Karte hat.
* **Anisotropie**: *0.0 - 1.0* fügt dem Weichzeichnungseffekt optional eine Richtungsfunktion hinzu. Gesteuert durch den Parameter Winkel.
* **Asymmetrie**: *0.0 - 1.0* Fügt optional der Sampling-Funktion eine Voreinstellung hinzu. Gesteuert durch den Parameter Winkel.
* **Winkel**: *0.0 - 1.0* Winkel zum Festlegen der Richtungsabhängigkeit und des Sampling-Bias.
* **Beispiele**: *1 - 16* Anzahl der Samples, bestimmt die Qualität. Multipliziert mit der Anzahl der Blades.
* **Blades**: *1 -* 9\
  Die Anzahl der Stichprobensektoren bestimmt die Qualität. Multipliziert mit der Anzahl der Samples.

## Beispielbilder

Das Beispiel *Unten wird von einer Verlaufsrampe (bei 90 Grad) im Steckplatz &quot;Weichzeichnermatrix&quot; gesteuert.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>

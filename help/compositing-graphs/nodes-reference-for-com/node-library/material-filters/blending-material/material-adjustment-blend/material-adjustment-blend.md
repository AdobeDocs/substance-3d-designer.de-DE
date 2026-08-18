---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialkorrektur-Überblendung , um Materialkorrekturen zwischen Materialien zu überblenden und Composite-Effekte zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialanpassungsüberblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Materialanpassungsüberblendung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## Materialanpassungsüberblendung

**In:** *Materialfilter/Füllmethode*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ermöglicht die Anpassung aller Kanäle eines Vollmaterials auf Basis einer Maske. Sie soll einen vollständigen Material-Workflow einfacher und schneller machen.

Dies ist nützlich, wenn Sie einige Kanäle eines Materials anpassen möchten (z. B. diffuses Licht und Raueit dunkler machen), die auf derselben Maske basieren.

## Parameter

### Eingaben

* **Farb-ID-Maske**: *Farbeingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Graustufenmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Kanäle**\
  Schaltet die Materialkanäle in dieser Gruppe ein und aus, z. B. bei Verwendung von Specular-/Glanzkarten anstelle von Metallisch/Raueit.\
  Dadurch wird auch das Erscheinungsbild der relevanten Gruppen des Kanals aktiviert und deaktiviert.
* **Diffus**\
  Führt Korrekturvorgänge für den Diffuse-Kanal in Bereichen durch, die durch die Maske definiert sind.
* **Grundfarbe**\
  Führt Korrekturvorgänge für den Kanal &quot;Grundfarbe&quot; in Bereichen durch, die durch die Maske definiert sind.
* **Normal**
  * **Intensität**: *0.0 - 1.0* Töne nach unten Normalintensität
* **Specular**\
  Führt Korrekturvorgänge für den Specular-Kanal in Bereichen durch, die durch die Maske definiert sind.
* **Ausstrahlend**\
  Führt Anpassungsvorgänge auf dem Emissionskanal in Bereichen durch, die durch die Maske definiert werden.
* **Glossarität**\
  Führt Korrekturvorgänge für den Glossiness-Kanal in Bereichen durch, die durch die Maske definiert werden.
* **Raueit**\
  Führt Anpassungsvorgänge für den Kanal &quot;Raueit&quot; in Bereichen durch, die durch die Maske definiert werden.
* **Metallisch**\
  Führt Korrekturvorgänge für den metallischen Kanal in Bereichen durch, die durch die Maske definiert sind.
* **Specular level**\
  Führt Korrekturoperationen auf dem Specular level-Kanal in Bereichen durch, die durch die Maske definiert werden.
* **Umgebungs-Verdeckung**\
  Führt Korrekturvorgänge für den Umgebungsmaskenkanal in den von der Verdeckung definierten Bereichen durch.
* **Height**\
  Führt Korrekturvorgänge für den Height-Kanal in den von der Maske definierten Bereichen durch.
* **Deckkraft**\
  Führt Korrekturvorgänge für den Kanal &quot;Deckkraft&quot; in den von der Maske definierten Bereichen durch.
* **Farb-ID-Maske**: *Falsch/Wahr* Legen Sie fest, dass Farb-ID-Maske anstelle der Graustufenmaske verwendet wird.
* **Unschärfe**: *0.01 - 1.0* Wenn Farb-ID-Maske aktiviert ist, bestimmt dies den Farbauftrag der Farbauswahlfarbe.
* **Farbe**: *(Farbwert)*Legt fest, welche Farbe aus der Farb-ID-Karte und der Maske ausgewählt werden soll.
* **Auffüllen**: *0.0 - 1.0* Bestimmt den Mischkontrast/die Übergänge der Farb-ID-Maskierung.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

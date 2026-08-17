---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Uber-Relief, um erweiterte Reliefeffekte mit anpassbaren Steuerelementen für Tiefe, Winkel und Beleuchtung zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Relief
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Uber Relief

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Uber Relief

**In:** *Filter/Effekte*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erweiterte, funktionsreiche Version von [Relief](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Führt einen aufwändigen gefälschten 2D-Beleuchtungseffekt auf der Grundlage einer Höhenkarte durch.

Nützlich, wenn du bei bestimmten Texturierungs-Stilen eine Beleuchtung einbauen möchtest, die du nicht brauchst, aber viel Kontrolle erfordert.

## Parameter

### Eingaben

* **Farbe**: *Farbeingabe*\
  Zu änderndes Basis-Image.
* **Height**: *Graustufen-Eingabe*\
  Als Treiber für den Effekt verwendete Höhenkarte.

### Parameter

* **Umgebungsfarbe**: *(Farbwert)*Farbe, die in schattierten Bereichen verwendet wird.
* **Diffuse Farbe**: *(Farbwert)*In beleuchteten Bereichen verwendete Farbe.
* **Specular-Farbe**: *(Farbwert)*Für Specular-Reflexionen verwendete Farbe
* **Lichtintensität**: *0.0 - 1.0*\
  Intensität des (gefälschten) Lichts.
* **Lichtwinkel**: *0.0 - 1.0*\
  Einfallswinkel des (gefälschten) Lichts
* **Specular-Intensität**: *0.0 - 1.0* Intensität der Specular-Reflexionen.
* **Specular-Glossarität**: *0.0 - 1.0* Größe der Specular-Markierung.
* **Diffuse Raueit**: *0.0 - 1.0* Raueit, die bei der Berechnung der diffusen Beleuchtung verwendet wird.
* **Schattendeckkraft**: *0.0 - 1.0* Deckkraft der schattierten Bereiche.

## Beispielbilder

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>

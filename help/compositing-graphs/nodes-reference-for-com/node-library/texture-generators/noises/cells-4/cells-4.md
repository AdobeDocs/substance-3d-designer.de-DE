---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Zellen 4, um fortgeschrittene Zellmuster zu erzeugen, um organische und biologische Textureffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ZELLEN 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# ZELLEN 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Zellen 4 - Symbol](cells-4.resources/cells_4.png "Zellen 4 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>Zellen</b> von Walled Noise.

Jeder Zelle ist eine flache Farbe zugewiesen, die zufällig oder aus einem Eingabebild aufgenommen werden kann.

Siehe auch: [Zellen 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Zellen 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Zellen 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Graustufen</i> |  |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Das erzeugte Rauschen als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>Integer</i> | Die Unterteilung des Rasters, das zum Erzeugen der Rauschkacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Störung</b> <i>Gleitend</i> | Versetzt die Bestandteile des Rauschens.    So kannst du das Rauschen animieren. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Farbquelle</b> <i>Integer</i> | Die Quelle der auf die Zellen angewendeten einheitlichen Farbe:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>Zufällig:</i></b> Verwenden Sie eine zufällige Farbe, die durch die zufällige Seed des Knotens gesteuert wird.</li> <li data-preserve-html="true"><b><i>Pseudozufall:</i></b> Verwenden Sie eine zufällige Farbe, der ein separater Wert für den Benutzersatz zugewiesen ist</li> <li data-preserve-html="true"><b><i>Bildeingabe:</i></b> Verwenden der an der Zellenposition im Eingabebild aufgenommenen Farbe</li> </ul> |
| <b>Pseudozufallssaatgut</b> <i>Integer</i>   *Verfügbar, wenn &quot;Farbquelle&quot; auf &quot;Pseudozufallsdatum&quot; festgelegt ist* | Ermöglicht das Ändern des Startwerts für die Farbe getrennt vom Startwert des Knotens. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Zellen 4 - Beispiel 1](cells-4.resources/cells_4_1.png "Zellen 4 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Zellen 4 - Beispiel 2](cells-4.resources/noise_cells_4_v2_speed0.3_aniso0.6.gif "Zellen 4 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-2.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten BnW-Punkte 2, um Schwarz-Weiß-Volltonfarbmuster mit erweiterten Steuerelementen für Strukturvariationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BnW-Punkte 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# BnW-Punkte 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![BnW-Punkte 2 - Symbol](bnw-spots-2.resources/bnw_spots_2.png "BnW-Punkte 2 - Symbol"){width="200px"}

<b>In:</b> Texturgeneratoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variante der groben <b>Schwarz-Weiß-Flecken (BnW)</b> Rauschen.

Siehe auch: [BnW-Punkte 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-1/bnw-spots-1.md), [BnW-Punkte 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

</td>
</tr>
</table>

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
| <b>Anisotropie der Störung</b> <i>Gleitend</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnW-Punkte 2 - Beispiel 1](bnw-spots-2.resources/bnw_spots_2_1.png "BnW-Punkte 2 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnW-Punkte 2 - Beispiel 2](bnw-spots-2.resources/noise_bnw_spots_2_v2_speed0.6_aniso0.gif "BnW-Punkte 2 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnW-Punkte 2 - Beispiel 3](bnw-spots-2.resources/noise_bnw_spots_2_v2_speed0.6_aniso1.gif "BnW-Punkte 2 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnW-Punkte 2 - Beispiel 4](bnw-spots-2.resources/noise_bnw_spots_2_v2_speed0.3_aniso0.6.gif "BnW-Punkte 2 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

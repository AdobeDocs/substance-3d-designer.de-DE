---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Zellen 3, um Zellmuster zwischen den Zellen zu erzeugen, um organische und biologische Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ZELLEN 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# ZELLEN 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Zellen 3 - Symbol](cells-3.resources/cells_3.png "Zellen 3 - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine Variation der <b>Zellen</b> ummauerten Rauschen.

Der Schnittpunkt von Scheiben erzeugt Zellen mit dünnen Wänden von unebener Weichheit.

Siehe auch: [Zellen 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Zellen 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Zellen 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Die generierte Rauschen als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>Ganzzahl</i> | Die Unterteilung des Rasters, der zum Generieren der Rauschen-Kacheln verwendet wird.    Ein höherer Wert führt dazu, dass mehr Kacheln gezeichnet werden und das Rauschen dichter ist. |
| <b>Härte</b> <i>Fließkommazahl</i> | Die Definition der Zellwände, bei denen ein höherer Wert zu definierten, scharfen Wänden führt. |
| <b>Umkehren</b> <i>Boolesche Wert</i> | Kehrt die Graustufenwerte des Bildausgangs um. |
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Gleitend</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Mit dieser Option können Sie die Geschwindigkeit des Versatzes bei der Animation des Rauschens steuern. |
| <b>Anisotropie der Störung</b> <i>Gleitend</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Anisotropie wird durch den Parameter <b>Disorder Direction Angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Gleitend</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der Parameter &quot;Disorder Anisotropie&quot; nicht Null ist. |
| <b>Mustergröße</b> <i>Float2</i> | Ein Multiplikator für die Größe einer gestreuten Festplatte in ihrer Zelle., wobei 1,0 die gesamte Spanne der Zelle ist. |
| <b>Musterskala</b> <i>Gleitend</i> | Ein Multiplikator für die <b>Mustergröße</b>, wobei 1,0 die volle Größe ist. |
| <b>Winkel</b> <i>Gleitend</i> | Der Winkel, der zur Einstellung der Richtung der Scheiben verwendet wird, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Gleitend</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Kachelversatz</b> <i>Float2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschens verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolescher Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Zellen 3 - Beispiel 1](cells-3.resources/cells_3_1.png "Zellen 3 - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Zellen 3 - Beispiel 2](cells-3.resources/noise_cells_3_v2_speed0.6_aniso0.gif "Zellen 3 - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Zellen 3 - Beispiel 3](cells-3.resources/noise_cells_3_v2_speed0.6_aniso1.gif "Zellen 3 - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Zellen 3 - Beispiel 4](cells-3.resources/noise_cells_3_v2_speed0.3_aniso0.6.gif "Zellen 3 - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

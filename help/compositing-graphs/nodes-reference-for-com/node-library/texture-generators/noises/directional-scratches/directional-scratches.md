---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Richtungsabhängige Scratches , um gerichtete Kratzmuster zu erstellen, um Materialien Abnutzungs- und Schadenseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Richtungsverkratzungen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1241ebb4d1e67c9ed9d86285a6397ddc335e0f37
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Richtungsverkratzungen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Richtungsabhängige Kratzer - Symbol](directional-scratches.resources/directional_scratches.png "Richtungsabhängige Kratzer - Symbol"){width="200px"}

<b>In:</b> Texturen-Generatoren > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Eine zufällige Streuung von Kratzmustern mit einstellbarem Winkel und Größe.

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
| <b>Störung</b> <i>Fließkommazahl</i> | Versetzt die Bestandteile der Rauschen.    So animierst du die Rauschen. |
| <b>Störungsgeschwindigkeit</b> <i>Fließkommazahl</i> | Passt den Abstand des Versatzes an, der vom <b>Disorder</b>-Parameter angewendet wird.    Dies kann verwendet werden, um die Geschwindigkeit des Versatzes bei der Animation des Rauschen zu steuern. |
| <b>Anisotropie der Störung</b> <i>Fließkommazahl</i> | Steuert die Richtungsspanne des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wobei ein höherer Wert zu einer engeren, definierteren Richtung führt.    Die Richtung wird durch den Parameter <b>Disorder anisotropy angle</b> gesteuert. |
| <b>Disorder anisotropy angle</b> <i>Fließkommazahl</i> | Steuert die Richtung des Versatzes, der vom <b>Disorder</b>-Parameter angewendet wird, wenn der <b>Disorder Anisotropie</b>-Parameter nicht Null ist. |
| <b>Winkel</b> <i>Fließkommazahl</i> | Der Winkel, der verwendet wird, um die Richtung der Kratzer festzulegen, in der Anzahl der Windungen und ausgehend von der horizontalen rechten Seite. |
| <b>zufälliger Winkel</b> <i>Fließkommazahl</i> | Die maximale Anzahl zufälliger Variationen, die auf den Wert <b>Winkel</b> in der Anzahl der Windungen angewendet werden. |
| <b>Mustermenge</b> <i>Fließkommazahl</i> | Ein Multiplikator für die Anzahl der gestreuten Kratzmuster. |
| <b>Mustergröße</b> <i>Fließkommazahl2</i> | Die Größe des Begrenzungsrahmens für das neue Muster.    Der Y-Wert steuert die maximale Länge der Kratzer. |
| <b>Zufällige Mustergröße</b> <i>Fließkommazahl2</i> | Ein Multiplikator für den zufälligen Umfang der Downskalierung, der auf die Kratzer angewendet wird.    Der Y-Wert wird auf die Länge der Kratzer angewendet. |
| <b>Kachelversatz</b> <i>Fließkommazahl2</i> | Steuert die Position des Abschnitts der unendlichen Ebene, der zum Rendern des Rauschen verwendet wird. |
| <b>Nicht quadratische Erweiterung</b> <i>Boolesche Wert</i> | Bei nicht quadratischen Bildern bleibt das erzeugte Kachelquadrat erhalten und erweitert die Rauscherzeugung auf die Grenzen des Bildes. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungskratzer - Beispiel 1](directional-scratches.resources/directional_scratches_1.png "Richtungskratzer - Beispiel 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungskratzer - Beispiel 2](directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.gif "Richtungskratzer - Beispiel 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungskratzer - Beispiel 3](directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.6.gif "Richtungskratzer - Beispiel 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Richtungskratzer - Beispiel 4](directional-scratches.resources/noise-directional-scrat-1.gif "Richtungskratzer - Beispiel 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Richtungskratzer - Beispiel 5](directional-scratches.resources/noise-directional-scrat-2.gif "Richtungskratzer - Beispiel 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

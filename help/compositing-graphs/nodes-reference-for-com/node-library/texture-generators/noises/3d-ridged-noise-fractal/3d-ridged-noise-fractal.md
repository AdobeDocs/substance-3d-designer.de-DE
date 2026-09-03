---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "3D-Ridge-Noise Fractal", um gekräuselte fraktale Rauschmuster im 3D-Raum zu generieren, um bergartige Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Fraktal mit verkipptem Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 3D-Fraktal mit verkipptem Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-01.png){width="200px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten <b>3D Ridge Noise Fractal</b> generiert ein <i>fraktales</i> Ridge-Rauschen im 3D-Raum basierend auf der <b>Positionszuordnung</b>-Eingabe.

Dieser Knoten kann mit [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer tatsächlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

</td>
</tr>
</table>

>[!WARNING]
>
> Dieses Geräusch soll nur mit dem <i>GPU-Modul verwendet werden</i> (d. h. <b>Direct3D</b> oder <b>OpenGL</b>). Wechseln Sie zu <b>Extras > Modul wechseln...</b> oder drücken Sie die Taste <b>F9</b>, um das gewünschte Modul auszuwählen.

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Umkehren</b> <i>Boolescher Wert</i> | Kehrt das Ausgabebild um. |
| <b>Skalierung</b> <i>Gleitend</i> | Steuert die Skalierung des fraktalen 3D-Rauschens mit Ridge. |
| <b>Größe</b> <i>Float3</i> | Steuert die Größe des fraktalen 3D-Ridge-Rauschens in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b>. Nicht einheitliche Werte führen zu einem <i>Dehnungs- oder Squashing</i>-Effekt. |
| <b>Offset</b> <i>Float3</i> | Wendet einen Offset auf die <i>Position</i> des fraktalen 3D-Rauschens mit Ridge in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b> an. |
| <b>Intensität der Verzerrung</b> <i>Gleitend</i> | Steuert die Intensität eines <i>Verkrümmungseffekts</i>, der auf das fraktale 3D-Rauschen mit Ridge angewendet wird. |
| <b>Verzerrungen-Skalierungsmultiplikator</b> <i>Gleitend</i> | Steuert die Skalierung des <i>sich verformenden Musters</i>, das im Verkrümmungseffekt verwendet wird, der durch die <b>Intensität der Verzerrung</b> gesteuert wird. |
| <b>Min. Stufe</b> <i>Integer</i> | Die minimale <i>Wiederholungsstufe</i>, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem <i>reicheren Muster</i> mit Variationen in mehr Frequenzbereichen. |
| <b>Max. Stufe</b> <i>Integer</i> | Die maximale <i>Wiederholungsstufe </i>, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem <i>reicheren Muster</i> mit Variationen in mehr Frequenzbereichen. |
| <b>Raueit</b> <i>Gleitend</i> | Steuert die <i>Balance</i> zwischen niedrigen und hohen <i>Wiederholungsstufen</i> im fraktalen Muster.<br><br><i>Hinweis</i>: Ein Wert von <b>0</b> führt zu einer Ausgabe, die <i> nicht in Zeile </i> enthält, auf die andere niedrige Werte folgen. Dies wird erwartet. |
| <b>Lakunarität</b> <i>Gleitend</i> | Steuert, wie das angewendete fraktale Muster &quot;<i>&quot; Leerzeichen &quot;</i>&quot; ausfüllt. Ein <i>höherer</i> Wert führt zu <i>weniger Lücken</i> im Muster und einem <i>dichteren</i> Rauschen. |
| <b>Globale Deckkraft</b> <i>Gleitend</i> | Steuert den <i>Bereich</i> der fraktalen 3D-Rauschwerte mit Ridge <i> um </i> den <b>Grundlinienwert</b>. |
| <b>Grundlinie</b> <i>Gleitend</i> | Wendet einen <i>Versatz</i> auf den Grundlinienwert <i>Luminanz</i> für die 3D-Rauschwertverteilung an. |
| <b>Kontrast</b> <i>Gleitend</i> | Passt den Kontrast des 3D-Rauschens mit gekräuselten Linien an. |
| <b>Kachelung aktivieren</b> <i>Boolescher Wert</i> | Passt das 3D-Rauschen an, sodass sich das resultierende Muster <i></i> in der X-, Y- und Z-Achse wiederholt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-03.jpg" />
        </td>
    </tr>
</table>

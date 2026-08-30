---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D Perlin Noise Fractal , um fraktale Perlin-Rauschmuster im 3D-Raum für die Erstellung detaillierter volumetrischer Texturen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Perlin-Rauschen Fraktal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# 3D-Perlin-Rauschen Fraktal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise-fractal.resources/3dperlinnoisefractal.png){width="200px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten <b>3D Perlin Noise Fractal</b> generiert ein <i>Fraktal</i> Perlin-Rauschen im 3D-Raum basierend auf der <b>Positionszuordnung</b>-Eingabe.

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
| <b>Skalierung</b> <i>Gleitend</i> | Steuert die Skalierung des fraktalen 3D-Perlin-Rauschens. |
| <b>Größe</b> <i>Float3</i> | Steuert die Größe des fraktalen 3D-Perlin-Rauschens in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b>. Nicht einheitliche Werte führen zu einem <i>Dehnungs- oder Squashing</i>-Effekt. |
| <b>Offset</b> <i>Float3</i> | Wendet einen Offset auf die <i>Position</i> des fraktalen 3D-Perlin-Rauschens in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b> an. |
| <b>Intensität der Verzerrung</b> <i>Gleitend</i> | Steuert die Intensität eines <i>Verkrümmungseffekts</i>, der auf das fraktale 3D-Perlin-Rauschen angewendet wird. |
| <b>Verzerrungen-Skalierungsmultiplikator</b> <i>Gleitend</i> | Steuert die Skalierung des <i>sich verformenden Musters</i>, das im Verkrümmungseffekt verwendet wird, der durch die <b>Intensität der Verzerrung</b> gesteuert wird. |
| <b>Min. Stufe</b> <i>Integer</i> | Die minimale <i>Wiederholungsstufe</i>, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem <i>reicheren Muster</i> mit Variationen in mehr Frequenzbereichen. |
| <b>Max. Stufe</b> <i>Integer</i> | Die maximale <i>Wiederholungsstufe </i>, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem <i>reicheren Muster</i> mit Variationen in mehr Frequenzbereichen. |
| <b>Raueit</b> <i>Gleitend</i> | Steuert die <i>Balance</i> zwischen niedrigen und hohen <i>Wiederholungsstufen</i> im fraktalen Muster.<br><br><i>Hinweis</i>: Ein Wert von <b>0</b> führt zu einer Ausgabe, die <i> nicht in Zeile </i> enthält, auf die andere niedrige Werte folgen. Dies wird erwartet. |
| <b>Lakunarität</b> <i>Gleitend</i> | Steuert, wie das angewendete fraktale Muster &quot;<i>&quot; Leerzeichen &quot;</i>&quot; ausfüllt. Ein <i>höherer</i> Wert führt zu <i>weniger Lücken</i> im Muster und einem <i>dichteren</i> Rauschen. |
| <b>Globale Deckkraft</b> <i>Gleitend</i> | Steuert den <i>Bereich</i> der fraktalen 3D-Perlin-Rauschen-Werte <i> um </i> den <b>Grundlinienwert</b>. |
| <b>Grundlinie</b> <i>Gleitend</i> | Wendet einen <i>offset</i> auf den Basiswert <i>Luminanz</i> für die Werteverteilung der 3D-Perlin-Rauschen an. |
| <b>Kontrast</b> <i>Gleitend</i> | Passt den Kontrast des 3D-Perlin-Rauschens an. |
| <b>Absolut</b> <i>Boolescher Wert</i> | Verwendet absolute Werte im 3D-Perlin-Rauschen. Dadurch wird <i>die Wertverteilung für die Werte <i> unter 0,5</i> effektiv umgekehrt</i>. |
| <b>Kachelung aktivieren</b> <i>Boolescher Wert</i> | Passt das 3D-Perlin-Rauschen so an, dass sich das resultierende Muster <i></i> in der X-, Y- und Z-Achse wiederholt. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dfractal.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dperlinnoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dperlinnoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>

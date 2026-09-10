---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D-Knoten Perlin Rauschen, um sanfte Perlin-Rauschen-Muster im 3D-Raum zu erstellen, um natürlich aussehende volumetrische Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin Rauschen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# 3D Perlin Rauschen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3dperlinnoise.png){width="200px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten <b>3D Perlin Rauschen</b> generiert eine Perlin-Rauschen im 3D-Raum auf der Grundlage der Eingabe <b>Positionszuordnung</b>.

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
| <b>Skalierung</b> <i>Gleitend</i> | Steuert die Skalierung der 3D-Perlin-Rauschen. |
| <b>Größe</b> <i>Float3</i> | Steuert die Größe der 3D-Perlin-Rauschen in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b>. Nicht einheitliche Werte führen zu einem <i>Dehnungs- oder Squashing</i>-Effekt. |
| <b>Offset</b> <i>Float3</i> | Wendet einen Offset auf die <i>Position</i> der 3D-Perlin-Rauschen in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b> an. |
| <b>Intensität der Verzerrung</b> <i>Gleitend</i> | Steuert die Intensität eines <i>Verkrümmungseffekts</i>, der auf der 3D-Perlin-Rauschen angewendet wird. |
| <b>Verzerrungen-Skalierungsmultiplikator</b> <i>Gleitend</i> | Steuert die Skalierung des <i>sich verformenden Musters</i>, das im Verkrümmungseffekt verwendet wird, der durch die <b>Intensität der Verzerrung</b> gesteuert wird. |
| <b>Grundlinie</b> <i>Gleitend</i> | Wendet einen <i>offset</i> auf den Basiswert <i>Luminanz</i> für die Werteverteilung der 3D-Perlin-Rauschen an. |
| <b>Kontrast</b> <i>Gleitend</i> | Passt den Kontrast der 3D-Perlin-Rauschen an. |
| <b>Absolut</b> <i>Boolescher Wert</i> | Verwendet absolute Werte auf der 3D-Perlin-Rauschen. Dadurch wird <i>die Wertverteilung für die Werte <i> unter 0,5</i> effektiv umgekehrt</i>. |
| <b>Kachelung aktivieren</b> <i>Boolescher Wert</i> | Passt die 3D-Perlin-Rauschen so an, dass sich das resultierende Muster <i>in X-, Y- und Z-Achse wiederholt</i>. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlin.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant.jpg" />
        </td>
    </tr>
</table>

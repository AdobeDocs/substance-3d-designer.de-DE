---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D-Textur - Lautstärke-Rendering , um volumetrische Texturen aus 3D-Daten zu rendern und so Cloud- und Nebeleffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Textur Volume Render
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# 3D Textur Volume Render

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

<b>In:</b> Filter > Effekt

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Textur Volume Render** rendert die Lautstärke einer Form, die durch eine *3D-Textur* beschrieben wird, und verwendet dabei das dazugehörige *vorzeichenbehaftete Abstandsfeld* aus der Bildeingabe **3D Vorzeichenbehaftetes Abstandsfeld**.

Das Volume wird innerhalb der Grenzen eines *Einheitscube* dargestellt. Die Beleuchtung wird mit *gerichtetem Licht* und einem *halbkugelförmigen Oberlicht* berechnet.

>[!NOTE]
>
> Es wird erwartet, dass das vorzeichenbehaftete Abstandsfeld eine **4096x4096**-Textur ist, die die Form mit einem **16x16**-Raster von 256 Slices beschreibt.\
> Sie können den Knoten [3D Textur SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das vorzeichenbehaftete Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>3D Vorzeichenbehaftetes Abstandsfeld</b> <i>Graustufen</i> | Das Bild 4096x4096, das die 256 <i>Slices</i> des <i>vorzeichenbehafteten Abstandsfelds</i> einer Form darstellt, angeordnet in einem 16x16-Raster.<br>Sie können den Knoten [3D Textur SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das vorzeichenbehaftete Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen. |
| <b>Dichte</b> <i>Graustufen</i> | Das 4096x4096-Bild, das die 256 <i>Slices</i> der <i>Dichte</i> einer Form darstellt, angeordnet in einem 16x16-Raster. Die Dichte wird mithilfe von Graustufenwerten von 0 (völlig transparent) bis 1 (völlig undurchsichtig) zugeordnet.<br>Sie können [3D-Volumenmaske](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) oder 3D-Rauschen-Nodes ([3D Perlin Rauschen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [3D Voronoi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [3D Ridge Rauschen Fraktal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) usw.) in Kombination mit einem [3D-Texturen-](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md)-Node als Positionseingabe verwenden, um eine Volumenmaske als 3D-Textur von 25 zu generieren. 6 Slices. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabeauflösung</b> <i>Integer2</i> | Die Auflösung des Ausgabebilds in <b>X</b> und <b>Y</b>, ausgedrückt als <i>Potenz von zwei</i>. |
| <b>Position der Kamera</b> <i>Float2</i> | Die Position der Kamera um die Form.<br>Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der <b>2D-Ansicht</b> bis <i>Umlaufbahn</i> der Kamera verwenden. |
| <b>Lichtposition</b> <i>Float2</i> | Die Position des <i>Richtungslichts</i> um die Form.<br>Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der <b>2D-Ansicht</b> bis <i>Bahn</i> der Lichtquelle verwenden. |
| <b>Kameras-Entfernung</b> <i>Gleitend</i> | Der Abstand zwischen Kamera und Form. |
| <b>Kamera FOV</b> <i>Gleitend</i> | Das Sichtfeld der Kamera in <i>Grad</i>. |
| <b>Absorption</b> <i>Gleitend</i> | Legt fest, wie viel Licht absorbiert wird, wenn es <i> durch </i> die Lautstärke hindurchtritt. |
| <b>Feder</b> <i>Gleitend</i> | Multipliziert den von der <b>Dichte</b>-Eingabe angegebenen Wert mit dem <i>inneren</i>-Abstandsfeldwert.<br>Dadurch wird die Breite des <i>Überblendungsverlaufs</i> von der äußeren Begrenzung des Volumes nach innen angepasst. |
| <b>Lichtfarbmodus</b> <i>Integer</i> | Legt die Methode zum Erfassen der Farbe des Richtungslichts fest:<br>- <i>Temperatur (Kelvin)</i>: Die Farbe ergibt sich aus der Lichttemperatur, bei der ein <i>niedrigerer</i> Wert zu einer <i>wärmeren</i> Farbe<br>- <i>RGB Color</i> führt: Definieren der Farbe mithilfe von RGB-Werten |
| <b>Lichttemperatur (Kelvin)</b> <i>Gleitend</i> | Die Temperatur des Richtungslichts, die sich auf die <i>Farbe</i> auswirkt. Ein <i>niedrigerer</i>-Wert führt zu einer <i>wärmeren</i> Farbe.<br>Nützliche Werte:<br>1800 K - Kerzenlicht<br>2800 K - Glühbirne<br>5500 K - Tageslicht<br>6200 K - Naturweiß<br>7000 K - Bewölkter Himmel<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Lichtfarbmodus</b> auf <i>Temperatur (Kelvin)</i> festgelegt ist. |
| <b>Helle Farbe</b> <i>Float3</i> | Die Farbe des Richtungslichts.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Lichtfarbmodus</b> auf <i>RGB-Farbe</i> festgelegt ist. |
| <b>Lichtintensität</b> <i>Gleitend</i> | Die Intensität des gerichteten Lichts. |
| <b>Umgebungsfarbe</b> <i>Float3</i> | Die Farbe des Umgebungslichtes. |
| <b>Umgebungsintensität</b> <i>Gleitend</i> | Die Intensität des Umgebungslichtes. |
| <b>Albedo</b> <i>Float3</i> | Die Albedo der Lautstärke. |
| <b>Hintergrundmodus</b> <i>Integer</i> | Die Methode zur Schattierung des Hintergrunds der gerenderten Szene, die auf der <b>Hintergrundfarbe</b>:<br>- <i>Schattiert</i> basiert: Die Farbe wird von der <i>Farbe</i> und der <i>Intensität</i><br>- <i>konstanten Farbe</i> des Richtungslichts beeinflusst: Die Farbe wird gleichmäßig <i>angewendet, unabhängig</i> von der Lichtrichtung |
| <b>Hintergrundfarbe</b> <i>Float4</i> | Die Farbe, die zum Füllen des Hintergrunds der gerenderten Szene verwendet wird. |
| <b>Dithering</b> <i>Gleitend</i> | Passt die Intensität des <i>blauen Rauschen-Dithering</i> an, der zum Glätten der Schattierung verwendet wird. |
| <b>Boden-Ebene aktivieren</b> <i>Boolescher Wert</i> | Wenn <i>Wahr</i>, wird eine <i>unendliche</i> Boden-Ebene gerendert. Der <i>Einheitswürfel</i>, der die Form umschließt, liegt auf dieser Ebene. |
| <b>Unendliche Ebene</b> <i>Boolescher Wert</i> | Setzt die Ebene des Bodens auf <i>unendlich</i> bis zum Horizont.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Enable Boden Plane</b> auf <i>True</i> festgelegt ist. |
| <b>Boden-Ebenengröße</b> <i>Float2</i> | Passt die Größe der Boden-Ebene an.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Grundebene aktivieren</b> auf <i>Wahr</i> und der Parameter <b>Unendliche Ebene</b> auf <i>Falsch</i> festgelegt ist. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-node.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D-Textur-Oberflächen-Rendering , um Oberflächenstrukturen aus 3D-Daten zu rendern und so prozedurale Oberflächeneffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D-Textur - Oberflächenrendern
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# 3D-Textur - Oberflächenrendern

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>In:</b> Filter > Effekt

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Texture Surface Render** rendert die Oberfläche einer Form, die durch eine *3D-Textur* beschrieben wird, und verwendet dabei das entsprechende *Abstandsfeld* aus dem **3D-Abstandsfeld**-Bildeingang.

Die Oberfläche wird innerhalb der Grenzen eines *Einheitswürfels* dargestellt. Die Beleuchtung wird mit dem Eingabebild **Umgebung** berechnet, das einer unendlichen Kugel zugeordnet ist.

>[!NOTE]
>
> Es wird erwartet, dass das Abstandsfeld eine **4096x4096**-Textur ist, die die Form mit einem **16x16**-Raster von 256 Slices beschreibt.\
> Sie können den Knoten [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>3D-Abstandsfeld</b> <i>Graustufen</i> | Das Bild 4096x4096, das die 256 <i>Slices</i> des <i>Abstandsfelds</i> einer Form darstellt, angeordnet in einem Raster von 16x16.<br>Sie können den Knoten [3D Textur SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen. |
| <b>Umgebung</b> <i>Farbe</i> | Das Bild, das die <i>Umgebung</i> darstellt, die einer unendlichen Kugel im Rendering zugeordnet werden soll und für die Berechnung der <i>Beleuchtung</i> verwendet wird.<br>Das Image wird auch zum Rendern des Hintergrunds der Szene verwendet, wenn der Parameter <b>Hintergrundmodus</b> auf <i>Umgebung</i> oder <i>Umgebung</i> festgelegt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ausgabeauflösung</b> <i>Integer2</i> | Die Auflösung des Ausgabebilds in <b>X</b> und <b>Y</b>, ausgedrückt als <i>Potenz von zwei</i>. |
| <b>Position der Kamera</b> <i>Float2</i> | Die Position der Kamera um die Form.<br>Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der <b>2D-Ansicht</b> bis <i>Umlaufbahn</i> der Kamera verwenden. |
| <b>Kameras-Entfernung</b> <i>Gleitend</i> | Der Abstand zwischen Kamera und Form. |
| <b>Kamera FOV</b> <i>Gleitend</i> | Das Sichtfeld der Kamera in <i>Grad</i>. |
| <b>Albedo</b> <i>Float3</i> | Die Albedo der Formoberfläche. |
| <b>Hintergrundmodus</b> <i>Integer</i> | Die Methode zur Darstellung des Hintergrunds der gerenderten Szene: <br>- <i>Boden Irradiance</i>: Die berechnete Bestrahlungsstärke der Boden-Ebene<br>- <i>Umgebung</i>: Die Umgebungsfarbe der Bildeingabe <b>Umgebung</b>, die einer unendlichen Kugel zugeordnet ist, die einer stark unscharfen Version des Bildes <br>- <i>Einheitliche Farbe</i> ähnelt: Füllen Sie den Hintergrund gleichmäßig mit einer angegebenen Farbe <br>- <i>Umgebung</i>: Die <b>Environment</b>-Bildeingabe, die einer unendlichen Kugel zugeordnet ist |
| <b>Hintergrundfarbe</b> <i>Float4</i> | Die Farbe, die verwendet wird, um den Hintergrund der gerenderten Szene gleichmäßig zu füllen.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Hintergrundmodus</b> auf <i>Einheitliche Farbe</i> festgelegt ist. |
| <b>Boden-Ebene aktivieren</b> <i>Boolescher Wert</i> | Wenn <i>True</i>, wird eine Grundebene gerendert. Der <i>Einheitswürfel</i>, der die Form umschließt, liegt auf dieser Ebene. |
| <b>Unendliche Ebene</b> <i>Boolescher Wert</i> | Setzt die Ebene des Bodens auf <i>unendlich</i> bis zum Horizont.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Enable Boden Plane</b> auf <i>True</i> festgelegt ist. |
| <b>Boden-Ebenengröße</b> <i>Float2</i> | Passt die Größe der Boden-Ebene an.<br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Grundebene aktivieren</b> auf <i>Wahr</i> und der Parameter <b>Unendliche Ebene</b> auf <i>Falsch</i> festgelegt ist. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>

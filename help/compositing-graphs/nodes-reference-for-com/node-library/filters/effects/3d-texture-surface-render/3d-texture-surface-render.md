---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# 3D-Textur - Oberflächenrendern

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**In:** *Filter/Effekt*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

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

## Parameter

### Eingaben

* **3D-Abstandsfeld** *Graustufen*\
  Das Bild 4096x4096, das die 256 *Slices* des *Abstandsfelds* einer Form darstellt, angeordnet in einem Raster von 16x16.\
  Sie können den Knoten [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen.
* **Umgebung** *Farbe*\
  Das Bild, das die *Umgebung* darstellt, die einer unendlichen Kugel im Rendering zugeordnet werden soll und für die Berechnung der *Beleuchtung* verwendet wird.\
  Das Bild wird auch zum Rendern des Szenenhintergrunds verwendet, wenn der Parameter **Hintergrundmodus** auf *Umgebung* oder *Umgebung* festgelegt ist.

### Parameter

* **Ausgabeauflösung** *Integer2*\
  Die Auflösung des Ausgabebilds in **X** und **Y**, ausgedrückt als *Potenz von zwei*.
* **Kameraposition** *Gleitkomma2*\
  Die Position der Kamera um die Form.\
  Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der **2D-Ansicht** verwenden, um *die Kamera um* zu kreisen.
* **Kameraabstand** *Gleitend*\
  Der Abstand zwischen Kamera und Form.
* **Camera FOV** *Float*\
  Das Sichtfeld der Kamera in *Grad*.
* **Albedo** *Gleitend3*\
  Die Albedo der Formoberfläche.
* **Hintergrundmodus** *Ganzzahl*\
  Die Methode zur Darstellung des Hintergrunds der gerenderten Szene:
  * *Bodenbestrahlung*: Die berechnete Bestrahlungsstärke der Grundebene
  * *Umgebung*: Die Umgebungsfarbe der Bildeingabe **Umgebung**, die einer unendlichen Kugel zugeordnet ist, die einer stark unscharfen Version des Bildes ähnelt
  * *Einheitliche Farbe*: Den Hintergrund gleichmäßig mit einer bestimmten Farbe füllen
  * *Umgebung*: Die **Environment**-Bildeingabe, die einer unendlichen Kugel zugeordnet ist
* **Hintergrundfarbe** *Unverankert4*\
  Die Farbe, die verwendet wird, um den Hintergrund der gerenderten Szene einheitlich zu füllen.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Hintergrundmodus** auf *Einheitliche Farbe* festgelegt ist.
* **Grundebene aktivieren** *Boolesch*\
  Wenn *True*, wird eine Grundebene gerendert. Der *Einheitswürfel*, der die Form umschließt, liegt auf dieser Ebene.
* **Unendliche Ebene** *Boolesch*\
  Setzt die Grundebene auf *unendlich* bis zum Horizont.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Grundebene aktivieren** auf *Wahr* festgelegt ist.
* **Grundebenengröße** *Gleitkomma2* Passt die Größe der Grundebene an.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Grundebene aktivieren** auf *Wahr* und der Parameter **Unendliche Ebene** auf *Falsch* festgelegt ist.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>

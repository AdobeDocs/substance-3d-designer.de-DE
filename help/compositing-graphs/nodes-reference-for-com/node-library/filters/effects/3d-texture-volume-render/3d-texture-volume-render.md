---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten 3D Texture Volume Render, um volumetrische Texturen aus 3D-Daten zu rendern und so Cloud- und Nebeleffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Texture Volume Render
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# 3D Texture Volume Render

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**In:** *Filter/Effekt*

**Einfach**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Texture Volume Render** rendert die Lautstärke einer Form, die durch eine *3D-Textur* beschrieben wird, und verwendet dabei das entsprechende *vorzeichenbehaftete Abstandsfeld* aus der Bildeingabe **3D Vorzeichenbehaftetes Abstandsfeld**.

Das Volume wird innerhalb der Grenzen eines *Einheitscube* dargestellt. Die Beleuchtung wird mit *gerichtetem Licht* und einem *halbkugelförmigen Oberlicht* berechnet.

>[!NOTE]
>
> Es wird erwartet, dass es sich bei dem vorzeichenbehafteten Abstandsfeld um eine **4096x4096**-Textur handelt, die die Form mit einem **16x16**-Raster von 256 Slices beschreibt.\
> Sie können den Knoten [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das vorzeichenbehaftete Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen.

</td>
</tr>
</table>

## Parameter

### Eingaben

* **3D Vorzeichenbehaftetes Abstandsfeld** *Graustufen*\
  Das Bild 4096x4096, das die 256 *Slices* des *vorzeichenbehafteten Abstandsfelds* einer Form darstellt und in einem Raster von 16x16 angeordnet ist.\
  Sie können den Knoten [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) verwenden, um das vorzeichenbehaftete Abstandsfeld für eine 3D-Textur von 256 Slices zu berechnen.
* **Dichte** *Graustufen*\
  Das Bild mit einer Auflösung von 4096x4096, das die 256 *Slices* der *Dichte* einer Form darstellt, die in einem Raster von 16x16 angeordnet sind. Die Dichte wird mithilfe von Graustufenwerten von 0 (völlig transparent) bis 1 (völlig deckend) zugeordnet.\
  Sie können [3D-Volumenmaske](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) oder 3D-Rauschknoten ([3D Perlin Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [3D Voronoi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [3D Ripped Noise Fractal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) usw.) in Kombination mit einem [3D Texture Position](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md)-Knoten als Positionseingabe verwenden, um eine Volumenmaske als 3D-Textur von 256 Slices zu generieren.

### Parameter

* **Ausgabeauflösung** *Integer2*\
  Die Auflösung des Ausgabebilds in **X** und **Y**, ausgedrückt als *Potenz von zwei*.
* **Kameraposition** *Gleitkomma2*\
  Die Position der Kamera um die Form.\
  Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der **2D-Ansicht** verwenden, um *die Kamera um* zu kreisen.
* **Lichtposition** *Gleitkomma2*\
  Die Position des *Richtungslichts* um die Form.\
  Wenn der Knoten ausgewählt ist, können Sie das Positions-Gizmo in der **2D-Ansicht** bis *Umkreisung* der Lichtquelle verwenden.
* **Kameraabstand** *Gleitend*\
  Der Abstand zwischen Kamera und Form.
* **Camera FOV** *Float*\
  Das Sichtfeld der Kamera in *Grad*.
* **Absorption** *Gleitend*\
  Legt fest, wie viel Licht absorbiert wird, wenn es *durch* die Lautstärke hindurchtritt.
* **Feder** *Gleitend*\
  Multipliziert den von der **Dichte**-Eingabe angegebenen Wert mit dem *inneren*-Abstandsfeldwert.\
  Dadurch wird die Breite des *Überblendungsverlaufs* von der äußeren Begrenzung des Volumes nach innen angepasst.
* **Lichtfarbmodus** *Ganze Zahl*\
  Legt die Methode zum Erfassen der Farbe des Richtlichts fest:
  * *Temperatur (Kelvin)*: Die Farbe ergibt sich aus der Lichttemperatur, bei der ein *niedrigerer* Wert zu einer *wärmeren* Farbe führt
  * *RGB Color*: Definieren der Farbe mithilfe von RGB-Werten
* **Lichttemperatur (Kelvin)** *Gleitend*\
  Die Temperatur des Richtungslichts, die sich auf die *Farbe* auswirkt. Ein *niedrigerer*-Wert führt zu einer *wärmeren* Farbe.\
  Nutzwerte:\
  1800 K - Kerzenlicht\
  2800 K - Glühbirne\
  5500 K - Tageslicht\
  6200 K - Naturweiß\
  7000 K - Bewölkter Himmel\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Lichtfarbmodus** auf *Temperatur (Kelvin)* festgelegt ist.
* **Lichtfarbe** *Unverankert3*\
  Die Farbe des gerichteten Lichts.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Lichtfarbmodus** auf *RGB-Farbe* festgelegt ist.
* **Lichtintensität** *Unverankert*\
  Die Intensität des gerichteten Lichts.
* **Umgebungsfarbe** *Unverankert3*\
  Die Farbe des Umgebungslichtes.
* **Umgebungsintensität** *Gleitend*\
  Die Intensität des Umgebungslichtes.
* **Albedo** *Gleitend3*\
  Die Albedo der Lautstärke.
* **Hintergrundmodus** *Ganzzahl*\
  Die Methode zur Schattierung des Hintergrunds der gerenderten Szene, die auf der **Hintergrundfarbe** basiert:
  * *Schattiert*: Die Farbe wird von der *Farbe* und *Intensität*- *konstanten Farbe* des Richtungslichts beeinflusst: Die Farbe wird gleichmäßig *angewendet, unabhängig* von der Lichtrichtung
* **Hintergrundfarbe** *Unverankert4*\
  Die Farbe, die zum Füllen des Hintergrunds der gerenderten Szene verwendet wird.
* **Dithering** *Gleitkomma*\
  Passt die Intensität des *blauen Rauschens* an, das zum Glätten der Schattierung verwendet wird.
* **Grundebene aktivieren** *Boolesch*\
  Wenn *Wahr*, wird eine *unendliche* Grundebene gerendert. Der *Einheitswürfel*, der die Form umschließt, liegt auf dieser Ebene.
* **Unendliche Ebene** *Boolesch*\
  Setzt die Grundebene auf *unendlich* bis zum Horizont.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Grundebene aktivieren** auf *Wahr* festgelegt ist.
* **Grundebenengröße** *Gleitkomma2* Passt die Größe der Grundebene an.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Grundebene aktivieren** auf *Wahr* und der Parameter **Unendliche Ebene** auf *Falsch* festgelegt ist.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>

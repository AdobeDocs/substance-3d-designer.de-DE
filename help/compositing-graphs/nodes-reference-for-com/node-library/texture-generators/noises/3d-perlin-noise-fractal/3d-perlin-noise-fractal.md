---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# 3D-Perlin-Rauschen Fraktal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal.png){width="200px"}

**In:** *Texturgeneratoren**/Noises*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Perlin Noise Fractal** generiert ein *Fraktal* Perlin-Rauschen im 3D-Raum basierend auf der **Positionszuordnung**-Eingabe.

Dieser Knoten kann mit [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer tatsächlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

>[!WARNING]
>
> Dieses Geräusch soll nur mit dem *GPU-Modul verwendet werden* (d. h. **Direct3D** oder **OpenGL**). Wechseln Sie zu **Extras > Modul wechseln...** oder drücken Sie die Taste **F9**, um das gewünschte Modul auszuwählen.

</td>
</tr>
</table>

## Parameter

* **Umkehren** *Boolesch*\
  Kehrt das Ausgabebild um.
* **Skalierung** *Gleitend*\
  Steuert die Skalierung des fraktalen 3D-Perlin-Rauschens.
* **Größe** *Gleitend3*\
  Steuert die Größe des fraktalen 3D-Perlin-Rauschens in den Achsen **X**, **Y** und **Z**. Nicht einheitliche Werte führen zu einem *Dehnungs- oder Squashing*-Effekt.
* **Offset** *Float3*\
  Wendet einen Offset auf die *Position* des fraktalen 3D-Perlin-Rauschens in den Achsen **X**, **Y** und **Z** an.
* **Intensität der Verzerrung** *Gleitend*\
  Steuert die Intensität eines *Verkrümmungseffekts*, der auf das fraktale 3D-Perlin-Rauschen angewendet wird.
* **Verzerrung-Skalierungsmultiplikator** *Gleitend*\
  Steuert die Skalierung des *sich verformenden Musters*, das im Verkrümmungseffekt verwendet wird, der durch die **Intensität der Verzerrung** gesteuert wird.
* **Min Level** *Integer*\
  Die minimale *Wiederholungsstufe*, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem *reicheren Muster* mit Variationen in mehr Frequenzbereichen.
* **Max. Stufe** *Ganze Zahl*\
  Die maximale *Wiederholungsstufe*, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem *reicheren Muster* mit Variationen in mehr Frequenzbereichen.
* **Unregelmäßigkeit** *Unregelmäßigkeit*\
  Steuert die *Balance* zwischen niedrigen und hohen *Wiederholungsstufen* im fraktalen Muster.\
  *Hinweis*: Ein Wert von **0** führt zu einer Ausgabe, die *nicht in Zeile* enthält, auf die andere niedrige Werte folgen. Dies wird erwartet.
* **Lakunarität** *Gleitend*\
  Steuert, wie das angewendete fraktale Muster &quot;*&quot; Leerzeichen &quot;*&quot; ausfüllt. Ein *höherer* Wert führt zu *weniger Lücken* im Muster und einem *dichteren* Rauschen.
* **Globale Deckkraft** *Gleitend*\
  Steuert den *Bereich* der fraktalen 3D-Perlin-Störungswerte *um* den **Grundlinienwert**.
* **Grundlinie** *Gleitend*\
  Wendet einen *offset* auf den Grundwert *luminance* für die 3D-Perlin-Rauschwertverteilung an.
* **Kontrast** *Gleitend*\
  Passt den Kontrast des 3D-Perlin-Rauschens an.
* **Absolut** *Boolesch*\
  Verwendet absolute Werte im 3D-Perlin-Rauschen. Dadurch wird *die Wertverteilung für die Werte* unter 0,5 *effektiv umgekehrt*.
* **Kachelung aktivieren** *Boolesch*\
  Passt das 3D-Perlin-Rauschen so an, dass sich das resultierende Muster ** in der X-, Y- und Z-Achse wiederholt.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dfractal.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>

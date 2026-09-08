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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 3D Perlin Rauschen

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**In:** *Texturgeneratoren**/Noises*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Perlin Rauschen** generiert eine Perlin-Rauschen im 3D-Raum auf der Grundlage der Eingabe **Positionszuordnung**.

Dieser Knoten kann mit [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer tatsächlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

>[!WARNING]
>
> Dieses Geräusch soll nur mit dem *GPU-Modul verwendet werden* (d. h. **Direct3D** oder **OpenGL**). Wechseln Sie zu **Extras > Modul wechseln...** oder drücken Sie die Taste **F9**, um das gewünschte Modul auszuwählen.

</td>
</tr>
</table>

## Parameter

* **Umkehren** *Boolesche Wert*\
  Kehrt das Ausgabebild um.
* **Skalierung** *Fließkommazahl*\
  Steuert die Skalierung der 3D-Perlin-Rauschen.
* **Größe** *Fließkommazahl3*\
  Steuert die Größe der 3D-Perlin-Rauschen in den Achsen **X**, **Y** und **Z**. Nicht einheitliche Werte führen zu einem *Dehnungs- oder Squashing*-Effekt.
* **Offset** *Float3*\
  Wendet einen Offset auf die *Position* der 3D-Perlin-Rauschen in den Achsen **X**, **Y** und **Z** an.
* **Intensität der Verzerrung** *Gleitend*\
  Steuert die Intensität eines *Verkrümmungseffekts*, der auf der 3D-Perlin-Rauschen angewendet wird.
* **Verzerrung-Skalierungsmultiplikator** *Fließkommazahl*\
  Steuert die Skalierung des *sich verformenden Musters*, das im Verkrümmungseffekt verwendet wird, der durch die **Intensität der Verzerrung** gesteuert wird.
* **Grundlinie** *Fließkommazahl*\
  Wendet einen *offset* auf den Basiswert *Luminanz* für die Werteverteilung der 3D-Perlin-Rauschen an.
* **Kontrast** *Fließkommazahl*\
  Passt den Kontrast der 3D-Perlin-Rauschen an.
* **Absolut** *Boolesche Wert*\
  Verwendet absolute Werte auf der 3D-Perlin-Rauschen. Dadurch wird *die Wertverteilung für die Werte* unter 0,5 *effektiv umgekehrt*.
* **Kachelung aktivieren** *Boolesche Wert*\
  Passt die 3D-Perlin-Rauschen so an, dass sich das resultierende Muster *in X-, Y- und Z-Achse wiederholt*.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>

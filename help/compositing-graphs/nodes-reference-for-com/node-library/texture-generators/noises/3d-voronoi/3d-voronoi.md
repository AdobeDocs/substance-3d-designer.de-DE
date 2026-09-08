---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: Verwenden Sie den 3D-Voronoi-Knoten, um Voronoi-Muster zu generieren, die auf der 3D-Weltposition basieren, um volumetrische zelluläre Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi.png){width="200px"}

**In:** *Texturgeneratoren* */Noises*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **3D Voronoi** generiert eine Voronoi-Rauschen im 3D-Raum auf der Grundlage der Eingabe **Positionsmap**.

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
  Steuert die Skalierung der 3D-Voronoi-Rauschen.\
  *Hinweis*: Wenn **Kacheln** auf *einer Achse* aktiviert ist, ist die Skalenanpassung *gestuft*. Dies wird erwartet.
* **Größe** *Fließkommazahl3*\
  Steuert die Größe der 3D-Voronoi-Rauschen in den Achsen **X**, **Y** und **Z**. Nicht einheitliche Werte führen zu einem *Dehnungs- oder Squashing*-Effekt.\
  *Hinweis*: Wenn **Kachelung** für *eine beliebige Achse* aktiviert ist, ist die Größenanpassung *schrittweise*. Dies wird erwartet.
* **Offset** *Float3*\
  Wendet einen Offset auf die *Position* der 3D-Voronoi-Rauschen in den Achsen **X**, **Y** und **Z** an.
* **Störung** *Float3*\
  Die Intensität des *zufälligen Versatzes*, der auf jeden Punkt des Rauschens in den Achsen **X**, **Y** und **Z** angewendet wird.
* **Intensität der Verzerrung** *Gleitend*\
  Steuert die Intensität eines *Verkrümmungseffekts*, der auf das 3D-Voronoi-Rauschen angewendet wird.
* **Verzerrung-Skalierungsmultiplikator** *Fließkommazahl*\
  Steuert die Skalierung des *sich verformenden Musters*, das im Verkrümmungseffekt verwendet wird, der durch die **Intensität der Verzerrung** gesteuert wird.
* **Abgerundete Kurve** *Gleitkomma*\
  Rundet die *Steigung* um jeden Punkt des Rauschens, um sie *konvex* zu machen.\
  *Hinweis* : Dieser Parameter ist nicht verfügbar, wenn der **Style**-Parameter auf *Edge* festgelegt ist.
* **Abstandsskala** *Gleitend*\
  Passt den *Abstand des Farbverlaufs* um jeden Punkt des Rauschens an.
* **Entfernungsmodus** *Ganzzahl*\
  Legt die Methode auf *fest, um den Abstandsverlauf* um jeden Punkt der Rauschen zu berechnen:
  * *Euklidean*
  * *Manhattan*
  * *Chebyshev*
  * *Minkowski*
* **Minkowski-Zahl** *Gleitend*\
  Die Reihenfolge *p* der Minkowski-Entfernung. Wenn wir den Abstandsverlauf in Quadranten unterteilen, wirkt sich diese Zahl wie folgt auf diese Quadranten aus:
  * p ist *genau* 1: Gerade
  * p ist *niedriger* als 1: konkav
  * p ist *größer* als 1: konvex\
    Interessante Werte:\
    *- 1.0*: Entfernung von Manhattan\
    *- 2.0*: Euklidische Entfernung\
    *- Unendlich*: Chebyshev-Abstand\
    *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Entfernungsmodus** auf *Minkowski* festgelegt ist.
* **Stil** *Ganzzahl* Legt die *-Methode für das Rendern der Daten* der 3D-Voronoi-Rauschen fest, da die Rauschen auf einem Satz von 3D-Leerzeichen basiert:
  * *F1*: der Abstand zum *nächstgelegenen Punkt* im 3D-Raum
  * *F2*: der Abstand zum *zweitnächsten Punkt* im 3D-Raum
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: die* Kante zwischen jeder Zelle* der Rauschen im 3D-Raum
  * *Zufallsfarbe*: jeder Zelle der Rauschen im 3D-Raum eine *zufällige Flächenfarbe* zuweisen
* **Edge-Thickness** *Fließkommazahl* Passt die Thickness der Kanten an, die zwischen den Zellen der 3D-Voronoi-Rauschen erkannt werden. Kanten werden in der X-, Y- und Z-Achse erkannt, daher können einige Stärken schneller zunehmen als andere, je nach *Tiefe* der Zellen.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Edge* festgelegt ist.
* **Kachelung aktivieren** *Boolesche Wert*\
  Passt die 3D-Voronoi-Rauschen so an, dass sich das resultierende Muster *in X-, Y- und Z-Achse wiederholt*.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>

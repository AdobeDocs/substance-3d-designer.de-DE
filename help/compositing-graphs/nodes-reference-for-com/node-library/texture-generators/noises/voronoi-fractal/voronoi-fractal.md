---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Voronoi Fractal, um fraktale Voronoi-Muster zur Erstellung organischer zellulärer Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal.png){width="200px"}

**In:** *Texturgeneratoren* */Noises*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Voronoi Fractal** erzeugt ein *fraktales* 3D-Voronoi-Rauschen, das einem 2D-Bild mithilfe einer orthografischen *Z-down-Projektion* zugeordnet ist.

Dieser Knoten kann mit [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer eigentlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

>[!WARNING]
>
> Dieses Geräusch darf nur mit dem *GPU-Modul verwendet werden* (d. h. **Direct** oder **OpenGL**). Wechseln Sie zu **Extras > Modul wechseln...** oder drücken Sie die Taste **F9**, um das gewünschte Modul auszuwählen.

</td>
</tr>
</table>

## Parameter

* **Umkehren** *Boolesch*\
  Kehrt das Ausgabebild um.
* **Skalierung** *Gleitend*\
  Steuert die Skalierung des fraktalen Voronoi-Rauschens.\
  *Hinweis*: Wenn **Kacheln** auf *einer Achse* aktiviert ist, ist die Skalenanpassung *gestuft*. Dies wird erwartet.
* **Größe** *Gleitend3*\
  Steuert die Größe des fraktalen Voronoi-Rauschens in den Achsen **X**, **Y** und **Z**. Nicht einheitliche Werte führen zu einem *Dehnungs- oder Squashing*-Effekt.\
  *Hinweis*: Wenn **Kacheln** auf *einer Achse* aktiviert ist, ist die Größenanpassung *schrittweise*. Dies wird erwartet.
* **Offset** *Float3*\
  Wendet einen Offset auf die *Position* des fraktalen Voronoi-Rauschens in den Achsen **X**, **Y** und **Z** an.
* **Störung** *Float3*\
  Die Intensität des *zufälligen Versatzes*, der auf jeden Punkt des Rauschens in den Achsen **X**, **Y** und **Z** angewendet wird.
* **Intensität der Verzerrung** *Gleitend*\
  Steuert die Intensität eines *Verkrümmungseffekts*, der auf das fraktale Voronoi-Rauschen angewendet wird.
* **Verzerrung-Skalierungsmultiplikator** *Gleitend*\
  Steuert die Skalierung des *sich verformenden Musters*, das im Verkrümmungseffekt verwendet wird, der durch die **Intensität der Verzerrung** gesteuert wird.
* **Min Level** *Integer*\
  Die minimale *Wiederholungsstufe*, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem *reicheren Muster* mit Variationen in mehr Frequenzbereichen.
* **Max. Stufe** *Ganze Zahl*\
  Die maximale *Wiederholungsstufe*, die im fraktalen Muster verwendet wird. Ein größerer Mindest-/Höchstbereich führt zu einem *reicheren Muster* mit Variationen in mehr Frequenzbereichen.
* **Unregelmäßigkeit** *Unregelmäßigkeit*\
  Steuert die *Balance* zwischen niedrigen und hohen *Wiederholungsstufen* im fraktalen Muster.\
  *Hinweis*: Ein Wert von **0** führt zu einer Ausgabe, die *nicht in Zeile* enthält, auf die andere niedrige Werte folgen. Dies wird erwartet.\
  *Hinweis 2*: Dieser Parameter ist nur verfügbar, wenn der Parameter **Überblendmodus** auf *Hinzufügen* festgelegt ist.
* **Lakunarität** *Gleitend*\
  Steuert, wie das angewendete fraktale Muster &quot;*&quot; Leerzeichen &quot;*&quot; ausfüllt. Ein *höherer* Wert führt zu *weniger Lücken* im Muster und einem *dichteren* Rauschen.
* **Globale Deckkraft** *Gleitend*\
  Steuert den *Bereich* der fraktalen Perlin-Rauschwerte von 0.
* **Abgerundete Kurve** *Gleitkomma*\
  Rundet die *Steigung* um jeden Punkt des Rauschens, um sie *konvex* zu machen.\
  *Hinweis*: Dieser Parameter ist nicht verfügbar, wenn der **Style**-Parameter auf *Edge* festgelegt ist.
* **Abstandsskala** *Gleitend*\
  Passt den *Abstand des Farbverlaufs* um jeden Punkt des Rauschens an.
* **Abstandsmodus** *Ganze Zahl*\
  Legt die Methode auf *Berechnen des Abstandsverlaufs* um jeden Punkt des Rauschens fest:
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
* **Füllmethode** *Ganzzahl*\
  Legt die Methode für das Mischen der Werte von *überlappenden Zellen* im Raum fest:
  * *Hinzufügen*: Werte hinzufügen.
  * *Max*: *höchster* Wert beibehalten
  * *Min*: *niedrigste* Werte beibehalten
* **Stil** *Ganzzahl* Legt die Methode *fest, die die Daten* des fraktalen Voronoi-Rauschens rendert, da das Rauschen auf einem Satz von Punkten im Raum basiert:
  * *F1*: der Abstand zum *nächstgelegenen Punkt* im Raum
  * *F2*: der Abstand zum *zweitnächsten Punkt* im Raum
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: die* Kante zwischen jeder Zelle* des Rauschens im Raum
  * *Zufallsfarbe*: jeder Zelle des Rauschens im Raum eine *zufällige flache Farbe* zuweisen
* **Kantenzelle** *Unverankert* Passt die Thickness der Thicknessen an, die zwischen den Zellen des fraktalen Voronoi-Rauschens erkannt werden. Kanten werden in der X-, Y- und Z-Achse erkannt, daher können einige Stärken schneller zunehmen als andere, je nach *Tiefe* der Zellen.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Edge* festgelegt ist.
* **Zufälliger Farbmodus** *Ganzzahl*\
  Legt die Methode für *fest, mit der* der Zufallswert für die Farbauswahl pro Zelle erfasst wird:
  * *Globale Zufallsverteilung*: Verwenden Sie das vom Knoten geerbte Seed *geerbt*
  * *Manuelles Seed*: Verwenden eines *einzelnen*-Seeds\
    *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Random color* festgelegt ist.
* **Zufallsfarbausgang** *Ganzzahl*\
  Der diskrete Zufallswert, der für die Farbauswahl pro Zelle verwendet werden soll.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Zufallsfarbe* und der **Zufallsfarben-Übertragungsmodus**-Parameter auf *Manuelle Übertragung* festgelegt ist.
* **Kachelung aktivieren** *Boolesch*\
  Passt das fraktale Voronoi-Rauschen so an, dass sich das resultierende Muster ** in der X-, Y- und Z-Achse wiederholt.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-sea.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-scifi-panel.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant4.jpg){width="256px"}

</td>
</tr>
</table>

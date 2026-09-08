---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Verwenden Sie den Voronoi-Knoten, um Voronoi-Muster zu generieren, um zelluläre Texturen und organische Materialeffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**In:** *Texturgeneratoren* */Noises*

**Fortgeschrittene**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten **Voronoi** erzeugt ein 3D-Voronoi-Rauschen, das einem 2D-Bild mithilfe einer orthografischen *Z-down-Projektion* zugeordnet ist.

Dieser Knoten kann mit [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer eigentlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

>[!WARNING]
>
> Dieses Geräusch darf nur mit dem *GPU-Modul verwendet werden* (d. h. **Direct** oder **OpenGL**). Wechseln Sie zu **Extras > Modul wechseln...** oder drücken Sie die Taste **F9**, um das gewünschte Modul auszuwählen.

</td>
</tr>
</table>

## Parameter

* **Umkehren** *Boolesche Wert*\
  Kehrt das Ausgabebild um.
* **Skalierung** *Fließkommazahl*\
  Steuert den Umfang des Voronoi-Rauschens.\
  *Hinweis*: Wenn **Kacheln** auf *einer Achse* aktiviert ist, ist die Skalenanpassung *gestuft*. Dies wird erwartet.
* **Größe** *Fließkommazahl3*\
  Steuert die Größe des Voronoi-Rauschens in den Achsen **X**, **Y** und **Z**. Nicht einheitliche Werte führen zu einem *Dehnungs- oder Squashing*-Effekt.\
  *Hinweis*: Wenn **Kachelung** für *eine beliebige Achse* aktiviert ist, ist die Größenanpassung *schrittweise*. Dies wird erwartet.
* **Offset** *Float3*\
  Wendet einen Offset auf die *Position* des Voronoi-Rauschens in den Achsen **X**, **Y** und **Z** an.
* **Störung** *Float3*\
  Die Intensität des *zufälligen Versatzes*, der auf jeden Punkt des Rauschens in den Achsen **X**, **Y** und **Z** angewendet wird.
* **Intensität der Verzerrung** *Gleitend*\
  Steuert die Intensität eines *Verkrümmungseffekts*, der auf die Voronoi-Rauschen angewendet wird.
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
* **Stil** *Ganzzahl* Legt die *Methode zum Rendern der Daten* der Voronoi-Rauschen fest, da die Rauschen auf einer Menge von Leerzeichen basiert:
  * *F1*: der Abstand zum *nächstgelegenen Punkt* im Raum
  * *F2*: der Abstand zum *zweitnächsten Punkt* im Raum
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: die* Kante zwischen jeder Zelle* des Rauschens im Raum
  * *Zufallsfarbe*: jeder Zelle der Rauschen im Raum eine *zufällige flache Farbe* zuweisen
* **Edge-Thickness** *Fließkommazahl* Passt die Thickness der Kanten an, die zwischen den Zellen der Voronoi-Rauschen erkannt werden. Kanten werden in der X-, Y- und Z-Achse erkannt, daher können einige Stärken schneller zunehmen als andere, je nach *Tiefe* der Zellen.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Edge* festgelegt ist.
* **Zufallsfarben-Startmodus** *Ganzzahl*\
  Legt die Methode für *fest, mit der* den zufälligen Seed für die Farbauswahl pro Zelle erfasst wird:
  * *Globale Zufallsverteilung*: Verwenden Sie das vom Knoten geerbte Seed *geerbt*
  * *Manuelles Seed*: Verwenden eines *einzelnen*-Seeds\
    *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Random color* festgelegt ist.
* **Zufallsfarbensamen** *Ganzzahl*\
  Der diskrete Zufallswert, der für die Farbauswahl pro Zelle verwendet werden soll.\
  *Hinweis*: Dieser Parameter ist nur verfügbar, wenn der **Style**-Parameter auf *Zufallsfarbe* und der **Zufallsfarben-Übertragungsmodus**-Parameter auf ***Manuelle Übertragung*** festgelegt ist.
* **Quadratische Ausbreitung** *Boolesche Wert*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.

## Beispielbilder

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>

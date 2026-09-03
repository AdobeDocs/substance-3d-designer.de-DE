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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3d-voronoi-01.png){width="200px"}

<b>In:</b> Textur Generators > Rauschen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der Knoten <b>3D Voronoi</b> generiert eine Voronoi-Rauschen im 3D-Raum auf der Grundlage der Eingabe <b>Positionsmap</b>.

Dieser Knoten kann mit [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) als Eingabe anstelle einer tatsächlichen durch Baking erzeugte Map (wie im folgenden Beispielbild) getestet werden.

</td>
</tr>
</table>

>[!WARNING]
>
> Dieses Geräusch soll nur mit dem <i>GPU-Modul verwendet werden</i> (d. h. <b>Direct3D</b> oder <b>OpenGL</b>). Wechseln Sie zu <b>Extras > Engine wechseln...</b> oder drücken Sie die Taste <b>F9</b>, um das gewünschte Engine auszuwählen.

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Umkehren</b> <i>Boolescher Wert</i> | Kehrt das Ausgabebild um. |
| <b>Skalierung</b> <i>Fließkommazahl</i> | Steuert die Skalierung der 3D-Voronoi-Rauschen.<br><br><i>Hinweis</i>: Wenn <b>Kacheln</b> auf <i>einer Achse</i> aktiviert ist, ist die Skalenanpassung <i>gestuft</i>. Dies wird erwartet. |
| <b>Größe</b> <i>Fließkommazahl3</i> | Steuert die Größe der 3D-Voronoi-Rauschen in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b>. Nicht einheitliche Werte führen zu einem <i>dehnend oder auslöschenden </i>-Effekt.<br><br><i>Hinweis</i>: Wenn <b>Kachelung</b> für <i>eine beliebige Achse</i> aktiviert ist, ist die Größenanpassung <i>schrittweise</i>. Dies wird erwartet. |
| <b>Offset</b> <i>Float3</i> | Wendet einen Offset auf die <i>Position</i> der 3D-Voronoi-Rauschen in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b> an. |
| <b>Störung</b> <i>Fließkommazahl3</i> | Die Intensität des <i>zufälligen Versatzes</i>, der auf jeden Punkt des Rauschens in den Achsen <b>X</b>, <b>Y</b> und <b>Z</b> angewendet wird. |
| <b>Intensität der Verzerrung</b> <i>Gleitend</i> | Steuert die Intensität eines <i>Verkrümmungseffekts</i>, der auf das 3D-Voronoi-Rauschen angewendet wird. |
| <b>Verzerrungen-Skalierungsmultiplikator</b> <i>Gleitend</i> | Steuert die Skalierung des <i>sich verformenden Musters</i>, das im Verkrümmungseffekt verwendet wird, der durch die <b>Intensität der Verzerrung</b> gesteuert wird. |
| <b>Abgerundete Kurve</b> <i>Gleitend</i> | Rundet die <i>Steigung</i> um jeden Punkt der Rauschen, um sie <i>konvex</i> zu machen.<br><br><i>Hinweis</i>: Dieser Parameter ist nicht verfügbar, wenn der <b>Style</b>-Parameter auf <i>Edge</i> festgelegt ist. |
| <b>Entfernungsskala</b> <i>Gleitend</i> | Passt den <i>Abstand des Farbverlaufs</i> um jeden Punkt des Rauschens an. |
| <b>Entfernungsmodus</b> <i>Integer</i> | Legt die Methode auf <i>Berechnen des Abstandsverlaufs</i> um jeden Punkt der Rauschen fest:<br><br>- <i>Euklidean</i><br>- <i>Manhattan</i><br>- <i>Chebyshev</i><br>- <i>Minkowski</i> |
| <b>Minkowski-Zahl</b> <i>Gleitend</i> | Die Reihenfolge <i>p</i> der Minkowski-Entfernung. Wenn wir den Abstandsverlauf in Quadranten unterteilen, wirkt sich diese Zahl wie folgt auf diese Quadranten aus:<br><br>- p ist <i>genau</i> 1: Straight<br>- p ist <i>niedriger</i> als 1: Konkav<br>- p ist <i>größer</i> als 1: Konvex<br><br>Interessante Werte:<br>- <i>1.0</i>: Entfernung von Manhattan<br>- <i>2.0</i>: Euklidische Entfernung<br>- <i>Unendlich</i>: Chebyshev-Abstand<br><br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der Parameter <b>Entfernungsmodus</b> auf <i>Minkowski</i> festgelegt ist. |
| <b>Stil</b> <i>Integer</i> | Legt die <i>-Methode zum Rendern der Daten</i> der 3D-Voronoi-Rauschen fest, da die Rauschen auf einer Punktmenge im 3D-Raum basiert:<br><br>- <i>F1</i>: Abstand zum <i>nächstgelegenen Punkt</i> im 3D-Raum<br>- <i>F2</i>: der Abstand zum <i>zweitnächsten Punkt</i> im 3D-Raum<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Edge</i>: die <i>Kante zwischen jeder Zelle</i> der Rauschen im 3D-Raum<br>- <i>Zufallsfarbe</i>: jeder Zelle der Rauschen im 3D-Raum eine <i>zufällige flache Farbe</i> zuweisen |
| <b>Edge-Thickness</b> <i>Gleitend</i> | Passt die Thickness der Kanten an, die zwischen den Zellen der 3D-Voronoi-Rauschen erkannt werden. Kanten werden in den X-, Y- und Z-Achsen erkannt, daher können einige Stärken schneller zunehmen als andere, je nach <i>Tiefe</i> der Zellen.<br><br><i>Hinweis</i>: Dieser Parameter ist nur verfügbar, wenn der <b>Style</b>-Parameter auf <i>Edge</i> festgelegt ist. |
| <b>Kachelung aktivieren</b> <i>Boolescher Wert</i> | Passt die 3D-Voronoi-Rauschen so an, dass sich das resultierende Muster <i>in X-, Y- und Z-Achse wiederholt</i>. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-07.jpg" />
        </td>
    </tr>
</table>

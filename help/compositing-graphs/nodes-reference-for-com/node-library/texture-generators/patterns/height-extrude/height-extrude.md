---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Über den Knoten "Höhenextrusion" können Sie Formen auf Basis von Höhen-Map extrudieren, um 3D-ähnliche Tiefen in Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Höhenextrusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# Höhenextrusion

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude.png){width="200px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Höhenextrusion rendert 3D Z-Tiefe von einer Eingabe-Höhen-Map. Genau wie bei [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) und [Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) können Sie eine Kamera in der 2D-Ansicht drehen. Sein Hauptziel ist es, als Generator zum Erstellen von 3D-gedrehten Formen aus einer flachen Höhenkarte zu dienen. Diese Formen können dann mit [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) verwendet werden.

Der Hauptunterschied zu [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) besteht darin, dass der Eingabe-Map kein binärer &quot;Alpha&quot;-Typ der Map sein muss, sondern eine Graustufenmap mit vollem Bereich. Das bedeutet, dass Sie mehr Kontrolle über das Extrusionsprofil haben (organische, komplexe Formen), aber keine Kontrolle über so etwas wie Abschrägungsprofile (Hard-Surface, einfachere Formen).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kamera Winkel</b> | Euler Winkel der Kamera, in halben Windungen. Bitte beachten Sie, dass horizontale Drehung und Skalierung direkt auf die Eingabe angewendet werden. |
| <b>Skalierung der Kamera</b> <i>0.001 - 3.0</i> | Auf die Ausgabe angewendete globale Skalierung. |
| <b>Height-Skalierung</b> <i>0.0 - 2.0</i> | Wendet einen globalen Faktor auf die Werte des Eingabe-Heights an. |
| <b>Vertikaler Versatz</b> <i>-1.0 - 1.0</i> | Verschiebt die endgültige Ausgabe nach oben oder unten. |
| <b>Boden</b> <i>Aus/Ein</i> | Wenn der Boden ausgeschaltet ist, wird ein schwarzer Hintergrund angezeigt, bei dem die Eingabe 0 ist, anstatt einer Boden-ähnlichen Ebene. |
| <b>Normales Format</b> <i>DirectX/OpenGL</i> | Der Parameter &quot;<b>Normalformat</b>&quot; kehrt die y-Koordinate der Normalen-Map um. |
| <b>Normalintensität</b> <i>0.0 - 256.0</i> | Entspricht dem <b>Intensität</b>-Parameter des <b>Normal</b>-Knotens. Setzen Sie den Wert auf 256, um beim Drehen eine schubfreie Normale zu erhalten. |

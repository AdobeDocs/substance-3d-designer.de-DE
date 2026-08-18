---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Über den Knoten "Höhenextrusion" können Sie Formen auf Basis von Height Maps extrudieren, um 3D-ähnliche Tiefen in Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Höhenextrusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Höhenextrusion

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## Höhenextrusion

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Höhenextrusion rendert 3D Z-Tiefe von einer Eingabe-Height-Map. Genau wie bei [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) und [Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) können Sie eine Kamera in der 2D-Ansicht drehen. Sein Hauptziel ist es, als Generator zum Erstellen von 3D-gedrehten Formen aus einer flachen Höhenkarte zu dienen. Diese Formen können dann mit [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) verwendet werden.

Der Hauptunterschied zu [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) besteht darin, dass die Eingabemap kein binärer &quot;Alpha&quot;-Typ der Map sein muss, sondern eine Graustufenmap mit vollem Bereich. Das bedeutet, dass Sie mehr Kontrolle über das Extrusionsprofil haben (organische, komplexe Formen), aber keine Kontrolle über so etwas wie Abschrägungsprofile (Hard-Surface, einfachere Formen).

## Parameter

* **Kamerawinkel**:\
  Euler Winkel der Kamera, in halben Umdrehungen. Bitte beachten Sie, dass horizontale Drehung und Skalierung direkt auf die Eingabe angewendet werden.
* **Kameraskala**: *0.001 - 3.0*\
  Auf die Ausgabe angewendete globale Skalierung.
* **Height-Skalierung**: *0.0 - 2.0*\
  Wendet einen globalen Faktor auf die Werte des Eingabe-Heights an.
* **Vertikaler Versatz**: *-1.0 - 1.0*\
  Verschiebt die endgültige Ausgabe nach oben oder unten.
* **Boden**: *Aus/Ein*\
  Wenn &quot;Ground&quot; deaktiviert ist, wird ein schwarzer Hintergrund angezeigt, bei dem die Eingabe 0 ist, nicht wie bei einer bodenähnlichen Ebene.
* **Normales Format**: *DirectX/OpenGL*\
  Der Parameter &quot;**Normalformat**&quot; kehrt die y-Koordinate der normalen Map um.
* **Normalintensität**: *0.0 - 256.0*\
  Entspricht dem **Intensität**-Parameter des **Normal**-Knotens. Setzen Sie den Wert auf 256, um beim Drehen eine schubfreie Normale zu erhalten.

## Beispielbilder

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Greifen Sie auf Samplerknoten in Substance 3D Designer-Funktionsdiagrammen zu, um Texturen auszuprobieren und Farbwerte zu extrahieren.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Sampler Nodes

![Sampler-Knoten](../../../../assets/image2016-1-12-14-45-43.png "Sampler-Knoten")

Diese Knoten nehmen einen Wert in einem Eingabebild an den angegebenen 2D-Koordinaten auf:

<b>Sample Gray</b> tastet einen Luminanzwert an der Eingabe <b>Position</b> in einem Graustufenbild ab und gibt diesen als <b>Float</b>-Wert aus.

<b>Sample Color</b> tastet einen RGBA-Wert an der Eingabe <b>Position </b> in einem Farbbild ab und gibt diesen als <b>Float4</b>-Wert aus, wobei die R-, G-, B- und A-Komponenten den X-, Y-, Z- bzw. W-Komponenten zugeordnet werden.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Koordinaten beginnen in der linken oberen Ecke einer Eingabe und liegen zwischen 0 und 1 horizontal und vertikal.

Positionen außerhalb dieses Bereichs werden gemäß dem ausgewählten <b>Adressierungsmodus</b> (siehe unten) behandelt.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Pixelkoordinaten](../../../../assets/samplercoords.png "Pixelkoordinaten")

</td>
</tr>
</table>

>[!NOTE]
>
> Die <b>Position</b>-Eingabe sollte ein Float2-Wert sein, bei dem die X- und Y-Koordinaten des Bildes den X- bzw. Y-Komponenten des Werts zugeordnet sind.

## Parameter

+++Eingabebild
Ermöglicht die Auswahl der Knoteneingabe, die für das Sampling verwendet werden soll.

Die Liste passt sich dynamisch an die aktuell angeschlossenen Eingänge an. Das bedeutet, dass Einträge hinzugefügt werden, wenn Sie Knoteneingänge verbinden.

Die Nummerierung der Eingänge beginnt bei 0, sodass ein Bild, das mit dem ersten Eingang des Knotens verbunden ist, als *Eingabebild 0* aufgeführt wird.

+++

+++Filtermodus
Hier können Sie festlegen, wie mit Interpolation umgegangen werden soll, wenn Pixel aus dem aufgenommenen Bild aufgrund von Auflösungsunterschieden nicht genau dem Ausgabebild zugeordnet werden.

<b>Nächste</b>\
Das Pixel wird dem Ziel &quot;*wie vorhanden*&quot; an der entsprechenden Koordinate zugeordnet. Wenn das Ziel eine niedrigere Auflösung hat, kann das Pixel vollständig ignoriert werden. wenn das Ziel eine höhere Auflösung hat; es wird allen Pixeln zugeordnet, die seine Spanne abdecken. Die Ausgabe ist *schärfer* und sieht leicht *verzerrt* aus.

<b>Bilineare Filterung</b>\
Ein Filtervorgang wird auf das Quellbild angewendet, sodass seine Pixel der Zielauflösung auf eine Weise zugeordnet werden, dass *die Übergänge zwischen den Pixeln glättet*. Die Ausgabe ist *glatter* und sieht leicht *unscharf* aus.

+++

+++Adressierungsart
Steuert, wie Positionswerte außerhalb des Bereichs [0;1] behandelt werden.

<b>Wiederholen</b>\
Schleifen über den Bereich [0;1], wenn der Wert zunimmt.\
Beispiel: 3.4 ist 0.4, -1.7 ist 0.3.

<b>An Kante festhalten</b>\
Klammert Werte bis zum Bereich [0;1] an den nächstgelegenen Grenzwert an.\
Beispiel: .3.4 ist 1, -1.7 ist 0.

+++

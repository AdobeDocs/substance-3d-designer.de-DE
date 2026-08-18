---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Pfade, Scheitelpunkt-Prozessor", um Pfadscheitelpunkte mit erweiterten Optionen zu transformieren und zu bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfade-Scheitelpunktprozessor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# Pfade-Scheitelpunktprozessor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/paths-vertex-processor-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine Transformation auf die Scheitelpunkt-Position der Eingabe <b>Pfade</b> an.

Der Knoten sollte wie folgt verwendet werden:

1. Bearbeiten Sie die <b>Parameterfunktion der </b>Funktion pro Vertex.
1. <b>Float2</b>-Knoten zum Abrufen verwenden; die Variablen *vertex.pos*, *prev.pos* und/oder *next.pos*
1. Führen Sie einige Vorgänge mit diesen Werten durch (z. B. Multiplizieren, um die Pfade zu skalieren).
1. Legen Sie das Ergebnis Ihrer Berechnung als Ausgabe fest.

</td>
</tr>
</table>

Stellen Sie sicher, dass Sie die entsprechenden <b>Werte für frühere Scheitelpunkte, auf die zugegriffen wurde</b>, und <b>Werte für nächste Scheitelpunkte, auf die zugegriffen wurde</b>, festlegen, bevor Sie *prev.pos* oder *next.pos* abfragen.\
Sie können auch Eingabebilder hinzufügen und von der Funktion aufnehmen. Sie müssen zuerst einen Eingang verbinden, um ihn von der Funktion abtasten zu können. (Vorsicht, die erste Eingabe ist *Image 1*!)\
Sie können auch auf die Variablen *prev[2].pos* (Float2), *next[2].pos* (Float2), *vertex.corner* (bool) und *path.id* (float) zugreifen.

>[!TIP]
>
> Für fortgeschrittene Benutzer wird in der [Paths Format Specification](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) erläutert, wie die Daten von Pfaden in Farbbildern codiert werden, und es werden Tipps zum direkten Bearbeiten dieser Daten bereitgestellt.

>[!NOTE]
>
> Siehe auch [Paths Vertex Processor Simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

## Eingangsanschlüsse

<b>Pfade</b> *Farbe*\
Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen *Pfad*-Verarbeitungsknoten.

<b>Eingabe #</b> *Farbe/Graustufen*\
Eingaben für Bilder, die in der Parameterfunktion <b>Funktion pro Vertex</b> gesampelt werden sollen.

## Ausgangsanschlüsse

<b>Pfade</b> *Farbe*\
Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten.

## Parameter

<b>Zugriff auf vorherige Eckpunkte</b> *Integer*\
Mit diesem Parameter können Sie die Position des vorherigen Scheitelpunkts entlang des Pfads (*prev.pos*) und des vorherigen vorherigen Scheitelpunkts (*prev[2].pos*) mithilfe von <b>Get</b>-Knoten in der Parameterfunktion <b>Funktion pro Vertex</b> abrufen.

<b>Zugriff auf nächste Eckpunkte</b> *Integer*\
Mit diesem Parameter können Sie die Position des folgenden Scheitelpunkts entlang des Pfads (*next.pos*) und des folgenden Scheitelpunkts (*next[2].pos*) mithilfe von <b>Get</b>-Knoten in der Parameterfunktion <b>Funktion pro Vertex</b> abrufen.

<b>Anzahl der Bildeingaben</b> *Integer*\
Die Anzahl der sichtbaren <b>Eingabe-#</b>-Eingangsverbindungen zum Verbinden von Bildern, die in der Parameterfunktion <b>Funktion pro Vertex</b> abgetastet werden sollen.\
Wenn Sie alle gewünschten Samples eingerichtet haben, können Sie nicht verwendete Pins ausblenden, indem Sie den Wert dieses Parameters auf 0 zurücksetzen.

<b>Funktion pro Vertex</b> *Float2*\
Funktion angewendet für jeden Scheitelpunkt. Die neue Scheitelpunktposition muss zurückgegeben werden.\
Weitere Informationen finden Sie im Abschnitt <b>Beschreibung</b> auf dieser Seite.

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](../../../../../../assets/PathsVertexProcessor-Demo2.gif "Knotenbeispiel 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

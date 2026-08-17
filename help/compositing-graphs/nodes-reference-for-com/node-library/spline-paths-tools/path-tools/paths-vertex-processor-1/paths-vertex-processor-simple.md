---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Pfade, Scheitelpunkt-Prozessor einfach , um Pfadscheitelpunkte mit vereinfachten Transformationsoptionen zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pfade Scheitelpunktprozessor Einfach
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Pfade Scheitelpunktprozessor Einfach

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](../../../../../../assets/paths-vertex-processor-simple-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine Transformation auf die Scheitelpunkt-Position der Eingabe <b>Pfade</b> an.

1. Bearbeiten Sie die Parameterfunktion <b>Funktion pro Vertex</b>.
1. Verwenden Sie einen <b>Get Float2</b>-Knoten in der *vertex.pos*-Variablen.
1. Führen Sie einige Vorgänge für diesen Wert aus (z. B. multiplizieren Sie ihn, um die Pfade zu skalieren).
1. Legen Sie das Ergebnis Ihrer Berechnung als Ausgabe fest.

</td>
</tr>
</table>

Sie können Eingabebilder verwenden und sie von der Funktion aufnehmen. Sie müssen zuerst einen Eingang verbinden, um ihn von der Funktion abtasten zu können. (Vorsicht, die erste Eingabe ist *Image 1*!)\
Sie können auch auf die Variablen *vertex.corner* (bool) und *path.id* (float) zugreifen.

>[!TIP]
>
> Für fortgeschrittene Benutzer wird in der [Paths Format Specification](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) erläutert, wie die Daten von Pfaden in Farbbildern codiert werden, und es werden Tipps zum direkten Bearbeiten dieser Daten bereitgestellt.

>[!NOTE]
>
> Siehe auch [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

## Eingangsanschlüsse

<b>Pfade</b> *Farbe*\
Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten.

<b>Eingabe #</b> *Farbe/Graustufen*\
Eingaben für Bilder, die in der Parameterfunktion <b>Funktion pro Vertex</b> gesampelt werden sollen.

## Ausgangsanschlüsse

<b>Pfade</b> *Farbe*\
Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten.

## Parameter

<b>Anzahl der Bildeingaben</b> *Integer* Die Anzahl der sichtbaren <b>Eingabe-#</b>-Eingangsverbindungen zum Verbinden von Bildern, die in der Parameterfunktion <b>Funktion pro Vertex</b> abgetastet werden sollen.\
Wenn Sie alle gewünschten Samples eingerichtet haben, können Sie nicht verwendete Pins ausblenden, indem Sie den Wert dieses Parameters auf 0 zurücksetzen.\
Wenn Sie mehr Eingaben benötigen, verwenden Sie stattdessen den [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

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

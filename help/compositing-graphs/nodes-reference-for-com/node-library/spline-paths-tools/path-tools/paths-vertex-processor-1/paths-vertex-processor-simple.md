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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Pfade Scheitelpunktprozessor Einfach

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine Transformation auf die Position des Scheitelpunkts der Eingabe <b>Pfade</b> an.

1. Bearbeiten Sie die Parameterfunktion <b>Funktion pro Vertex</b>.
1. Verwenden Sie einen <b>Get Fließkommazahl2</b>-Knoten in der *Scheitelpunkt.pos*-Variablen.
1. Führen Sie einige Vorgänge für diesen Wert aus (z. B. multiplizieren Sie ihn, um die Pfade zu skalieren).
1. Legen Sie das Ergebnis Ihrer Berechnung als Ausgabe fest.

</td>
</tr>
</table>

Sie können Eingabebilder verwenden und sie von der Funktion aufnehmen. Sie müssen zuerst einen Eingang verbinden, um ihn von der Funktion abtasten zu können. (Vorsicht, die erste Eingabe ist *Image 1*!)\
Sie können auch auf die Variablen *Scheitelpunkt.corner* (bool) und *path.id* (float) zugreifen.

>[!TIP]
>
> Für fortgeschrittene Benutzer wird in der [Paths Format Specification](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) erläutert, wie die Daten von Pfaden in Farbbildern codiert werden, und es werden Tipps zum direkten Bearbeiten dieser Daten bereitgestellt.

>[!NOTE]
>
> Siehe auch [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen Pfadverarbeitungsknoten. |
| <b>Eingabe #</b> <i>Farbe/Graustufen</i> | Eingaben für Bilder, die in der Parameterfunktion <b>Funktion pro Vertex</b> gesampelt werden sollen. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Die veränderten Pfade. Sie können entweder [Pfadevorschau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) verwenden, um eine Vorstellung davon zu erhalten, was das Ergebnis darstellt, einen anderen Pfadeverarbeitungsknoten verwenden oder ihn in einen [Pfad zu Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) eingeben, um ihn als Splines weiter zu verarbeiten. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Anzahl der Bildeingaben</b> <i>Integer</i> | Die Anzahl der sichtbaren <b>Eingabe-#</b>-Eingangsverbindungen zum Verbinden von Bildern, die in der Parameterfunktion <b>Funktion pro Vertex</b> abgetastet werden sollen.<br>Nachdem Sie alle gewünschten Beispiele eingerichtet haben, können Sie nicht verwendete Nadeln ausblenden, indem Sie den Wert dieses Parameters auf 0 zurücksetzen.<br>Wenn Sie weitere Eingaben benötigen, verwenden Sie stattdessen den [Pfade-Scheitelpunkt-Prozessor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). |
| <b>Funktion pro Vertex</b> <i>Float2</i> | Funktion angewendet für jeden Scheitelpunkt. Die neue Scheitelpunktposition muss zurückgegeben werden.<br>Weitere Informationen finden Sie im Abschnitt <b>Beschreibung</b> auf dieser Seite. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](paths-vertex-processor-simple.resources/PathsVertexProcessor-Demo2.gif "Knotenbeispiel 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

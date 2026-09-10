---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
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
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Pfade-Scheitelpunktprozessor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Knotensymbol](paths-vertex-processor.resources/paths-vertex-processor-icon.png "Knotensymbol")

<b>In:</b> Spline &amp; Path Tools > Path Tools

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Wendet eine Transformation auf die Position des Scheitelpunkts der Eingabe <b>Pfade</b> an.

Der Knoten sollte wie folgt verwendet werden:

1. Bearbeiten Sie die <b>Parameterfunktion der </b>Funktion pro Vertex.
1. <b>Fließkommazahl2</b>-Knoten zum Abrufen verwenden; die Variablen *Scheitelpunkt.pos*, *prev.pos* und/oder *next.pos*
1. Führen Sie einige Vorgänge mit diesen Werten durch (z. B. Multiplizieren, um die Pfade zu skalieren).
1. Legen Sie das Ergebnis Ihrer Berechnung als Ausgabe fest.

</td>
</tr>
</table>

Stellen Sie sicher, dass Sie die entsprechenden <b>Werte für die vorherigen Scheitelpunkt, auf die zugegriffen wurde</b>, und <b>Werte für die nächsten Scheitelpunkt, auf die zugegriffen wurde</b>, festlegen, bevor Sie *prev.pos* oder *next.pos* abfragen.\
Sie können auch Eingabebilder hinzufügen und von der Funktion aufnehmen. Sie müssen zuerst einen Eingang verbinden, um ihn von der Funktion abtasten zu können. (Vorsicht, die erste Eingabe ist *Image 1*!)\
Sie können auch auf die Variablen *prev[2].pos* (Fließkommazahl2), *next[2].pos* (Fließkommazahl2), *Scheitelpunkt.corner* (bool) und *path.id* (float) zugreifen.

>[!TIP]
>
> Für fortgeschrittene Benutzer wird in der [Paths Format Specification](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) erläutert, wie die Daten von Pfaden in Farbbildern codiert werden, und es werden Tipps zum direkten Bearbeiten dieser Daten bereitgestellt.

>[!NOTE]
>
> Siehe auch [Paths Vertex Processor Simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Pfade</b> <i>Farbe</i> | Eine Liste der codierten Segmentpfade. Verbinden Sie diese Eingabe mit dem Ergebnis einer [Maske mit Pfaden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) oder mit einem anderen *Pfad*-Verarbeitungsknoten. |
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
| <b>Zugriff auf vorherige Eckpunkte</b> <i>Integer</i> | Mit diesem Parameter können Sie die Position des vorherigen Scheitelpunkts entlang des Pfads (*prev.pos*) und des vorherigen vorherigen Scheitelpunkts (*prev[2].pos*) mithilfe von <b>Get</b>-Knoten in der Parameterfunktion <b>Funktion pro Vertex</b> abrufen. |
| <b>Zugriff auf nächste Eckpunkte</b> <i>Integer</i> | Mit diesem Parameter können Sie die Position des folgenden Scheitelpunkts entlang des Pfads (*next.pos*) und des folgenden Scheitelpunkts (*next[2].pos*) mithilfe von <b>Get</b>-Knoten in der Parameterfunktion <b>Funktion pro Vertex</b> abrufen. |
| <b>Anzahl der Bildeingaben</b> <i>Integer</i> | Die Anzahl der sichtbaren <b>Eingabe-#</b>-Eingangsverbindungen zum Verbinden von Bildern, die in der Parameterfunktion <b>Funktion pro Vertex</b> abgetastet werden sollen.<br>Nachdem Sie alle gewünschten Beispiele eingerichtet haben, können Sie nicht verwendete Nadeln ausblenden, indem Sie den Wert dieses Parameters auf 0 zurücksetzen. |
| <b>Funktion pro Vertex</b> <i>Float2</i> | Funktion angewendet für jeden Scheitelpunkt. Die neue Scheitelpunktposition muss zurückgegeben werden.<br>Weitere Informationen finden Sie im Abschnitt <b>Beschreibung</b> auf dieser Seite. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Knotenbeispiel 2](paths-vertex-processor.resources/PathsVertexProcessor-Demo2.gif "Knotenbeispiel 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

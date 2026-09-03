---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence-nodes.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie SetSequence-Knoten in FXMaps verwenden, um sequenzielle Muster und prozedurale Varianten zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the SetSequence nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verwenden der SetSequence-Knoten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---


# Verwenden der Set-/Sequenzknoten

Auf dieser Seite werden die Knoten &quot;**Set**&quot; und &quot;**Sequence**&quot; beschrieben und ein Anwendungsbeispiel im Kontext von &quot;**FX-Maps**&quot; bereitgestellt.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Überblick

Bei der Arbeit mit Funktionen in <b>FX-Maps</b> befinden Sie sich gelegentlich in Situationen, in denen Sie einen Wert aus dem *[Substance-Funktionsdiagramm eines Parameters](../../../../function-graphs/the-function-graph/the-function-graph.md)* ausgeben möchten, sodass Sie ihn *in einem anderen Funktionsdiagramm verwenden können.* Standardmäßig gibt ein Substance-Funktionsdiagramm jedoch nur den Wert *one* aus: der, der den zugehörigen Parameter steuert.

</td>
<td style="border: 0;" valign="top">

![Set- und Sequenzknoten](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-01.png "Set- und Sequenzknoten")

</td>
</tr>
</table>

In diesem Fall können Sie die Kombination aus <b>Set</b> und <b>Sequence</b>-Knoten verwenden, mit der Sie Variablen über eine einzelne oder mehrere Funktionen hinweg steuern können.

Dieser Vorgang umfasst zwei Schritte:

1. Mit dem Knoten <b>Set</b> können Sie eine neue Variable erstellen, sodass Sie sie an einer anderen Stelle aufrufen und ihr einen Wert zuweisen können.
1. Der Knoten <b>Sequenz</b> wird verwendet, um die Logik in Schritt 1 vollständig auszuführen, *bevor ein weiterer Zweig* des Grafen ausgeführt wird - z. B. die Logik, die tatsächlich an der Ausgabe des erwarteten Werts für den aktuellen Graf beteiligt ist.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Der Knoten &quot;Festlegen&quot;

Mit dem Knoten <b>Set</b> können Sie eine neue Variable festlegen und ihr den Typ und den Wert zuweisen, der mit dem Eingang ** des Knotens verbunden ist.

Der *Name* der Variable wird vom Benutzer in die Eigenschaften des Knotens eingegeben.

Standardmäßig ist die von diesem Graf festgelegte Variable *only*, auf die im Rahmen des *übergeordneten* dieses Funktionsknotens zugegriffen werden kann, z. B. der Substance, der den von der definierten Parameter hostet.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Knoten festlegen](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-02.png "Knoten festlegen")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In diesem Beispiel wurde der Variablenname auf &quot;**`myVariable`**&quot; festgelegt und sein Wert ist &quot;**1**&quot;.

</td>
<td style="border: 0;" valign="top">

![Knotenbeispiel festlegen](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-03.png "Knotenbeispiel festlegen")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Der Sequenzknoten

Der Knoten <b>Sequenz</b> gibt Ihnen die Kontrolle über den *Ausführungsfluss* der Substance-Funktionsdiagramme, indem Sie sicherstellen, dass die *erste Verzweigung vollständig vor der zweiten Verzweigung ausgeführt wird*.

Die Ausgabe der *zweiten Verzweigung* wird dann an die Ausgabe des Knotens übergeben.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Sequenzknoten](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-04.png "Sequenzknoten")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In diesem Beispiel wird der Knoten <b>Sequenz</b> als Ausgabe des Diagramms festgelegt. Die Ausgabe der Funktion ist somit der vom Knoten <b>Float</b> ausgegebene Wert <b>0.5</b>.

Zuvor wird jedoch die Variable &quot;`<b>myVariable</b>`&quot; mit dem Gleitkommawert &quot;<b>1.0</b>&quot; festgelegt. Diese Variable kann dann *an einer anderen Stelle* im Kontext des Knotens verwendet werden.

</td>
<td style="border: 0;" valign="top">

![Beispiel für Sequenzknoten](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-05.png "Beispiel für Sequenzknoten")

</td>
</tr>
</table>

**Sequenz**-Knoten können *verkettet* sein, um den Ausführungsfluss des Diagramms zu steuern.

Sie können beispielsweise *zuerst eine Variable festlegen*, *ihren Wert zu einem späteren Zeitpunkt aktualisieren* und dann *ihren endgültigen Wert lesen*, während Sie sicherstellen, dass diese Aktionen *in einer bestimmten Reihenfolge ausgeführt werden*.

![Sequenzknoten verkettet](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-06.png "Sequenzknoten verkettet")

## Variable Sichtbarkeit

Beachten Sie, dass auf eine deklarierte Variable von überall aus *nicht* zugegriffen werden kann!\
Während auf eine auf übergeordneter Ebene deklarierte Variable auf untergeordneten Ebenen zugegriffen werden kann, ist das Gegenteil *nicht true*.

Daher sind im Knoten festgelegte Variablen auf Diagrammebene *nicht* verfügbar, während auf auf der Diagrammebene *festgelegte Variablen in den Parameterfunktionen des Knotens* zugegriffen werden kann.

Diese Regel ist zum Beispiel der Kern des *Verfügbarmachens eines Parameters*, zum Verfügbarmachen umfasst tatsächlich die folgenden Schritte:

1. Erstellen eines Diagrammeingabeparameters
1. Zugriff auf den Parameter im Substance-Funktionsdiagramm
1. Festlegen des Werts als Ausgabe der Funktion

Lassen Sie uns ein kleines Beispiel anführen: Stellen Sie sich vor, dass der Wert <b>Drehung</b> eines <b>Quadranten</b>-Knotens durch den Wert <b>Farbe/Luminanz</b> beeinflusst werden soll: Je heller die Luminanz, desto stärker die Drehung.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Wir werden die gesamte Berechnung in der Parameterfunktion <b>Farbe/Luminanz</b> durchführen. Dieser Parameter wird *zuerst* berechnet. Daher stehen alle darin festgelegten Variablen den anderen Knotenparametern zur Verfügung.

</td>
<td style="border: 0;" valign="top">

![Quadranteneigenschaften](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-07.png "Quadranteneigenschaften")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Unsere Aufgabe wird einfach sein: Wenn die Luminanz ein zufälliger Wert zwischen **0** und **1** ist, wird dieser Wert in der `myRotation`-Variablen gespeichert, dann legen wir den Wert als Ausgabe der Funktion fest.

Dies bedeutet, dass der Wert des Parameters **Farbe/Luminanz** zufällig *ist und* in der Variablen `myRotation` gespeichert wird.

Beachten Sie, dass die **Position**-Eigenschaft bereits durch einen Zufallswert definiert ist und ein **Iterate**-Knoten verwendet wird, um mehrere zufällig platzierte Muster abzurufen.

</td>
<td style="border: 0;" valign="top">

![Funktion für Farbe/Luminanz des Quadranten](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-08.png "Funktion für Farbe/Luminanz des Quadranten")

</td>
</tr>
</table>

![Verstreute Muster](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-09.png "Verstreute Muster")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Nachdem die Variable &quot;`myRotation`&quot; vorhanden ist und einen Wert aufweist, können wir jetzt auf das Funktionsdiagramm der Eigenschaft &quot;<b>Pattern Rotation</b>&quot; für die Substance zugreifen.

</td>
<td style="border: 0;" valign="top">

![Menü für die Parameterfunktion der Musterrotation](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-10.png "Menü für die Parameterfunktion der Musterrotation")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

In der Funktion wird der Wert des `myRotation`-Parameters mithilfe eines **Get Float**-Knotens gelesen - wir wissen, dass die Variable einen Float-Wert enthält - und als Ausgabe der Funktion festgelegt.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Gleitende Ausgabe der Musterrotation abrufen](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-11.png "Gleitende Ausgabe der Musterrotation abrufen")

</td>
</tr>
</table>

Die Luminanz steuert jetzt auch die Drehung.

![Gedrehte Muster](using-the-set-sequence-nodes.resources/using-the-set-sequence-nodes-12.png "Gedrehte Muster")

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Verwenden Sie das Eigenschaftenfenster in Substance 3D Designer, um Knoteneigenschaften und Diagrammparameter anzuzeigen und zu bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Eigenschaften
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Eigenschaften

Auf dieser Seite werden der Bereich <b>Eigenschaften </b> von Substance 3D Designer, sein Layout sowie die verschiedenen Rollouts und Kategorien und Parameter, die Sie darin finden, angezeigt. Der Schwerpunkt liegt auf Eigenschaften für [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md). [Funktionsgraphen](../../function-graphs/function-graphs.md) und [FX-Map-Graphen](../../function-graphs/fxmaps/fxmaps.md) haben einfachere Layouts.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Überblick

Der Bereich <b>Eigenschaften </b> ist ein kontextsensitiver Bereich, der sich je nach Ihrer Auswahl in [der Diagrammansicht](../../interface/the-graph-view/the-graph-view.md) und im Fenster [Explorer](../the-explorer-window/the-explorer-window.md) ändert.

</td>
<td style="border: 0;" valign="top">

![Eigenschaften-Dock](properties.resources/image2020-11-9-13-49-48.png "Eigenschaften-Dock")

</td>
</tr>
</table>

Sie können die Eigenschaften der ausgewählten Knoten und Ressourcen sowie [die Diagrammansicht](../../interface/the-graph-view/the-graph-view.md) ändern. Dies ist wahrscheinlich das am zweithäufigsten verwendete Bedienfeld der Benutzeroberfläche in Designer.

Das Eigenschaftenfenster ist in verschiedene Rollouts unterteilt, je nach Auswahl, z. B.:

* <b>Basisparameter</b> und <b>Eingabe-</b> oder <b>Spezifische Parameter</b> für Knoten
* <b>Attribute</b> und <b>Metadaten</b> für die meisten Knoten und Pakete

Eine wichtige Funktion des Substance-Ökosystems, [Verfügbarmachen von Parametern](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), erfolgt über das Eigenschaftenfenster.

>[!NOTE]
>
> Die meisten Zahlenfelder unterstützen *einfache mathematische Formeln* als Eingabe, z. B. `17+3.5`, `7/3`, `(4+2)*3`. Drücken Sie *Eingabe*, um die Formel zu validieren, und das Ergebnis wird in das Feld eingegeben. Wenn die Formel ungültig ist, wird das Feld auf den vorherigen Wert zurückgesetzt.\
> Einige numerische Felder in anderen Teilen der Anwendung, z. B. das Dialogfeld &quot;[Parameter verfügbar machen](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)&quot;, unterstützen diese Funktion ebenfalls.

## Nodes &amp; Substance Graphen

Knoten und [Substance-Diagramme](../../compositing-graphs/substance-compositing-graphs.md) weisen einen leicht überlappenden Satz von Eigenschaftenkategorien auf, und ihre Funktionalität ist ähnlich.

<b>Basisparameter</b> und <b>Attribute</b> sind zwischen Knoten und Diagrammen identisch.

Knoten bieten <b>Spezifische Parameter</b> oder <b> Instanzparameter</b> (abhängig davon, ob es sich um [Atomknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) oder [Instanzen](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) handelt) sowie <b>Eingabewerte</b> für die Arbeit mit [Werten](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

[Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) und [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)atomare Knoten sind Ausnahmen, da sie <b>Integrationsattribute</b> und <b>Bedingungen</b> für die Sichtbarkeit aufweisen. Auf diese beiden Eigenschaftensätze kann auch zentral in den Graph-Eigenschaften unter &quot;Eingaben&quot; und &quot;Ausgaben&quot; zugegriffen werden.

Diagramme lassen sich in einige zusätzliche Kategorien einteilen. <b>Eingabeparameter</b> listet [verfügbar gemachte Parameter](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) auf, <b>Eingaben</b> und <b>Ausgaben</b> listen alle Eigenschaften von Eingabe- und Ausgabeknoten auf. [Sie finden alle Diagrammeigenschaften, die detailliert auf einer dedizierten Seite erläutert werden.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Ressourcen und Pakete

Der Eigenschaftenbereich reagiert auch auf Auswahländerungen im [Explorer](../the-explorer-window/the-explorer-window.md). Sie können auch einen Graf auswählen (anstatt auf einen leeren Bereich zu doppelklicken) und die Eigenschaften &quot;Package&quot; und &quot;[Resource](../../resources/resources.md)&quot; ändern.

Pakete haben **Informationen**, **Attribute** und **Metadaten** Abschnitte. [Die Paketmetadaten werden auf einer dedizierten Seite beschrieben.](../../package-metadata/package-metadata.md)

Ressourcen verfügen über typspezifische Eigenschaften, [detailliert auf dedizierten Seiten](../../resources/resources.md).

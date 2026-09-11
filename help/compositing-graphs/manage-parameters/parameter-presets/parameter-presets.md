---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Parametervorgaben in Substance 3D Designer erstellen und verwenden, um Parameterkonfigurationen zu speichern und anzuwenden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parametervorgaben
user-guide-description: ''
user-guide-title: ''
source-git-commit: 69056338cc47db71e0754c72495d33a2a3c36dea
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Parametervorgaben

Parametervorgaben geben dem Benutzer die Möglichkeit, große Mengen vorkonfigurierter Werte für einen Satz von Parametern zu speichern und zu übertragen.Sie können in vielen Szenarien hilfreich sein und sind am nützlichsten, wenn eine große Anzahl von Parametern mit einer großen Bandbreite von Möglichkeiten vorhanden ist.

Es gibt zwei Möglichkeiten, Vorgaben zu speichern und zu laden. Beide bieten unterschiedliche Anwendungsfälle, die nachfolgend beschrieben werden.

![Dropdown-Menü &quot;Vorgabe laden/speichern&quot;](parameter-presets.resources/preset-menu.gif "Dropdown-Menü &quot;Vorgabe laden/speichern&quot;"){width="512px"}

## Externe Vorgaben

Externe Vorgaben umfassen eine externe Datei auf dem Datenträger, eine \*.SBSPRS-Datei. Sie können zwischen verschiedenen Graphen und Knoten übertragen werden, jedoch nur innerhalb der Anwendung. Ihr Hauptzweck ist genau das: mehrere Werte zu groß übertragen, um sie einzeln zu kopieren.

Externe Vorgaben sind für alle spezifischen Parameter auf [Grapheninstanzen](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), für die meisten spezifischen Parameter auf [Elementaren Knoten](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ([Ausnahmen sind die Parameter, die nicht gelegt werden können](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)) und für die gelegt Eingabeparameter in den [Parametern](../../graph-parameters/graph-parameters.md) eines Substance-Grafen verfügbar.

Sie werden einfach gespeichert und über dieses Menü geladen. Die gespeicherten SBSPRS-Dateien können auf jedem anderen Knoten oder Diagramm geladen werden.

>[!NOTE]
>
> Auch Teilübereinstimmungen funktionieren: Parameter, die in einem SBSPRS gespeichert sind, die auf dem geladenen Knoten nicht vorhanden sind, werden einfach ignoriert. Dies bedeutet, dass Sie Eigenschaften zwischen Knoten übertragen können, die meist ähnlich sind, [, wie die Farb- und Graustufenversion von Tile Sampler](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)! Alle freigegebenen Parameter werden geladen. Die Zuordnung erfolgt für Bezeichner und Typ.

![Bearbeitung eingebetteter Vorgaben](parameter-presets.resources/preset-embed.gif "Bearbeitung eingebetteter Vorgaben"){width="512px"}

## Eingebettete Vorgaben

Eingebettete Vorgaben funktionieren anders als externe Vorgaben. Ihr Hauptvorteil ist, dass sie in der SBS- oder SBSAR-Datei enthalten sind, sodass sie problemlos in Substance Painter, Maya und 3DS Max (derzeit nicht in Substance 3D Sampler, UE4 und Unity verfügbar) übertragen und geladen werden können. Der Benutzer muss sich auch nicht mit SBSPRS-Dateien herumschlagen.

Sie dienen einem anderen Zweck: Es ist nicht möglich, sie zwischen Knoten und Diagrammen zu übertragen (hierfür müssten Sie externe Vorgaben verwenden). Sie können auch nur in den Eingabeparametern der Eigenschaften eines Diagramms erstellt werden und nur im Vorschaumodus.

Der Arbeitsablauf ist wie folgt:

1. Wechseln Sie in den <b>Vorschaumodus</b> für die <b>Eingabeparameter</b>.
1. Werte auf das gewünschte Ergebnis festlegen
1. Klicken Sie auf <b>+</b> neben der Dropdown-Liste &quot;Vorgaben&quot;, um eine neue eingebettete Vorgabe zu erstellen. Die Vorgabe wird dann sofort erstellt und gespeichert

Eingebettete Vorgaben können danach nicht mehr geändert werden, sie können jedoch umbenannt werden. Sie können sie ändern oder entfernen, indem Sie auf das Zahnradsymbol neben der Dropdown-Liste und das + -Symbol klicken. Drücke auf das Minuszeichen neben einer Vorgabe, um sie zu entfernen.

Es müssen keine weiteren Schritte unternommen werden, um Vorgaben zu aktivieren: Nach der Veröffentlichung als SBSAR sind Ihre Vorgaben nach dem Import im Substance Painter verfügbar.

>[!IMPORTANT]
>
> Die Registerkarte <b>Vorgaben</b> ist deaktiviert, wenn [kontextbezogene Bearbeitung](../../../interface/preferences-window/preferences-window.md) verwendet wird.

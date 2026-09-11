---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: Lernen Sie die wichtigsten Konzepte der Diagramme zur Materialdefinition in Substance 3D Designer für die Materialerstellung kennen.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hauptkonzepte für MDL-Diagramme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# Hauptkonzepte für MDL-Diagramme

Auf dieser Seite werden die Hauptkonzepte vorgestellt, die *spezifisch* bis [MDL-Diagramme](../../mdl-graphs/mdl-graphs.md) sind. Sie sollten gut verstanden werden, um diesen Diagrammtyp in Substance 3D Designer optimal zu nutzen.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

MDL-Materialien verwenden eine Beschreibung für physikalisch basierte Rendering-Lösungen, die der in Designer eingebettete Renderer [Iray](../../interface/3d-view/iray/iray.md) unterstützt. Um das Ergebnis eines MDL-Diagramms &quot;*&quot; anzuzeigen, muss daher der Iray-Renderer &quot;*&quot; in einem aktiven Bedienfeld &quot;[3D view](../../interface/3d-view/3d-view.md)&quot; ausgewählt sein.

</td>
<td style="border: 0;" valign="top">

[![NVIDIA Iray-Logo](../../assets/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

Beim Erstellen oder Laden eines MDL-Diagramms wechselt das erste von Designer gefundene [nicht angeheftete](../../interface/customizing-your-wor/customizing-your-workspace.md) 3D-Ansichtsfenster *automatisch* zum Renderer [Ira](../../interface/3d-view/iray/iray.md). Wenn keine 3D-Ansicht verfügbar ist, wird ein *neues* 3D-Ansichtsfenster erstellt und auf den Iray-Renderer umgestellt, um das Rendering des MDL-Materials, das bearbeitet wird, zu hosten.

Wenn der Iray-Renderer in einem Bedienfeld &quot;3D-Ansicht&quot; ausgewählt ist, können Sie im Menü &quot;Materialien&quot; dieses Bedienfelds zwischen verfügbaren MDL-Materialien wechseln, zu denen im Explorer-Bedienfeld geladene Materialien und Materialien in der MDL-Bibliothek von Designer gehören. Weitere Informationen zum Arbeiten mit MDL-Materialien in Iray finden Sie im Abschnitt [Iray](../../interface/3d-view/iray/iray.md) dieser Dokumentation.

## Stammknoten

Das Ergebnis eines MDL-Diagramms wird vom Knoten <b>Root</b> definiert. Jeder Knoten des Diagramms kann als root festgelegt werden, solange er Daten vom Typ <b>Material</b> ausgibt, d. h. eine *Materialdefinition*. Ein MDL-Diagramm kann nur *einen*-Stammknoten aufweisen.

Im Allgemeinen kann ein Knoten, der als Root festgelegt werden kann, *autark* sein, da er bereits eine Materialdefinition enthält, die angepasst werden kann, indem Daten an seine *Eingaben* übergeben werden.\
Wenn Sie beispielsweise an einem glasartigen Material arbeiten möchten, können Sie eine Glasmaterialdefinition als Stammknoten als Ausgangspunkt verwenden, der jedoch *nicht obligatorisch* ist. Viele Materialknoten sind Vorlagen, die mit der umfangreichen Liste von MDL-Knoten in jedes komplexe Material umgewandelt werden können.

Der Stammknoten enthält eine Miniaturansicht mit einer Vorschau seiner aktuellen Ausgabe.

![Stammknoten des MDL-Diagramms](../../assets/mdl-root-hl.png "Stammknoten des MDL-Diagramms")

*Stammknoten in einem MDL-Diagramm und seine Eigenschaften werden im [Eigenschaften](../../interface/properties/properties.md)* *Bedienfeld* angezeigt.

## Verbindungen und Typen

Da es in MDL-Diagrammen viel mehr Datentypen gibt als in anderen Diagrammen in Designer, werden möglicherweise einzigartige Erscheinungsbilder von Knoten-Connectoren angezeigt. Die wichtigsten Konzepte, die Sie verstehen müssen, sind unten aufgeführt.

Verbinder-Shape

Die *-Form des Connectors* gibt an, ob der Datentyp *einheitlich* (Kreis) oder *variabel* (Quadrat) ist.

&quot;Eine Variable eines einheitlichen Typs kann nur auf einen einheitlichen Wert gesetzt werden. Eine Variable unterschiedlicher Art kann sowohl auf einen variablen Wert als auch auf einen einheitlichen Wert eingestellt werden. Der resultierende Wert in der Variablen wird dann immer als variierend angesehen.&quot; (Quelle: Abschnitt 6.3 der [MDL-Spezifikation](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf))

Im Folgenden finden Sie einige Beispiele:

* Ein <b>Textur</b>-Sample ist *variabel*, da Werte von dem aufgenommenen Pixel betroffen sind.
* Ein <b>Color</b>-Wert ist *uniform*, da er unabhängig vom Kontext gleichmäßig übergeben wird.
* <b>BRDF</b> ist *variabel*, da Werte vom Einfallswinkel betroffen sind.
* Ein <b>Float</b>- oder <b>Boolean</b>-Wert ist *uniform*, da er unabhängig vom Kontext gleichmäßig übergeben wird.

Connector-Farbe

Der *-Datentyp*, der von einem Ausgabestecker ausgeht oder von einem Eingabestecker erwartet wird, ist farbcodiert und wird zwischen Klammern nach dem Bezeichner/der Bezeichnung angezeigt, wenn der Mauszeiger über dem Stecker positioniert wird.

>[!WARNING]
>
> Nur Connectors für *übereinstimmende Datentypen* können miteinander verknüpft werden. Der einzige Zweck der Farbcodierung besteht darin, die Lesbarkeit in Bezug auf die Art der Daten, die im Diagramm übergeben werden, und auf die Art und Weise zu erhöhen, wie Connectors miteinander verknüpft werden können.

![MDL-Knotenverbindungstypen](../../assets/mdl-connector-types.png "MDL-Knotenverbindungstypen"){width="512px"}

*Das Seitenverhältnis der Connectors variiert je nach I/O-Werttyp, der in Klammern nach der I/O-ID angezeigt wird*

## Erstellung gefilterter Knoten

Sie können einen beliebigen Knoten hinzufügen, der in der <b>mdl</b>-Kategorie der <b>Bibliothek</b> im Diagramm verfügbar ist, indem Sie *den Knoten* aus der <b>Bibliotheksansicht</b> in die <b>Diagrammansicht</b> ziehen oder indem Sie <b>Leertaste</b> drücken, um das <b>Knotenmenü</b> in der Diagrammansicht zu öffnen, wenn *nichts ausgewählt ist*. In diesem Fall wird eine *ungefilterte* Liste von Knoten angezeigt.

Es gibt jedoch Fälle, in denen die Knotenliste im Menü &quot;Knoten&quot; so gefiltert wird, dass nur Knoten mit dem entsprechenden Datentyp für die Zieleingabe oder -ausgabe angezeigt werden:

* Wenn ein *-Knoten in der Diagrammansicht ausgewählt ist* und <b>Leertaste</b> gedrückt wird
* Wenn auf <b>LMB</b> geklickt wird, halten Sie einen Link aus einem *Knotenverbinder* gedrückt und *ziehen*.

Beachten Sie die *Regeln*, die für die Filterung angewendet wurden:

* Wenn das Knotenmenü durch Drücken der <b>Leertaste</b> angezeigt wird, wenn ein *einzelner* Knoten ausgewählt ist, enthält die Liste Knoten, bei denen der Datentyp der *ersten Eingabe* mit dem *Ausgabe*-Datentyp des ausgewählten Knotens übereinstimmt.
* Wenn das Knotenmenü angezeigt wird, indem <b>Leertaste</b> gedrückt wird, wenn *mehrere* Knoten ausgewählt sind, enthält die Liste Knoten, bei denen der Datentyp der *ersten Eingabe* mit dem *letzten ausgewählten* Knoten des *Ausgabedatentyps* übereinstimmt.
* Wenn das Knotenmenü angezeigt wird, indem *einen Link* aus einem *Output*-Connector zieht, enthält die Liste Knoten, bei denen der Datentyp der *ersten Eingabe* mit dem ausgewählten *Output*-Datentyp übereinstimmt.
* Wenn das Knotenmenü angezeigt wird, indem *eine Verknüpfung* aus einem *Eingabe*-Connector gezogen wird, enthält die Liste Knoten, bei denen der Datentyp der *Ausgabe* mit dem *ausgewählten Eingabe*-Datentyp übereinstimmt.

![Gefilterte Knotenerstellung](../../assets/mdl-filtered-node-creation.gif "Gefilterte Knotenerstellung")

*Gefilterte Knotenerstellung im MDL-Diagramm. Beachten Sie, dass sich die Liste entsprechend dem Werttyp für den Connector ändert*

## Diagrammeingaben und Texturen

MDL-Materialien können Daten aus externen Quellen empfangen, beispielsweise in Form von Werten und Texturen. Dies wird erreicht, indem <b>ein Knoten </b> verfügbar gemacht wird, im Gegensatz zum [Substance-Diagramm &#x200B;](../../compositing-graphs/substance-compositing-graphs.md), in dem dedizierte Eingabeknoten für diesen Zweck vorhanden sind.

Daten können je nach *Typ* an den angezeigten Knoten übergeben werden. Zum Beispiel können Gleitkommawerte an einen exponierten <b>Gleitkommawert</b>-Knoten übergeben werden, und eine Textur kann an einen exponierten <b>color</b>-Knoten übergeben werden (in diesem Fall werden die RGBA-Werte der aufgenommenen Pixel als Farbwert übergeben).

![Verfügbare Diagrammeingaben](../../assets/mdl-graph-inputs-samplers.png "Verfügbare Diagrammeingaben")

*Verfügbare Knoten erstellen Diagrammeingaben, bei denen es sich sowohl um Rohwerteingaben als auch um Sampler für Texturen handelt*

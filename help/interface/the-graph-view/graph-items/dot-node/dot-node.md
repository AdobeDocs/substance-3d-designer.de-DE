---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/the-graph-view/graph-items/dot-node.html"
breadcrumb-title: ''
description: Verwenden Sie Punktknoten und Portalknoten in Substance 3D Designer, um Verbindungspunkte zu erstellen und den Graf-Flow zu organisieren.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Knoten "Punkt" (auch Portal)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---


# Knoten &quot;Punkt&quot; (auch Portal)

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Punktknotensymbol](dot-node.resources/graphatomic-dot_1.png "Punktknotensymbol")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Der Knoten &quot;<b>Dot</b>&quot; ist ein Helfer, mit dem Sie Graf vereinfachen und bereinigen können, indem Sie Verbindungen umleiten und gruppieren. Dies ist besonders für Graf mit vielen langen Verbindungen, die über andere Verbindungen oder Knoten laufen, sinnvoll.

Ein Paar von Punktknoten kann als <b>Portale</b> verwendet werden, um eine Verbindung über eine große Entfernung auszublenden, oder an Orten, an denen das Routing der Verbindung eine Herausforderung darstellen würde.

</td>
</tr>
</table>

## Erstellen von Punktknoten

Punktknoten können in einem beliebigen Graf hinzugefügt werden, und zwar auf eine der folgenden Weisen:

+++In Link einfügen
Halten Sie die <b>Alt</b>-Taste gedrückt, während Sie mit dem Mauszeiger auf eine Verbindung zeigen, um die Vorschau des Punktknotens anzuzeigen, und klicken Sie dann auf &quot;LMB&quot;, um einen Punktknoten für die Verbindung an diesem Speicherort hinzuzufügen.

![Einfügen eines Punktknotens](dot-node.resources/dot-node-insert-optim.gif "Einfügen eines Punktknotens"){width="512px"}



+++

+++Node-Verbindung
Drücken Sie die Taste <b>Alt</b>, während Sie eine neue Verbindung von einer Knotenverbindung ziehen, um einen Punktknoten an dieser Position einzufügen.

Sie können mit dem Ziehen der neuen Verbindung fortfahren und den Vorgang wiederholen, um die Verbindung nach Ihren Wünschen zu routen.

![Punkt: Erstellen aus Verbindung](dot-node.resources/graph-dot_create-from-connector.gif "Punkt: Erstellen aus der Verbindung ")



+++

+++Knotenmenü
Drücken Sie die <b>Leertaste</b>, um das <b>Knotenmenü</b> anzuzeigen, und wählen Sie dann das Element &quot;Punkt&quot; aus oder geben Sie im Suchfeld &quot;Punkt&quot; ein, um das Element anzuzeigen und schneller zu finden.

![Punktknoten im Knotenmenü](dot-node.resources/dot-node-insert-menu.png "Punktknoten im Knotenmenü")



+++

>[!TIP]
>
> Wenn ein Punktknoten erstellt wird, erhält die Eigenschaft &quot;Name&quot; automatisch den Fokus, sodass Sie den Namen des Knotens sofort bearbeiten können.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Zusammenführen von Verknüpfungen

Drücken Sie ALT und verschieben Sie einen Punkt-Knoten über Verknüpfungen, um mehrere Knotenverbindungen zusammenzuführen.

</td>
<td style="border: 0;" valign="top">

![Verknüpfungen zusammenführen](dot-node.resources/dot-node-congrenate-links-optim.gif "Verknüpfungen zusammenführen"){width="512px"}

</td>
</tr>
</table>

## Portale

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Punktknoten als Portal - Symbol](dot-node.resources/DotNode_Portal-1.png "Punktknoten als Portal - Symbol")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Punktknoten können als <b>Portale</b> verwendet werden, um Daten über eine große Distanz im Diagramm zu senden, ohne dass ein sperriger langer Link die Lesbarkeit beeinträchtigt. Dadurch wird die Verknüpfung zwischen den Punktknoten ausgeblendet.

</td>
</tr>
</table>

![Punktknoten als Portal](dot-node.resources/DotNode_Portal.gif "Punktknoten als Portal")

### Erstellen von Portalen

Ein Portal wird automatisch zwischen zwei Dot-Knoten - einem Sender und einem Empfänger - erstellt, wenn der Dot-Knoten des Senders benannt wird. Das Benennen eines Punktknotens erfolgt durch Festlegen eines eindeutigen Bezeichners in der <b>Name</b>-Eigenschaft.

Wenn in einem Diagramm ein oder mehrere benannte Punktknoten vorhanden sind, kann jeder Punktknoten wie folgt als Empfänger mit diesem Knoten verbunden werden:

* Herstellen einer Verbindung zwischen dem Eingang des Empfängers und dem Ausgang des Senders;
* Auswählen des Sendernamens in der <b>Eingabeportal</b>-Eigenschaft des Empfängers.

Beim Duplizieren oder Kopieren von Empfängern bleibt die Verbindung zum Sender als Portal erhalten.

### Identifizieren von Portalen

Bei Punktknoten, die als Portale verwendet werden, befindet sich neben dem als Portal verwendeten Connector ein Wireless-Signalsymbol.

Wenn Sie einen beliebigen Punktknoten auswählen, der als Portal verwendet wird, werden seine ausgeblendeten Verbindungen zu anderen Portalen als gestrichelte Linie angezeigt.

### Portale löschen

Ein Portal wird gelöscht, wenn der <b>Name</b> des Senders gelöscht wird oder wenn die ausgeblendete Verbindung gelöscht wird durch:

* Auswählen eines Portals, dann Auswählen der ausgeblendeten Verbindung und Löschen;
* Auswählen des Empfängers und Drücken der Schaltfläche <b>X</b> neben dem Dropdownmenü <b>Eingabeportal</b> in den Eigenschaften.

>[!IMPORTANT]
>
> Die Verwendung von Punktknoten als Portale wird in [FX-Map-Graphen](../../../../function-graphs/fxmaps/fxmaps.md) nicht unterstützt.

Schauen Sie sich dieses Tutorial über Punktknoten als Portale an:

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Fügen Sie Substance 3D Designer-Diagrammen Kommentare hinzu, um Ihren Workflow zu dokumentieren und Knotenverbindungen zu erläutern.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kommentar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Kommentar

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Kommentarsymbol](../../../../assets/graphatomic-comment_1.png "Kommentarsymbol")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ein Kommentar ist einfach ein frei schwebender Text, der an einer beliebigen Stelle in einem Diagramm platziert werden kann.

Sie dient dazu, Teile eines Diagramms zu kommentieren und zu erklären. Die <b>Description</b>-Eigenschaft enthält den angezeigten Text.

</td>
</tr>
</table>

>[!NOTE]
>
> Kommentare haben einen automatischen Zeilenumbruch, der darauf abzielt, ihren Fußabdruck in einem Diagramm zu minimieren.

## Kommentare erstellen

Der Standardkommentartyp wird unabhängig von Knoten im Diagramm platziert.

Es kann auf folgende Weise erstellt werden:

+++Knotenmenü
Drücken Sie die <b>Leertaste</b> in der Diagrammansicht, um das <b>Knotenmenü</b> zu öffnen, und wählen Sie das Element &quot;Kommentar&quot; in der Liste aus.

Geben Sie &quot;comment&quot; in das Suchfeld ein, um das Element anzuzeigen und es schneller zu finden.

+++

+++Tastaturbefehl
Wenn dem Element &quot;Kommentar&quot; in [Voreinstellungen](../../../../interface/preferences-window/preferences-window.md) eine Tastenkombination zugeordnet ist, drücken Sie diese Tastenkombination, wenn die Diagrammansicht den Fokus hat.

+++

+++Kontextmenü
Drücken Sie in der Diagrammansicht <b>RMB</b> für ein beliebiges Objekt oder in einem leeren Bereich und wählen Sie die Option <b>Kommentar hinzufügen</b> aus.

+++

+++Diagrammsymbolleiste
Klicken Sie in der Diagrammansichtssymbolleiste auf die Schaltfläche &quot;Kommentar&quot; in der <b>Node-Palette</b>.

+++

+++Bibliothek
Wählen Sie in der Bibliothek die Kategorie <b>Diagrammelemente</b> aus, ziehen Sie dann das Element &quot;Kommentar&quot; per Drag &amp; Drop in die Diagrammansicht.

+++

>[!TIP]
>
> Wenn ein Kommentar erstellt wird, erhält die Eigenschaft &quot;Beschreibung&quot; automatisch den Fokus, sodass Sie den Text des Kommentars sofort bearbeiten können.

## Übergeordnete Kommentare

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Ein übergeordneter Kommentar ist ein Kommentar, der *an einen bestimmten Knoten* im Diagramm angehängt ist, sodass beim Verschieben des Knotens der Kommentar folgt und beim Löschen des Knotens der Kommentar zusammen mit diesem gelöscht wird.

Kommentare, die erstellt werden, wenn derzeit ein *einzelner*-Knoten ausgewählt ist, oder über das Kontextmenü eines einzelnen Knotens, sind diesem Knoten übergeordnet.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Kommentare: Übergeordnete Kommentare](../../../../assets/graph-comment_parented.gif "Kommentare: Übergeordnete Kommentare")

</td>
</tr>
</table>

## HTML-Formatierung

Der Text kann mit HTML-Tags formatiert werden. Diese Formatierung wird mithilfe der Schaltfläche ![](../../../../assets/graph-frames_html-markup-button.png) <b>HTML-Markup</b> in der Eigenschaft <b>Beschreibung</b> des Kommentars umgeschaltet.

>[!TIP]
>
> Weitere Informationen zu dieser Funktion finden Sie im Abschnitt <b>Beschreibung</b> der Dokumentation [Frames](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Kommentare: HTML-Markup](../../../../assets/graph-comment_html-markup.gif "Kommentare: HTML-Markup ")

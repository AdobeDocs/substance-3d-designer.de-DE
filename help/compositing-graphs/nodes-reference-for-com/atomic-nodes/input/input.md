---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Eingabe , um Eingabeparameter für Substance-Graphen zu erstellen, die von Benutzern angezeigt und angepasst werden können.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Eingabe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Eingabe

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Atomknoten: Eingabefarbe](input.resources/comp_inputcolor_1.png "Atomarer Knoten: Eingabefarbe"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Atomknoten: Eingabe-Graustufen](input.resources/comp_inputgrayscale_1.png "Atomic node: Eingabe-Graustufen"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Atomknoten: Eingabewert &#x200B;](input.resources/comp_inputnumeric_1.png "Atomischer Knoten: Eingabewert "){width="200px"}

</td>
</tr>
</table>

Eingabeknoten sind ein spezieller Knotentyp, der einen dynamischen Steckplatz in Ihrem Diagramm erstellt, sodass jeder Eingang verbunden werden kann, sobald Ihr Diagramm in einem anderen Kontext verwendet wird.

Im Gegensatz zu [Ausgabeknoten](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) müssen Sie explizit entweder eine Farb-, Graustufen- oder Werteingabe platzieren. Es ist nicht möglich, eigene &quot;agnostische&quot; Eingaben zu erstellen, die den Typ je nach Verbindung ändern.

Eingabeknoten sind nicht so wichtig wie [Ausgabeknoten](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md): können Sie perfekt funktionierende, erweiterte Diagramme nutzen, die keine Eingabe benötigen. Eingaben werden nur verwendet, wenn Sie das Ergebnis Ihrer Diagramm- oder Knoteninstanz auf einer externen Eingabe basieren möchten, z. B. beim Erstellen einer [Instanz](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) oder eines [Filters](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter) für Substance 3D Painter.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## PARAMETER

</td>
<td style="border: 0;" valign="top">

### TRIBUTE

</td>
<td style="border: 0;" valign="top">

### ERBSCHAFT

</td>
<td style="border: 0;" valign="top">

### INTEGRATIONSATTRIBUTE

</td>
</tr>
</table>

## Parameter

Standardmäßig gibt eine Eingabefarbe oder ein Graustufen schwarz zurück, wenn nichts angeschlossen ist. Sie können entweder einen anderen Standardwert festlegen oder eine vorhandene [Bitmapressource](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) aus dem [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) auf den Eingabeknoten in Ihrem Diagramm ziehen, um eine Vorschau dieser Daten im Steckplatz anzuzeigen. Dies funktioniert nur bei Farb- und Graustufeneingaben. Der Standardwert bleibt erhalten, wenn er in anderen Kontexten verwendet wird. Die Vorschaubitmap wird anderswo verworfen.

Wenn Sie das Diagramm mit den Ausgaben eines anderen Diagramms anzeigen möchten, müssen Sie dieses Diagramm entweder für die obige Methode in die Bitmap exportieren oder die kontextbezogene Bearbeitung verwenden.

|  |  |
| --- | --- |
| <b>PKG-Ressourcenpfad</b> *Zeichenfolge* | Zeigt auf eine benutzerdefinierte Bitmapressource für die Vorschau. |
| <b>Standardwert</b> *Farbe/Graustufen/Wert* | Ermöglicht es Ihnen, einen anderen Wert als Schwarz als Standardeingabe zu verwenden, wenn an diesen Steckplatz nichts angeschlossen ist. |

## Attribute

|  |  |
| --- | --- |
| <b>Kennung</b> *Zeichenfolge* | Das einzige obligatorische, eindeutige Attribut. Kann keine Leerzeichen enthalten.   Dieser wird zum Kennzeichnen von Eingaben verwendet, wenn kein Label eingerichtet ist, und zum Kennzeichnen verschiedener Ausgänge. Lassen Sie diese nicht einfach bei &quot;input\_1&quot; stehen! |
| <b>Beschreibung</b> *Zeichenfolge* | Optionale Beschreibung, die in der Designer-Bibliothek und im Painter-Regal verwendet wird. |
| <b>Bezeichnung</b> *Zeichenfolge* | UI-Label für ansprechende Beschriftungen in Designer und der Benutzeroberfläche von Painter. Kann Leerzeichen enthalten.   Es wird empfohlen, einen Namen festzulegen, der der Identifizierung ähnelt, nur mit Leerzeichen anstelle von Unterstrichen. |
| <b>Benutzerdaten</b> *Zeichenfolge* | Zusätzliche, optionale Benutzerdaten, die für bestimmte Datenvorgänge verwendet werden können, im Wesentlichen ein Platzhalter, benutzerdefiniertes Datenfeld. |
| <b>Gruppe</b> *Zeichenfolge* | Gruppenattribut, das zum Gruppieren von Eingaben für die [Verknüpfungserstellungsmodi](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) von Designer verwendet wird.   Eingaben mit einem identischen (Beachtung der Groß-/Kleinschreibung) Gruppenattribut werden im kompakten Materialmodus als Einzelverbindung dargestellt. |

## Vererbung

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Wenn mehrere Eingaben vorhanden sind, müssen Sie darauf achten, wie das Diagramm die Basisparameter[&#128279;](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) von diesen Eingaben erbt.\
Zu den Basisparametern gehören u. a. die <b>Ausgabegröße</b>, das <b>Ausgabeformat</b> und der <b>Anordnungsmodus</b>.

</td>
<td width="33.33%" style="border: 0;" valign="top">

[![Primäre Eingabe im Substance-Diagramm &#x200B;](input.resources/node-primary-input.png)](https://helpx.adobe.com/Primary%20input%20in%20Substance%20graph)

</td>
</tr>
</table>

Eine Eingabe kann als [Primäre Eingabe](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) definiert werden. Diese Eingabe steuert dann die Attribute aller Eingaben, deren Vererbungsmethode auf *Relativ zu übergeordnetem* festgelegt ist. Dies ist die Vererbungsmethode *, die standardmäßig* auf Eingabeknoten festgelegt ist.

Sie können einen Eingabeknoten als primäre Eingabe eines Diagramms festlegen, indem Sie auf *RMB* auf dem Knoten klicken und im Kontextmenü die Option <b>Als primäre Eingabe festlegen</b> auswählen.\
Die primäre Eingabe eines Knotens ist im Connector *mit einem* kleinen dunklen Punkt markiert (im Beispiel neben diesem Abschnitt rot eingekreist).

Alternativ erbt jede Eingabe, die auf die *Vererbungsmethode Relativ zur Eingabe* festgelegt ist, die Attribute von dem Knoten, mit dem sie verbunden ist, *unabhängig* von der primären Eingabe.

Schließlich können Sie jeden Wert für ein bestimmtes Attribut überschreiben, indem Sie die zugehörige Vererbungsmethode auf *Absolut* festlegen.

>[!TIP]
>
> Weitere Informationen zur Vererbung finden Sie auf der Seite [Vererbung in Substance-Graphen](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) in dieser Dokumentation.

>[!IMPORTANT]
>
> Die *Vererbungsmethode Relativ zu Eingabe* für Eingabeknoten wird *nicht unterstützt* in [Substance 3D Assets (SBSAR)](https://helpx.adobe.com/substance-3d-assets.html). Legen Sie vor dem Veröffentlichen des Pakets die Vererbungsmethoden aller Eingabeknoten auf *Relativ zu übergeordneten Knoten* fest.

## Integrationsattribute

Die Eingaben werden nicht direkt an die 3D-Ansicht gesendet, aber ihre Verwendungsattribute werden von [Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home) verwendet, um Steckplätze automatisch mit bestimmten Zuordnungen zu füllen (meist mit [Filtern](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter)).

Darüber hinaus werden die Verwendungsattribute auch mit [Verknüpfungserstellungsmodi](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) verwendet, um die richtigen Eingabe- und Ausgabeschlitze abzugleichen.

<b>Nutzung</b>

|  |  |
| --- | --- |
| <b>Komponente</b> *Zeichenfolge* | Dadurch wird festgelegt, welche Kanäle sich tatsächlich in der resultierenden Eingabe befinden.   Dies ist eine ältere Einstellung, die nicht mehr von Integrationen und Graphen verwendet wird. |
| <b>Nutzung</b> *Zeichenfolge* | Definieren Sie einen Typ oder eine Verwendung für diese Eingabe. Es gibt an, wie andere Knoten sich mit diesem Eingang verbinden sollen. |
| <b>Farbraum</b> *Zeichenfolge* | Legt den Farbraum fest, in dem diese Eingabe interpretiert werden soll. |

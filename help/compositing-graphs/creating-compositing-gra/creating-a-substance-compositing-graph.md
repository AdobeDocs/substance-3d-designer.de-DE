---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph.html"
breadcrumb-title: ''
description: Erfahre, wie du in Substance 3D Designer Compositing-Substance erstellst, um Workflows für prozedurale Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Creating a Substance graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Erstellen von Substance-Graphen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 1%

---


# Erstellen von Substance-Graphen

Das Erstellen von Texturen in Designer beginnt mit dem Erstellen eines Substance-Diagramms, entweder aus einer vordefinierten Vorlage oder aus einem leeren Diagramm.

<a name="create-graph"></a>

## Erstellen eines Diagramms

Sie können eine der folgenden Methoden verwenden, um das Erstellen eines neuen [Substance-Diagramms](../../compositing-graphs/substance-compositing-graphs.md) zu starten:

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Klicken Sie auf dem Startbildschirm auf die Schaltfläche <b>Neues Diagramm</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Vom Startbildschirm erstellen](../../assets/newGraphDialog-create-homeScreen.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Vom Startbildschirm erstellen"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Klicken Sie in einem beliebigen *vorhandenen*-Paketelement im [Explorer](../../interface/the-explorer-window/the-explorer-window.md) auf <b>RMB</b> und navigieren Sie im Kontextmenü zu <b>Neu > Substance-Diagramm</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Aus Explorer erstellen](../../assets/newGraphDialog-create-explorer.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Aus Explorer erstellen"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Klicken Sie in der Hauptsymbolleiste auf die Schaltfläche ![](../../assets/image2021-6-22-20-36-44.png) <b>Neues Substance-Diagramm</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Aus Hauptsymbolleiste erstellen](../../assets/newGraphDialog-create-mainToolbar.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Aus Hauptsymbolleiste erstellen"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Wechseln Sie im Hauptmenü zu <b>Datei > Neu > Substance-Diagramm...1</b>

  </td>
  <td style="border: 0;" valign="top">

  ![](../../assets/newGraphDialog-create-mainMenu.png)

  </td>
  </tr>
  </table>

* Drücken Sie den Tastaturbefehl <b>Strg+N</b> (Windows) bzw. <b>Befehl+N</b> (macOS).

Unabhängig von der gewählten Methode wird das Dialogfeld &quot;<b>Neues Substance-Diagramm</b>&quot; angezeigt.

<a name="graph-templates"></a>

## Diagrammvorlagen

Unabhängig von der Methode zum Erstellen eines neuen Substance-Diagramms wird Ihnen immer das Dialogfeld <b>Neues Substance-Diagramm</b> angezeigt, mit dem Sie das neue Diagramm konfigurieren können.

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Materialien](../../assets/newGraphDialog-materials.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Materialien"){zoomable="yes"}

### Vorlagen

Designer enthält Diagrammvorlagen mit vorkonfigurierten Knoten, damit Sie schneller durchstarten können. Sie können [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)-Knoten enthalten, einfache Knoten, um Werte an diese Ausgaben zu übergeben - z. B. [Einheitliche Farbe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) sowie [Eingabe](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) Knoten.

Doppelklicken Sie auf eine Vorlage in der Liste, oder wählen Sie sie aus, und klicken Sie auf die Schaltfläche <b>Erstellen</b>, um mithilfe dieser Vorlage ein neues Substance-Diagramm zu erstellen. Standardmäßig wird das neue Diagramm in einem neuen, nicht gespeicherten Paket platziert.

>[!TIP]
>
> Beginne ganz von vorne
> 
> Wählen Sie die Vorlage <b>Leer</b> in der Kategorie &quot;Leer&quot; aus, um mit einem vollständig leeren Diagramm zu beginnen.

>[!NOTE]
>
> Vorlagen wechseln
> 
> Wenn Sie die falsche Vorlage auswählen, können Sie *nicht* zu einer anderen Vorlage wechseln, nachdem Sie das Diagramm erstellt haben.
> 
> Um Ihr vorhandenes Diagramm auf eine andere Vorlage zu portieren, können Sie ein neues Diagramm mit der entsprechenden Vorlage erstellen und das Diagramm kopieren und in die neue Vorlage einfügen. Erneutes Verbinden von Knoten, insbesondere Ausgabeknoten.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Jede Vorlage wird nach ihrer Bezeichnung und ihrem Untertitel aufgelistet.

Der Untertitel bietet mehr Kontext zum *Anwendungsfall* für die Vorlage: das Materialmodell, auf dem es basiert, die Software, mit der es integriert werden soll, usw.

Im Modus <b>Miniaturansichten</b> wird der Untertitel in einem dunkleren, kleineren Text unter der Beschriftung platziert.

In den Ansichtsmodi <b>Liste</b>, <b>Pakete</b> und <b>Verzeichnisse</b> wird der Untertitel folgendermaßen an die Bezeichnung angehängt: *Bezeichnung - Untertitel*.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Miniaturkarte](../../assets/newGraphDialog-thumbnailCard.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Miniaturkarte")

</td>
</tr>
</table>

<a name="material-samples"></a>

### Material-Samples

Die Kategorie <b>Materialproben</b> enthält eine [kuratierte Auswahl von Diagrammen](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md), aus denen Sie lernen und mit denen Sie experimentieren können.

Sie können die Beispiele auch direkt vom Startbildschirm aus aufrufen, indem Sie die Schaltfläche <b>Zu den Beispielen wechseln</b> verwenden.

Alle Beispiele basieren auf dem [OpenPBR-Materialmodell](../../interface/3d-view/material-properties/material-properties.md#openpbr).

![Materialproben - Banner für den Startbildschirm](../../assets/materialSamples-banner.png "Materialproben - Banner für den Startbildschirm"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Info-QuickInfo

Wenn Sie mit dem Informationssymbol für jedes Vorlagenelement zeigen, wird eine QuickInfo mit zusätzlichen Informationen zur Vorlage angezeigt:

<b>Typ:</b> Der Typ des Assets, das mit der Vorlage erstellt werden soll. Dies kann in den [Diagrammeigenschaften](../../compositing-graphs/graph-parameters/graph-parameters.md) bearbeitet werden.

<b>Beschreibung:</b> Details zu der Vorlage, z. B. der Workflow, in den sie integriert ist, der beabsichtigte Anwendungsfall und Empfehlungen zu ihrer Verwendung.

<b>Ausgaben:</b> Die [Ausgabeknoten](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) der Vorlage, falls vorhanden.

</td>
<td style="border: 0;" valign="top">

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - QuickInfo für Vorlagen](../../assets/newGraphDialog-tooltipTemplate.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - QuickInfo für Vorlagen"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Ansichtsmodi

Die Vorlagenliste kann mithilfe der Schaltfläche &quot;<b>Ansichtsmodi</b>&quot; in verschiedenen Modi angezeigt werden.

Die von der ausgewählten Kategorie und Projektdatei durchgeführte Filterung wird in allen Ansichten angewendet.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Ansichtsmodi](../../assets/newGraphDialog-viewModes.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Ansichtsmodi"){zoomable="yes"}

</td>
</tr>
</table>

+++Ansichtsmodi
![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Miniaturansicht](../../assets/newGraphDialog-viewMode-thumbnails.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Miniaturansicht"){zoomable="yes"}



<b>Miniaturen</b>

Karten mit Miniaturen, die eine Vorschau oder ein Symbol des Vorlagentyps bereitstellen.

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Listenansicht](../../assets/newGraphDialog-viewMode-list.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Listenansicht"){zoomable="yes"}



<b>Liste</b>

Vorlagen werden nur nach ihrer Beschriftung aufgelistet.

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Paketansicht](../../assets/newGraphDialog-viewMode-packages.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Paketansicht"){zoomable="yes"}



<b>Pakete</b>

Vorlagen werden nach ihrer Bezeichnung als untergeordnete Elemente der Paketdatei aufgelistet, der sie angehören.

Bewegen Sie den Mauszeiger über ein Paketdateielement, um eine QuickInfo mit dem vollständigen Pfad anzuzeigen.

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - Verzeichnisansicht](../../assets/newGraphDialog-viewMode-directories.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - Verzeichnisansicht"){zoomable="yes"}



<b>Verzeichnisse</b>

Vorlagen werden anhand ihrer Bezeichnung als untergeordnete Elemente des Verzeichnisses aufgelistet, in dem sich die Paketdatei befindet, zu der sie gehören.

Bewegen Sie den Mauszeiger über ein Verzeichniselement, um eine QuickInfo mit dem vollständigen Pfad anzuzeigen.

+++

### Eigenschaften

Nachdem Sie die Vorlage ausgewählt haben, können Sie grundlegende Informationen zum neuen Diagramm einrichten. Er kann jederzeit nach der Erstellung des Diagramms geändert werden.

<b>Diagrammname</b>: den Bezeichner des Graphen. Sie muss für ein bestimmtes Paket eindeutig sein und darf keine Leerzeichen und einige Sonderzeichen enthalten.

<b>Größe</b>: die übergeordnete Auflösung des Diagramms, die die Ausgabeauflösung der meisten Knoten steuert - weitere Informationen finden Sie auf der Seite [Ausgabegröße](../../compositing-graphs/output-size/output-size.md). Die Felder &quot;width&quot; und &quot;Height&quot; sind standardmäßig miteinander verknüpft. Sie können die Verknüpfung wieder aufheben, indem Sie auf die Verknüpfungsschaltfläche zwischen den Kombinationsfeldern &quot;width&quot; und &quot;Height&quot; klicken.

<b>Diagramm in </b> erstellen: Mit diesem Kombinationsfeld können Sie ein *neues*-Paket für das neue Diagramm erstellen oder das neue Diagramm einem beliebigen *vorhandenen*-Paket hinzufügen, das bereits im [Explorer](../../interface/the-explorer-window/the-explorer-window.md)-Bedienfeld geladen wurde.

### Hilfe-QuickInfo

Bewegen Sie den Mauszeiger über das Fragezeichensymbol, um eine QuickInfo mit einer Schaltfläche anzuzeigen, die direkt auf diese Seite verweist, damit Sie bei Bedarf auf diese Dokumentation zurückgreifen können.

![Dialogfeld &quot;Neues Substance-Diagramm&quot; - QuickInfo für die Hilfe](../../assets/newGraphDialog-tooltipHelp.png "Dialogfeld &quot;Neues Substance-Diagramm&quot; - QuickInfo für die Hilfe"){zoomable="yes"}

<a name="managing-templates"></a>

## Vorlagen verwalten

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filtern nach Kategorie

Kategorien werden verwendet, um Vorlagen zu gruppieren, die nach Anwendungsfall oder Elementtyp miteinander verknüpft sind.

Verwenden Sie das Kombinationsfeld <b>Kategorie</b>, um die Kategorie auszuwählen, nach der Sie die Vorlagen filtern möchten.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Dialogfeld &quot;Neuer Substance-Graf&quot; - Filterungen nach Kategorie](../../assets/newGraphDialog-categories.png "Dialogfeld &quot;Neuer Substance-Graf&quot; - Filterungen nach Kategorie"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Für Vorlagen kann in den <b>Vorlagendaten</b> eine Kategorie eingerichtet sein. [Filterattribut &#x200B;](../../compositing-graphs/graph-parameters/graph-parameters.md), das als Graf verwendet wird, um die Vorlagenliste einzugrenzen:

&lt;category>;&lt;subtitle>

Benutzerdefinierte Kategorien können in den von Projektdateien bereitgestellten Vorlagen eingerichtet werden (siehe unten). Diese Kategorien werden dann der Liste im Kombinationsfeld hinzugefügt.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![Dialogfeld &quot;Neuer Substance-Graf&quot; - Vorlagenkategorie einrichten](../../assets/newGraphDialog-templateCategorySetup.png "Dialogfeld &quot;Neuer Substance-Graf&quot; - Vorlagenkategorie einrichten"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filterung nach Projektdatei

Wenn eine der aktiven [Projektdateien](../../interface/preferences-window/project-settings/project-settings.md) einen oder mehrere Vorlagenpfade enthält, werden die Graf in den Paketdateien, die unter diesen Pfaden gefunden wurden, der Vorlagenliste hinzugefügt.

Verwenden Sie dann die Schaltfläche <b>Nach Projektdatei filtern</b>, um die Liste der Vorlagen auf die Vorlagen einzugrenzen, die von einer bestimmten Projektdatei bereitgestellt werden.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Dialogfeld &quot;Neuer Substance-Graf&quot; - Filterungen nach Projektdatei](../../assets/newGraphDialog-projectFiles.png "Dialogfeld &quot;Neuer Substance-Graf&quot; - Filterungen nach Projektdatei"){zoomable="yes"}

</td>
</tr>
</table>

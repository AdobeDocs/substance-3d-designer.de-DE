---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie MDL-Inhalte aus Substance 3D Designer zur Verwendung in externen Renderern und Anwendungen exportieren.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL-Inhalte werden exportiert
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# MDL-Inhalte werden exportiert

Auf dieser Seite werden die Exportprozesse für [MDL-Diagramms](../../mdl-graphs/mdl-graphs.md) und Materials in Substance 3D Designer beschrieben.

## Überblick

Nachdem ein MDL-Material in Designer erstellt wurde, muss es in ein Format exportiert werden, das *die Definition des Materials enthalten kann*, und von Renderern gelesen werden, die MDL unterstützen. MDL verwendet proprietäre Formate für Materialien, so genannte MDL-Module, die in verschiedenen Formaten geschrieben und verpackt werden, die alle aus Designer exportiert werden können.

>[!NOTE]
>
> Alle diese Formate können direkt mit einem *Texteditor* geöffnet werden - manchmal nach dem Entpacken mit einem Archivmanager -, um die darin enthaltene Formatdefinition zu überprüfen.

## MDL-Modul (\*.mdl)

Dies ist das grundlegende Austauschdateiformat für Material-Definitionen. Ein MDL-Modul definiert Folgendes:

* Merkmale und Verhalten des Materials
* seine freigelegte Parameter und Standardwerte
* ihre Anmerkungen (d. h. Metadaten): Autor, Tags, Kategorien, ...

Das Exportieren eines MDL-Moduls wird auf der Ebene *Paket* ausgeführt. Um ein MDL-Modul für ein bestimmtes Paket zu exportieren, klicken Sie im [Explorer](../../interface/the-explorer-window/the-explorer-window.md) auf die Schaltfläche ![](exporting-mdl-content.resources/exporting-mdl-content-01.png) <b>MDL-Modul</b> exportieren, oder wählen Sie diese Option im Kontextmenü des *Pakets* aus. Wählen Sie einen Zielspeicherort und einen Namen für das exportierte MDL-Modul aus, und das Dialogfeld <b>Bericht exportieren</b> wird mit der Liste der während des Exportvorgangs protokollierten Nachrichten angezeigt.

Das exportierte Modul enthält die Definitionen von *allen* MDL-Materialien, die durch ein [MDL-Diagramm](../../mdl-graphs/mdl-graphs.md) im Paket definiert sind.

>[!NOTE]
>
> Erfahren Sie mehr über die MDL-Modul in den Abschnitten 4 und 15 der [MDL-Spezifikation von NVIDIA](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9).

>[!NOTE]
>
> Warnungen nach dieser Vorlage: `x appears to be invalid whereas it was expected to be an mdl::call` wird durch die Art und Weise verursacht, wie MDL-Material in MDL-Diagrammen verarbeitet werden, und *kann* sicher ignorieren.

![MDL-Exportpfad](exporting-mdl-content.resources/exporting-mdl-content-02.png "MDL-Exportpfad")

*Die &quot;MDL-Modul exportieren&quot;-Pfade im Explorer und das resultierende Dialogfeld &quot;Bericht exportieren&quot;*

### MDL-Vorgabe (\*.mdl)

Eine Modulvorgabe ist weitgehend identisch mit dem MDL-Modul, auf dem sie basiert. Der einzige Unterschied besteht darin, dass sie einen anderen Satz von Standardwerten enthält - weitere Informationen [hier](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details).

Eine Vorgabe für ein MDL-Material, das einem Szene-Material &quot;`my_material`&quot; zugewiesen ist, kann von den folgenden Speicherorten exportiert werden:

* Der Bereich &quot;[Explorer](../../interface/the-explorer-window/the-explorer-window.md)&quot;, indem Sie auf &quot;<b>RMB</b>&quot; in der Ressource &quot;MDL-Diagramm&quot; klicken und die Exportvorgabe &quot;<b>Exportieren&quot; auswählen...Option </b> im Kontextmenü
* Das [3D-Ansicht](../../interface/3d-view/3d-view.md)-Bedienfeld mit <b>Materials > my\_Material > Vorgabe exportieren...</b>-Menüoption

Die Menüoption öffnet das Dialogfeld <b>MDL-Material-Vorgabe exportieren</b>, das die folgenden Optionen bietet:

* <b>Verzeichnis</b>: Der Zielspeicherort, an den das MDL-Modul exportiert wird
* <b>MDL-Dateiname</b>: Der Name des MDL-Moduls
* <b>Importierte MDL-Module einbetten</b>: Wenn das MDL-Modul auf importierten Modulen basiert - d. h. über Modulabhängigkeiten verfügt, führt das Aktivieren dieser Option dazu, dass die Modulabhängigkeiten *in das exportierte MDL-Modul eingebettet* werden, sodass es effektiv *autark* ist, auf Kosten der Dateigröße und der dynamischen Vererbung

Die exportierte Voreinstellung verwendet die *aktuellen Werte* der Parameter des Materials in der 3D-Ansicht als *neue Standardwerte*. Diese Werte können mit der Option <b>Materials > my\_Material > Edit</b> geändert werden, die die freigelegte Parameter des Materials im Eigenschaftenfenster anzeigt.

>[!WARNING]
>
> Beim Exportieren eines MDL-Moduls aus dem [Explorer](../../interface/the-explorer-window/the-explorer-window.md)-Bedienfeld wird ein MDL-Modul mit *allen* MDL-Materialien, die durch ein MDL-Diagramm im Paket definiert sind, exportiert. Beim Exportieren einer MDL-Vorgabe aus [3D-Ansicht](../../interface/3d-view/3d-view.md) wird ein MDL-Modul mit *nur* MDL-Materialien exportiert, die auf das *ausgewählte Material* im Menü angewendet wurden - `my_material` in diesem Beispiel.

![MDL-Vorgabe-Exportpfad](exporting-mdl-content.resources/exporting-mdl-content-03.png "MDL-Vorgabe-Exportpfad")

*Der Pfad &quot;Exportvorgabe&quot; in der 3D-Ansicht und das resultierende Dialogfeld &quot;Exportvorgabe für MDL-Material&quot;*

## MDL-Modul-Archiv (\*.mdr)

Ein MDL-Modul-Archiv kombiniert MDL-Module (siehe oben) mit Ressourcen wie *Texturen* und Readme-Dateien in einer *einzelnen transportablen Datei*.

Das Exportieren eines Paketarchivs erfolgt auf der Ebene *MDL-Modul*. Um ein Paketarchiv für ein bestimmtes MDL-Modul zu exportieren, klicken Sie auf die Schaltfläche ![](exporting-mdl-content.resources/exporting-mdl-content-01.png) <b>MDL-Modul-Archiv exportieren</b> in [Explorer](../../interface/the-explorer-window/the-explorer-window.md), oder wählen Sie dieselbe Option im Kontextmenü des *Pakets* aus. Wählen Sie einen Zielspeicherort und einen Namen für das exportierte MDL-Modularchiv aus, und das Dialogfeld <b>Bericht exportieren</b> wird mit der Liste der während des Exportvorgangs protokollierten Nachrichten angezeigt.

Das exportierte Modularchiv enthält ein MDL-Modul, das die Definitionen von *allen* der MDL-Materialien enthält, die durch ein [MDL-Diagramm](../../mdl-graphs/mdl-graphs.md) im Paket definiert sind. Wenn ein [Substance-Diagramm](../../compositing-graphs/substance-compositing-graphs.md) [in ein MDL-Diagramm &#x200B;](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md) instanziiert und mit einem Stream verbunden ist, der an den [Root](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)-Knoten geht, werden die von ihm ausgegebenen Texturen *im Archiv gespeichert*.

Zusätzlich zu diesen Elementen enthält das Archiv eine <b>MANIFEST</b>-Datei, die die folgenden Metadaten für das MDL-Modularchiv beschreibt:

* `mdl` die zum Exportieren des Modularchivs verwendete MDL-Version - z. B. &quot;1.5&quot;
* `version` die Version des Modularchivs - z.B. &quot;1.0.0&quot;
* `module` den Namen des Modularchivs - z.B. &quot;::pbr\_metallic\_roughness\_basic&quot;
* `exports.material` den Namen der im Modularchiv definierten Materialien - z. B. &quot;::pbr\_metallic\_roughness\_basic::MDL\_graph&quot;

>[!NOTE]
>
> Erfahren Sie mehr über das MDL-Archivdateiformat in Anhang C der [MDL-Spezifikation von NVIDIA](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9).

![MDR-Exportpfad](exporting-mdl-content.resources/exporting-mdl-content-04.png "MDR-Exportpfad")

*Der Pfad &quot;MDL-Modularchiv exportieren&quot; im Explorer und das resultierende Dialogfeld &quot;Bericht exportieren&quot;*

## MDL-gekapseltes Modul (\*.mdle)

MDL-Grafiken mit exponierten Parametern können als gekapselte MDL-Materialien exportiert werden. Durch die *-Kapselung werden Daten* in eine dedizierte Klasse eingeschlossen, sodass auf Daten *nicht direkt zugegriffen werden kann*.

Während Sie beispielsweise noch die Werte der angezeigten Parameter ändern können, um das Verhalten eines Materials zu steuern, ist die *Definition* dieser Parameter *nicht verfügbar* in einem gekapselten MDL-Modul.

Das Exportieren eines gekapselten MDL-Moduls wird im [Explorer](../../interface/the-explorer-window/the-explorer-window.md) auf der MDL-Diagrammebene durchgeführt, indem die Option <b>Als .mdle</b> exportieren im Kontextmenü eines MDL-Diagramms ausgewählt wird. Wählen Sie einen Zielspeicherort und einen Namen für das exportierte MDL-gekapselte Modul aus, und das Dialogfeld <b>Bericht exportieren</b> wird mit der Liste der während des Exportvorgangs protokollierten Meldungen angezeigt.

*Nur* die Materialdefinition für das *ausgewählte MDL-Diagramm* wird in das exportierte gekapselte MDL-Modul aufgenommen.

>[!NOTE]
>
> Erfahren Sie mehr über Definitionen von gekapseltem Material in Abschnitt 13.5 der [MDL-Spezifikation von NVIDIA](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) und der [MDL SDK API](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html).

![MDLE-Exportpfad](exporting-mdl-content.resources/exporting-mdl-content-05.png "MDLE-Exportpfad")

*Der Pfad &quot;Als Mdle exportieren&quot; im Explorer und das resultierende Dialogfeld &quot;Bericht exportieren&quot;*

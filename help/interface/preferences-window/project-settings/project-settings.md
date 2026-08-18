---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window/project-settings.html"
breadcrumb-title: ''
description: Konfigurieren Sie die Projekteinstellungen in den Substance 3D Designer-Voreinstellungen, um das Standardprojektverhalten anzupassen.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Project settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Projekteinstellungen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7dbdf7d5539fcc9450150b699fbd588cb0889892
workflow-type: tm+mt
source-wordcount: '2712'
ht-degree: 1%

---


# Projekteinstellungen

Auf dieser Seite werden die <b>Projekteinstellungen</b> in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) und die darin enthaltenen Einstellungen angezeigt.

Mit Substance 3D Designer können Sie Voreinstellungen *pro Projekt* erstellen und auf Workstations freigeben. Diese Voreinstellungen finden Sie auf der Registerkarte <b>Projekte</b> im Fenster [Voreinstellungen](../../../interface/preferences-window/preferences-window.md).

Dies ist sehr hilfreich, wenn Sie eine gemeinsame Arbeitsumgebung für ein Team einrichten möchten, das an demselben Projekt arbeitet, indem Sie die *gleiche* Projektdatei auf *allen* Systemen verwenden.

>[!NOTE]
>
> Weitere Informationen zum Einrichten und Integrieren von Substance 3D Designer in einer **Produktionspipeline** erhalten Sie, wenn *ausdrücklich empfohlen wird,* auf den Abschnitt [Pipeline und Projektkonfiguration](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) der Dokumentation zu verweisen.

![Projekteinstellungen](../../../assets/2019-3-0-prefs-proj-01.png "Projekteinstellungen"){zoomable="yes"}

## Konfiguration

### Konfigurationsdatei

Dadurch können Sie den Pfad der <b>Konfigurationsdatei</b> für Substance 3D Designer festlegen. Eine Konfigurationsdatei verwendet die Erweiterung &quot;<b>\*.sbscfg</b>&quot; und enthält eine Liste der Projektdateien zusammen mit einer festgelegten Kompatibilitätsanzeigeeinstellung.

*Standard: default\_configuration.sbscfg*

>[!NOTE]
>
> Sie können die Befehlszeilenoption &quot;**—config-file**&quot; verwenden, um Designer mit einer bestimmten Konfigurationsdatei zu starten.\
> Weitere Informationen zu Konfigurationsdateien finden Sie auf der Seite [Konfigurationsliste - SBSCFG](../../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) der Dokumentation.

### Projektdateien

Eine Projektdatei enthält eine Reihe von Einstellungen, die die wichtigsten Aspekte der Arbeitsumgebung in Designer definieren. Diese Einstellungen sind in Registerkarten unterteilt. Diese Einstellungen sind im Kapitel &quot;Projekt&quot; auf dieser Seite aufgeführt. Projektdateien verwenden die Erweiterung <b>\*.sbsprj</b>.

Sie können mehrere Projektdateien importieren, die in Ihrer Arbeitsumgebung in Designer verwendet werden sollen. Wenn mehrere Projektdateien vorhanden sind, werden Einstellungen, die Listen sind (z. B. von der Bibliothek überwachte Pfade, Aliasse usw.), *kombiniert* sind und Einstellungen, die eindeutige Satzwerte sind, durch die *letzte Projektdatei der Liste* definiert sind.

*Standard: default\_project.sbsprj (schreibgeschützt), user\_project.sbsprj*

>[!NOTE]
>
> Weitere Informationen zur Verwendung von Projektdateien in einer Produktionspipeline finden Sie auf der Seite [Projektkonfigurationsdateien - SBSPRJ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) der Dokumentation.

### Kompatibilitätsanzeige

Einige der mit einer neueren Version von Designer erstellten Knoten sind nicht mit älteren Versionen des Substance Engine kompatibel.

Im <b>Kompatibilitätsmodus</b> werden die Knoten hervorgehoben, die *nicht* mit dem ausgewählten Substance Engine kompatibel sind, mit einer gelben Kontur.

*Standard: Substance Engine v7*

### 3D-Ansicht

|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Standard-Renderer</b> | Mit dieser Einstellung können Sie den [3D-Renderer](../../../interface/3d-view/3d-renderers/3d-renderers.md) auswählen, der standardmäßig verwendet werden soll, wenn eine *neue* [3D-Ansicht](../../../interface/3d-view/3d-view.md) gestartet wird.<br><br>*Standard: Standard (vordefinierter Renderer)* |
| <b>Standardshader</b> | Mit dieser Einstellung können Sie den Shader auswählen, der standardmäßig verwendet werden soll, wenn eine *neue* [3D-Ansicht ](../../../interface/3d-view/3d-view.md)<br><br>*Standardeinstellung: open_pbr.glslfx* |
| <b>Standardumgebungszuordnung</b> | Mit dieser Einstellung können Sie die Textur auswählen, die standardmäßig auf die Umgebung angewendet werden soll, wenn eine *neue* [3D-Ansicht ](../../../interface/3d-view/3d-view.md)<br><br>*Standard: panorama\_map.hdr* |
| <b>Standardstatusdatei </b> | Die [3D-Ansicht](../../../interface/3d-view/3d-view.md) **Szenenstatusdatei** enthält eine Reihe von Einstellungen für die 3D-Ansicht, z. B. Kameraposition, Umgebungsbelichtung und Gitter. Sie wird verwendet, um den Status der 3D-Ansicht zu speichern, sodass Sie schnell eine Szene laden können, die auf Ihre Bedürfnisse zugeschnitten ist. Szenenstatusdateien verwenden die Erweiterung **\*.sbsscn**.Mit dieser Einstellung können Sie die Szenenstatusdatei der 3D-Ansicht auswählen, die verwendet werden soll, wenn eine neue 3D-Ansicht gestartet wird.  **Warnung:** Einige Software-Updates können die Art und Weise ändern, wie Szenenstatus gespeichert/geladen werden. Wenn die Szene *nicht korrekt wiederhergestellt wurde*, wird empfohlen, den gewünschten Status der Szene manuell festzulegen und *die Szenenstatusdatei, die Sie als Standard verwenden, erneut zu exportieren*. <br><br>*Standard: Leer (in diesem Fall wird ein voreingestellter Szenenstatus verwendet)* |
| <b>Standardbeleuchtungsstatus</b> | Mit dieser Einstellung können Sie auswählen, welche der vordefinierten verfügbaren Lichter beim Starten einer neuen [3D-Ansicht](../../../interface/3d-view/3d-view.md), *aktiviert werden soll, wenn keine Datei im Feld **Standardstatusdatei**<br><br>* Standard: Nur Umgebungslicht ** |

### Aliase

Aliase werden verwendet, um *Systempfade zu verkürzen* und es Teams zu ermöglichen, *Assets effizienter freizugeben*. Aliase werden *in der gesamten Software* sowie in *SBS-Dateien* verwendet.

Mit diesen Einstellungen können Sie *Aliase hinzufügen* und *bearbeiten*. Wenn ein Alias angewendet wird, ersetzt ** den zugeordneten Pfad mithilfe der folgenden Syntax: <b>://</b>

Beispiel: Wenn eine Ressource &quot;*myResource*&quot; im Ordner &quot;*myFolder*&quot; am Speicherort &quot;*C:/Users/user/Documents*&quot; platziert wird, führt die Zuordnung dieses Speicherorts zu &quot;*myalias*&quot; dazu, dass der Pfad &quot;*myalias://myFolder/myResource*&quot; in der Anwendung &quot;*&quot; und &quot;*&quot; im SBS-Paket, zu dem die Ressource gehört, verwendet wird.

*Standard: sbs; sd-3dview-shapes; sd-3dview-maps; sd-3dview-shaders (Standardprojekt)*

>[!WARNING]
>
> Für die Anwendung *sind Aliase* global. Dies bedeutet, dass sie auf *alle in der Anwendung verwendeten Pfade* sowie auf alle Pfade in *geladenen SBSPRJ-Projekteinstellungsdateien* angewendet werden. Berücksichtigen Sie dies beim Einrichten Ihrer Projektumgebung!\
> Außerdem wird empfohlen, *keine* Aliase zu verschachteln, d. h. einen Pfad zu aliasing, der auch in einem anderen Alias enthalten ist.

### Baker

|                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Standardressourcenname</b> | Mit dieser Einstellung können Sie eine standardmäßige **-Benennungsvorlage** festlegen, die für die Ausgabebilddateien verwendet wird. Die Aliase, die im [Backing-Fenster](../../../bakers/bakers.md) verfügbar sind, können auch hier verwendet werden (d. h. *$(mesh)*, *$(bakername)*, *$(udim)*, *$(custom)*)<br><br>*Standard: $(mesh)\_$(bakername)* |
| <b>Standardvorgabe</b> | Wenn Sie das [Backing-Fenster](../../../bakers/bakers.md) öffnen, können Sie es **bereits mit bestimmten Backern und Einstellungen** konfigurieren lassen, indem Sie mit dieser Option auf eine Voreinstellungsdatei *JSON* verweisen. Diese Datei kann aus dem Backfenster exportiert werden, nachdem sie gemäß Ihren Anforderungen eingerichtet wurde <br><br>*Standard: Keine* |
| <b>Namensfiltermodus</b> | Das Szenenobjekt, dessen Name für den Abgleich der Objekte mit niedrigem und hohem Poly verwendet werden soll:<ul data-preserve-html="true"> <li data-preserve-html="true">Geometriename: den Namen des Gittergeometrieobjekts verwenden</li> <li data-preserve-html="true">Übergeordneter Name (veraltet): den Namen des übergeordneten Objekts für die Gittergeometrie verwenden (wie in Designer 14.1 und niedriger)</li> </ul>*Standard: Geometriename* |
| <b>Ressourcenname-Makros</b> | Anstelle des Alias *$(bakername)* können Sie Ihre eigenen Zeichenfolgen für [jeden Baker](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings) verwenden.  Wenn der Alias &quot;***$(custom)***&quot; im Namen des Ausgabebilds für einen Bäcker verwendet wird, wird er durch die Zeichenfolge ersetzt, die mit diesem Bäcker in der Liste übereinstimmt. Wenn eine Zelle in der Liste, die einem Bäcker entspricht, leer gelassen wird, wird der Alias *$(custom)* für diesen Bäcker *nicht* ersetzt.Beispiel: Der dem Baker &quot;Kurvenkarte aus Gitter&quot; zugewiesene Wert &quot;c-mesh&quot; benennt automatisch *t\_mymesh\_**$(custom)*** in *t\_mymesh\_**c-mesh*** für die Ausgabe des Bäckers &quot;Kurvenzeichner aus Gitter&quot; um *nur *<br><br>*Standard: Keine* |
| <b>Namensfilter für Teilnetze</b> | Bei Verwendung der Option &quot;**Match By Name**&quot; in &quot;[bakers](../../../bakers/bakers.md)&quot; sind die Teile der Low- und High-Definition-Versionen eines Gitters *identisch*, wenn der Name dieser Teile vor den definierten **Suffixen** *identisch* ist. Mit dieser Einstellung können Sie Ihre eigenen Suffixe für Ihren spezifischen Workflow festlegen. Passende Teile von Gittern können dazu führen, dass Strahlen unerwünschte Geometrie bei Backvorgängen ignorieren.Beispiel: Das *body-torso**\_low***-Objekt im *body.fbx*-Gitter würde mit dem *body-torso**\_high ***-Objekt in *body\_high.fbx,* *übereinstimmen, wenn diese Objekte vorhanden sind* in diesen Gittern *.**Standard: \_low (Gitter mit niedriger Polung) / \_high (Gitter mit hoher Polung)*Ebenso können **Hintergrundflächen***selektiv ignoriert werden* für die Teile eines Gitters, deren Name das definierte **Suffix**enthält, für [spezifische Bäcker](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings), die die **Option &quot;Hintergrundfläche ignorieren&quot;** enthalten. Standardeinstellung: \_ignorebf *<br><br>*Hinweis:* Die Suffixe &quot;Hintergrundfläche ignorieren&quot; und &quot;Gitter mit niedriger/hoher Polung&quot; können * in beliebiger Reihenfolge kombiniert werden* (z. B. *Body-Torso\_low\_ignorebf*)<br><br>* |

### Farbmanagement

Weitere Informationen finden Sie auf der Seite [Farbmanagement](../../../color-management/color-management.md).

>[!WARNING]
>
> Die Änderungen an diesen Einstellungen werden nach dem Neustart von Designer wirksam.

### Allgemein

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Substance von Vorlagen</b> | Wenn Sie ein neues Diagramm erstellen, werden Sie aufgefordert, mit der Arbeit an einer **Vorlage** zu beginnen, die eine Reihe von Einstellungen und Inhalt *vorkonfiguriert* enthalten kann, z. B. Ausgaben (z. B. *PBR (Metallic/Roughness)*).Mit dieser Einstellung können Sie Designer auf Verzeichnisse verweisen, in denen Sie Ihre eigenen SBS-Dateien zur Verwendung als Vorlagen speichern können. Ihre benutzerdefinierten Vorlagen werden dann *der Liste hinzugefügt*, wenn ein neues Diagramm erstellt wird <br><br>*Standard: Keine *<br><br>*Hinweis:* Wir empfehlen, die aktuellen Vorlagen als Referenz für die Konfiguration und Formatierung Ihrer SBS-Vorlagendateien zu verwenden.  Die Vorlagen befinden sich im Ordner **Ressourcen > Vorlagen** im Substance 3D Designer-Installationsverzeichnis. |
| <b>3D-Szenen</b> | Standardmäßig verwendet Designer den Tangentenraum **MikkT** in der 3D-Ansicht. MikkT wird häufig verwendet und ist die Standardeinstellung in Programmen wie Unity, Unreal Engine 4, Blender und xNormal. Sie können **Ihren eigenen Tangentenraum** für die 3D-Ansicht verwenden, den Sie Designer in Form einer *DLL-Datei* in dieser Einstellung zur Verfügung stellen. Die Bezeichnung wird automatisch in der DLL-Datei erkannt, und Sie können die Beschreibung für das Plug-In bearbeiten <br><br>*Standard: mikktspace.dll* Tangentenrahmen immer neu berechnen <br><br>*Standard: Deaktiviert* Normal und Tangentialglättungswinkel <br><br>*Standard: 180.0°* |
| <b>Sonstiges</b> | Normale Zuordnungen können mit dem Format <b>DirectX</b> oder <b>OpenGL</b> generiert oder verarbeitet werden. Diese Einstellung legt den Wert für dieses Format an mehreren Stellen fest, z. B. [Materialeigenschaften](../../../interface/3d-view/material-properties/material-properties.md) in der [3D-Ansicht](../../../interface/3d-view/3d-view.md) und die [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)-Filterknotenparameter.<br><br>*Standard: DirectX*<br><br> In Bezug auf den Filterknoten [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) können Sie den Standardwert für den Parameter <b>Alpha Channel Content</b> festlegen. Sie können entweder festlegen, dass der Alpha-Wert in allen Fällen auf 1 gesetzt wird, oder ihn mit Informationen aus der Eingabe füllen.<br><br>*Standard: Alpha auf 1* erzwingen |
| <b>Bildformate</b> | Dadurch können Sie die Standardformateinstellungen für *exportierte* Bilder <br><br>*Standard festlegen: Standard (BMP)/Piz-basiertes Wavelet, deaktiviert, deaktiviert (EXR)/deaktiviert, deaktiviert, 75 (JPG)/Beste Geschwindigkeit, deaktiviert (PNG)/Standard (TGA)/LZW (TIF)/deaktiviert, 75 (WEBP)* |
| <b>Abhängigkeitspfade</b> | <p>SBS-Pakete weisen im Allgemeinen <b>Abhängigkeiten</b> auf, d. h. die Abhängigkeit von <i>externen Ressourcen</i>, wie z. B. anderen SBS-Paketen, Bitmaps oder Vektordateien.<br>Diese Abhängigkeiten, die im [Abhängigkeitsmanager](../../../interface/dependency-manager/dependency-manager.md) aufgeführt sind, werden gespeichert und <i>im SBS-Paket</i> mit einem <b>Pfad</b> referenziert, der auf diese Ressourcen verweist.</p><p>Für Abhängigkeiten, die den <i>gleichen Pfad</i> wie das SBS-Paket enthalten (d. h., sie befinden sich an denselben Speicherorten oder Unterordnern von diesem Speicherort), wird der Referenzpfad <b>relativ zum </b> Speicherort des SBS-Pakets geschrieben.</p><p>Beispiel: für ein SBS-Paket <code>myproject/mypackage.sbs</code>, ein Bild <code>myproject/myfolder/myimage.png</code> wird auf <code>myfolder/myimage.png verwiesen.</code> Pfad in <code>mypackage.sbs</code>).</p><p>Für Abhängigkeiten, die <i>nicht</i> enthalten, den gleichen Pfad wie das SBS-Paket (d. h. sie befinden sich an einem anderen Speicherort als das SBS-Paket), können Sie auswählen, wie der Pfad geschrieben wird.</p><p>Wenn sie auf <b>relative Pfade</b> festgelegt ist, wird auf die Ressource auf die gleiche Weise wie oben beschrieben verwiesen.</p><p>Beispiel: für ein SBS-Paket <code>myparentfolder/myproject/mypackage.sbs</code>, ein Bild <code>myparentfolder/myotherfolder/myimage.png</code> wird auf <code>../myotherfolder/myimage.png verwiesen.</code> Pfad in <code>mypackage.sbs</code>.</p><p>Wenn sie auf <b>absolute Pfade</b> festgelegt ist, wird die Ressource durch ihren vollständigen Systempfad referenziert.</p><p>Beispiel: für ein SBS-Paket <code>myparentfolder/myproject/mypackage.sbs</code>, ein Bild <code>myparentfolder/myotherfolder/myimage.png</code> wird auf diesen vollständigen Pfad in <code>mypackage.sbs verwiesen.</code></p><p><i>Standard: ...Relative Pfade.</i></p><p><i>Hinweis:</i> Das Verschieben der Ressourcen unterbricht in allen Fällen <i>Abhängigkeiten</i> , was zu <b>Ghost instance</b> Knoten in Diagrammen führt.  Um <i>alle Abhängigkeiten in einem einzelnen Projektordner zusammen mit dem SBS-Paket zu konsolidieren</i>, können Sie den <b>Export mit Abhängigkeiten verwenden...</b> Features im Bereich [Explorer](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html). Dadurch wird ein <i>eigenständiger </i>-Projektordner erstellt, der frei verschoben werden kann. |

### Bibliothek

In diesem Abschnitt können Sie <b>den benutzerdefinierten Inhalt</b> der [Bibliothek](../../../interface/the-library/the-library.md) verwalten.

Der Inhalt aller Ordner, die in der Liste <b>Hinzugefügte Pfade</b> aufgeführt sind, wird in die Bibliothek aufgenommen. Änderungen am Inhalt werden in der Bibliothek nach einem Aktualisierungszeitraum widergespiegelt, der in der [Bibliothek](../../../interface/preferences-window/preferences-window.md) [Registerkarte](../../../interface/preferences-window/preferences-window.md) des Fensters [Voreinstellungen](../../../interface/preferences-window/preferences-window.md) festgelegt werden kann.

In den Spalten der Liste finden Sie Optionen, die Ihnen eine detailliertere Kontrolle darüber geben, wie der Inhalt dieser Ordner der Bibliothek hinzugefügt wird:

* **Aktiviert:** Der Inhalt des Ordners wird in der Bibliothek angezeigt (*Standard: Aktiviert*)
* **Rekursiv:** Der Inhalt aller untergeordneten Ordner wird auch in der Bibliothek angezeigt (*Standard: Aktiviert*)
* **Muster ausschließen:** Dateien, deren *Name* mit dem eingegebenen Regex (regulärer Ausdruck) übereinstimmt, sind *nicht*, die in der Bibliothek angezeigt werden (z. B. `wip-*`) . Weitere Informationen zur Syntax für reguläre Ausdrücke [finden Sie hier](https://doc.qt.io/qt-5/qregularexpression.html#wildcardToRegularExpression)
* **Erweiterung ausschließen:** Dateien, die *Erweiterung* die Eingabetextzeichenfolge enthalten, sind *nicht*, die in der Bibliothek angezeigt werden. Mehrere Zeichenfolgen sollten durch `;` Semikolons getrennt werden. (E.g. `jpg;png;tif;fbx`)

Wenn SBS-Pakete zur Bibliothek hinzugefügt werden, können die **Diagramme** und **Ressourcen**, die darin enthalten sind, *in der Bibliothek* als separate Einträge angezeigt werden, wenn ihr Parameter **Sichtbar in Bibliothek** auf &quot;Ja&quot; festgelegt ist.\
Es sind Optionen verfügbar, mit denen definiert werden kann, ob dieser Parameter beim Erstellen/Hinzufügen eines neuen Diagramms oder einer neuen Ressource in einem Paket standardmäßig auf &#39;Yes&#39; ** festgelegt werden soll.

*Standard: Aktiviert*

Wenn ein in der Library enthaltenes [Photoshop](https://www.adobe.com/products/photoshop.html)-Dokument (\*.PSD-Datei) <b>mehrere Ebenen</b> enthält, können Sie den Inhalt von* jeder Ebene als separaten Bildeintrag* in der Library anzeigen.

*Standard: Aktiviert*

>[!NOTE]
>
> Ihre benutzerdefinierten Ressourcen werden der Bibliothek hinzugefügt. Möglicherweise ist *nicht sichtbar*, da die Filterregeln für die vorhandenen Bibliothekskategorien festgelegt wurden. Wir empfehlen, *eigene Filter* zu erstellen, die in Ordnern organisiert sind, um sicherzustellen, dass Ihre Inhalte während der Arbeit an Ihren Projekten zuverlässig gefunden werden können.\
> Weitere Informationen finden Sie im Abschnitt [Verwalten von benutzerdefiniertem Inhalt und Filtern](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/creating-library-filters-for-projects-170459772.html) der Dokumentation.

### Python

Substance 3D Designer lädt automatisch alle [Plug-ins](../../../scripting/plugin-basics/plugin-basics.md), die sich in den Ordnern befinden, die Sie der Liste <b>URL</b> hinzufügen.

*Standard: Keine*

>[!WARNING]
>
> Die Änderungen an diesen Einstellungen werden nach dem Neustart von Designer wirksam.\
> [Plug-In-Pakete](../../../scripting/plugins-packages/plugins-packages.md) müssen noch *manuell* mithilfe des [Plug-In-Managers](../../../scripting/plugin-manager/plugin-manager.md) installiert werden.

### Skripting

>[!WARNING]
>
> Diese Funktion wird in einer zukünftigen Version *eingestellt* sein und die robustere **Python-API** unterstützen. Daher empfehlen wir, den Wechsel in Ihren Skripten so schnell wie möglich vorzunehmen.\
> Sie können die Seite [Anwendungsrückrufe](../../../scripting/application-callbacks/application-callbacks.md) im Abschnitt [Skripterstellung](../../../scripting/scripting.md) unserer Dokumentation aufrufen, um loszulegen.

In diesem Abschnitt können Sie *Skripte* einrichten und steuern, die ausgeführt werden sollen, wenn bestimmte *Ereignisse* in Designer stattfinden. Dies ist besonders nützlich, wenn es in Verbindung mit der [Perforce](https://www.perforce.com/)-Integration verwendet wird, die auf der Registerkarte Versionskontrolle der Projekteinstellungen konfiguriert werden kann.

|                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Aktionen</b> | Designer hat **Rückrufauslöser** vorkonfiguriert, die *das Skript* ausführen, das Sie mithilfe des Interpreters bereitstellen, der in der unten beschriebenen Liste **Interpreters** eingerichtet ist.Folgende Rückrufe sind enthalten:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>onBeforeFileLoaded</strong> - führt das Skript <em>aus, bevor </em> ein SBS-Paket geladen wurde.</li><li data-preserve-html="true"><strong>onAfterFileLoaded</strong> - führt das Skript <em>aus, nachdem </em> ein SBS-Paket geladen wurde.</li><li data-preserve-html="true"><strong>onBeforeFileSaved</strong> - führt das Skript <em>aus, bevor </em> ein SBS-Paket gespeichert wird.</li><li data-preserve-html="true"><strong>onAfterFileSaved</strong> - führt das Skript <em>aus, nachdem </em> ein SBS-Paket gespeichert wurde.</li><li data-preserve-html="true"><strong>getGraphExportOptions</strong> - führt das Skript aus, wenn die [Exportausgabeoptionen](../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) aufgerufen werden.</li></ul>Ein [Python](https://www.python.org/)-Skript ist in den Installationsdateien enthalten, wobei die Funktionen, die durch jeden Rückruf *ausgelöst werden, bereits eingerichtet sind* und einsatzbereit sind. Sie können sie als Ausgangspunkt verwenden und Ihren Anforderungen entsprechende Funktionen hinzufügen. Dieses Skript ist **functions.py** und befindet sich im Ordner **tools > scripting** der Installationsdateien <br><br>*Standard: Keine *<br><br>*Hinweis:* Wenn Sie zunächst ein Skript für einen der Rückrufe auswählen, wird dieses Skript aus Zweckmäßigkeitsgründen in *alle* Rückrufe eingegeben. Sie können verschiedene Skripte für bestimmte Rückrufe nach diesem Zeitpunkt frei einrichten. |
| **Dolmetscher** | In dieser Liste können Sie bestimmte *Interpreter* angeben, die Designer verwenden sollte, um die Skripts auszuführen, die in der oben beschriebenen Liste **Aktionen** eingerichtet wurden. Interpreter werden mit einem *benutzerdefinierten Alias* identifiziert, das Sie im Textfeld jedes Eintrags in der Liste bearbeiten können. Ein [Python](https://www.python.org/) 3.6-Interpreter wird mit den Installationsdateien von Designer gebündelt. Sie finden sie im Ordner **plugins > pythonsdk** der Installationsdateien <br><br>*Standard: Keine* |

### Versionskontrolle

>[!WARNING]
>
> [Perforce](https://www.perforce.com/) ist das *only*-Tool, das derzeit für die Versionskontrolle unterstützt wird.

Weitere Informationen finden Sie auf der Seite [Versionskontrolle](../../../interface/preferences-window/version-control/version-control.md).

**Wie sollten Sie das verwenden?**

Sie sollten alle Voreinstellungen festlegen, die *projektspezifisch* in einer Projektdatei (\*.sbsprj) in Designer sind. Zu diesen Voreinstellungen gehören:

* Tangent-Space-Modul
* Bibliothek
* Aliase
* 3D-Anzeigeeinstellungen
* Backeinstellungen
* [Versionskontrolle-Einstellungen](../../../interface/preferences-window/version-control/version-control.md)

Alle Pfade werden *relativ zu* der Projektdatei (.spsprj) gespeichert. , damit Sie einen Ordner **library** am selben Speicherort wie Ihre Projektdatei in Perforce mit der folgenden Unterordnerstruktur haben können:

* maps/
* Meshes/
* sbs/
* sbsar/
* psd/
* 3Dview/
* ...

Auf derselben Ebene wie die Projektdatei können Sie auch ein Tangentenraum-Plugin oder einen Standard-Shader speichern.

Die Konfigurationsdatei (\*.sbscfg) sollte neben der Projektdatei im Perforce-Arbeitsbereich platziert werden.

>[!NOTE]
>
> Für weitere Informationen zum Einrichten und Integrieren von Substance 3D Designer in einer **Produktionspipeline** empfehlen wir *dringend,* auf den Abschnitt [Pipeline und Projektkonfiguration](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) der Dokumentation zu verweisen.

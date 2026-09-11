---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: Greifen Sie auf die vollständige Substance 3D Designer Python-Skript-API-Referenz für die Entwicklung von Plug-ins zu.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scripting-API-Referenz
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Scripting-API-Referenz

Auf dieser Seite werden die Hauptkonzepte der API beschrieben.

Weitere Informationen finden Sie in der Dokumentation, die mit der Anwendung geliefert wurde und die unter <b>Hilfe > Python-API-Dokumentation verfügbar ist...</b> Führen Sie in dieser Dokumentation eine <b>Schnellsuche</b> nach den Modulnamen (in Klammern unten) durch, um ihre Definition leicht zu finden.

## Context

Das Kontextobjekt (*Context*) ist der <b>Haupteinstiegspunkt zur API </b>. Es wird erstellt, wenn der Benutzer es zum ersten Mal abruft, indem die Methode &quot;<b>*getContext()*</b>&quot; aus dem Modul &quot;*sd*&quot; verwendet wird.

Mit diesem Objekt kann das Anwendungsobjekt </b> (*SDApplication*) im Wesentlichen <b>abgerufen werden.

## Anwendung (SDApplication)

Die Anwendung (*SDApplication*) ist das Objekt, das <b>Zugriff auf die Haupt-API-Manager ermöglicht</b>, z. B.:

* das <b>Paket </b>Manager (*SDPackageMgr*), das alle <b>Pakete</b> der Anwendung verwaltet;
* das <b>Modul </b>Manager (*SDModuleMgr*), das alle <b>Module</b> der Anwendung verwaltet;
* der <b>UI </b>Manager (*SDUIMgr*), der <b>Menüs und Docks </b> im Anwendungsfenster erstellen kann.

Sie können <b>Rückrufe</b> bei der Anwendung registrieren, die aufgerufen wird, wenn bestimmte Ereignisse eintreten.

## Package Manager (SDPackageMgr)

Dieses Objekt verwaltet alle <b>Pakete</b> der Anwendung. Die Pakete werden in der Komponente &quot;<b>*Explorer*</b>&quot; angezeigt.

Damit haben Sie folgende Möglichkeiten:

* <b>Erstellen</b> eines neuen Pakets
* <b>Laden/Entladen</b> eines Pakets;
* <b>Speichern</b> eines Pakets;
* <b>ein Paket finden</b>.

## Paket (SDPackage)

Ein Paket (*SDPackage*) ist eine <b>Sammlung von Ressourcen</b> (*SDResource*).

Der Inhalt eines Pakets kann <b>gespeichert</b> in eine Datei mit der Erweiterung <b>.sbs</b> über das Objekt &#39;*SDPackageMgr*&#39; sein. Mit diesem Objekt können Sie <b> </b> spezifische Ressourcen abrufen.

Informationen zum <b>Erstellen</b> einer bestimmten Ressource finden Sie unter den statischen Methoden für verwandte Objekte (Beispiel: &#39;*SDSBSCompGraph.sNew()*&#39;).

Ein Paket enthält auch ein Metadatenwörterbuch (SDMetadataDict). Weitere Informationen zu den Metadaten [&#x200B; finden Sie hier: &#x200B;](../../package-metadata/package-metadata.md).

## Ressource (SDR-Ressource)

Eine Ressource (*SDResource*) ist ein Objekt, auf das von einer anderen Ressource <b>verwiesen</b> werden kann.

Es sind mehrere Ressourcen <b>Typen</b> vorhanden:

* Ordner (*SDResourceFolder*);
* Graf (*SDGraph*);
* Bitmaps (*SDResourceBitmap*);
* SVG Images (*SDResourceSVG*);
* Schriftarten (*SDResourceFont*);
* Szenen (*SDResourceScene*);
* BSDF-Messungen (*SDResourceBSDFMesurement*);
* Lichtprofile (*SDResourceLightProfile*).

Eine Ressource kann <b>erstellt</b> von der statischen Methode &#39;*sNew()*&#39; unter dem folgenden Pfad sein:

* ein Paket;
* einem Ordner.

Eine Ressource kann mehrere <b>Eigenschaften</b> (*SDProperty*) aufweisen.

## UI-Manager (SDUIMgr)

Mit dem UI-Manager kann <b>Benutzeroberflächenelemente</b> im Hauptfenster des Substance Designers erstellen, z. B. <b>Menüs</b>, <b>Docks</b>, und die Registrierung von <b>Rückrufen</b> kann aufgerufen werden, wenn Ereignisse im Zusammenhang mit der Benutzeroberfläche eintreten.

Außerdem hat der UI-Manager Zugriff auf den <b>aktuellen aktiven Graf</b> und die <b>Auswahl</b> des aktiven Grafen.

## Graf (SDGraph)

Ein Graf (*SDGraph*) ist ein Objekt, das Folgendes enthält:

* <b>Knoten </b>(*SDNode*);
* <b>Graf-Objekte</b> (*SDGraphObjects*);
* <b>Eigenschaften </b>(*SDProperty*).

Es gibt vier verschiedene Graf-Typen:

* Substance-Graf (*SDSBSCompGraph*)
* Substance function Graf (*SDSBSFunctionGraph*)
* Substance FXMap Graf (*SDSBSFxMapGraph*)

Ein Graf kann einen oder mehrere <b>Ausgabeknoten</b> haben. Die Ausgabeknoten stellen die <b>Ergebnisse</b> des Diagramms dar.

Alle für einen Graf verfügbaren Knoten können <b>abgerufen</b> mit der *getNodeDefinitions()*-Methode sein.

Ein neuer Knoten kann <b>erstellt</b> mit der Methode &#39;*newNode()*&#39; sein.

Ein neuer <b>Instance</b>-Knoten kann aus einer Ressource (*SDResource*) mit der Methode &#39;*newInstanceNode()*&#39; erstellt werden.

## Knoten (SDNode)

Ein Knoten (*SDNode*) stellt einen <b>Vorgang</b> dar, der für ein Objekt ausgeführt wird.

Sie kann aus folgenden Quellen erstellt werden:

* eine <b>Definition</b> (*SDDefinition*) (siehe &quot;*SDGraph.newNode()&quot;*);
* <b>Ressource</b> (*SDResource*) (siehe &quot;*SDGraph.newInstanceNode()&quot;*).

Ein Knoten kann mehrere <b>Eigenschaften</b> haben.

Es gibt mehrere <b>Typen</b> von Knoten:

* *<b>SDSBSCompNode</b>*: Ein Knoten des Substance-Grafen (*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: Ein Knoten des Substance-Funktionsgraphen (*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: Ein Knoten des Substance FXMap Graph (*SDSBSFxMapGraph*);

## Graf-Objekte (SDGraphObjects)

Ein Graf-Objekt (*SDGraphObject*) ist ein Objekt, das <b>dem Graf zusätzliche Informationen</b> hinzufügt, das jedoch <b>*nicht* während des Graf-Evaluierungsprozesses berücksichtigt</b> wird.

Es gibt <b>3 Typen</b> von Graf-Objekten:

* <b>Nadel</b> (*SDGraphObjectPin*)
* <b>Kommentar</b> (*SDGraphObjectComment*)
* <b>Rahmen</b> (*SDGraphObjectFrame*)

Weitere Informationen zum Erstellen von <b>sNew()</b>-Objekten finden Sie in der statischen Methode &#39;*sNew()*&#39; für diese Objekte.

## Eigenschaften (SDProperty)

Eine Eigenschaft (*SDProperty*) ist ein Objekt, das <b>eine Eigenschaft von <b>einem anderen Objekt</b> (Graf, Knoten, Ressource usw.) beschreibt</b>.

Sie gehört zu einer bestimmten <b>Kategorie</b> (*SDPropertyCategory*):

* <b>Eingabe</b>: klassifiziert die Eingabeeigenschaften eines Objekts, die in der Regel <b> Auswirkungen auf den vom aktuellen Objekt ausgeführten Vorgang </b> haben;
  * Beispiel: Die *color*-Eigenschaft eines Einheitliche Farbe-Knotens in einem Substance-Graf ist eine Eingabeeigenschaft.
* <b>Ausgabe</b>: klassifiziert die Ausgabeeigenschaften eines Objekts. Es wird verwendet, um ein <b>Ergebnis</b> eines Objekts zu identifizieren.
* <b>Anmerkung</b>: klassifiziert Eigenschaften, die <b>*sich nicht* auf den von einem Objekt ausgeführten Vorgang </b> auswirken;
  * Beispiel: Die *Bezeichnung* eines Diagramms ist eine Anmerkungseigenschaft, da sie sich nicht auf die Diagrammberechnung auswirkt.

Es enthält die folgenden <b>Mitglieder</b>:

* <b>ID</b>: die Bezeichnung der Eigenschaft im Kontext dieser Kategorie;
* <b>Typen</b>: Die von der aktuellen Eigenschaft unterstützten Typen. Einige Eigenschaften können *mehrere* Typen unterstützen: &#39;*int*&#39;, &#39;*float*&#39; usw.;
  * Beispiel: Die Eingabeeigenschaften eines Knotens &quot;*sbs::function::add*&quot; können verschiedene Typen unterstützen: &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39; usw.;*
* <b>Kategorie</b>: Die Kategorie, zu der die Eigenschaft gehört (Eingabe, Ausgabe, Anmerkung);
* <b>Bezeichnung</b>: Die Bezeichnung der Eigenschaft, die für die Anzeige *only* verwendet wird;
* <b>Beschreibung</b>: die Beschreibung der Eigenschaft;
* <b>Standardwert</b>: Der Standardwert;
* <b>IsConnectable</b>: Zeigt an, ob eine Verbindung (*SDConnection*) *für diese Eigenschaft ausgeführt werden kann*;
* <b>isReadyOnly</b>: Gibt an, ob die Eigenschaft schreibgeschützt ist. Wenn &quot;true&quot;, kann der damit verknüpfte Wert *nicht* geändert werden.
* <b>isVariadic</b>: Wenn &quot;true&quot;, wird diese Eigenschaft als *mehrere* Eigenschaften für das Objekt dargestellt.
* <b>isPrimary</b>: Gibt an, ob die angegebene Eigenschaft die *Prinzipal*-Eigenschaft ist, die einige andere Eigenschaften steuert. *Hinweis:* Dies ist spezifisch für Substance *Compositing* Nodes (*SDSBSCompNode*).

Beispiele:

* Eigenschaften des Knotens &quot;*sbs::compositing::input*&quot;:

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::input</th></tr><tr><td style="text-align: left;"><strong>Eingabe</strong></td><td style="text-align: left;"><strong>Anmerkung</strong></td><td style="text-align: left;"><strong>Ausgabe</strong></td></tr><tr><td>$outputsize</td><td>Etikett</td><td><p>unique_filter_output (CONNECTABLE)</p></td></tr><tr><td>$format</td><td>Beschreibung</td><td><br/></td></tr><tr><td>$pixelsize</td><td>Kennzeichen</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$Kachelung</td><td>Gruppe</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleF</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>Verwendungen</td><td><br/></td></tr></tbody></table>

* Eigenschaften des Knotens &quot;*sbs::compositing::blend*&quot;:

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::blend</th></tr><tr><td style="text-align: left;"><strong>Eingabe</strong></td><td style="text-align: left;"><strong>Anmerkung</strong></td><td style="text-align: left;"><strong>Ausgabe</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONNECTABLE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$Kachelung</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.Verbindung (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.Verbindung (CONNECTABLE)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td>Deckkraft</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">Füllmethode</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">Farbmischung</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">Maskenrechteck</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## Typ (SDType)

Ein Typ (*SDType*) enthält Informationen mit dem Wert <b>type</b>, z. B.:

* <b>ID</b>: die Identifizierung des Typs;
* <b>Modifizierer</b>: Der Typmodifizierer, der einer der *SDTypeModifier&#39;* <b>enum</b>-Werte sein kann:
  * *Auto*;
  * *Einheitlich*: Der Wert wird *einmal* pro Vorgang ausgewertet.
  * *Variieren*: Der Wert wird *mehrmals* pro Vorgang ausgewertet (z. B.: für jedes Texel).

Es sind mehrere Typen definiert, z. B.:

* <b>Enums</b> (*SDTypeEnum*): beschreibt einen <b>Enumeration</b>-Typ mit allen zugehörigen Eigenschaften;
* <b>Strukturen</b> (*SDTypeStruct*): beschreibt einen Typ <b>structure</b> mit allen zugehörigen Eigenschaften;
* <b>Array</b> (*SDTypeArray*): beschreibt ein <b>Array</b>.
* usw.

Die vollständige Liste finden Sie in der *Python-API-Dokumentation des Substance Designers*.

## Werte (SDValue)

Ein Wert (*SDValue*) ist ein Objekt, das <b>einen *Basistyp*-Wert kapselt</b>.

Beispiel:

* Ein <b>*SDValueInt*</b>-Objekt kapselt einen *int*-Wert.
* Ein <b>*SDValueFloat4*</b>-Objekt kapselt einen *float4*-Wert.
* usw.

Der Basistypwert kann in der Regel <b>abgerufen</b> mit der <b>get()</b>-Methode sein, aber dies kann von dem *Typ* von *SDValue* abhängen, der zurückgegeben wurde.

## Verbindung (SDConnection)

Eine Verbindung (*SDConnection*) stellt eine <b>Verbindung</b> zwischen zwei verschiedenen <b> Eigenschaften</b> von zwei verschiedenen <b> Knoten</b> dar.

Es enthält:

* Der <b>Zielknoten</b>;
* Die <b>Zieleigenschaft</b> des Zielknotens;

Alle <b>Verbindungsvorgänge</b> werden auf einem Knoten ausgeführt:

* <b>Erstellen</b> einer neuen Verbindung, siehe &#39;*SDNode.newPropertyConnection()*&#39;
* <b>Löschen</b> einer vorhandenen Verbindung, siehe &quot;*SDNode.deletePropertyConnection()*&quot;.
* <b>Abrufen</b> der Verbindungen einer Eigenschaft, siehe &quot;*SDNode.getPropertyConnections()*&quot;

## Modul (SDModul)

Ein Modul ist eine <b>Sammlung von Definitionen und Typen</b>.

Es ermöglicht das einfache Abrufen aller Informationen über die Knoten, die erstellt werden können, sowie über Enumerationen und Strukturen.

Es enthält:

* eine <b>Identifizierung</b> (*ID*), die im Kontext des Modulmanagers (*SDModuleMgr*) eindeutig ist;
* eine Liste von <b>Definitionen</b> (*SDDefinition*);
* eine Liste von <b>Typen</b> (*SDType*).

## Definition (SDDefinition)

Ein Definitionsobjekt (*SDDefinition*) enthält Informationen zur Definition eines bestimmten <b>Objekts</b>, das auf <b>Eigenschaften</b> basiert (&#39;*SDNode&#39;* usw.).

Es enthält:

* <b>ID</b>: die Identifizierung der Begriffsbestimmung;
* <b>Bezeichnung</b>: Bezeichnung der Definition;
* <b>Beschreibung</b>: Beschreibung der Definition;
* <b>Eigenschaften</b>: Die Eigenschaften aller verfügbaren Eigenschaften *Kategorien* (*SDPropertyCategory*).

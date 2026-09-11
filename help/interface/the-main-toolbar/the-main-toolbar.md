---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über die Hauptsymbolleiste in Substance 3D Designer, um auf allgemeine Werkzeuge und Befehle für Ihren Arbeitsablauf zuzugreifen.
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Haupt-Werkzeugleiste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2a6e26cc03e887569a518cadd171ae1b51ae6abd
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# Die Hauptsymbolleiste

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Auf dieser Seite werden die Hauptsymbolleiste und das Menü von [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) beschrieben, die oben links im Hauptfenster angezeigt werden.Es besteht aus zwei Teilen: die Dropdown-Hauptmenüs und Schaltflächen mit Schnellzugriff. Auf alle Schaltflächenfunktionen für den Schnellzugriff kann auch über die Menüs <b>Datei</b> und <b>Bearbeiten</b> zugegriffen werden.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Hauptsymbolleiste](the-main-toolbar.resources/mainmenu.png "Hauptsymbolleiste")

</td>
</tr>
</table>

## Schaltflächen für den Schnellzugriff

![](the-main-toolbar.resources/newsubstance.png) <b>Neuer Substance-Graf...:</b> (Strg+N)Zeigt das Fenster [Neuer Graf](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) an und erstellt dann ein neues Paket mit einem [Substance-Graf](../../compositing-graphs/substance-compositing-graphs.md).

![](the-main-toolbar.resources/open.png) <b>Öffnen...:</b> (Strg+O) Öffnen Sie ein vorhandenes [Substance-Paket (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

![](the-main-toolbar.resources/saveall.png) <b>Alle speichern:</b> (Strg+⇧+S) Speichert alle Pakete, die im [Explorer](../../interface/the-explorer-window/the-explorer-window.md) aufgelistet sind.

![](the-main-toolbar.resources/undo.png) <b>Rückgängig:</b> (Strg+Z) Macht den letzten Vorgang rückgängig.

![](the-main-toolbar.resources/redo.png) <b>Wiederholen:</b> (Strg+Y) Wiederholen Sie den letzten rückgängig gemachten Vorgang.

## Datei

<b>Neu:</b> öffnet ein Untermenü zum Erstellen eines Grafen oder Pakets:

* <b>Neuer Substance-Graf..:</b>(Strg+N) Zeigt das Fenster [Neuer Graf](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) an, in dem Sie einen neuen [Substance-Graf](../../compositing-graphs/substance-compositing-graphs.md) einrichten können;
* <b>Neuer Substance-Funktions-Graf:</b> Erstellt ein neues Paket mit einem [Substance-Funktions-Graf &#x200B;](../../function-graphs/function-graphs.md);
* <b>Leer:</b> Erstellt ein leeres Paket.

<b>Öffnen...:</b> (Strg+O) Öffnen Sie ein vorhandenes [Substance-Paket (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

<b>Zuletzt verwendete Pakete:</b> Zeigt eine Liste der zuletzt geöffneten Pakete an. Klicken Sie auf einen Eintrag, um ihn zu öffnen.

<b>Letzte Sitzungspakete öffnen (#)</b>: Öffnet alle Pakete, die beim Schließen oder Beenden der letzten Sitzung geöffnet waren.

<b>Alle speichern:</b> (Strg+⇧+S) Speichert alle offenen Pakete, einschließlich im Hintergrund geladener Pakete.

<b>Alle schließen:</b> Schließt alle geöffneten Pakete.

<b>Ressourcen neu laden:</b> Erzwingt, dass Designer [alle Ressourcen, einschließlich Bitmaps und SVG-Daten, neu lädt](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

<b>Beenden:</b> (Strg+Q) - Schließen Sie Substance 3D Designer.

## Bearbeiten

<b>Rückgängig:</b> (Strg+Z) Letzten Vorgang rückgängig machen.

<b>Wiederholen:</b> (Strg+Y) Wiederholen Sie den zuletzt rückgängig gemachten Vorgang.

<b>Voreinstellungen...:</b> Öffnet das Fenster &quot;Voreinstellungen&quot;.

>[!NOTE]
>
> Dieses Dialogfeld finden Sie im Substance 3D Designer-Menü in der Taskleiste auf dem macOS.

## Werkzeuge

<b>Rendern abbrechen:</b> (Esc) Stoppt den aktuellen Vorgang für das Substance Engine. Kann verwendet werden, um einen unerwünschten, schweren Vorgang abzubrechen.

<b>Modul anhalten:</b> (⇧+Esc): Das Rendermodul wird angehalten. Dies kann die Bearbeitung komplexer [Substance-Graphen](../../compositing-graphs/substance-compositing-graphs.md) beschleunigen.

<b>Modul wechseln..: </b>(F9) Bietet verschiedene Rendering-Engines, einschließlich GPU-Engines (&quot;DirectX&quot; unter Windows, &quot;OpenGL&quot; unter macOS) sowie die CPU-Engine (&quot;NEON&quot; unter Apple Silicon, &quot;SSE&quot; unter allen anderen).

<b>Substance Player:</b> Verwalten der Integration von Designer mit Substance Player:

* <b>Player suchen...:</b> Designer mitteilen, wo Player installiert ist;
* <b>Player herunterladen...:</b> Öffnet die [Landingpage](https://helpx.adobe.com/substance-3d-player/home.html) der Substance Player-Dokumentation, auf der der Player heruntergeladen werden kann.

<b>Plug-In-Manager...1: Öffnet das Fenster &quot;Plug-in-Manager&quot;, in dem Sie [Python-Plug-ins für Substance 3D Designer installieren, laden und entladen können.](../../scripting/scripting.md)</b>

## Windows

<b>Neuer Explorer:</b> Öffnet ein neues Explorer-Dock. Es können mehrere Explorer-Docks geöffnet sein.

<b>Neue 3D-Ansicht:</b> Öffnet ein neues 3D-Ansicht-Dock. Sie können mehrere 3D-Ansicht-Docks geöffnet haben.

<b>Neue Bibliotheksansicht:</b> Öffnet ein neues Bibliotheksdock. Sie können mehrere Bibliotheks-Docks geöffnet haben.

<b>Python-Editor:</b> Öffnet den Python-Editor, der zum [Auswerten und Erstellen von Skripten verwendet wird](../../scripting/scripting.md).

<b>Layout zurücksetzen:</b> Setzt den Arbeitsbereich auf das Standardlayout zurück. Alle Fenster werden neu angeordnet, und einige Fenster werden möglicherweise wieder ausgeblendet. Anwendung bei Problemen mit dem Programmlayout.

<b>Fenster nicht maximieren:</b> Wenn ein Fenster *maximiert* ist, wird es mit dieser Option nicht maximiert und das Layout wird wiederhergestellt, wie es *vor* war, als das Fenster maximiert wurde.

<b>Explorer:</b> Den [Explorer anzeigen/ausblenden](../the-explorer-window/the-explorer-window.md).

<b>Diagramm:</b> Zeigen/Ausblenden des [Diagrammfensters](../../interface/the-graph-view/the-graph-view.md)(s) an.

<b>Parameter:</b> Die [Eigenschaften](../properties/properties.md) ein-/ausblenden.

<b>Konsole:</b> Das Konsolenfenster ein-/ausblenden.

<b>3D-Ansicht:</b> [3D-Ansicht(en) anzeigen/ausblenden](../../interface/3d-view/3d-view.md).

<b>Abhängigkeitsmanager:</b> Den [Abhängigkeitsmanager anzeigen/ausblenden](../../interface/dependency-manager/dependency-manager.md).

<b>2D-Ansichten:</b> Anzeigen/Ausblenden der [2D-Ansichten](../2d-view/2d-view.md).

<b>Bibliothek:</b> Das [Bibliotheksfenster ein-/ausblenden.](../../interface/the-library/the-library.md)

<b>Hauptsymbolleiste:</b> Anzeigen/Ausblenden der Hauptsymbolleiste (nur Schnellzugriffsschaltflächen).

>[!NOTE]
>
> Weitere Informationen über die Bedienfeldverwaltung von Designer, die Anpassungs- und Workflow-optimierenden Funktionen finden Sie auf der Seite [Anpassen Ihres Arbeitsbereichs](../../interface/customizing-your-wor/customizing-your-workspace.md)dieser Dokumentation.

## Hilfe

<b>Tutorials:</b> Öffnet die [Substance 3D-Tutorials](https://substance3d.adobe.com/tutorials/)-Website (früher Substance Academy).<b>\
</b>

<b>Versionshinweise:</b> Öffnet ein Fenster mit dem Änderungsprotokoll der neuesten Version.

<b>Technische Anforderungen:</b> Zeigt die technischen Anforderungen zum Ausführen der Anwendung an.

<b>Dokumentation:</b> Öffnet Ihren Standard-Webbrowser auf [dieser Dokumentation](https://www.adobe.com/go/Substance-3D-doc-Designer_de).

<b>Skriptdokumentation:</b> Öffnet Ihren Webbrowser in den lokalen Python-API-Dokumenten.

<b>Foren...:</b> Öffnet Ihren Webbrowser in unserem [Support Community](https://forum.substance3d.com/) Forum, um sich mit der Community in Verbindung zu setzen und Fragen zu stellen.

<b>Fehler melden...:</b> Öffnen Sie das Fenster zur Fehlerberichterstattung.

<b>Protokoll exportieren...:</b> Exportiert die aktuellen Protokolldateien in eine komprimierte ZIP-Datei, um sie dem technischen Support zur Verfügung zu stellen.

<b>Feedback geben...:</b> Öffnet Ihren Webbrowser auf der Startseite der [Support Community](https://www.adobe.com/go/Substance-3D-feedback-Designer_de) von Adobe.

<b>Substance 3D-Assets:</b> Durchsuchen Sie [Premium-3D-Inhalte](https://substance3d.adobe.com/assets) nach Abonnenten (früher Substance Source).

<b>Substance 3D Community-Assets:</b> Sie können [kostenlose Community-Assets](https://substance3d.adobe.com/community-assets/) (früher Substance share) durchsuchen.

<b>Konto verwalten\*:</b> Öffnet die Webseite für Ihr Adobe-Konto.

<b>Anmelden/Abmelden...\*:</b> Ermöglicht die Anmeldung bei Ihrem Adobe-Konto.

<b>Startbildschirm...:</b> Zeigt das Dialogfeld [Startbildschirm](../../interface/home-screen/home-screen.md) an.

<b>Neue Funktionen...:</b> Zeigt einen Bildschirm an, in dem die Funktionen hervorgehoben werden, die der neuesten Version von Designer hinzugefügt wurden

<b>Begrüßungsbildschirm...\*:</b> Zeigt einen Bildschirm an, der neue Benutzer durch den Zweck von Designer und seine Position im [Substance 3D-Ökosystem führt](https://helpx.adobe.com/de/substance-3d.html)

<b>Partner:</b> Ermöglicht Ihnen den Zugriff auf die Haftungsausschlüsse und Hinweise für Integrationen von Drittanbietern von unseren Partnern in Designer.

<b>Info zu Substance 3D Designer..:</b> Zeigt Informationen über die Anwendung und ihre Komponenten an, z. B. die Versionsnummer.

\*: Diese Optionen sind nur in der Designer-Version verfügbar, die über [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud) installiert wurde. Hierfür ist ein [Substance 3D-Abonnement](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar) erforderlich.

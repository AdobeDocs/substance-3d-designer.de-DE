---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: Konfigurieren Sie die Versionskontrolleinstellungen in den Substance 3D Designer-Voreinstellungen, um sie mit Git und anderen Systemen zu integrieren.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versionskontrolle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Versionskontrolle

>[!IMPORTANT]
>
> Substance 3D Designer-Version <b>14.0.0</b> aktualisiert die Perforce-Unterstützung auf <b>Python 3</b>.
> 
> Stellen Sie sicher, dass Ihre anderen Skripte und die Umgebung zur Versionskontrolle entsprechend angepasst sind.

Designer bietet eine Python-Integration des Versionskontrollsystems [Perforce](https://www.perforce.com/) (P4).

Die Integration fügt dem Kontextmenü von Paketen im [Explorer](../../../interface/the-explorer-window/the-explorer-window.md) ein benutzerdefiniertes Untermenü &quot;Versionskontrolle&quot; sowie benutzerdefinierte Symbole hinzu, die dem Paketstatus in P4 entsprechen.

## Vorbereiten von P4

Notieren Sie sich in [P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v) den Namen und Pfad des Arbeitsbereichs, wie unten gezeigt:

![Informationen zum P4V-Arbeitsbereich](version-control.resources/p4v-workspace-strings.jpg "Informationen zum P4V-Arbeitsbereich"){zoomable="yes"}

Öffnen Sie dieses Skript in einem Texteditor oder einer IDE, der sich in der Installation von Designer befindet: &#39;*tools/version\_control/perforce.py*&#39;.

Bearbeiten Sie in Zeile 19 den Pfad zum Speicherort der ausführbaren Datei </b> von <b>&#39;p4&#39; auf Ihrem System.\
Im folgenden Beispiel lautet dieser Pfad &quot;*c:/Program Files/Perforce/p4.exe*&quot;.

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Einrichten in Designer

Die Versionskontrolle wird in den [Projekteinstellungen](../../../interface/preferences-window/project-settings/project-settings.md) konfiguriert, die in den [Voreinstellungen](../../../interface/preferences-window/preferences-window.md) von Designer verfügbar sind.

Registerkarte ![ &quot;Versionskontrolle&quot; in den Projekteinstellungen ](version-control.resources/p4v-project-settings.jpg " Registerkarte &quot;Versionskontrolle&quot; in den Projekteinstellungen "){zoomable="yes"}

1. Gehen Sie zu &quot;Bearbeiten > Voreinstellungen&quot;.
1. Wechseln Sie zu &quot;Projekte&quot;, wählen Sie die Zielprojektdatei &quot;[&quot; aus ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) und wechseln Sie zur Registerkarte &quot;Versionskontrolle&quot;.
1. Aktivieren Sie &quot;Versionskontrolle aktiviert&quot;.
1. Füllen Sie diese Informationen im Abschnitt &quot;Arbeitsbereich&quot; aus:

   * <b>Name:</b> Geben Sie den Arbeitsbereichsnamen ein, den Sie zuvor von P4V abgerufen haben.
   * <b>Pfad:</b> Geben Sie den &#39;Workspace-Pfad&#39; ein, den Sie zuvor von P4V abgerufen haben

![P4-Setup in Designer: Arbeitsbereich](version-control.resources/p4v-project-settings-workspace.jpg "P4-Einrichtung in Designer: Arbeitsbereich"){zoomable="yes"}

### Einrichten von Aktionen

Die Aktionen sind im Kontextmenü eines Pakets im Explorer verfügbar. Es gibt vordefinierte Aktionen, die mit den meisten Konzepten des Versionskontroll-Tools übereinstimmen:

* Alle Aktionsbezeichnungen können nach Bedarf geändert werden.
* Alle Aktionen benötigen ein Skript, damit sie gültig sind.

Sie können Folgendes verwenden:

* Ein Skript *pro* Aktion
* Ein Skript für *alle* Aktionen

Ein Starterskript für alle Aktionen ist in der Installation von Designer verfügbar: &#39;*tools/version\_control/perforce.py*&#39;.

>[!IMPORTANT]
>
> Um verfügbar zu sein, muss das Paket unter dem &#39;Workspace-Pfad&#39; gespeichert werden (z. B. unter &#39;*f:/Dev/perforce*&#39;).

1. Klicken Sie in der Gruppe &quot;<b>Aktionen</b>&quot; auf die Schaltfläche &quot;...&quot;. Schaltfläche der Aktion <b>Hinzufügen</b>
1. Wählen Sie bei der Installation von Designer das folgende Skript aus: *Tools/version\_control/perforce.py*
1. Das Skript sollte automatisch für alle anderen Aktionen eingerichtet werden.

![P4-Setup in Designer: actions](version-control.resources/p4v-project-settings-actions.jpg "P4 setup in Designer: Aktionen"){zoomable="yes"}

### Benutzerdefinierte Aktionen einrichten

Da alle Versionskontrollwerkzeuge unterschiedlich sind und viele Funktionen enthalten, ermöglichen wir dem Benutzer, benutzerdefinierte Aktionen hinzuzufügen.

1. Auf &quot;Element hinzufügen&quot; klicken
1. Geben Sie die Beschriftung der neuen Aktion ein und legen Sie ihren Skriptpfad fest.

### Einrichten des Skriptinterpreters

1. Klicken Sie im Abschnitt &quot;Interpreter&quot; auf &quot;Element hinzufügen&quot;.
1. Legen Sie eine Skriptdateierweiterung oder ein Suffix sowie den Pfad zur ausführbaren Interpreterdatei fest.
1. Bearbeiten Sie das Skript perforce.py, um den Speicherort der Binärdatei &#39;p4&#39; zu aktualisieren.

![P4-Setup in Designer: Interpreter](version-control.resources/p4v-project-settings-interpreters.jpg "P4-Setup in Designer: Interpreter"){zoomable="yes"}

## Verwendung der Versionskontrolle

1. Neues Paket erstellen
1. Speichern Sie das Paket im Verzeichnis &quot;Workspace-Pfad&quot;
1. Klicken Sie auf RMB im Paket: Sie haben jetzt Zugriff auf das Untermenü &quot;Versionskontrolle&quot;.
1. Je nach Status der Paketdatei im Arbeitsbereich stehen mehrere Aktionen zur Verfügung:

   * <b>Hinzufügen:</b> Markieren Sie die Dateien als &quot;ToAdd&quot;.
   * <b>Senden:</b> Senden Sie die ausgewählten Pakete. Mit dieser Aktion wird ein Dialogfeld zum Festlegen einer Änderungsnachricht angezeigt (siehe unten).
   * <b>Zurücksetzen:</b> Stellen Sie die Änderungen wieder her. Diese Aktion zeigt ein Dialogfeld zum Auswählen der Dateien an, die zurückgesetzt werden sollen (siehe unten)
   * <b>Auschecken:</b> Auschecken der Datei aus dem Depot
   * <b>Letzte Version abrufen:</b> Abrufen der neuesten Version aus dem Depot
   * <b>Status aktualisieren:</b> Status der Paketdatei aktualisieren

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   ![ Dialogfeld &quot;Senden&quot;](version-control.resources/p4v-submit.jpg " Dialogfeld &quot;Senden&quot;"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   ![ Dialogfeld &quot;Zurücksetzen&quot; ](version-control.resources/p4v-revert.jpg " Dialogfeld &quot;Zurücksetzen&quot; "){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> Alle Aktionen unterstützen Mehrfachauswahl.
> 
> Bei P4- und anderen Versionskontrolltools, die schreibgeschützte Dateiberechtigungen verwenden, um Änderungen einzuschränken, muss der Benutzer das Paket zuerst auschecken, bevor er es ändert.
> 
> Schreibgeschützte Paketdateien können in SD nicht geändert werden.

Das Paket verfügt je nach Status über die folgenden Symbole:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Paketsymbol: Aktuell](version-control.resources/p4-up-to-date.png "Paketsymbol: Aktuell")

Aktuell

</td>
<td style="border: 0;" valign="top">

![Paketsymbol: Ausgecheckt](version-control.resources/p4-checked-out.png "Paketsymbol: Ausgecheckt")

Ausgecheckt

</td>
<td style="border: 0;" valign="top">

![Paketsymbol: Hinzugefügt](version-control.resources/p4-added.png "Paketsymbol: Hinzugefügt")

Zum Hinzufügen markiert

</td>
<td style="border: 0;" valign="top">

![Paketsymbol: Nicht im Depot](version-control.resources/p4-not-in-depot.png "Paketsymbol: Nicht im Depot ")

Nicht im Lager

</td>
</tr>
</table>

Beachten Sie, dass ein Paket, das nicht auf dem neuesten Stand ist, mit einem Warnzeichen gekennzeichnet ist.

## Aktionsskripte

Der Befehl, der von jeder Aktion ausgeführt wird, wird folgendermaßen erstellt:

my\_script <b>*WorkspaceName WorkspacePath ActionName[ActionArgs]*</b>

<b>Arbeitsbereichsname:</b> Name des Arbeitsbereichs

<b>WorkspacePath:</b> den Pfad des Stammverzeichnisses des Arbeitsbereichs

<b>ActionName:</b> Name der Aktion:

* *Hinzufügen:* für die Aktion &quot;Hinzufügen&quot;
* *Auschecken:* für die Aktion &quot;Auschecken&quot;
* *Senden:* für die Aktion &quot;Senden&quot;
* *Zurücksetzen:* für die Aktion &quot;Zurücksetzen&quot;
* *get\_last\_version:* für die Aktion &quot;Letzte Version abrufen&quot;
* *get\_status:* für die Aktion &quot;Status abrufen&quot;

Die Beschriftung wird in den Projekteinstellungen eingerichtet, wobei das Zeichen &#39; &#39; durch das Zeichen &#39;\_&#39; ersetzt wird - z. B.: &quot;Meine Aktion&quot; => &quot;Meine\_Aktion&quot;.

<b>ActionArgs:</b> Argumente der Aktion:

* *-desc*: Eine Beschreibungszeichenfolge, die von der Aktion &quot;Senden&quot; verwendet wird
* *-Dateien:* Eine Dateiliste
* *-files\_list:* Eine Textdatei, die eine Liste von Dateien pro Zeile enthält

<b>get\_status</b>: Gibt einen Wert zurück, der vom Status der angegebenen Datei abhängt:

* 0: Nicht definierter Status
* 1: nicht im Lager
* 2: Vorherige Version (nicht aktuell)
* 3: neueste Version (auf dem neuesten Stand)
* 4: ausgecheckt
* 5: zur Addition markiert
* sonstige Maßnahmen:
  * 0: Erfolg
  * andere: Fehler

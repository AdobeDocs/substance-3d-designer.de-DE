---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: Hier erfahren Sie, wie Sie Substance 3D Designer aktivieren und Lizenzen für den Zugriff auf alle Funktionen verwalten.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aktivierung und Lizenzen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# Aktivierungsprozess nach Anwendungstyp

Der Aktivierungsprozess hängt davon ab, wo Sie Designer erworben haben oder Zugriff darauf haben:

| Edition | Aktivierungsprozess |
| --- | --- |
| Creative Cloud Desktop | Weitere Informationen finden Sie auf der entsprechenden Seite in der [HilfeX-Dokumentation](https://helpx.adobe.com/support/substance-3d-designer.html). Falls Probleme auftreten, kann die [Creative Cloud-Dokumentation](https://helpx.adobe.com/creative-cloud/user-guide.html) zusätzliche Antworten liefern. |
| dämpfen | Starten Sie das Produkt direkt aus Ihrer Steam-Bibliothek. |
| Substance (eigenständig) | Weitere Informationen finden Sie im unten beschriebenen Aktivierungsprozess. |

## Aktivierungsschritte (Substance-Edition)

### AKTIVIERUNGSASSISTENT VERWENDEN

Es stehen drei Optionen zur Auswahl:

* <b>Dieses Produkt auswerten</b>: Ältere Testversionen sind nicht mehr verfügbar. Sie können stattdessen eine 30-tägige Testversion für jede Substance 3D-Anwendung [hier](https://www.adobe.com/creativecloud/3d-augmented-reality.html) oder mit Creative Cloud Desktop starten. Jede Testversion ist unabhängig von den anderen Substance 3D-Programmen. Sie können also einzeln oder alle Applikationen gleichzeitig testen.
* <b>Mit einer Lizenzdatei aktivieren</b>: Aktivieren Sie das Produkt mit einer Lizenzdatei (<b>\*.key</b>), die Sie vor dem 30. September 2022 von Ihrer Kontoseite auf der [Substance 3D-Website](https://store.substance3d.com/user) heruntergeladen haben.
* <b>Aktivieren mit Ihrem Konto</b>: Ältere Substanzkonten können nicht mehr für die Aktivierung verwendet werden.

>[!IMPORTANT]
>
> Um die Lizenzdatei mit dem Aktivierungsassistenten zu installieren, müssen Sie Designer als Administrator ausführen und das Antivirenprogramm vorübergehend deaktivieren.

![Aktivierungsassistent](../../assets/activation-wizard.png "Aktivierungsassistent")

### Manuelle Aktivierung

Sie können Designer manuell aktivieren, indem Sie die Datei license.key in den folgenden Ordner kopieren:

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Plattform</th>
<th style="text-align: left;">Version</th>
<th colspan="2" style="text-align: left;">Pfad</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b> oder höher</td>
<td style="text-align: left;">AppData &gt; Lokal</td>
<td style="text-align: left;">C:\Users\[Benutzername]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[Benutzername]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b> oder niedriger</td>
<td style="text-align: left;">AppData &gt; Lokal</td>
<td style="text-align: left;">C:\Users\[Benutzername]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData &gt; Roaming</td>
<td style="text-align: left;">C:\Users\[Benutzername]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b> oder höher<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[Benutzername]/Library/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> oder niedriger<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[Benutzername]/Library/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b> oder höher</td>
<td colspan="2" style="text-align: left;">/home/[Benutzername]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b> oder niedriger<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[Benutzername]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> Einige der Verzeichnisse in den oben genannten Pfaden sind möglicherweise standardmäßig ausgeblendet. Geben Sie den Pfad manuell im Datei-Explorer ein oder zeigen Sie ausgeblendete Dateien an, um sie anzuzeigen.

>[!IMPORTANT]
>
> Stellen Sie sicher, dass die Datei &quot;**license.key**&quot; heißt, andernfalls kann sie von der Anwendung nicht gefunden werden.

### UMGEBUNGSVARIABLE

Sie können den Speicherort, an dem Designer die Datei <b>license.key</b> sucht, mit einer [Umgebungsvariablen](../../pipeline-and-project-con/environment-variables/environment-variables.md) überschreiben.

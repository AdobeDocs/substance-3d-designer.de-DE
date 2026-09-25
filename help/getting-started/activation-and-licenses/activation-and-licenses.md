---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ""
description: Hier erfahren Sie, wie Sie Substance 3D Designer aktivieren und Lizenzen für den Zugriff auf alle Funktionen verwalten.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aktivierung und Lizenzen
user-guide-description: ""
user-guide-title: ""
source-git-commit: 21ee545724852c876444dcf3ed4a82af8d1e3715
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%
---

# Aktivierungsprozess nach Anwendungstyp

Der Aktivierungsprozess hängt davon ab, wo Sie Designer erworben haben oder Zugriff darauf haben:

| Edition | Aktivierungsprozess |
|:-----------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creative Cloud Desktop (CCD) | Installieren Sie das Produkt über die CCD-App und starten Sie es. Gehen Sie zu diesen Seiten, wenn Sie Probleme mit Ihrer Lizenz haben: [Anwendungen werden aufgrund eines Abonnementfehlers nicht gestartet](https://helpx.adobe.com/de/creative-cloud/apps/troubleshoot/launch-issues/apps-wont-launch-due-to-subscription-error.html) / [Konto, Abonnements und Abrechnungshilfe](https://helpx.adobe.com/de/account/individual.html) |
| dämpfen | Starten Sie das Produkt direkt aus Ihrer Steam-Bibliothek. |
| Substance (eigenständig) | Weitere Informationen finden Sie im unten beschriebenen Aktivierungsprozess. |

## Aktivierungsschritte (Substance-Edition)

### Verwenden des Aktivierungsassistenten

Wenn Sie Designer zum ersten Mal starten, wird der Aktivierungsassistent geöffnet und Sie werden durch den Aktivierungsprozess geführt.

Es stehen drei Optionen zur Auswahl:

* <b>Dieses Produkt auswerten</b>: Ältere Testversionen sind nicht mehr verfügbar. Sie können stattdessen eine 30-tägige Testversion für jede Substance 3D-Anwendung [hier](https://www.adobe.com/creativecloud/3d-augmented-reality.html) oder mit Creative Cloud Desktop starten. Jede Testversion ist unabhängig von den anderen Substance 3D-Programmen. Sie können also einzeln oder alle Applikationen gleichzeitig testen.
* <b>Mit einer Lizenzdatei aktivieren</b>: Aktivieren Sie das Produkt mit einer Lizenzdatei (<b>\*.key</b>), die Sie vor dem 30. September 2022 von Ihrer Kontoseite auf der [Substance 3D-Website](https://store.substance3d.com/user) heruntergeladen haben.
* <b>Aktivieren mit Ihrem Konto</b>: Ältere Substanzkonten können nicht mehr für die Aktivierung verwendet werden.

>[!IMPORTANT]
>
> Um die Lizenzdatei mit dem Aktivierungsassistent zu installieren, stellen Sie sicher, dass Sie Designer als Administrator ausführen und Ihr Antivirenprogramm vorübergehend deaktivieren.

![Aktivierungsassistent](activation-and-licenses.resources/activation-wizard.png "Aktivierungsassistent")

### Manuelle Aktivierung

Sie können Designer manuell aktivieren, indem Sie die Datei license.key in den folgenden Ordner kopieren:

<table data-preserve-html="true" style="table-layout:auto">
    <tbody>
        <tr>
            <th style="text-align: left;">Plattform</th>
            <th style="text-align: left;">Version</th>
            <th colspan="2" style="text-align: left;">Pfad</th>
        </tr>
        <tr>
            <td rowspan="4" style="text-align: left;"><b>Windows</b></td>
            <td rowspan="2" style="text-align: left;"><b>11.2</b> oder höher</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>11.1</b> oder niedriger</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>macOS</b></td>
            <td style="text-align: left;"><b>11.2</b> oder höher<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b> oder niedriger<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Allegorithmic/Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>Linux</b></td>
            <td style="text-align: left;"><b>11.2</b> oder höher</td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b> oder niedriger<br/></td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Allegorithmic/Substance Designer</code></td>
        </tr>
    </tbody>
</table>

>[!NOTE]
>
> Einige der Verzeichnisse in den oben genannten Pfaden sind möglicherweise standardmäßig ausgeblendet. Geben Sie den Pfad manuell in den Datei-Explorer ein oder zeigen Sie ausgeblendete Dateien an, um sie anzuzeigen.

>[!IMPORTANT]
>
> Stellen Sie sicher, dass die Datei `license.key` heißt, andernfalls kann sie von der Anwendung nicht gefunden werden.

### Umgebungsvariable

Sie können den Speicherort, den Designer für die Datei &quot;`license.key`&quot; überprüft, mit einer [Umgebungsvariablen &quot;](../../pipeline-and-project-con/environment-variables/environment-variables.md)&quot; überschreiben.

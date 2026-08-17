---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Hier erfahren Sie, wie Sie Python-Plug-ins für Substance 3D Designer für die Verteilung und Installation verpacken.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plug-ins verpacken
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# Plug-ins verpacken

## Inhalt des Plug-In-Pakets

Pakete sind eine einzelne Datei, intern ein Zip-Archiv, die eine Datei **pluginInfo.json** mit Metadaten zum Plug-in enthält.

den Plug-in-Code und alle anderen Dateien oder Ressourcen, die das Plug-in benötigt, um zu funktionieren.

**PluginInfo.json-Einträge:**

| Eintrag | Beschreibung | Standardwert | Anmerkungen |
| --- | --- | --- | --- |
| metadata\_format\_version | Das Format der Metadatendatei. | 1 | Erforderlich. Derzeit muss auf 1 gesetzt werden. |
| Name | Der Name des Plug-ins. |  | Erforderlich. Der Name des Python-Moduls, das den Plug-In-Code enthält, muss übereinstimmen. |
| Version | Die Plug-in-Version. |  | Optional. |
| Autorin | Der Autor des Plug-ins. |  | Optional. |
| email | Die E-Mail des Plug-in-Autors. |  | Optional. |
| min\_designer\_version | Die Mindestversion der Anwendung, die für das Plug-in erforderlich ist, um zu funktionieren. | 2019.2 | Optional. |
| Plattform | Plattform, auf der das Plug-in ausgeführt wird. | alle | Optional. Bei Plug-ins, die kompilierten Code enthalten, kann dieser Eintrag verwendet werden, um das Plug-in auf nicht unterstützten Plattformen zu deaktivieren.Mögliche Werte: win, linux, osx, any. |

## Erstellen eines neuen Plug-in-Paketprojekts

Wir stellen ein [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/)-Vorlagenprojekt bereit, um die Erstellung von Plug-In-Paketprojekten zu vereinfachen.

Sie können sie direkt verwenden oder an Ihre eigenen Anforderungen anpassen.

Die Vorlage befindet sich im Anwendungsverzeichnis unter <b>plugins/tools/pkgplugintemplate</b>.

1. <b>Installieren Sie Python, wenn es nicht bereits auf Ihrem System installiert ist</b>

   Cookiecutter ist sowohl mit Python 2 als auch mit Python 3 kompatibel
1. <b>Cookiecutter installieren, wenn Sie es noch nicht haben</b>

   Normalerweise kann dies mit pip erfolgen:

   ```
   pip install cookiecutter
   ```


   Für alternative Möglichkeiten zur Installation von Cookiecutter oder für weitere Informationen über Cookiecutter können Sie die Dokumentation unter <https://cookiecutter.readthedocs.io/en/latest/installation.html> überprüfen.
1. <b>Neues Plug-In-Paketprojekt erstellen</b>

   Führen Sie in einem Terminalfenster Folgendes aus:

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   Füllen Sie die erforderlichen Informationen aus. Das neue Projekt wird im angegebenen Verzeichnis erstellt.
1. <b>Nach Abschluss der Entwicklung das Plug-in verpacken</b>

   Führen Sie in einem Terminalfenster Folgendes aus:

   ```
   python makepackage.py
   ```

1. Das Plug-in-Paket wird im Buildverzeichnis generiert.

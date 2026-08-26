---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie den Installationspfad von Substance 3D Designer für Skript- und Automatisierungszwecke abrufen.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ermitteln des Installationspfads
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Ermitteln des Installationspfads

Auf dieser Seite werden Informationen über Möglichkeiten zum Abrufen des Installationspfads von [Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html) je nach Version und Plattform neu gruppiert.

## Windows

### Creative Cloud Desktop

1. <b>Windows-Registrierungseditor </b> öffnen (regedit)
1. Navigieren Sie zum Registrierungsschlüssel: <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Pfade\&lt;/b>
1. Öffnen Sie den Unterschlüssel &quot;<b>Adobe Substance 3D Designer.exe</b>&quot;.
1. Der Wert des Schlüssels enthält den Pfad zur ausführbaren Anwendungsdatei, in der er installiert ist

>[!NOTE]
>
> Dieser Registrierungsschlüssel ist nur seit Version 11.2 verfügbar.\
> Bei älteren Versionen kann der Installationspfad aus den Dateizuordnungen in HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts abgerufen werden.

### Substance-Edition (eigenständig)

1. <b>Windows-Registrierungseditor </b> öffnen (regedit)
1. Navigieren Sie zum Registrierungsschlüssel: <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. Suchen Sie den Unterschlüssel, der mit <b>AppID</b> Ihrer Anwendungsversion übereinstimmt (siehe Tabelle unten).
1. Der Wert des Schlüssels enthält den Pfad zum Speicherort der Anwendungsinstallation

| Version | AppId |
| --- | --- |
| **Version 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **Version 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **Version 7.x (2017.x) bis 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **Version 11.2 (oder höher)** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Steam-Edition

Die Anwendung wird im Unterordner steamapps/common/ des Steam-Installationsordners installiert.

## macOS

Unter Mac wird die Anwendung wie folgt installiert:

| Version | Pfad |
| --- | --- |
| **11.2 oder neuer** | **/Applications/Adobe Substance 3D Designer.app** |
| **Veraltet** | **/Applications/Substance Designer.app** |

## Linux

Unter Linux wird das rpm-Paket unter folgendem Pfad installiert:

| Version | Pfad |
| --- | --- |
| **11.2 oder neuer** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **Veraltet** | **/opt/Allegorithmic/Substance\_Designer** |

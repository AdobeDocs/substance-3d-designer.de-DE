---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Konfigurieren Sie Plug-in-Suchpfade in Substance 3D Designer, um anzugeben, wo sich Python-Plug-ins befinden.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Suchpfade einfügen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Suchpfade einfügen

Designer sucht nach Plug-ins in bestimmten Verzeichnissen (z. B. Suchpfaden). Auf dieser Seite wird erläutert, wie diese Pfade konfiguriert werden.

Benutzer können *benutzerdefinierte Verzeichnisse* manuell in den Softwarevoreinstellungen hinzufügen oder sie mithilfe von Umgebungsvariablen angeben.

## Plugin-Suchpfade manuell hinzufügen

1. Wechseln Sie zu <b>Bearbeiten > Voreinstellungen...1</b>
1. Wählen Sie die Kategorie <b>Projekte</b> aus.
1. Wählen Sie die <b>Projektdatei</b> aus, die Sie bearbeiten möchten
1. Klicken Sie auf der Registerkarte <b>Python</b> auf die Schaltfläche *<b>+</b>*, um das Verzeichnis hinzuzufügen, das die Plug-ins enthält
1. Klicken Sie zum Überprüfen auf <b>OK</b>.

![Einstellungen für Python-Plug-ins Suchpfade Projekteinstellungen](../../assets/image-70.png "Einstellungen für Python-Plug-ins Suchpfade Projekteinstellungen")

## Verwenden von Umgebungsvariablen

Die Anwendung sucht in allen Pfaden nach Plug-ins, die mit der Umgebungsvariablen <b>SBS\_DESIGNER\_PYTHON\_PATH </b> angegeben wurden.

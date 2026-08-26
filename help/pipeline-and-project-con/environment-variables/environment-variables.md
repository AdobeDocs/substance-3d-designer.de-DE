---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie in Substance 3D Designer Umgebungsvariablen zum Konfigurieren von Pfaden und Systemeinstellungen verwenden.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Umgebungsvariablen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Umgebungsvariablen

Auf dieser Seite werden Umgebungsvariablen aufgelistet, die verwendet werden können, um das Standardverhalten der Anwendung zu überschreiben.

| Variable | Beschreibung |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Der Pfad, von dem Designer [Python-Plug-ins](../../scripting/plugin-basics/plugin-basics.md) lädt. |
| **SUBSTANCE\_DESIGNER\_LICENSE** | Der Speicherort der Lizenzdatei (*license.key*), die von Designer verwendet werden soll.   Überschreibt den Pfad, der im [Aktivierungs-Assistenten](../../getting-started/activation-and-licenses/activation-and-licenses.md) von Designer festgelegt wurde.  **Hinweis:** Alte Versionen müssen möglicherweise einen alternativen Variablennamen verwenden:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | Der Pfad zur OCIO-Konfigurationsdatei, die verwendet werden soll, wenn OpenColorIO [Farbmanagement](../../color-management/color-management.md) verwendet wird.   Überschreibt den Pfad, der in den Farbmanagementeinstellungen von Designer in den [Projekteinstellungen](../../interface/preferences-window/project-settings/project-settings.md) festgelegt wurde. |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | Die Verzögerung in Sekunden vor dem Freigeben eines Lizenzsitzes bei einer Mehrbenutzerkonfiguration Der Standardwert beträgt 7200 Sekunden (2 Stunden). |

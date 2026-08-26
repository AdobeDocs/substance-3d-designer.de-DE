---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: Hier erfahren Sie, wie Sie Plug-ins aus früheren Versionen von Substance Designer an die aktuelle Python-API portieren.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Portieren früherer Plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Portieren früherer Plug-ins

Aufgrund der Änderungen, die an der Unterstützung von Qt für Python vorgenommen wurden, funktionieren **vorherige Plug-ins nicht mehr**.\
Beachten Sie insbesondere Folgendes:

## Laden und Entladen von Plug-ins

Plug-Ins werden jetzt geladen, wenn die Anwendung <b>gestartet</b> wird, und entladen, wenn sie <b>beendet</b> wird.\
Daher ist es *nicht erforderlich*, damit Plug-Ins von &quot;*sdplugins.Plugin*&quot; erben können.

Weitere Informationen finden Sie im Abschnitt [Grundlagen zu Plug-ins](../../scripting/plugin-basics/plugin-basics.md).

## Erstellen von Benutzeroberflächenelementen

Plug-Ins *benötigen* nicht mehr, um eine &#39;*sdplugins.PluginDesc*&#39; zu definieren.\
Stattdessen können Plug-Ins das <b>neue [UI-Manager](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)-Objekt</b> und <b>Qt für Python</b> verwenden, um alle erforderlichen Benutzeroberflächenelemente zu erstellen.

Kleine Codebeispiele finden Sie im Abschnitt [Erstellen von Benutzeroberflächenelementen](../../scripting/creating-user-interface/creating-user-interface-elements.md).

## Ersetzen von Benutzern des Standortkontexts

Die *SDLocationContext*-Klasse wurde *aus der Python-API entfernt*.\
Plug-Ins können das <b>[UI Manager](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)-Objekt</b> verwenden, um auf das derzeit aktive Diagramm und die Auswahl zuzugreifen.

Einige Beispiele finden Sie im Abschnitt [Zugriff auf Diagramme und Auswahlen](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md).

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Lernen Sie die Grundlagen zur Erstellung von Python-Plug-ins für Substance 3D Designer, um die Anwendungsfunktionalität zu erweitern.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grundlagen zu Plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Grundlagen zu Plug-ins

Ein Plug-In ist eine Python-Datei oder ein Python-Modul, das eine <b>initializeSDPlugin()</b>-Funktion definiert.

Die <b>initializeSDPlugin()</b>-Funktion wird aufgerufen, wenn das Plug-In geladen wird.\
In dieser Funktion können Sie Benutzeroberflächenelemente erstellen, Rückrufe registrieren und andere Funktionen, die Sie möglicherweise benötigen.

Optional kann das Plug-In eine <b>uninitializeSDPlugin()</b>-Funktion definieren, die beim Entladen des Plug-Ins aufgerufen wird.\
Sie können diese Funktion verwenden, um Ressourcen freizugeben, Netzwerkverbindungen zu schließen und Ähnliches.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```

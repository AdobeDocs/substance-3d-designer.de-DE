---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/application-callbacks.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Anwendungsrückrufe in Substance 3D Designer Python-Plug-ins verwenden, um auf Anwendungsereignisse zu reagieren.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Application callbacks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anwendungsrückrufe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# Anwendungsrückrufe

Es ist möglich, <b>Python-Rückrufe</b> bei dem Anwendungsobjekt zu registrieren, das Designer aufruft, wenn bestimmte Ereignisse eintreten.

Benutzeroberflächenobjekte wie Menüs und Schaltflächen können Rückrufe mithilfe der Bibliothek <b>Qt für Python</b> auslösen. Weitere Informationen finden Sie unter [Erstellen von Benutzeroberflächenelementen](../../scripting/creating-user-interface/creating-user-interface-elements.md).

```
import sd 

 

## Our callbacks.

def onBeforeFileLoadedCallback(filePath): 

    print("Before file loaded, file: %s" % filePath) 

 

def onAfterFileLoadedCallback(filePath, succeed, updated): 

    print("After file loaded, file: %s, succeed: %s, updated: %s" % (filePath, succeed, updated)) 

     

def onBeforeFileSavedCallback(filePath, parentPackagePath): 

    print("Before file saved, file: %s, parentPackage: %s" % (filePath, parentPackagePath)) 

 

def onAfterFileSavedCallback(filePath, succeed): 

    print("After file saved, file: %s, succeed: %s" % (filePath, succeed)) 

 

## Get the application.

app = sd.getContext().getSDApplication() 

 

## Register our callbacks.

beforeFileLoadedCallbackID = app.registerBeforeFileLoadedCallback(onBeforeFileLoadedCallback) 

afterFileLoadedCallbackID = app.registerAfterFileLoadedCallback(onAfterFileLoadedCallback) 

beforeFileSavedCallbackID = app.registerBeforeFileSavedCallback(onBeforeFileSavedCallback) 

afterFileSavedCallbackID = app.registerAfterFileSavedCallback(onAfterFileSavedCallback) 

 

## Unregister callbacks when no longer needed.

app.unregisterCallback(beforeFileLoadedCallbackID) 

app.unregisterCallback(afterFileLoadedCallbackID) 

app.unregisterCallback(beforeFileSavedCallbackID) 

app.unregisterCallback(afterFileSavedCallbackID)
```

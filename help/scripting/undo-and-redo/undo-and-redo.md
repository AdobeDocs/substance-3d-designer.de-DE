---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Funktionen zum Rückgängigmachen und Wiederholen in Substance 3D Designer Python-Skripten für Benutzeraktionen implementieren.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rückgängig machen und Wiederholen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# Rückgängig machen und Wiederholen

Mit der <b>SDHistoryUtils.UndoGroup</b>-Klasse können Benutzer *Gruppenaktionen* in einem Befehl *rückgängig machen oder wiederholen*.

Diese Gruppen werden von Benutzern *benannt* und mit diesem Namen in der Liste &quot;Rückgängig&quot;/&quot;Wiederholen&quot; in der Benutzeroberfläche angezeigt.  Dadurch wird eine große Anzahl von Aktionen leichter zu handhaben.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```

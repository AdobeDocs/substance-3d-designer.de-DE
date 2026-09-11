---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie auf Graf und Knotenauswahl in Substance 3D Designer Python-Skripten zugreifen und diese bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Zugriff auf Grafen und Auswahlbereiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Zugriff auf Grafen und Auswahlbereiche

Die <b>SDApplication</b>-Klasse enthält einige hilfreiche Methoden, mit denen Sie auf den *aktuell aktiven*-Graf und die *aktuelle Auswahl* darin zugreifen können.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


Auf einen Graf, der in einer *spezifischen*-Graphansicht angezeigt wird, kann mit einer <b>graphViewID</b> zugegriffen werden.

Diese Methode ist hilfreich beim Erstellen benutzerdefinierter Graphansicht-Symbolleisten. Weitere Informationen finden Sie im Beispiel <b>Erstellen von Symbolleisten in Graphansichten</b> im Kapitel [Erstellen von Benutzeroberflächenelementen](../../scripting/creating-user-interface/creating-user-interface-elements.md).

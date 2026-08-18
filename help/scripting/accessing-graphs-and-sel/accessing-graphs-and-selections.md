---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie auf Diagramme und Knotenauswahlen in Substance 3D Designer Python-Skripten zugreifen und diese bearbeiten können.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Zugreifen auf Diagramme und Auswahlen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Zugreifen auf Diagramme und Auswahlen

Die <b>SDApplication</b>-Klasse enthält einige hilfreiche Methoden, mit denen Sie auf das Diagramm *aktuell aktiv* und die *aktuelle Auswahl* in diesem Diagramm zugreifen können.

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


Auf ein Diagramm, das in einer *spezifischen* Diagrammansicht angezeigt wird, kann mit einer <b>graphViewID</b> zugegriffen werden.

Diese Methode ist nützlich, wenn benutzerdefinierte Symbolleisten für die Diagrammansicht erstellt werden. Das Beispiel <b>Erstellen von Symbolleisten in Diagrammansichten</b> im Kapitel [Erstellen von Benutzeroberflächenelementen](../../scripting/creating-user-interface/creating-user-interface-elements.md) enthält weitere Details.

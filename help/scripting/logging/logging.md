---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie die Protokollierung in Substance 3D Designer Python-Plug-ins zum Debuggen und Überwachen implementieren.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Protokollieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# Protokollieren

Wir empfehlen, das Standard-Protokollierungsmodul von Python für die Protokollierung zu verwenden.

Das <b>sd</b>-Modul enthält Helfer-Klassen, um die Protokollierung an die Designer-Konsole umzuleiten.

## An der Designer-Konsolenleiste anmelden

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```

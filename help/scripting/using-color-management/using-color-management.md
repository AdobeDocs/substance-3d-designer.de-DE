---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Farbmanagementfunktionen in Substance 3D Designer Python-Skripten für präzise Farben verwenden.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbmanagement verwenden
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Farbmanagement verwenden

Die <b> SDColorManagementEngine </b>-Klasse, auf die von der <b>SDApplication</b>-Klasse zugegriffen werden kann, enthält Informationen zu den *aktuellen Farbmanagementeinstellungen*.

## Zugreifen auf die Farbmanagement-Engine und Abfragen

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


Darüber hinaus ist es möglich *Farbräume* Bitmapressourcen von Python zuzuweisen.

### Festlegen von Farbräumen für Bitmapressourcen

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## Schreiben von SDTexturen mit Farbraumkonvertierungen

Die **save**-Methode der **SDTexture**-Klasse akzeptiert jetzt einen optionalen **outputColorSpace**-Parameter. Wenn angegeben, wird die Farbraumkonvertierung *angewendet, bevor das Bild* gespeichert wird.

Wenn der Farbmanagementmodus eingebettete ICC-Profile &quot;*&quot; und &quot;*&quot; unterstützt, werden diese auch vom Zieldateiformat unterstützt, wird das ICC-Farbraumprofil &quot;*&quot; in die resultierende Bilddatei &quot;*&quot; eingebettet.

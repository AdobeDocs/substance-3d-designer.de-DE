---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Samplerknoten in FXMaps verwenden, um Texturen zu testen und prozedurale Materialvariationen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verwenden der Sampler-Knoten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Verwenden der Sampler-Knoten

![](using-the-sampler-nodes.resources/sampler-graph.jpg)

Der Samplerknoten kann verwendet werden, um Pixelwerte in einem Bildeingang zu testen, der an den fx-map-Knoten angeschlossen ist. Die abgetasteten Werte können dann verwendet werden, um beliebige Parameter mit Funktionen zu steuern.

## einfaches Beispiel

In diesem Beispiel wurde eine Kette von Quadrantenknoten erstellt, um einen Raster des Musters zu erzeugen. Eine Funktion wird im Parameter &quot;Deckkraft/Luminanz&quot; des letzten Quadranten erstellt.

![](using-the-sampler-nodes.resources/sampler-function.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-1.jpg){width="300px"}

Der Knoten Sample verwendet einen float2-Eingang als Sampling-Koordinaten (x, y). In diesem Beispiel haben wir die Variable $pos verwendet: für jedes Muster wird der Pixelwert an der Musterposition im ersten Bildeingang abgetastet, der an den FxMap-Knoten angeschlossen ist.

Der Knoten &quot;Beispielgrau&quot; gibt einen float1-Wert im Bereich 0,1 zurück.

Der Knoten &quot;Beispielfarbe&quot; gibt einen float4(rgba)-Wert im Bereich 0,1 zurück.

## Beispiel für Fortgeschrittene

Hier wird der Abtastwert mit einer Konstanten (0,3) verglichen. Wenn der aufgenommene Wert größer als 0,3 ist, gibt die Funktion 1 zurück, ansonsten 0.

![](using-the-sampler-nodes.resources/sampler-function-advanced.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-advanced.jpg){width="300px"}

## Beispiel herunterladen

[![SBS Dateisymbol](using-the-sampler-nodes.resources/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)

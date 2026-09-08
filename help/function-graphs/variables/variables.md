---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Variablen in Substance 3D Designer-Funktions-Grafen verwenden, um Werte effizient zu speichern und wiederzuverwenden.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variablen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Variablen

>[!NOTE]
>
> Informationen zur Erstellung und Verwendung von Variablenknoten finden Sie im Abschnitt *[Variablenknoten](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*.

## Definition

Wenn Sie wenig Programmierkenntnisse haben, sind Sie möglicherweise mit dem Konzept der Variablen vertraut.

Falls nicht, gibt es eine einfache Definition:

>[!NOTE]
>
> Eine Variable ist nur ein &quot;Container&quot; mit einem bestimmten Namen, der einen Wert enthält.
> 
> Sie können den in einer Variablen enthaltenen Wert verwenden, indem Sie sie mit ihrem Namen aufrufen.

## Variablentypen

In Substance 3D Designer gibt es zwei Variablenfamilien: Numerisch und boolesche Zeichen.

## Numerische Variablen

Numerische Variablen sind im Grunde Zahlen. Aber wir unterscheiden klar zwischen zwei Arten von Zahlen:

* GANZZAHLEN : 0 | 1 | -1 | 203568 usw.
* Fließkommazahlen: 0,23 | 1,0 | -0,3546 | usw.

>[!WARNING]
>
> Designer unterscheidet klar zwischen Ganzzahlen und Animationsvorlagen: standardmäßig können Sie sie nicht zusammen bedienen.
> 
> Glücklicherweise können Sie die Knoten *In Ganzzahl* oder In Fließkommazahl verwenden, um Typkonvertierungen durchzuführen.

### Mehrere numerische Werte in derselben Variable

Je nach Bedarf können Sie innerhalb derselben Variablen bis zu 4 numerische Werte akkumulieren.

Auch hier müssen alle Werte vom gleichen Typ sein.

Dazu haben Sie die Wahl zwischen all diesen numerischen Werten:

![](../../assets/image2015-12-18-14-10-36.png)

## Boolescher Wert

Ein Boolesche Wert ist ein reiner Binärwert, d. h., sein Wert kann nur *True* oder *False* sein (Sie können auch 0 oder 1 sagen).

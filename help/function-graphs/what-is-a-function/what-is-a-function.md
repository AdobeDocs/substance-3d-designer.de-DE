---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Erfahren Sie, welche Funktionen Substance 3D Designer bietet und wie Sie damit wiederverwendbare Knotennetzwerke erstellen können.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Was ist eine Funktion? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Was ist eine Funktion?

Mit Funktionen in Substance 3D Designer können Sie Ergebnisse mit der Logik generieren, die Sie sonst in einer Programmiersprache finden würden.

Aber anstatt Codezeilen zu verwenden, verwenden Funktionen in Designer denselben knotenartigen Ansatz. Auf den ersten Blick sieht ein Graf wie ein normaler Graf aus.

![](../../assets/image2015-12-17-18-19-37.png)

Funktionen können in zwei Hauptfällen auftreten:

* das Ergebnis eines Parameters steuern
* wenn Sie einen Pixelprozessor bearbeiten

## Steuern des Ergebnisses eines Parameters

In Substance 3D Designer kann jeder Parameter über eine Funktion gesteuert werden.

![](../../assets/image2015-12-17-21-3-46.png)

Daher können Sie sich Regeln und Abhängigkeiten zwischen Teilen Ihres Grafen vorstellen, um einzigartige Ergebnisse zu erzielen.

So können Sie beispielsweise festlegen, dass die Deckkraft eines Überblendungsknotens die Hälfte der Intensität eines Verkrümmungsknotens beträgt:

![](../../assets/warpblend.gif)

Tatsächlich haben Sie möglicherweise bereits Funktionen erstellt, ohne sich dessen bewusst zu sein:

Wenn Sie einen Parameter gelegt haben, haben Sie automatisch eine Funktion und eine Variable erstellt: Die Funktion enthält einen get float -Knoten, der den Wert der neu erstellten Variablen abfängt:

![](../../assets/expose.gif)

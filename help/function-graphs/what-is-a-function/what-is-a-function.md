---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/what-is-a-function.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Was ist eine Funktion?

Mit Funktionen in Substance 3D Designer können Sie Ergebnisse mit der Logik generieren, die Sie sonst in einer Programmiersprache finden würden.

Aber anstatt Codezeilen zu verwenden, verwenden Funktionen in Designer denselben knotenartigen Ansatz. Auf den ersten Blick sieht ein Graf wie ein normaler Graf aus.

![](what-is-a-function.resources/what-is-a-function-01.png)

Funktionen können in zwei Hauptfällen auftreten:

* das Ergebnis eines Parameters steuern
* wenn Sie einen Pixelprozessor bearbeiten

## Steuern des Ergebnisses eines Parameters

In Substance 3D Designer kann jeder Parameter über eine Funktion gesteuert werden.

![](what-is-a-function.resources/what-is-a-function-02.png)

Daher können Sie sich Regeln und Abhängigkeiten zwischen Teilen Ihres Grafen vorstellen, um einzigartige Ergebnisse zu erzielen.

So können Sie beispielsweise festlegen, dass die Deckkraft eines Überblendungsknotens die Hälfte der Intensität eines Verkrümmungsknotens beträgt:

![](what-is-a-function.resources/what-is-a-function-03.gif)

Tatsächlich haben Sie möglicherweise bereits Funktionen erstellt, ohne sich dessen bewusst zu sein:

Wenn Sie einen Parameter gelegt haben, haben Sie automatisch eine Funktion und eine Variable erstellt: Die Funktion enthält einen get float -Knoten, der den Wert der neu erstellten Variablen abfängt:

![](what-is-a-function.resources/what-is-a-function-04.gif)

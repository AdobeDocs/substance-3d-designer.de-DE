---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Variablenwerte in Substance 3D Designer-Funktionsknoten mithilfe des Grafen "Variable abrufen" abrufen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Abrufen eines Variablenwerts
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Abrufen eines Variablenwerts

Um eine Variable in einer Funktion zu verwenden, müssen Sie sie &quot;aufrufen&quot;, d. h. den Wert der Variablen in die Funktion importieren.

Dazu müssen Sie einen *Get*-Knoten verwenden:

![](get-a-variable-value.resources/image2015-12-21-7-29-51.png)

Es gibt verschiedene Arten von Get-Knoten: Wählen Sie das richtige für den Werttyp, den Sie importieren möchten:

![](get-a-variable-value.resources/image2015-12-21-7-31-4.png)

## Zuweisen einer Variablen zu einem Get-Knoten

Standardmäßig zeigt ein get-Knoten ein Warnzeichen an: es bedeutet, dass es noch nicht mit einer Variablen verknüpft ist.

Um eine Variable zu verknüpfen, gehen Sie zu den Parametern und wählen Sie eine Variable in der Liste &quot;Variablen/Get \*\*\*&quot; aus (\*\*\* wird durch den Werttyp ersetzt, den Ihr Get-Knoten aufrufen kann).

Der Variablenname wird im Knoten angezeigt:

![](get-a-variable-value.resources/assign-getfloat.gif)

Beachten Sie, dass nur die Variablen in der Liste angezeigt werden, die vom gleichen Typ des Get-Knotens stammen.

>[!WARNING]
>
> Beachten Sie, dass Variablen, die mit einem *Set*-Knoten erstellt wurden, nicht in einer *Get*-Knotenliste angezeigt werden.
> 
> Sie können die Variable jedoch trotzdem abrufen, indem Sie den Namen manuell in die Liste schreiben.
> 
> Denken Sie daran, dass Sie eine Variable, die mit einem Knoten Set erstellt wurde, in folgenden Fällen aufrufen können:
> 
> * Die Knoten Get und Set befinden sich in Funktions-Grafen, die die Parameter desselben Knotens steuern.
> * Der vom *Get*-Knotenparameter gesteuerte Graf ist entweder derselbe oder befindet sich im Stapel &quot;parameters&quot; unter dem Graf des *Set*-Knotenparameters.

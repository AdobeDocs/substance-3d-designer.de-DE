---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie Variablenwerte in Substance 3D Designer-Funktionsdiagrammen mithilfe des Knotens "Variable abrufen" abrufen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Abrufen eines Variablenwerts
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Abrufen eines Variablenwerts

Um eine Variable in einer Funktion zu verwenden, müssen Sie sie &quot;aufrufen&quot;, d. h. den Wert der Variablen in die Funktion importieren.

Dazu müssen Sie einen *Get*-Knoten verwenden:

![](../../../assets/image2015-12-21-7-29-51.png)

Es gibt verschiedene Arten von Get-Knoten: Wählen Sie das richtige für den Werttyp, den Sie importieren möchten:

![](../../../assets/image2015-12-21-7-31-4.png)

## Zuweisen einer Variablen zu einem Get-Knoten

Standardmäßig zeigt ein get-Knoten ein Warnzeichen an: es bedeutet, dass es noch nicht mit einer Variablen verknüpft ist.

Um eine Variable zu verknüpfen, gehen Sie zu den Parametern und wählen Sie eine Variable in der Liste &quot;Variablen/Get \*\*\*&quot; aus (\*\*\* wird durch den Werttyp ersetzt, den Ihr Get-Knoten aufrufen kann).

Der Variablenname wird im Knoten angezeigt:

![](../../../assets/assign-getfloat.gif)

Beachten Sie, dass nur die Variablen in der Liste angezeigt werden, die vom gleichen Typ des Get-Knotens stammen.

>[!WARNING]
>
> Beachten Sie, dass Variablen, die mit einem *Set*-Knoten erstellt wurden, nicht in einer *Get*-Knotenliste angezeigt werden.
> 
> Sie können die Variable jedoch trotzdem abrufen, indem Sie den Namen manuell in die Liste schreiben.
> 
> Denken Sie daran, dass Sie eine Variable, die mit einem Knoten Set erstellt wurde, in folgenden Fällen aufrufen können:
> 
> * Die Knoten &quot;Abrufen&quot; und &quot;Festlegen&quot; befinden sich in Funktionsdiagrammen, die die Parameter desselben Knotens steuern.
> * Der vom Knotendiagramm *Get* gesteuerte Parameter ist entweder derselbe oder befindet sich im Parameterstapel unter dem Parameter des Knotendiagramms *Set*.

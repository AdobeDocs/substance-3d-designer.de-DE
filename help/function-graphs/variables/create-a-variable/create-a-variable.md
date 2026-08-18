---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie benutzerdefinierte Variablen in Substance 3D Designer-Funktionsdiagrammen für wiederverwendbare Werte und Parameter erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Erstellen einer Variablen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Erstellen einer Variablen

Es gibt verschiedene Möglichkeiten, eine Variable in Substance 3D Designer zu erstellen:

* Verwenden eines Eingabeparameters
* Verwenden Sie einen Set-Knoten.

## Verwenden eines Eingabeparameters

Wenn Sie einen Eingabeparameter erstellen, wird eine Variable erstellt und mit diesem verknüpft. Sie können diese Variable dann in jeder Funktion Ihres Diagramms wiederverwenden.

Daher kann ein einzelner exponierter Parameter einen Einfluss auf mehrere Teile Ihres Diagramms haben.

## Verwenden eines Set-Knotens

Ein Set-Knoten ist ein Knoten, der nur in den Funktionsdiagrammen verfügbar ist:

Es ermöglicht dem Benutzer, eine benutzerdefinierte Variable zu erstellen:

* Der Name wird in den Parametern deklariert.
* Der Wert wird durch die Eingabe definiert.

### Verwenden des Knotens *Set*

Die Verwendung eines Set-Knotens ist ein bisschen speziell:

Wenn Sie es deklarieren, ist es nur innerhalb des Graphen verfügbar, was standardmäßig nicht wirklich nützlich ist (schließlich können Sie seinen Wert bereits mit Links ausgeben).

Daher müssen Sie diese neue Variable außerhalb dieses Diagramms deklarieren.

Dazu müssen Sie einen Sequenzknoten verwenden und die folgenden Schritte ausführen:

* Den eigentlichen Ausgabeknoten mit dem &quot;letzten&quot; Eingang des Sequenzknotens verknüpfen
* Verknüpfen Sie den Knoten &quot;Set&quot; mit dem Eingang &quot;In&quot; des Sequenzknotens.
* Sequenz als Ausgabeknoten festlegen

Wenn Sie dies getan haben, ist die Variable im anderen Funktionsdiagramm desselben Knotens verfügbar.

>[!WARNING]
>
> Wenn ein Knoten von der Substanz Engine verarbeitet wird, werden seine Parameter (und die Funktionen, die sie steuern könnten) von oben nach unten gelesen. Daher kann auf einen Set-Knoten nur über die Parameter zugegriffen werden, die sich darunter im Knotenparameterstapel befinden.

>[!NOTE]
>
> Wenn Sie mehrere Variablen erstellen müssen, wiederholen Sie einfach den Erstellungsvorgang für *Set*- und *Sequence*-Knoten und legen Sie den letzten Sequenzknoten als Ausgabeknoten fest:
> 
> ![](../../../assets/image2015-12-18-18-43-8.png)

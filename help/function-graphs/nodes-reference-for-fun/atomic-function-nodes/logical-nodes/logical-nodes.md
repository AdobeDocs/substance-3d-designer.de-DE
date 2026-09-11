---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Greifen Sie in Substance 3D Designer-Funktionsknoten auf logische Graf zu, um boolesche Logikoperationen und -vergleiche auszuführen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logisch
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Logische Knoten

Logische Knoten werden verwendet, um dem Graf mehrere Bedingungen hinzuzufügen:

![](logical-nodes.resources/image2015-12-23-11-23-21.png)

## Der Knoten &quot;*and*&quot;

![](logical-nodes.resources/image2015-12-23-11-30-9.png)

Der Und-Knoten nimmt zwei Boolesche Wert-Knoten als Eingabe an:

* Wenn beide Eingaben &quot;True&quot; sind, ist die Ausgabe des Knotens &quot;*And*&quot; *True*
* In jedem anderen Fall gibt der Knoten *And* *False* zurück.

## Der Knoten *Or*

![](logical-nodes.resources/image2015-12-23-11-30-44.png)

Der Knoten Or nimmt zwei Boolesche Wert-Knoten als Eingabe an:

* Wenn mindestens einer der Eingaben True (1) ist, ist die Ausgabe des Knotens *Or* *True*
* Wenn beide Eingaben False sind, gibt der Knoten *Or* *False* zurück.

## Der Knoten *Not*

![](logical-nodes.resources/image2015-12-23-11-31-46.png)

Der Node Not nimmt einen Boolesche Wert als Eingabe an: wird der Eingabewert überprüft und das Gegenteil zurückgegeben:

* *True*-Eingabe ergibt *False*-Ausgabe
* *False*-Eingabe ergibt *True*-Ausgabe

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über die integrierten Systemvariablen, die in den Substance 3D Designer-Funktions-Grafen für erweiterte Workflows verfügbar sind.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Integrierte Variablen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# Integrierte Variablen

Sie können integrierte Variablen in [Substance-Funktionsvariablen &#x200B;](../../../function-graphs/function-graphs.md) verwenden, um auf bestimmte Graf zuzugreifen. Sie beginnen immer mit einem `$`-Symbol (Dollar).

Einige Variablen sind nur in bestimmten Kontexten verfügbar.

<b>Alle Knoten</b>

Systemvariablen

| Name | Typ | Zweck |
| --- | --- | --- |
| $size | Float2 | Gibt die Größe des aktuellen Knotens in Pixel zurück.   Wenn der Parameter &quot;[Ausgabegröße](../../../compositing-graphs/output-size/output-size.md)&quot; auf &quot;*Relativ zu&quot; festgelegt ist...* [Vererbung-Methode &#x200B;](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) gibt den *geerbten Wert* zurück. |
| $sizelog2 | Float2 | Wie oben, gibt aber die Größe als Power-of-2-Werte zurück (z. B.: Für Bild 2048\*2048 gibt `$sizelog2` 11) zurück.   Wenn der Parameter &quot;[Ausgabegröße](../../../compositing-graphs/output-size/output-size.md)&quot; auf &quot;*Relativ zu&quot; festgelegt ist...* [Vererbung-Methode &#x200B;](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) gibt den *geerbten Wert* zurück. |
| $pixelratio | Ganzzahl | Gibt einen Wert für die Ganzzahl zurück, der dem aktuellen Pixelverhältnis des Knotens entspricht (geerbt oder absolut):   0: Dehn 1: Quadrat |
| $Kachelung | Ganzzahl | Gibt einen Wert für die Ganzzahl zurück, der dem aktuellen Knoten-Kachelung-Modus (geerbt oder absolut) entspricht:   0: Keine Kachelung 1: Horizontale Kachelung 2 Kachelung 3: H- und V-Kachelung |
| $physicalsize | Float3 | Gibt den Eigenschaftswert [Graf](../../../compositing-graphs/graph-parameters/graph-parameters.md) <b>Physische Größe</b> zurück. |
| $uvtile | Integer2 | Bei Verwendung von UDIM-Workflows gibt diese Variable den Index des aktuellen Audiomaterials in U und V zurück.   Beispiel: (2, 0) für Kachel 1003, (7, 11) für Kachel 1118, ... |

<b>FX-Map</b>

Systemvariablen

| Name | Typ | Zweck |
| --- | --- | --- |
| $pos | Float2 | Gibt die Geburtsstellung des Musters zurück. Der Ursprung (0, 0) befindet sich in der linken oberen Ecke des Bildes. |
| $Tiefe | Float | Gibt die Oktavnummer (Level) des Knotens [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) zurück. Dadurch kann ein Knoten sein Verhalten ändern, je nachdem, welche Ebene in der Quad-Tree er repräsentiert. |
| $depthpow2 | Float | Wie oben, aber gibt die multiplikative Inverse von 2 erhöht auf die Potenz der Oktave (Level) Zahl - d.h. 1/(2^Octave). Dies ist ein Hilfswert, der für einige gängige Berechnungen nützlich ist. |
| $number | Float | Gibt die Nummer des gezeichneten Musters zurück. Auf diese Funktion können dynamische Funktionsdiagramme zugreifen, die einen [Iterate](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md)-Knoten steuern, um sein Verhalten bei jedem Iterationsschritt zu ändern.   Beachten Sie, dass `$number` mit dem Zählen von 0 beginnt, nicht von 1.   Bei Verwendung einer Kette von Iterate-Knoten gibt die `$number`-Variable die Iterationsnummer des letzten Iterate-Knotens zurück, der vor dem verwendeten Funktionsparameter verbunden ist. Wenn Sie die Iterationsnummer von mehreren Iterate-Knoten abrufen möchten, sollten Sie &quot;benutzerdefinierte Variablen&quot; über [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)-Knoten verwenden. |

<b>Pixelprozessor</b>

Systemvariablen

| Name | Typ | Zweck |
| --- | --- | --- |
| $pos | Float2 | Gibt die Position des auszuwertenden Pixels zurück. |

<b>Global</b>

Systemvariablen

| Name | Typ | Zweck |
| --- | --- | --- |
| $time | Float | Diese Variable gibt die Zeit in Sekunden zurück, seit das Substance Engine gestartet wurde. Es kann in Grafen verwendet werden, deren Ergebnis sich entsprechend der verstrichenen Zeit ändern sollte.  **Hinweis:** Dieser Wert kann derzeit in Designer nicht geändert werden. Anwendungen, die das Substance Engine integrieren, können ihn jedoch nutzen, z. B. [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) für Animationen oder [Substance 3D Painter](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/home) für [Dynamische Pinselstriche](https://experienceleague.adobe.com/de/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes). |
| $normalformat | Ganzzahl | Das Normalformat (d. h. DirectX oder OpenGL), das in der aktuellen Umgebung verwendet wird.  **Hinweis:** Diese Variable hat keine Auswirkungen auf Designer und kann von anderen Anwendungen verwendet werden, die das Substance Engine integrieren. |

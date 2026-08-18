---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über atomare Funktionsknoten, die kleinsten Knoteneinheiten in Substance-Funktionsdiagrammen zum Erstellen benutzerdefinierter Funktionen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atomare Funktionsknoten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 17%

---


# Atomare Funktionsknoten

Ähnlich wie [Atomknoten in Substance-Graphen](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) sind Atomknoten in Substance-Funktionsgraphen die kleinsten Knoteneinheiten in diesem Diagrammtyp.

Sie können je nach ihrem Zweck in mehrere Kategorien eingeteilt werden:

| Kategorie | Knoten | Eingabetyp(en) | Ausgabetyp | Beschreibung |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Konstante](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Float | - | Float | Definiert einen konstanten Gleitkommawert, z. B. 0,1 |
|                                                                                                                                        | Float2 | - | Float2 | Definiert einen konstanten Vektor mit 2 gleitenden Werten, z. B. (0,1, 0,2) |
|                                                                                                                                        | Float3 | - | Float3 | Definiert einen konstanten Vektor mit 3 gleitenden Werten, z. B. (0,1, 0,2, 0,3) |
|                                                                                                                                        | Float4 | - | Float4 | Definiert einen konstanten Vektor mit 4 gleitenden Werten, z. B. (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Ganzzahl | - | Ganzzahl | Definiert einen konstanten Ganzzahlwert, z. B. 1 |
|                                                                                                                                        | Integer2 | - | Integer2 | Definiert einen konstanten Vektor mit 2 Ganzzahlwerten, z. B. (1, 2) |
|                                                                                                                                        | Integer3 | - | Integer3 | Definiert einen konstanten Vektor mit 3 Ganzzahlwerten, z. B. (1, 2, 3) |
|                                                                                                                                        | Integer4 | - | Integer4 | Definiert einen konstanten Vektor mit 4 ganzzahligen Werten, z. B. (1, 2, 3, 4) |
|                                                                                                                                        | Boolescher Wert | - | Boolescher Wert | Definiert einen konstanten booleschen Wert, z. B. True oder False. |
|                                                                                                                                        | Zeichenfolge | - | Zeichenfolge | Definiert einen konstanten String-Wert, z. B. &quot;Substance&quot; |
| [Vektor](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vektor-Gleitkommawert2 | Float1 | Fließkommawert 2 | Zeigt 2 schwebende Werte in einem Vektor mit 2 Koordinaten an. |
|                                                                                                                                        | Vektor-Gleitkommawert3 | Float1/Float2 | Fließkomma 3 | Zeigt 2 schwebende Werte in einem Vektor mit 3 Koordinaten an. |
|                                                                                                                                        | Vektor-Gleitkommawert4 | Float1 / 2 / 3 | Float4 | Zeigt 2 schwebende Werte in einem Vektor mit 4 Koordinaten an. |
|                                                                                                                                        | Swizzle-Gleitkommawert1 | Vektor-Float | Float1 | Extrahiert eine gleitende Koordinate aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert2 | Vektor-Float | Float2 | Extrahiert 2 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert3 | Vektor-Float | Float3 | Extrahiert 3 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert4 | Vektor-Float | Float4 | Extrahiert 4 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Vektor-Ganzzahl2 | Integer2 | Vektor-Ganzzahl2 | Zeigt 2 ganzzahlige Werte in einem Vektor mit 2 Koordinaten an |
|                                                                                                                                        | Vektor-Ganzzahl3 | Integer3 | Integer3 | Zeigt 2 ganzzahlige Werte in einem Vektor mit 3 Koordinaten an |
|                                                                                                                                        | Vektor-Ganzzahl4 | Integer4 | Integer4 | Zeigt 2 ganzzahlige Werte in einem Vektor mit 4 Koordinaten an |
|                                                                                                                                        | Swizzle-Ganzzahl1 | Vector Integer | Integer1 | Extrahiert eine Ganzzahlkoordinate aus einem Vektor |
|                                                                                                                                        | Swizzle-Ganzzahl2 | Vector Integer | Integer2 | Extrahiert 2 Ganzzahlkoordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Ganzzahl3 | Vector Integer | Integer3 | Extrahiert 3 Ganzzahlkoordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Ganzzahl4 | Vector Integer | Integer4 | Extrahiert 4 Ganzzahlkoordinaten aus einem Vektor |
| [Variablen](../../../function-graphs/variables/variables.md) | Festgelegt | alle | Eingabetyp | Festlegen einer Variablen |
|                                                                                                                                        | Integer1 abrufen | - | Integer1 | Abrufen einer Funktion oder eines Diagramms Integer-Werteingabe |
|                                                                                                                                        | Integer2 abrufen | - | Integer2 | Abrufen einer Funktion oder eines Diagramms Integer2-Werteingabe |
|                                                                                                                                        | Integer3 abrufen | - | Integer3 | Abrufen einer Funktion oder eines Diagramms vom Typ Integer3-Wert |
|                                                                                                                                        | Integer4 abrufen | - | Integer4 | Abrufen einer Funktion oder eines Diagramms vom Typ Integer4, Werteingabe |
|                                                                                                                                        | Float1 abrufen | - | Float1 | Abrufen einer Funktion oder eines Graphen einer Gleitkommaeingabe |
|                                                                                                                                        | Float2 abrufen | - | Float2 | Abrufen einer Funktion oder eines Diagramms Float2-Werteingabe |
|                                                                                                                                        | Float3 abrufen | - | Float3 | Abrufen einer Funktion oder eines Diagramms Float3-Werteingabe |
|                                                                                                                                        | Float4 abrufen | - | Float4 | Abrufen einer Funktion oder eines Diagramms Float4-Werteingabe |
|                                                                                                                                        | Booleschen Wert abrufen | - | Boolescher Wert | Abrufen einer Funktion oder eines Graphen einer booleschen Werteingabe |
| Sampler | Beispielgrau | Vektor-Gleitkommawert2 | Float4 | Gibt den Graustufenwert eines Eingabebildes bei den angegebenen UV-Koordinaten (float2) zurück. |
|                                                                                                                                        | Farbe aufnehmen | Vektor-Gleitkommawert2 | Float4 | Gibt den Farbwert eines Eingabebildes bei den angegebenen UV-Koordinaten (float2) zurück. |
| Konvertieren | Zu Gleitkommawert | Integer1 | Float1 | Konvertiert eine ganze Zahl in einem Gleitkomma |
|                                                                                                                                        | Zu Gleitkommawert2 | Integer2 | Float2 | Konvertiert einen Integer2-Wert in einem Float2-Wert |
|                                                                                                                                        | Zu Gleitkommawert3 | Integer3 | Float3 | Konvertiert einen Integer3-Wert in einen Float3-Wert |
|                                                                                                                                        | Zu Gleitkommawert4 | Integer4 | Float4 | Konvertiert eine Integer4 in einem Float4-Objekt |
|                                                                                                                                        | Zu Ganzzahl | Float1 | Integer1 | Konvertiert einen Float in einer Ganzzahl |
|                                                                                                                                        | Zu Ganzzahl2 | Float2 | Integer2 | Konvertiert ein Float2 in Integer2 |
|                                                                                                                                        | Zu Ganzzahl3 | Float3 | Integer3 | Konvertiert ein Float3 in Integer3 |
|                                                                                                                                        | Zu Ganzzahl4 | Float4 | Integer4 | Konvertiert ein Float4-Element in ein Integer4-Element |
| [Operator](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Addieren | Vector Float/Integer | Typ von a &amp; b | Fügt 2 Werte desselben Typs hinzu: a + b |
|                                                                                                                                        | Subtraktion | Vector Float/Integer | Typ von a &amp; b | Subtrahiert 2 Werte desselben Typs: a - b |
|                                                                                                                                        | Multiplikation | Vector Float/Integer | Typ von a &amp; b | Multipliziert 2 Werte desselben Typs: a \* b |
|                                                                                                                                        | Skalarmultiplikation | Vektor-Float | Typ eines | Multipliziert einen Wert mit einem variablen Wert: a \* skalar |
|                                                                                                                                        | Division | Float1 / Integer1 | Typ von a &amp; b | Dividiert 2 Werte desselben Typs: a / b |
|                                                                                                                                        | Negation | Float1 / Integer1 | Typ eines | Gibt den Negationswert zurück: -a |
|                                                                                                                                        | Modulo | Float1 / Integer1 | Typ eines | Gibt den Modulo-Wert zurück: mod(a, divisor) |
|                                                                                                                                        | Skalarprodukt | Vektor-Float | Typ von a &amp; b | Gibt das Punktprodukt von 2 Werten desselben Typs zurück: Buchstabe a, b |
| [Logisch](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | Und | Boolescher Wert | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn die beiden booleschen Einträge &quot;true&quot; sind. Gibt false zurück, wenn einer der Einträge false ist. |
|                                                                                                                                        | Or | Boolescher Wert | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn 1 der booleschen Einträge &quot;true&quot; ist. Gibt false zurück, wenn beide false sind. |
|                                                                                                                                        | Nicht | Boolescher Wert | Boolescher Wert | Gibt den booleschen Wert der Negation des Eintrags zurück: !a |
| [Vergleich](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Equal | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a = b |
|                                                                                                                                        | Not Equal | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a != b |
|                                                                                                                                        | Größer | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a > b |
|                                                                                                                                        | Größer oder gleich | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a >= b |
|                                                                                                                                        | Kleiner | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a &lt; b |
|                                                                                                                                        | Kleiner oder gleich | Float1 / Integer1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a &lt;= b |
| Funktion | Absolut | Float1 / Integer1 | Float1 | Gibt den absoluten Wert von a zurück: abs(a) |
|                                                                                                                                        | Floor | Float1 / Integer1 | Float1 | Gibt den höchsten Wert (kleiner oder gleich a) zurück: Stockwerk a |
|                                                                                                                                        | Aufrunden | Float1 / Integer1 | Float1 | Gibt den kleinsten Wert zurück, der größer oder gleich a ist: ceil(a) |
|                                                                                                                                        | Cosine | Float1 / Integer1 | Float1 | Gibt den Cosinuswert eines Werts zurück: cos(a) |
|                                                                                                                                        | Sine | Float1 / Integer1 | Float1 | Gibt den Sinuswert von a zurück: sin(a) |
|                                                                                                                                        | Tangent | Float1 / Integer1 | Float1 | Gibt den Tangentenwert von a zurück: tan(a) |
|                                                                                                                                        | Arkustangens 2 | Vektor-Gleitkommawert2 | Float1 | Gibt den Wert für arc tan 2 eines vector2 -Eintrags zurück: arctan2(xa, ya) |
|                                                                                                                                        | Kartesisch | Float1 | Float2 | Konvertiert 2 Polarkoordinaten in kartesische Koordinaten: carth(rho, theta) |
|                                                                                                                                        | Square Root | Float1 / Integer1 | Float1 | Gibt den Quadratwurzelwert eines |
|                                                                                                                                        | Logarithmisch | Float1 / Integer1 | Float1 | Gibt den logarithmischen Wert von a zurück: log(a) |
|                                                                                                                                        | Exponentiell | Float1 / Integer1 | Float1 | Gibt den exponentiellen Wert von a zurück: exp(a) |
|                                                                                                                                        | Pow 2 | Float1 / Integer1 | Float1 | Gibt den Potenzwert 2 von a zurück. |
|                                                                                                                                        | Lineare Interpolation | Float1 / Integer1 | Float1 | Gibt die lineare Interpolation zwischen 2 Werten zurück, abhängig von einem Gleitkommawert: (1-x)a + x \* b |
|                                                                                                                                        | Minimum | Float1 / Integer1 | Typ von a &amp; b | Gibt den Mindestwert zwischen a und b zurück. |
|                                                                                                                                        | Maximum | Float1 / Integer1 | Typ von a &amp; b | Gibt den Maximalwert zwischen a und b zurück. |
| Zufallswert |                       | Float1 | Float1 | Generiert einen Gleitkommawert zwischen 0 und einem |
| [Steuerelement](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Abfolge | alle | Eingabetyp | Ermöglicht die Auswahl des zuerst zu berechnenden Werts zwischen 2 Werten. |
|                                                                                                                                        | If...Else | Boolesch / a &amp; b | Typ von a &amp; b | Gibt den Wert &quot;true&quot; zurück, wenn die Bedingung in &quot;If&quot; &quot;true&quot; ist. Gibt false zurück, wenn es false ist. |

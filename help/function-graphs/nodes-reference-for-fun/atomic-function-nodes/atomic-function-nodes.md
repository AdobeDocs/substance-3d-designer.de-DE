---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Erfahren Sie mehr über atomare Funktionsknoten, die kleinsten Knoteneinheiten in Substance-Funktions-Graf zum Erstellen benutzerdefinierter Funktionen.
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

Ähnlich wie [elementare Knoten in Substance-Graf](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) sind elementare Knoten in Substance-Funktions-Graf die kleinsten Knoteneinheiten in diesem Graf.

Sie können je nach ihrem Zweck in mehrere Kategorien eingeteilt werden:

| Kategorie | Knoten | Eingabetyp(en) | Ausgabetyp | Beschreibung |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Konstante](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Float | - | Float | Definiert einen konstanten Fließkommawert, z. B. 0,1 |
|                                                                                                                                        | Float2 | - | Float2 | Definiert einen konstanten Vektor von 2 Fließkommawerten, z. B. (0,1, 0,2) |
|                                                                                                                                        | Float3 | - | Float3 | Definiert einen konstanten Vektor von 3 Fließkommawerten, z. B. (0,1, 0,2, 0,3) |
|                                                                                                                                        | Float4 | - | Float4 | Definiert einen konstanten Vektor von 4 Fließkommawerten, z. B. (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Ganzzahl | - | Ganzzahl | Definiert eine konstante Ganzzahl, z. B. 1. |
|                                                                                                                                        | Integer2 | - | Integer2 | Definiert einen konstanten Vektor mit 2 Ganzzahlen Werten, z. B. (1, 2) |
|                                                                                                                                        | Integer3 | - | Integer3 | Definiert einen konstanten Vektor mit 3 Ganzzahlen Werten, z. B. (1, 2, 3) |
|                                                                                                                                        | Integer4 | - | Integer4 | Definiert einen Konstantvektor mit 4 Ganzzahlen Werten, z. B. (1, 2, 3, 4) |
|                                                                                                                                        | Boolescher Wert | - | Boolescher Wert | Definiert einen konstanten booleschen Wert, z. B. True oder False. |
|                                                                                                                                        | Zeichenfolge | - | Zeichenfolge | Definiert einen konstanten String-Wert, z. B. &quot;Substance&quot; |
| [Vektor](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vektor-Gleitkommawert2 | Fließkommazahl1 | Fließkommawert 2 | Wirft 2 Fließkommawert in einem Vektor mit 2 Koordinaten |
|                                                                                                                                        | Vektor-Gleitkommawert3 | Fließkommazahl1 / Fließkommazahl2 | Fließkomma 3 | Wirft 2 Fließkommawert in einem Vektor mit 3 Koordinaten |
|                                                                                                                                        | Vektor-Gleitkommawert4 | Fließkommazahl1 / 2 / 3 | Float4 | Wirft 2 Fließkommawert in einem Vektor mit 4 Koordinaten |
|                                                                                                                                        | Swizzle-Gleitkommawert1 | Vektor-Gleitkommazahl | Fließkommazahl1 | Extrahiert eine gleitende Koordinate aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert2 | Vektor-Gleitkommazahl | Float2 | Extrahiert 2 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert3 | Vektor-Gleitkommazahl | Float3 | Extrahiert 3 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Gleitkommawert4 | Vektor-Gleitkommazahl | Float4 | Extrahiert 4 schwebende Koordinaten aus einem Vektor |
|                                                                                                                                        | Vektor-Ganzzahl2 | Integer2 | Vektor-Ganzzahl2 | Wirft 2 Ganzzahlen in einem Vektor mit 2 Koordinaten |
|                                                                                                                                        | Vektor-Ganzzahl3 | Integer3 | Integer3 | Zeigt 2 ganzzahlige Werte in einem Vektor mit 3 Koordinaten an |
|                                                                                                                                        | Vektor-Ganzzahl4 | Integer4 | Integer4 | Wirft 2 Ganzzahlen in einem Vektor mit 4 Koordinaten |
|                                                                                                                                        | Swizzle-Ganzzahl1 | Vector Integer | Integer1 | Extrahiert eine Ganzzahl-Koordinate aus einem Vektor. |
|                                                                                                                                        | Swizzle-Ganzzahl2 | Vector Integer | Integer2 | Extrahiert 2 Ganzzahlkoordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Ganzzahl3 | Vector Integer | Integer3 | Extrahiert 3 Ganzzahlkoordinaten aus einem Vektor |
|                                                                                                                                        | Swizzle-Ganzzahl4 | Vector Integer | Integer4 | Extrahiert 4 Ganzzahlkoordinaten aus einem Vektor |
| [Variablen](../../../function-graphs/variables/variables.md) | Festgelegt | alle | Eingabetyp | Festlegen einer Variablen |
|                                                                                                                                        | Ganzzahl abrufen1 | - | Integer1 | Wert für Funktion oder Graf-Ganzzahl abrufen |
|                                                                                                                                        | Integer2 abrufen | - | Integer2 | Abrufen einer Funktion oder eines Grafen Ganzzahl2-Wert-Eingabe |
|                                                                                                                                        | Integer3 abrufen | - | Integer3 | Abrufen einer Funktion oder eines Grafen Ganzzahl3-Werteingabe |
|                                                                                                                                        | Integer4 abrufen | - | Integer4 | Abrufen einer Funktion oder eines Grafen Ganzzahl4-Wert-Eingabe |
|                                                                                                                                        | Fließkommazahl abrufen1 | - | Fließkommazahl1 | Abrufen einer Funktion oder eines Graf-Fließkommawerts |
|                                                                                                                                        | Float2 abrufen | - | Float2 | Abrufen einer Funktion oder eines Grafen Fließkommazahl2-Wert-Eingabe |
|                                                                                                                                        | Float3 abrufen | - | Float3 | Abrufen einer Funktion oder eines Grafen Fließkommazahl3-Werteingabe |
|                                                                                                                                        | Float4 abrufen | - | Float4 | Abrufen einer Funktion oder eines Grafen Fließkommazahl4-Wert-Eingabe |
|                                                                                                                                        | Booleschen Wert abrufen | - | Boolescher Wert | Abrufen einer Eingabe für einen booleschen Wert für eine Funktion oder einen Graf |
| Sampler | Beispielgrau | Vektor-Gleitkommawert2 | Float4 | Gibt den Graustufenwert eines Eingabebilds bei den angegebenen UV-Koordinaten (float2) zurück. |
|                                                                                                                                        | Farbe aufnehmen | Vektor-Gleitkommawert2 | Float4 | Gibt den Farbwert eines Eingabebilds bei den angegebenen UV-Koordinaten (float2) zurück. |
| Konvertieren | Zu Gleitkommawert | Integer1 | Fließkommazahl1 | Konvertiert eine Ganzzahl in einem Gleitkomma |
|                                                                                                                                        | Zu Gleitkommawert2 | Integer2 | Float2 | Konvertiert eine Ganzzahl2 in einer Fließkommazahl2 |
|                                                                                                                                        | Zu Gleitkommawert3 | Integer3 | Float3 | Konvertiert eine Ganzzahl3 in einer Fließkommazahl3 |
|                                                                                                                                        | Zu Gleitkommawert4 | Integer4 | Float4 | Konvertiert eine Ganzzahl 4 in einer Fließkommazahl 4 |
|                                                                                                                                        | Zu Ganzzahl | Fließkommazahl1 | Integer1 | Konvertiert eine Fließkommazahl in einer Ganzzahl |
|                                                                                                                                        | Zu Ganzzahl2 | Float2 | Integer2 | Konvertiert eine Fließkommazahl2 in einer Ganzzahl2 |
|                                                                                                                                        | Zu Ganzzahl3 | Float3 | Integer3 | Konvertiert eine Fließkommazahl3 in einer Ganzzahl3 |
|                                                                                                                                        | Zu Ganzzahl4 | Float4 | Integer4 | Konvertiert ein Float4-Element in ein Integer4-Element |
| [Operator](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Addieren | Vektor-Gleitkommazahl/Ganzzahl | Typ von a &amp; b | Fügt 2 Werte desselben Typs hinzu: a + b |
|                                                                                                                                        | Subtraktion | Vektor-Gleitkommazahl/Ganzzahl | Typ von a &amp; b | Subtrahiert 2 Werte desselben Typs: a - b |
|                                                                                                                                        | Multiplikation | Vektor-Gleitkommazahl/Ganzzahl | Typ von a &amp; b | Multipliziert 2 Werte desselben Typs: a \* b |
|                                                                                                                                        | Skalarmultiplikation | Vektor-Gleitkommazahl | Typ eines | Multipliziert einen Wert mit einem variablen Wert: a \* skalar |
|                                                                                                                                        | Division | Fließkommazahl1 / Ganzzahl1 | Typ von a &amp; b | Dividiert 2 Werte desselben Typs: a / b |
|                                                                                                                                        | Negation | Fließkommazahl1 / Ganzzahl1 | Typ eines | Gibt den Negationswert zurück: -a |
|                                                                                                                                        | Modulo | Fließkommazahl1 / Ganzzahl1 | Typ eines | Gibt den Modulo-Wert zurück: mod(a, divisor) |
|                                                                                                                                        | Skalarprodukt | Vektor-Gleitkommazahl | Typ von a &amp; b | Gibt das Punktprodukt von 2 Werten desselben Typs zurück: Buchstabe a, b |
| [Logisch](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | Und | Boolescher Wert | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn die beiden booleschen Einträge &quot;true&quot; sind. Gibt false zurück, wenn einer der Einträge false ist. |
|                                                                                                                                        | Or | Boolescher Wert | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn 1 der booleschen Einträge &quot;true&quot; ist. Gibt false zurück, wenn beide false sind. |
|                                                                                                                                        | Nicht | Boolescher Wert | Boolescher Wert | Gibt den booleschen Wert der Negation des Eintrags zurück: !a |
| [Vergleich](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Equal | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a = b |
|                                                                                                                                        | Not Equal | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a != b |
|                                                                                                                                        | Größer | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a > b |
|                                                                                                                                        | Größer oder gleich | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a >= b |
|                                                                                                                                        | Kleiner | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a &lt; b |
|                                                                                                                                        | Kleiner oder gleich | Fließkommazahl1 / Ganzzahl1 | Boolescher Wert | Gibt &quot;true&quot; zurück, wenn a &lt;= b |
| Funktion | Absolut | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den absolute Wert von a zurück: abs(a) |
|                                                                                                                                        | Floor | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den höchsten Wert (kleiner oder gleich a) zurück: Stockwerk a |
|                                                                                                                                        | Aufrunden | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den kleinsten Wert zurück, der größer oder gleich a ist: ceil(a) |
|                                                                                                                                        | Cosine | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den Cosinuswert eines Werts zurück: cos(a) |
|                                                                                                                                        | Sine | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den Sinuswert von a zurück: sin(a) |
|                                                                                                                                        | Tangent | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den Wert der Tangente a zurück: tan(a) |
|                                                                                                                                        | Arkustangens 2 | Vektor-Gleitkommawert2 | Fließkommazahl1 | Gibt den Wert für arc tan 2 eines vector2 -Eintrags zurück: arctan2(xa, ya) |
|                                                                                                                                        | Kartesisch | Fließkommazahl1 | Float2 | Konvertiert 2 Polarkoordinaten in kartesische Koordinaten: carth(rho, theta) |
|                                                                                                                                        | Square Root | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den Quadratwurzelwert eines |
|                                                                                                                                        | Logarithmisch | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den logarithmischen Wert von a zurück: log(a) |
|                                                                                                                                        | Exponentiell | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den exponentiellen Wert von a zurück: exp(a) |
|                                                                                                                                        | Pow 2 | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt den Potenzwert 2 von a zurück. |
|                                                                                                                                        | Lineare Interpolation | Fließkommazahl1 / Ganzzahl1 | Fließkommazahl1 | Gibt die lineare Interpolation zwischen 2 Werten zurück, abhängig von einem Fließkommawert : (1-x)a + x \* b |
|                                                                                                                                        | Minimum | Fließkommazahl1 / Ganzzahl1 | Typ von a &amp; b | Gibt den Mindestwert zwischen a und b zurück. |
|                                                                                                                                        | Maximum | Fließkommazahl1 / Ganzzahl1 | Typ von a &amp; b | Gibt den Maximalwert zwischen a und b zurück. |
| Zufallswert |                       | Fließkommazahl1 | Fließkommazahl1 | Generiert einen Fließkommawert zwischen 0 und a |
| [Steuerelement](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Abfolge | alle | Eingabetyp | Ermöglicht die Auswahl des zuerst zu berechnenden Werts zwischen 2 Werten. |
|                                                                                                                                        | If...Else | BOOLESCHE WERT / a &amp; b | Typ von a &amp; b | Gibt den Wert &quot;true&quot; zurück, wenn die Bedingung in &quot;If&quot; &quot;true&quot; ist. Gibt false zurück, wenn es false ist. |

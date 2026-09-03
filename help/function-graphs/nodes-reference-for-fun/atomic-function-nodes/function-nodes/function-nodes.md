---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Greifen Sie auf Funktionsknoten in Substance 3D Designer-Funktionsdiagrammen zu, um benutzerdefinierte Funktionsdiagramme aufzurufen und auszuführen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Funktion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Funktionsknoten

Funktionsknoten transformieren den Eingabewert entsprechend der mathematischen Funktion, die sie darstellen.

Obwohl ihre Eingangsanschlüsse im Allgemeinen nicht typisiert sind, unterstützen sie nicht alle Werttypen.

## Knotenliste

+++Pow
![Pow-Knotensymbol](function-nodes.resources/function-nodes-01.jpg "Pow-Knotensymbol")



Gibt den ersten Eingang zurück, der mit der Leistung des zweiten Eingangs erhöht wurde: <b>X^Y</b>.

+++

+++2Pow
![Knotensymbol &#x200B;](function-nodes.resources/function-nodes-02.jpg "2Knotensymbol ")



Gibt 2 an die Stärke des Eingangswerts zurück: <b>2^X</b>.

+++

+++Quadratwurzel
![Quadratisches Stammknotensymbol](function-nodes.resources/function-nodes-03.jpg "Quadratisches Stammknotensymbol")



Gibt die Quadratwurzel des Eingabewerts zurück: <b>√X</b>.

+++

+++Exponentiell
![Exponentielles Knotensymbol](function-nodes.resources/function-nodes-04.jpg "Exponentielles Knotensymbol")



Gibt den Exponentialwert des Eingabewerts zurück: <b>e^X</b>

<b>e</b> ist ungefähr gleich 2,7182818.

+++

+++Logarithmus
![Symbol für Logarithmus-Knoten](function-nodes.resources/function-nodes-05.jpg "Symbol für Logarithmus-Knoten")



Gibt den natürlichen Logarithmus des Eingabewerts zurück: <b>ln(X)</b>.

+++

+++Logarithmusbasis 2
![Symbol für Logarithmus Base 2-Knoten](function-nodes.resources/function-nodes-06.jpg "Symbol für Logarithmus Base 2-Knoten")



Gibt den Logarithmus zur Basis 2 des Eingabewerts zurück: <b>log2(X)</b>.

+++

+++Absolut
![Absolutes Knotensymbol](function-nodes.resources/function-nodes-07.jpg "Absolutes Knotensymbol")



Gibt den absoluten Wert der Eingabe zurück: <b>abs(X)</b>.

+++

+++Aufrunden
![Ceil-Knotensymbol](function-nodes.resources/function-nodes-08.jpg "Ceil-Knotensymbol")



Rundet den Eingabewert auf. Es gibt den kleinsten ganzzahligen Wert zurück, der nicht kleiner als X ist: <b>ceil(X)</b>.

+++

+++Floor
![Symbol für Bodenknoten](function-nodes.resources/function-nodes-09.jpg "Symbol für Bodenknoten")



Rundet den Eingabewert ab. Es gibt den größten ganzzahligen Wert zurück, der nicht größer als X ist: <b>floor(X)</b>.

+++

+++Lineare Interpolation
![Symbol für linearen Interpolationsknoten](function-nodes.resources/function-nodes-10.jpg "Symbol für linearen Interpolationsknoten")



Gibt die lineare Interpolation zwischen zwei Werten in Funktion eines Gleitkommawertes zurück: <b>(1 - X)\*A + X\*B</b>.

+++

+++Minimum
![Mindestknotensymbol](function-nodes.resources/function-nodes-11.jpg "Mindestknotensymbol")



Gibt den niedrigsten der beiden Eingabewerte zurück: <b>Min(A, B)</b>.

+++

+++Maximum
![Maximales Knotensymbol](function-nodes.resources/function-nodes-12.jpg "Maximales Knotensymbol")



Gibt den höchsten der beiden Eingabewerte zurück: <b>max(A, B)</b>.

+++

+++Cosine
![Symbol für Kosinusknoten](function-nodes.resources/function-nodes-13.jpg "Symbol für Kosinusknoten")



Gibt den Kosinus des Eingabewerts in Bogenmaß zurück: <b>cos(X)</b>.

+++

+++Sine
![Sinusknotensymbol](function-nodes.resources/function-nodes-14.jpg "Sinusknotensymbol")



Gibt den Sinus des Eingabewerts in Bogenmaß zurück: <b>sin(X)</b>.

+++

+++Tangent
![Tangent-Knotensymbol](function-nodes.resources/function-nodes-15.jpg "Tangent-Knotensymbol")



Gibt die Tangente des Eingangswerts in Bogenmaß zurück: <b>tan(X)</b>.

+++

+++Arkustangens 2
![Knotensymbol &quot;Arc Tangent 2&quot;](function-nodes.resources/function-nodes-16.jpg "Knotensymbol &quot;Arc Tangent 2&quot;")



Gibt den Winkel zwischen dem eingegebenen 2D-Vektor und der Horizontalen zurück.

Dies ist der reziproke Wert der <b>kartesischen</b>-Funktion.

Es ist nicht erforderlich, die X- und Y-Komponente des Eingangsvektors wie in der üblichen <b>atan2</b>-Funktion zu wechseln.

+++

+++Kartesisch
![Absolutes Knotensymbol](function-nodes.resources/function-nodes-07.jpg "Absolutes Knotensymbol")



Konvertiert Polarkoordinaten in kartesische Koordinaten.

Dies ist der reziproke Wert der <b>Arc-Tangente 2 </b>-Funktion: <b>Länge \* Float2(cos(Angle), sin(Angle).</b>

Polarkoordinaten sind ein Abstand zum Ursprung und ein Winkel in Radianten zur Horizontalen.

+++

+++Zufallswert
![Symbol für zufälligen Knoten](function-nodes.resources/function-nodes-17.jpg "Symbol für zufälligen Knoten")



Gibt einen zufälligen Wert zwischen 0 und dem Eingabewert <b>X</b> zurück.

+++

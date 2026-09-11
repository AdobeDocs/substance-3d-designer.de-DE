---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Funktionsknoten

Funktionsknoten transformieren den Eingabewert entsprechend der mathematischen Funktion, die sie darstellen.

Obwohl ihre Eingangsanschlüsse im Allgemeinen nicht typisiert sind, unterstützen sie nicht alle Werttypen.

## Knotenliste

+++Pow
![Pow-Knotensymbol](../../../../assets/Pow_Node.jpg "Pow-Knotensymbol")



Gibt den ersten Eingang zurück, der mit der Leistung des zweiten Eingangs erhöht wurde: <b>X^Y</b>.

+++

+++2Pow
![Knotensymbol &#x200B;](../../../../assets/2Pow_Node.jpg "2Knotensymbol ")



Gibt 2 an die Stärke des Eingangswerts zurück: <b>2^X</b>.

+++

+++Quadratwurzel
![Quadratisches Stammknotensymbol](../../../../assets/SquareRoot_Node.jpg "Quadratisches Stammknotensymbol")



Gibt die Quadratwurzel des Eingabewerts zurück: <b>√X</b>.

+++

+++Exponentiell
![Exponentielles Knotensymbol](../../../../assets/Exponential_Node.jpg "Exponentielles Knotensymbol")



Gibt den Exponentialwert des Eingabewerts zurück: <b>e^X</b>

<b>e</b> ist ungefähr gleich 2,7182818.

+++

+++Logarithmus
![Symbol für Logarithmus-Knoten](../../../../assets/Logarithm_Node.jpg "Symbol für Logarithmus-Knoten")



Gibt den natürlichen Logarithmus des Eingabewerts zurück: <b>ln(X)</b>.

+++

+++Logarithmusbasis 2
![Symbol für Logarithmus Base 2-Knoten](../../../../assets/LogarithmBase2_Node.jpg "Symbol für Logarithmus Base 2-Knoten")



Gibt den Logarithmus zur Basis 2 des Eingabewerts zurück: <b>log2(X)</b>.

+++

+++Absolut
![Absolutes Knotensymbol](../../../../assets/Absolute_Node.jpg "Absolutes Knotensymbol")



Gibt den absoluten Wert der Eingabe zurück: <b>abs(X)</b>.

+++

+++Aufrunden
![Ceil-Knotensymbol](../../../../assets/Ceil_Node.jpg "Ceil-Knotensymbol")



Rundet den Eingabewert auf. Es gibt den kleinsten ganzzahligen Wert zurück, der nicht kleiner als X ist: <b>ceil(X)</b>.

+++

+++Floor
![Symbol für Bodenknoten](../../../../assets/Floor_Node.jpg "Symbol für Bodenknoten")



Rundet den Eingabewert ab. Es gibt den größten ganzzahligen Wert zurück, der nicht größer als X ist: <b>floor(X)</b>.

+++

+++Lineare Interpolation
![Symbol für linearen Interpolationsknoten](../../../../assets/LinearInterpolation_Node.jpg "Symbol für linearen Interpolationsknoten")



Gibt die lineare Interpolation zwischen zwei Werten in Funktion eines Gleitkommawertes zurück: <b>(1 - X)\*A + X\*B</b>.

+++

+++Minimum
![Mindestknotensymbol](../../../../assets/Minimum_Node.jpg "Mindestknotensymbol")



Gibt den niedrigsten der beiden Eingabewerte zurück: <b>Min(A, B)</b>.

+++

+++Maximum
![Maximales Knotensymbol](../../../../assets/Maximum_Node.jpg "Maximales Knotensymbol")



Gibt den höchsten der beiden Eingabewerte zurück: <b>max(A, B)</b>.

+++

+++Cosine
![Symbol für Kosinusknoten](../../../../assets/Cosine_Node.jpg "Symbol für Kosinusknoten")



Gibt den Kosinus des Eingabewerts in Bogenmaß zurück: <b>cos(X)</b>.

+++

+++Sine
![Sinusknotensymbol](../../../../assets/Sine_Node.jpg "Sinusknotensymbol")



Gibt den Sinus des Eingabewerts in Bogenmaß zurück: <b>sin(X)</b>.

+++

+++Tangent
![Tangent-Knotensymbol](../../../../assets/Tangent_Node.jpg "Tangent-Knotensymbol")



Gibt die Tangente des Eingangswerts in Bogenmaß zurück: <b>tan(X)</b>.

+++

+++Arkustangens 2
![Knotensymbol &quot;Arc Tangent 2&quot;](../../../../assets/ArcTangent2_Node.jpg "Knotensymbol &quot;Arc Tangent 2&quot;")



Gibt den Winkel zwischen dem eingegebenen 2D-Vektor und der Horizontalen zurück.

Dies ist der reziproke Wert der <b>kartesischen</b>-Funktion.

Es ist nicht erforderlich, die X- und Y-Komponente des Eingangsvektors wie in der üblichen <b>atan2</b>-Funktion zu wechseln.

+++

+++Kartesisch
![Absolutes Knotensymbol](../../../../assets/Absolute_Node.jpg "Absolutes Knotensymbol")



Konvertiert Polarkoordinaten in kartesische Koordinaten.

Dies ist der reziproke Wert der <b>Arc-Tangente 2 </b>-Funktion: <b>Länge \* Float2(cos(Angle), sin(Angle).</b>

Polarkoordinaten sind ein Abstand zum Ursprung und ein Winkel in Radianten zur Horizontalen.

+++

+++Zufallswert
![Symbol für zufälligen Knoten](../../../../assets/Random_Node.jpg "Symbol für zufälligen Knoten")



Gibt einen zufälligen Wert zwischen 0 und dem Eingabewert <b>X</b> zurück.

+++

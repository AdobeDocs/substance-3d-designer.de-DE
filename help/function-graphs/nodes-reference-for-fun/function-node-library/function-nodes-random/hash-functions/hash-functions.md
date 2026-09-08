---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: Verwenden Sie Hashfunktionen in Funktionsdiagrammen, um deterministische Zufallswerte basierend auf Eingangskoordinaten zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hash-Funktionen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Hash-Funktionen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Hashknoten: Symbol &#x200B;](../../../../../assets/hash-icon.png "Hashknoten: Symbol "){width="200px"}

<b>In:</b> Funktionen > Zufällig

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Berechnet einen pseudozufälligen Wert zwischen 0 und 1 basierend auf einem Eingabewert, der als Seed verwendet wird.

Die Zahl im Titel zeigt den Typ des Werts in und Wert out an. Beispiel: Hash 23 nimmt einen float2-Wert als Eingang und gibt einen float3-Wert aus.

</td>
</tr>
</table>

Wenn ein Hash-Knoten einen Wert von mehreren Komponenten ausgibt, hat jede Komponente einen anderen pseudo-zufälligen Wert.

Verfügbare Versionen mit Eingabe- und Ausgabetyp:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Hash 11:</b> Fließkommazahl → Fließkommazahl

<b>Hash 14:</b> Fließkommazahl → Fließkommazahl4

<b>Hash 21:</b> Fließkommazahl2 → Fließkommazahl

<b>Hash 22:</b> Fließkommazahl 2 → Fließkommazahl 2

</td>
<td style="border: 0;" valign="top">

<b>Hash 24:</b> Fließkommazahl 2 → Fließkommazahl 4

<b>Hash31:</b> Fließkommazahl3 → Fließkommazahl

<b>Hash 32:</b> Fließkommazahl 3 → Fließkommazahl 2

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> | Der Wert, der als Seed zur Berechnung der pseudozufälligen Ausgabe verwendet wird. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Beispiel für Hash 14](../../../../../assets/hash14-example.png "Beispiel für Hash 14"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Beispiel für Hash 32](../../../../../assets/hash32-example.png "Beispiel für Hash 32"){zoomable="yes"}

</td>
</tr>
</table>

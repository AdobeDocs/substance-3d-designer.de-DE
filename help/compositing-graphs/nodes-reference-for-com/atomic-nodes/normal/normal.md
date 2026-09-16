---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten Normal , um Normalen-Map-Texturen zur Steuerung von Oberflächendetails und Beleuchtung zu verarbeiten und zu bearbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%
---

# Normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Normal](normal.resources/comp_normal_1.png "Elementare Knoten: Normal")

</td>
<td style="border: 0;" valign="top">

Berechnet eine Normalen-Map aus einem Graustufenbild, das als Höhen-Map interpretiert wird.

Der Knoten konvertiert eine Graustufenzuordnung in eine Tangente-Raum-Normalen-Map-Ausgabe. Es gibt einige Benutzeroptionen, um Intensität und Codierung festzulegen.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="normal.resources/normal-tooltip.gif" alt="Normalwerkzeugspitze" /></div>

Es ist ein sehr nützlicher Knoten, der häufig verwendet wird, um Höhen-Map-Eingaben in Normalen-Map für Echtzeit-fähige Material zu konvertieren. Es gibt Alternativen in [Normal Sobel](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) und Height To Normal World Units.



## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Gleitend* | Ändert die Intensität des Höhen-Map.   Legt fest, wie intensiv die Eingabe-Höhen-Map für die Konvertierung in Normale interpretiert wird. Je nach Eingabe-Map haben Werte über 100 wenig mehr Wirkung. |
| <b>Normales Format</b> *Boolescher Wert* | Kehrt die Y-Koordinaten des Höhen-Map (OpenGL) um.   Legt fest, wie der grüne Kanal (Y) codiert wird. Grundsätzlich ein Schalter &quot;Grün/Y spiegeln&quot;. |
| <b>Inhalt des Alphakanals</b> *Boolescher Wert* | Füllen Sie den Alphakanal des Normalen-Map mit der Eingabe-Textur.   Alpha mit Eingabe füllen/Alpha auf 1 erzwingen:  Dadurch kann der Alphakanal auf &quot;solid&quot; gesetzt werden, anstatt den Eingang als zusätzliches Alpha zu verwenden. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen* PRIMÄR | Eingabebild wird als Höhen-Map interpretiert. |


## Beispiele

*Demnächst verfügbar.*

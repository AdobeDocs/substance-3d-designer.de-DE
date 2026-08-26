---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal , um normale Map-Texturen zu verarbeiten und zu bearbeiten, um Oberflächendetails und Beleuchtung zu steuern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomknoten: Normal](../../../../assets/comp_normal_1.png "Atomknoten: Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Berechnet eine Normalen-Map aus einem Graustufenbild, das als Höhen-Map interpretiert wird.

Der Knoten konvertiert eine Graustufen-Eingabemaske in eine normale Tangentenraum-Map-Ausgabe. Es gibt einige Benutzeroptionen, um Intensität und Codierung festzulegen.

</td>
</tr>
</table>

Es ist ein sehr nützlicher Knoten, der häufig verwendet wird, um Height-Map-Eingaben in normale Maps für Echtzeit-Materialien umzuwandeln. Es gibt Alternativen in [Normal Sobel](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) und Height To Normal World Units.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Beispiele

</td>
</tr>
</table>

## Parameter

|  |  |
| --- | --- |
| <b>Intensität</b> *Gleitend* | Ändert die Intensität der Height-Map.   Legt fest, wie intensiv die Eingabe-Height-Map für die Konvertierung in Normale interpretiert wird. Je nach Eingabemaps haben Werte über 100 wenig mehr Wirkung. |
| <b>Normales Format</b> *Boolescher Wert* | Kehrt die Y-Koordinaten der Heights-Map (OpenGL) um.   Legt fest, wie der grüne Kanal (Y) codiert wird. Grundsätzlich ein Schalter &quot;Grün/Y spiegeln&quot;. |
| <b>Inhalt des Alpha-Kanals</b> *Boolescher Wert* | Füllen Sie den Alphakanal der normalen Map mit der Eingabetextur.   Alpha mit Eingabe füllen/Alpha auf 1 erzwingen:  Auf diese Weise kann der Alpha-Kanal auf &quot;solid&quot; festgelegt werden, anstatt den Eingang als zusätzliches Alpha zu verwenden. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Eingabe</b> *Graustufen* PRIMÄR | Eingabebild, das als Height-Map interpretiert wird. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe* |  |

## Beispiele

*Demnächst verfügbar.*

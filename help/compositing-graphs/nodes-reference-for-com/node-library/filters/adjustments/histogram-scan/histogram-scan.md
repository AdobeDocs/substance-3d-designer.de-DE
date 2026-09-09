---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Histogramm-Scan, um Histogramme der Textur zur Farbkorrektur und Farbanpassung zu scannen und zu analysieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramm-Scan
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Histogramm-Scan

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-1.png){width="128px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein sehr einfacher, aber nützlicher Knoten, der eine intuitive Möglichkeit bietet, um den Kontrast und die Helligkeit von Eingabe-Graustufenbildern neu zuzuordnen. Kann verwendet werden, um Masken auf dynamische Weise zu &quot;vergrößern&quot; und zu &quot;verkleinern&quot;.

[Klicken Sie hier, um ein Substance Academy-Video über Histogrammoperationen anzuzeigen.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Position</b> <i>0.0 - 1.0</i> | Ähnlich wie bei einer Helligkeitssteuerung wird der Mittelpunkt des Ergebnisses verschoben. Bei Verwendung an einer Verlaufseingabe wird dadurch der Übergangspunkt erweitert und verkleinert.<br><br>Wichtig: Ein Standardwert von 0 bedeutet, dass das Endergebnis immer schwarz ist, also versuchen Sie, mit 0,5 zu beginnen! |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. Kann zum Festlegen der Härte der Überblendung verwendet werden. |
| <b>Position umkehren</b> <i>False/True</i> | Kehrt das Ergebnis um. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan3.gif" />
        </td>
    </tr>
</table>

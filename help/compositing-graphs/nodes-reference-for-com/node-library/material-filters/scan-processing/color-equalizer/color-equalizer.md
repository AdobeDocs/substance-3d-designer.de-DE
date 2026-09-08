---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Color Equalizer", um Farbvariationen in gescannten Materialien für ein konsistentes Texturaussehen auszugleichen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten funktioniert wie ein hochwertiger [Hochpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) für Farbunterschiede. Während ein normaler Hochpass die Sättigung entfernt und unerwünschte Schärfe verursachen kann, entfernt Color Equalizer unerwünschte Farbtöne in einer vom Benutzer auswählbaren Skala und sorgt so für einen gleichmäßigen Farbverlauf.

Dies ist sehr nützlich, wenn ein Foto oder Scan unerwünschte Farbunterschiede oder einen Farbton aufweist, den Sie entfernen möchten. Wenn Sie [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) verwendet haben, sollte dieser Knoten Ihnen bekannt vorkommen.

Die Maskierungsoptionen sind dazu bestimmt, sehr spezifische Farbtöne zu entfernen oder nur in bestimmten Wertebereichen zu arbeiten. Verwenden Sie diese, wenn Sie der Meinung sind, dass der Effekt zu breit ist.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbeingabe</i> |  |
| <b>Maskeneingabe</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Nur aktiv, wenn Maske auf &quot;Eingabe&quot; eingestellt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabetabelle</b> <i>False/True</i> | Behält optional die Kachelung an Kanten bei. |
| <b>Radius</b> <i>0.0 - 50.0</i> | Legt den Ausgleichsradius fest. Bei einem größeren Radius werden nur große Farbunterschiede entfernt. Dies erfordert Nachbearbeitung für jedes Bild. |
| <b>Helle/dunkle Balance</b> <i>0.0 - 1.0</i> | Bias, um dunklere Farbtöne zu entfernen. |
| <b>Benutzerdefinierte Farbvariation</b> <i>False/True</i> | Aktiviert die Möglichkeit, den Effekt in Richtung einer benutzerdefinierten Farbe zu variieren. |
| <b>Farbvariation</b> | Nur aktiv, wenn &quot;Benutzerdefinierte Farbvariation&quot; aktiviert ist. Mit den Einstellungen können Sie einen Farbtonversatz auswählen, zu dem die Entzerrung erfolgen soll. |
| <b>Farbton</b> <i>0.0 - 360.0</i> |  |
| <b>Chroma</b> <i>0.0 - 1.0</i> |  |
| <b>Luminanz</b> <i>0.0 - 1.0</i> |  |
| <b>Maskenquelle</b> <i>Keine, Bilddurchschnitt, Farbparameter, Eingabe</i> | Festlegen, ob eine Maskierung erfolgen soll. Der Farbparameter aktiviert die folgenden zusätzlichen Einstellungen, die Eingabe wechselt zu einer benutzerdefinierten Maskeneingabe. |
| <b>Maske</b> | Diese Option ist nur bei der Maskierung von Farbparametern aktiv. Zusätzliche Maskierungsparameter, um die Maske basierend auf dem Bild selbst zu bestimmen. Mit den folgenden Parametern können Sie einen Farbton präzise in eine Binärmaske konvertieren, auf die der Equalizer angewendet wird. Beachten Sie, dass die Effekte des Parameters &quot;Radius&quot; bei Verwendung dieser Einstellungen deutlich weniger ausgeprägt sein können. |
| <b>Farbe</b> <i>(Farbwert)</i> |  |
| <b>Farbtonbereich</b> <i>0.0 - 360.0</i> |  |
| <b>Chrominanzbereich</b> <i>0.0 - 1.0</i> |  |
| <b>Luminanzbereich</b> <i>0.0 - 1.0</i> |  |
| <b>Weichzeichnen</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |

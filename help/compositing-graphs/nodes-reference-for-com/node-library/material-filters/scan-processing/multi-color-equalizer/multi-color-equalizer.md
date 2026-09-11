---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Mehrere Color Equalizer", um die Farben über mehrere Texturkanäle hinweg auszugleichen und so eine konsistente Verarbeitung des gescannten Materials zu gewährleisten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrere Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# Mehrere Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multieingabeversion von [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Er gleicht Farbunterschiede aus und entfernt unerwünschte Farbtöne in einem vom Benutzer auswählbaren Maßstab. Es ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel zu Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie im ursprünglichen [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe 1-8</b> <i>Farbeingabe</i> | Mehrere Eingaben zur Verarbeitung. |
| <b>Maskeneingabe</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabeanzahl</b> <i>1 - 8</i> | Legt die Anzahl der parallel zu verarbeitenden Eingaben fest. |
| <b>Eingabetabelle</b> <i>False/True</i> | Behält optional die Kachelung an Kanten bei. |
| <b>Radius</b> <i>0.0 - 50.0</i> | Legt den Ausgleichsradius fest. Bei einem größeren Radius werden nur große Farbunterschiede entfernt. Dies erfordert Nachbearbeitung für jedes Bild. |
| <b>Helle/dunkle Balance</b> <i>0.0 - 1.0</i> | Bias, um dunklere Farbtöne zu entfernen. |
| <b>Benutzerdefinierte Farbvariation</b> <i>False/True</i> | Ermöglicht es Ihnen, den Effekt in Richtung einer benutzerdefinierten Farbe zu variieren. |
| <b>Farbvariation</b> | Nur aktiv, wenn &quot;Benutzerdefinierte Farbvariation&quot; aktiviert ist. Mit den Einstellungen können Sie einen Farbtonversatz auswählen, zu dem die Entzerrung erfolgen soll. |
| <b>Farbton</b> <i>0.0 - 360.0</i> |  |
| <b>Chroma</b> <i>0.0 - 1.0</i> |  |
| <b>Luminanz</b> <i>0.0 - 1.0</i> |  |
| <b>Maskenquelle</b> <i>Keine, Bilddurchschnitt, Farbparameter, Eingabe</i> | Legt fest, ob eine Maskierung erfolgen soll. Der Farbparameter aktiviert unten zusätzliche Einstellungen, die Eingabe wechselt zu einer benutzerdefinierten Maskeneingabe. |
| <b>Maske</b> | Nur aktiv mit Farbparameter-Maskierung. Enthält zusätzliche Maskierungsparameter, um die Maske basierend auf dem Bild selbst zu bestimmen. Mit den folgenden Parametern können Sie einen Farbton präzise in eine binäre Maske konvertieren, auf die die Entzerrung angewendet wird. Beachten Sie, dass die Effekte des Parameters &quot;Radius&quot; bei Verwendung dieser Einstellungen deutlich weniger ausgeprägt sein können. |
| <b>Farbe</b> <i>(Farbwert)</i> |  |
| <b>Farbtonbereich</b> <i>0.0 - 360.0</i> |  |
| <b>Chrominanzbereich</b> <i>0.0 - 1.0</i> |  |
| <b>Luminanzbereich</b> <i>0.0 - 1.0</i> |  |
| <b>Weichzeichnen</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Farbe in Maske , um bestimmte Farben in Masken zu konvertieren, um selektive Verarbeitungs- und Maskierungseffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbe zu maskieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# Farbe zu maskieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Farbe zu maskieren - Symbol](color-to-mask.resources/color_to_mask.png "Farbe zu maskieren - Symbol"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Extrahiert eine Graustufenmaske aus den ausgewählten Farben in einem Farbbild.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbe</i> | Das Eingabefarbbild, aus dem eine Maske basierend auf ihren Farben extrahiert werden soll. |
| <b>Farbeingabe</b> <i>Farbe</i>   *Verfügbar, wenn &quot;Farbeingabe verwenden&quot; auf &quot;Wahr&quot; festgelegt ist* | Das Eingabefarbbild, das zum Definieren der Referenzfarbe pro Pixel verwendet wird. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Die generierte Maske als Graustufen-Bitmap. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Farbeingabe verwenden</b> *Boolescher Wert* | Verwenden Sie ein Eingabebild anstelle einer einheitliche Farbe, um eine Referenzfarbe pro Pixel zu definieren.    Das Eingabebild wird von der <b>Farbeingabe</b> bereitgestellt. |
| <b>Farbe</b> *Fließkommazahl3* *Verfügbar, wenn &quot;Farbeingabe verwenden&quot; auf &quot;Falsch&quot; festgelegt ist* | Die Referenz-einheitliche Farbe, um die die Farbauswahl ausgeführt werden soll. |
| <b>Schwellenwert</b> *Gleitend* | Der Abstand zur Referenzfarbe, unter der die Farben ausgewählt sind. |
| <b>Auswahl-Verblassen</b> *Gleitend* | Verblassen der Farbauswahl anhand des Abstands zur Referenzfarbe. |
| <b>Entfernungsfarbraum</b> *Integer* | Beim Equalize-Prozess werden Farben verglichen, um den Abstand zwischen ihnen zu bestimmen. Bestimmte Farbräume und Abstandsalgorithmen sind für bestimmte Anwendungsfälle besser geeignet.   In dieser Dropdown-Liste können Sie den Farbraum auswählen, der zum Vergleichen der Farben verwendet wird:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB (Daten):</i></b> Die Farbe wird in Rot, Grün und Blau unterteilt und direkt entlang dieser Achse verteilt, wobei die menschliche Wahrnehmung ignoriert wird. Dies ist für Bilder mit Rohdaten geeignet.</li> <li data-preserve-html="true"><i>Linearer sRGB (Farbe):</i> Die Farbe wird in die Kanäle Rot, Grün und Blau aufgeteilt und linear zur Pixellichtintensität verteilt. Dies eignet sich für Bilder, die auf Displays visualisiert werden können.</li> <li data-preserve-html="true"><b><i>Luminanz (Farbe):</i></b> Die Farbe wird in Farbton-, Chrominanz- und Farbwerte aufgeteilt, wobei nur der Wert der Luminanz im Vergleich verwendet wird. Dies eignet sich für Bilder, die auf Displays visualisiert werden können.</li> <li data-preserve-html="true"><i>Labor (Color):</i> Ein standardisierter wahrnehmbarer Farbraum, der Farben so verteilt, dass Farben, die sich &quot;ähnlich&quot; fühlen, sich tatsächlich im Würfel befinden. Dies eignet sich für Bilder, die auf Displays visualisiert werden können.</li> <li data-preserve-html="true"><i>Winkel (Normal):</i> Die Farbe wird in die X-, Y- und Z-Achsen eines Vektors aufgeteilt und mit einem Punktprodukt verglichen. Dies eignet sich für Bilder, die &quot;Tangent-Leerzeichen-Normale&quot; enthalten.</li> </ul> |
| <b>Abstandsgewichte</b> *Float3* | Der Lab-Farbdistanz-Algorithmus (DeltaE2000) führt bestimmte Gewichtungsfaktoren für jeden Helligkeits-, Chroma- und Farbtonwert ein.   Niedrigere Werte verringern den Einfluss der Faktoren im Farbdifferenzalgorithmus.   Da das Auge in der Regel größere Unterschiede in der Helligkeit (L) akzeptiert als in Chroma (C) oder Farbton (H), ist das Standardverhältnis für (L:C:H) (0,5:1:1). Ein Verhältnis von 0,5:1:1 ermöglicht einen doppelt so großen Helligkeitsunterschied wie bei Chroma oder Farbton. |

## Beispiele

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

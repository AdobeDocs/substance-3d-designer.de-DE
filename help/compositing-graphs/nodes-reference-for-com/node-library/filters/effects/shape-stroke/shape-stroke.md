---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Formenkontur", um Konturen zu Formen hinzuzufügen, um Rahmen und Kanteneffekte zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Formenkontur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Formenkontur

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke.png){width="128px"}

![](shape-stroke.resources/shape-stroke-grayscale.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Fügt eine Kontur um eine Schwarz-weiße Maske (für die Graustufenversion) oder eine Form mit einem Alphakanal (für die Farbversion) hinzu, wie Sie es vielleicht aus anderen 2D-Bildbearbeitungsanwendungen kennen. Kann als vollständigere Version von [Edge Detect](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) angesehen werden.

Sehr nützlich für eine Vielzahl von Bildbearbeitungseffekten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Breite</b> <i>-1.0 - 1.0</i> | Breite des Kontureffekts. |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Globale Deckkraft des Effekts. |
| <b>(Konturfarbe) </b> <i>(Farbwert)</i> | Für den Kontureffekt verwendete Farbe. |
| <b>Maskenfarbe</b> <i>(Farbwert) (nur Graustufenversion)</i> | Volltonfarbe, die für die Ausgabe mit Transparenzzuordnung verwendet werden soll. |
| <b>Eingabe ist vormultipliziert</b> <i>False/True (nur Farbversion)</i> | Gibt an, ob die Eingabe als vormultipliziert angenommen werden soll. |
| <b>Ausgabe vormultiplizieren</b> <i>False/True</i> | Ob die Ausgabe vormultipliziert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shapestroke-ex.png" />
        </td>
    </tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Formenglühen", um Formen und Texturen Leuchteffekte hinzuzufügen, um helle und atmosphärische visuelle Effekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glühen in Formen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Glühen in Formen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-grayscale.png){width="128px"}

![](shape-glow.resources/shape-glow.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erstellt einen weichen Leuchteffekt um eine Eingabemaske (für die Graustufenversion) oder eine Form mit einem Alphakanal (für die Farbversion). Im Vergleich zu [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md) funktioniert dies in einer Weise, die der anderer 2D-Bildbearbeitungssoftware ähnlicher ist, da es ein umfassenderer Effekt mit mehr Steuerelementen ist.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Modus</b> <i>Weich, präzise</i> | Wechselt zwischen zwei Genauigkeitsmodi. |
| <b>Breite</b> <i>-1.0 - 1.0</i> | Steuert, wie weit der Schein reicht. |
| <b>Druckbogen</b> <i>0.0 - 1.0</i> | Schwellenwertabgrenzung für den Weichzeichnungseffekt, damit das Leuchten dicht an der Form fest erscheint. |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Fülldeckkraft für den Effekt &quot;Glühen&quot;. |
| <b>(Schatten) Farbe</b> <i>(Farbwert)</i> | Farbton, der auf den Schein angewendet werden soll. |
| <b>Maskenfarbe</b> <i>(Farbwert) (nur Graustufenversion)</i> | Volltonfarbe, die für die Ausgabe mit Transparenzzuordnung verwendet werden soll. |
| <b>Eingabe ist vormultipliziert</b> <i>False/True (nur Farbversion)</i> | Gibt an, ob die Eingabe als vormultipliziert angenommen werden soll. |
| <b>Ausgabe vormultiplizieren</b> <i>False/True</i> | Ob die Ausgabe vormultipliziert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shapeglow-ex.png" />
        </td>
    </tr>
</table>

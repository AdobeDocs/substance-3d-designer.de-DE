---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Shape-Schlagschatten", um den Formen Schlagschatteneffekte hinzuzufügen, um Tiefe und Dimension in Texturen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape-Schlagschatten
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Shape-Schlagschatten

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-dropshadow-grayscale.png){width="128px"}

![](shape-drop-shadow.resources/shape-dropshadow.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt den bekannten Effekt &quot;Schlagschatten&quot; anderer 2D-Bildverarbeitungssoftware auf einer Eingabe-Schwarzweiß-weiße Maske (für die Graustufenversion) oder einem Bild mit Transparenz (für die Farbversion) durch.

Er unterscheidet sich vom [Shadows](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md)-Effekt dadurch, dass er Bilder mit voller Transparenz zurückgibt, sodass ein vollständigerer Effekt erzielt wird, der dem ähnelt, was Sie in anderer Software erwarten würden.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Winkel</b> <i>0.0 - 1.0</i> | Einfallswinkel des (gefälschten) Lichts. |
| <b>Entfernung</b> <i>-0.5 - 0.5</i> | Entfernt den Schatten-Dropdown zur Form bzw. entfernt ihn davon. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Steuert die Unschärfe/Unschärfen des Schattens. |
| <b>Druckbogen</b> <i>0.0 - 1.0</i> | Schwellenwertabgrenzung für den Weichzeichnungseffekt, wodurch der Schatten weiter ausgebreitet wird. |
| <b>Deckkraft</b> <i>0.0 - 1.0</i> | Fülldeckkraft für den Schatteneffekt. |
| <b>(Schatten) Farbe</b> <i>(Farbwert)</i> | Farbton, der auf den Schatten angewendet werden soll. |
| <b>Maskenfarbe</b> <i>(Farbwert) (nur Graustufenversion)</i> | Volltonfarbe, die für die Ausgabe mit Transparenzzuordnung verwendet werden soll. |
| <b>Eingabe ist vormultipliziert</b> <i>False/True (nur Farbversion)</i> | Gibt an, ob die Eingabe als vormultipliziert angenommen werden soll. |
| <b>Ausgabe vormultiplizieren</b> <i>False/True</i> | Ob die Ausgabe vormultipliziert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/dropshadowex.png" />
        </td>
    </tr>
</table>

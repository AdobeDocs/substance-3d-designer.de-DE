---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Ziegel Generator, um prozedurale Ziegel-Muster mit anpassbaren Größen-, Offset- und Mörteleigenschaften zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ziegel-Generator
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# Ziegel-Generator

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erweiterter Ziegel-Mustergenerator. Verfügt über zahlreiche Optionen zum Generieren von selbst erstellten Ziegeln.

Weitere Optionen finden Sie unter [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ziegel</b> <i>1 - 64</i> | Legt die Anzahl der Ziegel in X- und Y-Achsen fest. |
| <b>Abgeflachte Kante</b> <i>0.0 - 1.0</i> | Ändert das Abschrägungsprofil für die Ziegel, ermöglicht es, in zwei Richtungen zu wechseln und Abstumpfprofil und Eckenrundung einzustellen. |
| <b>Verhältnis beibehalten</b> <i>False/True</i> | Legt fest, dass das abgeflachte Profil an die Größe des Ziegels gebunden ist. |
| <b>Lücke</b> <i>0.0 - 1.0</i> | Lücke zwischen den Ziegeln. Beachten Sie, dass durch die abgeflachte Kante auch eine Lücke entsteht. Wenn Sie also die abgeflachte Kante einstellen, müssen Sie diesen Parameter korrigieren. |
| <b>Mittlere Größe</b> <i>0.0 - 1.0</i> | Ziegel Pattern Offset, ändert die Größe aller anderen Spalten oder Zeilen. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Ändert Height profile. Ermöglicht die Einführung von Variation der Luminanz und aller Arten der Randomisierung. |
| <b>Steigung</b> <i>-1.0 - 1.0</i> | Führt eine Steigung pro Ziegel ein, als würden bestimmte Ziegel schräg liegen. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Versetzt Ziegel zeilenbasiert, wirkt sich auf den Abstand pro Zeile aus. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>

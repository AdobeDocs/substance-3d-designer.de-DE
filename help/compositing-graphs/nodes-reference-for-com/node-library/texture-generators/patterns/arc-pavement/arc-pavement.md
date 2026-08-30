---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Pflaster, um bogenförmige Pflastermuster zum Erstellen gekrümmter Texturen für Straßen und Pfade zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bogenpflaster
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# Bogenpflaster

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](arc-pavement.resources/arcpavement-ex.png)

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert ein Pariser Bogen-Straßenmuster. Dieser Effekt kann nicht mit dem Standardknoten &quot;[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)&quot; oder &quot;[Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)&quot; erzielt werden, daher dieser dedizierte Knoten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Skalierung</b> <i>1 - 8</i> | Legt die globale Skalierung/Kachelung fest. |
| <b>Mustermenge</b> <i>1 - 32</i> | Legt die Anzahl der Ziegel fest, die in jedem Bogen verwendet werden. |
| <b>Zufälliger Musterbetrag</b> <i>0.0 - 1.0</i> | Die Anzahl der Ziegel in jedem Bogen wird zufällig festgelegt. Nutzt zusätzlich den Effekt, dass Ziegeln verschiedene Maßstäbe zugewiesen werden. |
| <b>Mindestgröße des Musters</b> <i>1 - 10</i> | Steuert die Mindestanzahl an Ziegeln beim Zufallsgenerator von Bögen. |
| <b>Bogenbetrag</b> <i>0 - 20</i> | Legt die Stärke der vertikal gestapelten Bögen fest. Ändert das Height des Ziegels. |
| <b>Muster</b> <i>Eingabebild, Quadrat, Festplatte, Paraboloid, Bell, Gaußsch, Dorn, Pyramide, Ziegel, Abstufungen, Wellen, Halbglocke, Rändelglocke, Mondsichel, Kapsel, Kegel</i> | Wählt die zu verwendende Musterform aus. |
| <b>Filterungen des Eingabebilds</b> <i>Bilinear + Mipmaps, Bilinear, Nächste</i> |  |
| <b>Musterskalierung</b> <i>0.0 - 1.0</i> | Legt die Skalierung für jede Kachel fest. |
| <b>Musterbreite</b> <i>0.0 - 1.0</i> | Legt die Breite für jedes Teil fest. |
| <b>Pattern-Height</b> <i>0.0 - 1.0</i> | Legt das Height für jede Kachel fest. |
| <b>Musterbreite zufällig</b> <i>0.0 - 1.0</i> | Weist der Kachelbreite Zufallswerte zu. |
| <b>Muster-Height zufällig</b> <i>0.0 - 1.0</i> | Randomisiert Kachel-Height. |
| <b>Globale Musterbreite zufällig</b> <i>0.0 - 1.0</i> | Randomisiert die Kachelbreite, ohne größere Lücken zwischen den Kacheln zu erstellen. |
| <b>Pattern Height Verringern</b> <i>0.0 - 1.0</i> | Steuert das Ausstreichen des Heights an den Enden jedes Bogens. |
| <b>Farbzufall</b> <i>0.0 - 1.0</i> | Randomisiert Kachelfarben. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="arc-pavement.resources/arcpavement-ex.png" />
        </td>
    </tr>
</table>

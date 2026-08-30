---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "PBR-Rendering Mapping", um Material-Ausgaben in verschiedene PBR-Rendering-Zuordnungsformate zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR-Rendering Mapping
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# PBR-Rendering Mapping

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render-mapping.resources/pbr-render-mapping-color.png)![](pbr-render-mapping.resources/pbr-render-mapping-grayscale.png)

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Erweiterungsknoten für den [PBR-Rendering-Knoten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), mit dem Sie dem Shape eine separate Textur zuordnen können, die von einem vorherigen [PBR-Rendering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) abweicht. Das Hauptziel besteht darin, dass Sie jeden einzelnen Kanal von Ihrem [PBR-Rendering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) auf der Form neu zuordnen können, um wie in den folgenden Beispielen zusammengesetzte Aufschlüsselungen von Zuordnungskanälen zu erstellen. Sie können Ihre eigene Kompositionsmethode und Masken erstellen, indem Sie die PBR-Rendering-Zuordnungsknoten als Komponente verwenden.

Für die beiden Datentypen gibt es Farb- und Graustufenversionen: Farbe für Diffuse-Maps verwenden, Graustufen für Rauheit-, Metall- und andere Graustufenmaps verwenden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Struktur</b> <i>Farb-/Graustufeneingabe</i> | Textur, die der Form zugeordnet werden soll. |
| <b>UVs</b> <i>Farbeingabe</i> | Obligatorische UV-Dateneingabe von einem [PBR-Rendering-Knoten.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Legen Sie einen Farbflächenwert fest, der im Hintergrund verwendet werden soll. |

## Beispiele

Beispiel ist eine Komposition aus vier verschiedenen PBR-Rendering-Zuordnungsknoten, die eine [Histogrammauswahl](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) auf einem [linearen Verlauf](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) als  verwenden.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-ex.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-ex-2.png" />
        </td>
    </tr>
</table>

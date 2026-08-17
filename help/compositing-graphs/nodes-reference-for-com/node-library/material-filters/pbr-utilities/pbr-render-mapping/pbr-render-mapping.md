---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Verwenden Sie den PBR-Rendering-Zuordnungsknoten, um Materialausgaben in verschiedene PBR-Rendering-Zuordnungsformate zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR-Rendering Mapping
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# PBR-Rendering Mapping

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## PBR-Rendering-Zuordnung (Farbe/Graustufen)

**In:** *Materialfilter/PBR-Dienstprogramme*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Erweiterungsknoten für den [PBR-Rendering-Knoten](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), mit dem Sie der Form eine separate Textur aus einem vorherigen [PBR-Rendering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) zuordnen können. Das Hauptziel besteht darin, dass Sie jeden einzelnen Kanal von Ihrem [PBR-Rendering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) auf der Form neu zuordnen können, um wie in den folgenden Beispielen zusammengesetzte Aufschlüsselungen von Zuordnungskanälen zu erstellen. Sie können Ihre eigene Kompositionsmethode und Masken erstellen, indem Sie die PBR-Rendering-Zuordnungsknoten als Komponente verwenden.

Für die beiden Datentypen gibt es Farb- und Graustufenversionen: Farbe für diffuse Karten verwenden, Graustufen für Raueit verwenden, Metall- und andere Graustufenkarten.

### Eingaben

* **Struktur**: *Farb-/Graustufeneingabe*\
  Textur, die einer Form zugeordnet werden soll.
* **UVs**: *Farbeingabe* Obligatorische UV-Dateneingabe von einem [PBR-Rendering-Knoten.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## Parameter

* **Hintergrundfarbe**: *(Farbwert)*Legen Sie einen Farbflächenwert fest, der im Hintergrund verwendet werden soll.

## Beispielbilder

Beispiel ist eine Komposition aus vier verschiedenen PBR-Rendering-Zuordnungsknoten, die eine [Histogrammauswahl](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) auf einem [linearen Verlauf](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) als  verwenden.

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>

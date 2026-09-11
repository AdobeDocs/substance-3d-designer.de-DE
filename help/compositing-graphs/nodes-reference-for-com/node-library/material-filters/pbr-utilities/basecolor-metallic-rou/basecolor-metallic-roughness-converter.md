---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten BaseColor Metallische Rauheit Converter, um zwischen verschiedenen PBR-Material-Formaten und Workflows zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BaseColor-Metallische Rauheit-Konverter
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# BaseColor / Metallic / Rauheit Konverter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/pbr-convert.png){width="128px"}

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten konvertiert Grundfarben-, Metallic und Rauheit-Maps in verschiedene PBR-Modellausgaben, z. B. Specular/Glanz-Modell. Einige der enthaltenen Ausgabeziele sind bekannte Render-Engine wie Vray, Corona, Redshift, Renderman und Arnold.

Dies ist nützlich, wenn Sie Graf oder Materialien haben, die mit einem PBR-Modell erstellt wurden, während für Ihr Ziel ein anderes Modell erforderlich ist.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>SpecularLevel-Eingabe verwenden</b> <i>False/True</i> | Legt einen zusätzlichen Eingangssteckplatz für den SpecularLevel-Eingang. Dies wird auch bei der Konvertierung berücksichtigt. |
| <b>Ziel</b> <i>PBR Diffuse/Specular/Gloss, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)</i> | Legt das Konvertierungszielmodell fest. |

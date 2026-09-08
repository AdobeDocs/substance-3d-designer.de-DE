---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Materialkorrektur-Überblendung , um Materialkorrekturen zwischen Materialien zu überblenden und Composite-Effekte zu optimieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialanpassungsüberblendung
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Materialanpassungsüberblendung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

<b>In:</b> Materialfilter > Mischen

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ermöglicht die Anpassung aller Kanäle eines Vollmaterials auf Basis einer Maske. Sie soll einen vollständigen Material-Workflow einfacher und schneller machen.

Dies ist nützlich, wenn Sie einige Kanäle eines Materials anpassen möchten (z. B. diffuses Licht und Raueit dunkler machen), die auf derselben Maske basieren.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Farb-ID-Maske</b> <i>Farbeingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Graustufenmaske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schaltet Material-Kanäle in dieser Gruppe ein und aus, z. B. wenn Specular/Glanz-Maps anstelle von Metallic/Rauheit verwendet werden.<br><br>Dies aktiviert und deaktiviert auch das Erscheinungsbild der entsprechenden Gruppen des Kanals. |
| <b>Diffus</b> | Führt Korrekturvorgänge für den Diffuse-Kanal in Bereichen durch, die durch die Maske definiert sind. |
| <b>Grundfarbe</b> | Führt Korrekturvorgänge für den Kanal &quot;Grundfarbe&quot; in Bereichen durch, die durch die Maske definiert sind. |
| <b>Normal</b> |  |
| <b>Intensität</b> <i>0.0 - 1.0</i> | Tönt die normale Intensität ab |
| <b>Specular</b> | Führt Korrekturvorgänge für den Specular-Kanal in Bereichen durch, die durch die Maske definiert sind. |
| <b>Ausstrahlend</b> | Führt Anpassungsvorgänge auf dem Emissionskanal in Bereichen durch, die durch die Maske definiert werden. |
| <b>Glossarität</b> | Führt Korrekturvorgänge für den Maskenkanal in den von der Glanz definierten Bereichen durch. |
| <b>Raueit</b> | Führt Korrekturvorgänge für den Maskenkanal in den von der Rauheit definierten Bereichen durch. |
| <b>Metallisch</b> | Führt Korrekturvorgänge im Metallic Kanal in Bereichen durch, die durch die Maske definiert sind. |
| <b>Specular level</b> | Führt Korrekturoperationen auf dem Specular level-Kanal in Bereichen durch, die durch die Maske definiert werden. |
| <b>Umgebungs-Verdeckung</b> | Führt Korrekturoperationen auf dem Ambient occlusion-Kanal in Bereichen durch, die durch die Maske definiert werden. |
| <b>Height</b> | Führt Korrekturvorgänge für den Height-Kanal in den von der Maske definierten Bereichen durch. |
| <b>Deckkraft</b> | Führt Korrekturvorgänge für den Kanal &quot;Deckkraft&quot; in den von der Maske definierten Bereichen durch. |
| <b>Farb-ID-Maske</b> <i>False/True</i> | Farb-ID-Maske anstelle der Graustufenmaske verwenden. |
| <b>Unschärfe</b> <i>0.01 - 1.0</i> | Wenn Farb-ID-Maske aktiviert ist, wird hierdurch der Druckbogen der Farb-ID-Auswahlfarbe bestimmt. |
| <b>Farbe</b> <i>(Farbwert)</i> | Legt fest, welche Farbe auf dem ID-Map ausgewählt und maskiert werden soll. |
| <b>Auffüllen</b> <i>0.0 - 1.0</i> | Bestimmt den Mischkontrast/die Übergänge der Farb-ID-Maskierung. |

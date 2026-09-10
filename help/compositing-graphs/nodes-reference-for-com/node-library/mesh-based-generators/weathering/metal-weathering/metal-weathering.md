---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Metal Weathering", um metallischen Werkstoffen auf Basis der Gittergeometrie realistische Rost- und Korrosionseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metallverwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# Metallverwitterung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Verwitterung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normaler WS</b> <i>Farbeingabe</i> | Baked World Space Normalmap wird für interne Effekte und Maskierung verwendet. |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Erweitert</b> |  |
| <b>Normales Format</b> <i>Direct X, Open GL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Maske</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |
| <b>Effekt</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Schmutzigkeit</b> <i>0.0 - 1.0</i> |  |
| <b>Kanten, die </b> tragen <i>0.0 - 1.0</i> |  |
| <b>Malen Peeling</b> <i>0.0 - 1.0</i> |  |
| <b>Rost</b> <i>0.0 - 1.0</i> |  |
| <b>Rost-Peeling</b> <i>0.0 - 1.0</i> |  |
| <b>Rost Verdigris</b> <i>Rost, Verdigris</i> |  |
| <b>Skalierung von Malen-Rissen</b> <i>1.0 - 16.0</i> |  |
| <b>Verkrümmungsintensität der Malen-Risse</b> <i>0.0 - 1.0</i> |  |
| <b>Scratches mit scharfen Kanten skalieren</b> <i>1.0 - 32.0</i> |  |
| <b>Intensität der Verkrümmung der scharfen Kanten der Scratches</b> <i>0.0 - 1.0</i> |  |
| <b>Rohmetallfarbe</b> <i>(Farbwert)</i> |  |
| <b>Specular-Rohmetallfarbe</b> <i>(Farbwert)</i> |  |
| <b>Wert des Raw Metal-Glanzes</b> <i>(Graustufenwert)</i> |  |
| <b>Wert für die Rauheit von Rohmetallen</b> <i>(Graustufenwert)</i> |  |
| <b>Überblenden</b> |  |
| <b>Diffuse-Intensität</b> <i>0.0 - 1.0</i> | Mischungsstärke des Diffusors. |
| <b>Intensität der Grundfarbe</b> <i>0.0 - 1.0</i> | Mischungsstärke der Grundfarbe. |
| <b>Normalintensität</b> <i>0.0 - 64.0</i> | Die Füllkraft von &quot;Normal&quot;. |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Speculars. |
| <b>Glanz-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Glanzes beim Mischen. |
| <b>Intensität der Rauheit</b> <i>0.0 - 1.0</i> | Die Stärke der Raueit. |
| <b>Metallic Intensität</b> <i>0.0 - 1.0</i> | Mischfestigkeit des Metallic. |
| <b>Ambient occlusion-Intensität</b> <i>0.0 - 1.0</i> | Mischfestigkeit der Ambient-Verdeckung. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Heights beim Mischen. |

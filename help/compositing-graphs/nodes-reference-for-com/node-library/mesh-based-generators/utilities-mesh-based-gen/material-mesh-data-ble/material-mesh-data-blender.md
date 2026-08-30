---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Verwenden Sie den Material Mesh Data Blender-Mesh, um Material-Überblendungsknoten für fließende Übergänge zwischen verschiedenen Material-Zonen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Mesh Data Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# Material Mesh Data Blender

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten soll das Hinzufügen von Details basierend auf Baking geführt Daten erheblich erleichtern. Es verfügt über viele Schieberegler, um ein vollständiges Material für den Input zu ändern, das auf allen durch Baking erzeugte Map als Input basiert. Experimentieren Sie doch einmal damit, denn es gibt viele Möglichkeiten.

Es ist hilfreich, wenn Sie z. B. Kantenhervorhebung auf Basis einer Krümmung oder anderer Maps hinzufügen, AO-Elemente mit der Diffuse/Grundfarbe mischen, Specular-Verdeckung auf Basis der Krümmung und/oder AO hinzufügen usw.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Vollständige Material-Eingabe (Gruppe &quot;Material&quot;)</b> | Alle Materialien-Maps.<br><br>Diese werden von diesem Knoten geändert und dann erneut als Ausgabe zurückgegeben. |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Height</b> <i>Graustufen-Eingabe</i> |  |
| <b>Normal</b> <i>Farbeingabe</i> |  |
| <b>Farbe des Scheitelpunkts</b> <i>Farbeingabe</i> |  |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. Wirkt sich auf die Verfügbarkeit der folgenden Parameter aus. |
| <b>Durch Baking erzeugte Map</b> | Gibt an, ob die aufgelisteten durch Baking erzeugte Map für Berechnungen verwendet werden. Wirkt sich auf die Verfügbarkeit der folgenden Parameter aus. |
| <b>Diffusen AO</b> <i>0.0 - 1.0</i> | Die Menge an Ambient occlusion, die in die Diffuse eingepasst werden soll. |
| <b>Scharfe Kanten der Diffuse</b> <i>0.0 - 1.0</i> | Stärke der Krümmungsmatrix, die in den Diffuse-Effekt überblendet werden soll. |
| <b>Diffuse aus Scheitelpunkt-Farbe</b> <i>0.0 - 1.0</i> | Stärke der Scheitelpunktfarbe, die mit dem Diffus-Effekt überblendet werden soll. |
| <b>Diffuse-Vorbeleuchtung</b> <i>0.0 - 1.0</i> | Anzahl der (gefälschten) Vorbeleuchtung, basierend auf den World Space Normale. |
| <b>Diffuse Cartoon-Beleuchtungsbilanz</b> <i>0.0 - 1.0</i> | Verschiebt für das Diffuse zwischen realistischer und Cartoon-Beleuchtung. |
| <b>Diffuse-Cartoon-Pre-Lighting-Ebenen</b> <i>0 - 10</i> | Steuert den Look der cartoonartigen Beleuchtungsberechnungen. |
| <b>Diffusen Cartoon-Konturen</b> <i>0.0 - 1.0</i> | Steuert den Look der cartoonartigen Beleuchtungsberechnungen. |
| <b>Grundfarbe AO</b> <i>0.0 - 1.0</i> | Die Menge der Umgebungsfarbe, die in die Grundfarbe übergegangen werden soll. |
| <b>Grundfarbe Scharfe Kanten</b> <i>0.0 - 1.0</i> | Stärke der Krümmungszuordnung, die in die Grundfarbe übergegangen werden soll. |
| <b>Grundfarbe aus Scheitelpunkt-Farbe</b> <i>0.0 - 1.0</i> | Stärke der Scheitelpunktfarbe, die mit der Grundfarbe überblendet werden soll |
| <b>Normalintensität des Materials</b> <i>0.0 - 1.0</i> | Füllkraft der eingebrannten (Tangenten-)Normalmap. |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | Mischungsstärke des AO im Specular. |
| <b>Specular Hell scharfe Kanten</b> <i>0.0 - 1.0</i> | Die Stärke der Krümmung im Specular vermischen. |
| <b>Specular-Zeichentrickkonturen</b> <i>0.0 - 1.0</i> | Stärke eines Comic-Specular-Kanteneffekts beim Mischen auf Basis der Krümmung |
| <b>Glanz dunkelscharfe Kanten</b> <i>0.0 - 1.0</i> | Stärke der Krümmung im Glanz. |
| <b>Rauheit helle scharfe Kanten</b> <i>0.0 - 1.0</i> | Stärke der Krümmung in der Rauheit. |
| <b>Rauheit Cartoon-Konturen</b> <i>0.0 - 1.0</i> | Stärke eines Comic-Effekts &quot;Rauheit, Kante und Kontur&quot;, basierend auf der Krümmung |
| <b>Metallic scharfe Kanten</b> <i>0.0 - 1.0</i> | Die Stärke der Krümmung im Metallic. |
| <b>Metallic Cartoon-Konturen</b> <i>0.0 - 1.0</i> | Stärke eines Comic-Effekts mit Metallic Kante und Kontur, basierend auf der Krümmung. |
| <b>AO Materialintensität</b> <i>0.0 - 1.0</i> | Überblendung-Stärke von durch Baking erzeugte Map AO mit Material-generiertem AO, welcher Grad die Kombination beider AO-Maps ist. |
| <b>Intensität des Height-Materials</b> <i>0.0 - 1.0</i> | Überblendung Stärke von durch Baking erzeugte Map Height mit Material-generierten Height, welcher Grad beide Höhenkarten zu kombinieren. |
| <b>Height Material-Füllmethode </b> <i>Verstärkung, Interpolation</i> | Überblendung-Modus zum Kombinieren beider Höhenzuordnungen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/blenddata-ex.gif" />
        </td>
    </tr>
</table>

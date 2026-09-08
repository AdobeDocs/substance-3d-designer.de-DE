---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Leder-Verwitterung", um Ledermaterialien auf der Grundlage einer Gitterkrümmung Verschleißmuster und Alterungseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lederwetter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 9%

---


# Lederwetter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Verwitterung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Vollmaterial-Effekt, der auf mehreren Kanälen gleichzeitig funktioniert. Es fügt einen zufälligen Lederverschleißeffekt hinzu, mit Kontrolle für Alter und Schmutzigkeit. Es ähnelt [Fabric Weathering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), wurde aber speziell auf Leder abgestimmt.<br>Dieser Effekt funktioniert nur dann sehr gut, wenn Sie über die richtigen Baking geführt AO- und Welt-Raum-Normalmaps verfügen, da diese benötigt werden, um alles entsprechend zu berechnen und zu generieren.

Vergewissern Sie sich, dass Sie die [Link Creation Modes](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) vollständig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> |  |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Erweitert</b> |  |
| <b>Normales Format</b> <i>DirectX, OpenGL</i> | Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal). |
| <b>Maske</b> <i>False/True</i> | Schaltet die Verwendung der Maskenkarte ein oder aus. |
| <b>Effekt</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | Überblendungen mit dunklerer Dust, basierend auf den Bereichen, die in der Normalmap des Welt-Raums nach oben zeigen. |
| <b>Schmutzigkeit</b> <i>0.0 - 1.0</i> | Überblendungen mit globalem Dirt-/Verwischungseffekt, hauptsächlich aufgrund von verdeckten (dunklen) Bereichen in der AO. |
| <b>Kanten, die </b> tragen <i>0.0 - 1.0</i> | Fügt einen Scharfzeichner-/Verstärkereffekt für Kanten hinzu, der auf dem Material &quot;Normal&quot; basiert. |
| <b>Verwendet</b> <i>0.0 - 1.0</i> | Überblendungen in einem globalen Leder-Look. |
| <b>Alter</b> <i>0.0 - 1.0</i> | Überblendungen in einem abgenutzten Lederlook in Falten auf AO-Basis. Die Platzierung wird stark von Age Treshold beeinflusst. |
| <b>Altersschwellenwert</b> <i>0.0 - 1.0</i> | Legt den Aussehen-Schwellenwert für den Effekt &quot;Alter&quot; fest. |
| <b>Skalierung der Risse</b> <i>1.0 - 16.0</i> | Legt die Tiefe des abgenutzten Leders von Used and Age fest. |
| <b>Risse-Verkrümmungsintensität</b> <i>0.0 - 1.0</i> | Legt die Intensität des abgenutzten Leders von &quot;Verwendet&quot; und &quot;Alter&quot; fest. |
| <b>Scratches mit scharfen Kanten skalieren</b> <i>1.0 - 32.0</i> |  |
| <b>Intensität der Verkrümmung der scharfen Kanten der Scratches</b> <i>0.0 - 1.0</i> |  |
| <b>Verwendete Lederentsättigung</b> <i>0.0 - 1.0</i> | Legt die Sättigung des abgenutzten Lederlooks von den Effekten &quot;Alt&quot; und &quot;Verwendet&quot; fest. |
| <b>Verwendete Lederhelligkeit</b> <i>0.0 - 1.0</i> | Legt die Helligkeit des abgenutzten Leder-Looks von den Effekten &quot;Alt&quot; und &quot;Verwendet&quot; fest. |
| <b>Überblenden</b> |  |
| <b>Diffuse-Intensität</b> <i>0.0 - 1.0</i> | Mischungsstärke des Diffusors. |
| <b>Intensität der Grundfarbe</b> <i>0.0 - 1.0</i> | Mischungsstärke der Grundfarbe. |
| <b>Normalintensität</b> <i>0.0 - 1.0</i> | Die Füllkraft von &quot;Normal&quot;. |
| <b>Specular-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Speculars. |
| <b>Glanz-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Glanzes beim Mischen. |
| <b>Intensität der Rauheit</b> <i>0.0 - 1.0</i> | Die Stärke der Raueit. |
| <b>Ambient occlusion-Intensität</b> <i>0.0 - 1.0</i> | Mischfestigkeit der Ambient-Verdeckung. |
| <b>Height-Intensität</b> <i>0.0 - 1.0</i> | Die Stärke des Heights beim Mischen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex2.png" />
        </td>
    </tr>
</table>

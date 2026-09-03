---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Edge Wear "Metall", um auf Grundlage der Krümmung und der Position des Gitters Verschleißmasken an den Kanten des Metalls zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metal-Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# Metal-Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear-01.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske repräsentiert den Kantenverschleiß an einem Metallobjekt, wobei Kratzer und Späne an konvex erhöhten Kanten erscheinen, die möglicherweise durch gebackene dunkle AO-Bereiche maskiert werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Schmutz-Eingabe</b> <i>Graustufen-Eingabe</i> |  |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> |  |
| <b>Position</b> <i>Farbeingabe</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Verschleißstufe</b> <i>0.0 - 1.0</i> | Stellt die Gesamtverschleißmenge ein, die allmählich sichtbar wird. |
| <b>Kontrast tragen</b> <i>0.0 - 1.0</i> | Legt den Kontrast des Endergebnisses fest. |
| <b>Kanten Smoothness</b> <i>0.0 - 16.0</i> | Legt die Smoothness des Abfalls von den Kanten der Krümmung fest. |
| <b>Schmutz-Betrag</b> <i>0.0 - 1.0</i> | Legt den Schmutz fest, der zwischen den Kanten verblendet werden soll. |
| <b>Schmutz-Skalierung</b> <i>1 - 16</i> | Legt die Skalierung des Schmutzes fest. |
| <b>Ambient occlusion-Maskierung</b> <i>0.0 - 1.0</i> | Legt die Stärke des Effekts fest, den AO auf den endgültigen Effekt ausübt, wobei dunkle Bereiche ausgeblendet werden. |
| <b>Krümmung Weight</b> <i>0.0 - 1.0</i> | Legt den Umfang des Effekts fest, den die konvexen Kanten der Krümmung auf den endgültigen Effekt haben. |
| <b>Benutzerdefinierten Schmutz verwenden</b> <i>False/True</i> | Aktiviert einen benutzerdefinierten Schmutz-Map-Eingangssteckplatz. |
| <b>Triplanar verwenden</b> <i>False/True</i> | Aktivieren Sie die [Planare ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)-Projektion, um Nähte auszublenden. |
| <b>Triplanarer Mischkontrast</b> <i>0.0 - 1.0</i> | Legt den Mischkontrast für die Triplanare Projektion fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-02.gif" />
        </td>
    </tr>
</table>

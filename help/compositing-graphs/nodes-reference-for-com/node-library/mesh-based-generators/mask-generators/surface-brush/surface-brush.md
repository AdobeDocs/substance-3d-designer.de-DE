---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Oberflächenpinsel", um Masken basierend auf der Oberflächenausrichtung zu generieren, um gerichtete Verwitterungs- und Abnutzungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oberflächenpinsel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---


# Oberflächenpinsel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt einen interessanten Effekt des Metallpinselns auf eine Objektoberfläche dar, verdeckt von Objektgeometrie und AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> |  |
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für interne Effekte und Maskierung. |
| <b>Position</b> <i>Graustufen-Eingabe</i> |  |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Ebene</b> <i>0.0 - 1.0</i> | Legt die globale Effektstufe fest, die allmählich sichtbar wird. |
| <b>Kontrast</b> <i>0.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Scratches Länge</b> <i>0.0 - 8.0</i> | Legt die Länge von Kratzern fest. Kleinere Werte sind mehr wie Punkte, höhere Werte sind lange Streifen. |
| <b>Achse verschließen</b> <i>X, Y, Z, keine</i> | Achse des Objekts, das Kratzer erhalten soll. Ändert nicht die Richtung der Kratzer. |
| <b>Intensität der Achse ausschließen</b> <i>0.0 - 1.0</i> | Stärke des Effekts &quot;Verdeckung der Achse&quot;. |
| <b>Verdeckung</b> <i>0.0 - 1.0</i> | Stärke der AO auf verdeckenden Kratzern. |
| <b>Intensität schärfen</b> <i>0.0 - 1.0</i> | Legen Sie den Grad der Nachschärfung fest, der auf die Kratzer angewendet werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-ex.gif" />
        </td>
    </tr>
</table>

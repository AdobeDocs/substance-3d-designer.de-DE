---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Edge Wear "Glasfaserknoten", um Verschleißmasken auf Glasfaserkanten basierend auf der Gitterkrümmung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glasfaser-Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# Glasfaser-Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear.png){width="128px"}

<b>In:</b> Mesh-basierte Generatoren > Maskengenerator

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Stellt eine Maske dar, die speziell für einen Fiberglas-Verschleiß bestimmt ist, der möglicherweise für Tuch verwendet werden könnte. Durch die sehr geflieste, sich wiederholende Art der Fasern kann die Triplanar-Vermischung optional aktiviert werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Krümmung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map für die Kantenhervorhebung. Erforderlich! |
| <b>Umgebungs-Verdeckung</b> <i>Graustufen-Eingabe</i> | Durch Baking erzeugte Map zum Maskieren von verdeckten Bereichen. Nicht erforderlich, aber definitiv empfehlenswert. |
| <b>Schmutz-Eingabe</b> <i>Graustufen-Eingabe</i> | Optionaler benutzerdefinierter Steckplatz zum Überschreiben des Fasermusters. |
| <b>Maske (optional)</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Normaler Weltraum</b> <i>Farbeingabe</i> | Nur für Triplanar verwendet. |
| <b>Position</b> <i>Farbeingabe</i> | Nur für Triplanar verwendet. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Verschleißstufe</b> <i>0.0 - 1.0</i> | Wie bei einem [Histogrammscan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) wird der Verschleiß progressiv aufgedeckt. |
| <b>Kontrast tragen</b> <i>0.0 - 1.0</i> | Legt den Gesamteffektkontrast fest. |
| <b>Kanten Smoothness</b> <i>0.0 - 16.0</i> | Legt den Anschnitt bzw. die Weichzeichnung von hervorgehobenen Kanten fest. |
| <b>Schmutz-Betrag</b> <i>0.0 - 1.0</i> | Legt fest, wie viel des Fasereffekts zwischen den Rändern verblendet werden soll. Mit dem Wear Level kannst du das zusammen optimieren, um maximale Kontrolle zu erhalten. |
| <b>Ambient occlusion-Maskierung</b> <i>0.0 - 1.0</i> | Legt den Einfluss fest, den AO auf das Ausblenden des Effekts hat. |
| <b>Krümmung Weight</b> <i>0.0 - 1.0</i> | Legt den Einflussbetrag fest, den konvexe Kanten aus der Krümmung haben. |
| <b>Benutzerdefinierten Schmutz verwenden</b> <i>False/True</i> | Überschreibt integrierte Fasern mit benutzerdefinierter Karte. |
| <b>Triplanar verwenden</b> <i>False/True</i> | Aktiviert [Tri Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md), um Nähte auszublenden. |
| <b>Triplanarer Mischkontrast</b> <i>0.0 - 1.0</i> | Steuert den Kontrast des Triplanar-Effekts. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-ex.gif" />
        </td>
    </tr>
</table>

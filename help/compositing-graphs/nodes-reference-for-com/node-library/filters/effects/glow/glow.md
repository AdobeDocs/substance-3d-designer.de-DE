---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Glühen", um Texturen Leuchteffekte hinzuzufügen, um helle und emittierende Materialerscheinungen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glühen
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# Glühen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

<b>In:</b> Filters > Effects

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Führt einen Effekt vom Typ &quot;Schein nach außen&quot; aus, wie man ihn in anderen gängigen Bildbearbeitungsprogrammen sieht. Fügt im Wesentlichen eine verblassende Verlaufskontur um die Eingabe hinzu.

Beachten Sie, dass dies nicht für Bilder mit Alpha-Kanälen geeignet ist, wie Sie vielleicht erwarten. Selbst die Farbversion erwartet nur binäre, schwarz-weiße Masken als Eingabe. es erlaubt nur einen farbigen Schein zu verwenden. Wenn Sie nach einer Version suchen, die für Bilder mit Transparenz funktioniert, finden Sie weitere Informationen unter [Formenglühen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Wichtig: Achten Sie darauf, die passende Version für Ihre Eingabe zu verwenden! Verwenden Sie &quot;Glühen&quot; für Farbeingaben bzw. &quot;Graustufen glühen&quot; für Graustufeneingaben.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Glühstärke</b> <i>0.0 - 1.0</i> | Globale Deckkraft für den Effekt &quot;Glühen&quot;. |
| <b>Betrag löschen</b> <i>0.0 - 1.0</i> | Schwellenwert, um festzulegen, wann der Leuchteffekt abgeschnitten werden soll. Nützlich für halbtransparente Bereiche. |
| <b>Leuchtgröße</b> <i>0.0 - 20.0</i> | Steuert, wie weit der Leuchteffekt reicht. |
| <b>Leuchtfarbe</b> <i>(Farbwert) (Nur Farbversion)</i> | Legt die Farbe des Leuchteffekts fest. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/glow-ex.png" />
        </td>
    </tr>
</table>

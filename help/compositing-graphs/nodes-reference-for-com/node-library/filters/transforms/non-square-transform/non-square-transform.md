---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Nicht-quadratische Transformation", um nicht-quadratische Texturen mit unabhängiger X- und Y-Skalierung zu transformieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformieren ohne Quadrat
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# Transformieren ohne Quadrat

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Nicht quadratsichere Version von [2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) transformieren. Erkennt automatisch nicht quadratische Seitenverhältnisse und kann quadratische Eingabebilder auf eine nicht quadratische Arbeitsfläche transformieren.

Vergewissern Sie sich, dass Sie die [Graph-Parameter](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) vollständig verstehen, um diesen Knoten optimal zu nutzen, da Sie einige Einstellungen richtig festlegen müssen:

* Ihre **Graph**-Größe sollte nicht quadratisch sein, andernfalls ist dieser Knoten nicht erforderlich.
* Legen Sie die **-Ausgabegröße des Knotens &quot;**&quot; als &quot;Nicht quadratisch transformieren&quot; auf &quot;*Relativ zu übergeordneten Knoten*&quot; fest.
* Setzen Sie den **Kachelmodus des Knotens** auf &quot;*Keine Kachelung*&quot;, wenn Sie Ihre Eingabe nur in eine einzelne Position umwandeln möchten.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kachelmodus</b> <i>Automatisch, Manuell</i> | Aktivieren Sie automatische nichtquadratische Kompensationen oder nicht. |
| <b>Kachel</b> <i>1 - 16</i> | Nur verfügbar, wenn der Kachelmodus auf &quot;Manuell&quot; eingestellt ist. Ermöglicht das Ändern der Skalierung kachelsicher. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder verschiebt das Ergebnis. Doppelklicken Sie auf den Regler, um negative Werte einzugeben. |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Dreht das Eingabebild. |
| <b>Sichere Drehung (nur Quadrat)</b> <i>False/True</i> | Einrasten sicheren Werten bei, um die Schärfe der Pixel beizubehalten. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Hintergrundfarbe zum Füllen des Bildes. Nur sichtbar, wenn der [Kachelmodus in Basisparametern auf &quot;*Keine Kachelung*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) festgelegt ist. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonsquare-ex.png" />
        </td>
    </tr>
</table>

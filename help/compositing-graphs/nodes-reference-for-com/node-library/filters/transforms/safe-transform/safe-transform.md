---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Sicherer Transformieren", um Transformationen anzuwenden und dabei die Grenzen der Textur beizubehalten und Artefakte zu vermeiden.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sicheres Transformieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# Sicheres Transformieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform.png)

![](safe-transform.resources/safe-transform-grayscale.png)

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Für die Kachelung sichere Version von [2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) Transformieren. Ermöglicht Skalierung, Drehung und Versatz ohne Unterbrechung der Kachelung und ohne Verlust von Pixeldetails (Verlust von Genauigkeit/Schärfe) aufgrund kleiner Versätze und Drehungen.

Diese Option ist nützlich, um Rauschen transformieren, wenn maximale Kontrolle oder perfekte Schärfe erforderlich ist.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kachel</b> <i>1 - 16</i> | Verkleinert die Eingabe um die Kachelung. |
| <b>Offset-Modus</b> <i>Manuell, Zufällig</i> | Wechselt zu einem zufälligen Versatz anstelle eines manuell definierten. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder verschiebt das Ergebnis. Stellt sicher, dass die Pixel einrasten und nicht interpoliert sind. |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Dreht die Eingabe um einen Winkel. |
| <b>Sichere Drehung in Kacheln</b> <i>False/True</i> | Legt das Drehverhalten fest. Es gibt an, ob Werte einrasten werden sollen, bei denen keine Pixelfehler verschwinden. |
| <b>Symmetrie</b> <i>keine, X, Y, X+Y</i> |  |
| <b>Hintergrundfarbe</b> <i>(Farbwert) (Nur Farbversion)</i> |  |
| <b>Mipmap-Modus</b> <i>Automatisch, Manuell</i> | Bestimmt den Mipmapping-Modus. Die Einstellung auf Manuell führt zu schärferen Ergebnissen. |
| <b>Mipmap-Stufe</b> <i>0 - 10</i> | Wenn der Mipmap-Modus auf &quot;Manuell&quot; eingestellt ist, können Sie ein anderes Mipmap auswählen. |

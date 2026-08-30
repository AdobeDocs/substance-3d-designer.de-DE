---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Mit dem Filterknoten "Klon" können Sie Bereiche von Texturen duplizieren und versetzen, um nahtlose Muster und Effekte auf Kachelungen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Klonen (Filterknoten)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# Klonen (Filterknoten)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>In:</b> Filter > Transformieren

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Klons-Eingabebild einmal an einen bestimmten Speicherort. Kann als primitives Werkzeug zum &quot;Klonstempel&quot; fungieren.

Sorgfältig, um die gewünschten Ergebnisse zu erzielen:

* Idealerweise hat das Eingabebild einen Alphakanal (wie ein Aufkleber), da das Mischen nur eine gerade Kopie ist.
* Die Maske ist standardmäßig schwarz, sodass für alle Ergebnisse ein einheitlicher Graustufenwert für Weiß mindestens angeschlossen werden muss.
* Der Offset wird außerhalb des Bildes abgeschnitten, verwende also kleine Werte.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Quelle</b> <i>Farbeingabe</i> | Zu klonendes Bild. Wichtig: Idealerweise hat das Bild einen Alphakanal! |
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Standardmäßig ist es schwarz. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Offset</b> <i>-</i> | Verschiebt oder verschiebt das Ergebnis. &quot;Positiv&quot; steht für &quot;Links und oben&quot;, &quot;Negativ&quot; für &quot;Rechts und unten&quot;. Verwenden Sie kleine Werte, 1,0 und höher, um sie aus dem Bild zu verschieben! |
| <b>Weichzeichnungsmaske</b> <i>0.0 - 10.0</i> | Wende einen Weichzeichnungsfilter auf eine Maske an, um die Kanten weichzuzeichnen. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>

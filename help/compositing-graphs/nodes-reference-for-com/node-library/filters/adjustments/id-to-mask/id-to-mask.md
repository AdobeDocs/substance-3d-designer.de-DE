---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "ID To Mask Grayscale", um ID-Zuordnungswerte in Graustufenmasken für die Materialauswahl zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ID zum Maskieren von Graustufen
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# ID zum Maskieren von Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Symbol ![ID zum Maskieren von Graustufen](id-to-mask.resources/IDToMask.png "ID zum Maskieren von Graustufen"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erstellt eine Maske aus einer ID-Map, wobei die Pixel mit den ausgewählten Pixelwerten weiß sind.

Eine ID-Map ist ein Bild, bei dem Pixel, die Teil eines Ganzen sind (z. B. eine Form), alle denselben eindeutigen Identifikationswert aufweisen. In diesem Fall ist der Wert eine Ganzzahl.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>ID</b> <i>Graustufen</i> PRIMÄR | Die Eingabe-ID-Zuordnung, aus der eine Maske extrahiert werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Graustufen</i> | Die Binärmaske, die aus der Eingabe-ID-Map extrahiert wurde. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Auswahlmodus</b> *Integer* | Die Methode zum Auswählen der Pixelwerte in der ID-Map, die in der Maske weiß sein sollen:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Solo:</b> Wählen Sie einen einzelnen Pixelwert aus</li> <li data-preserve-html="true"><b>Bereich:</b> Wählen Sie einen Bereich von Pixelwerten aus.</li> </ul> |
| <b>ID Integer</b> *Integer* *Verfügbar, wenn &#39;Auswahlmodus&#39; auf &#39;Solo&#39; festgelegt ist* | Der Pixelwert in der ID-Map, der in der Ausgabemaske weiß sein sollte. |
| <b>ID-Bereich</b> *Ganzzahl2* *Verfügbar, wenn &quot;Auswahlmodus&quot; auf &quot;Bereich&quot; festgelegt ist* | Der Bereich der Pixelwerte in der ID-Map, von Anfang bis Ende, der in der Ausgabemaske weiß sein sollte. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Zu maskierende ![ID: Beispiel 2](id-to-mask.resources/id_to_mask_example_2.gif "ID zum Maskieren: Beispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

Zu maskierende ![ID: Beispiel 3](id-to-mask.resources/id_to_mask_example_3.png "ID zum Maskieren: Beispiel 3"){zoomable="yes"}

</td>
</tr>
</table>

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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# ID zum Maskieren von Graustufen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Symbol ![ID zum Maskieren von Graustufen](../../../../../../assets/IDToMask.png "ID zum Maskieren von Graustufen"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erstellt eine Maske aus einer ID-Map, wobei die Pixel mit den ausgewählten Pixelwerten weiß sind.

Eine ID-Map ist ein Bild, bei dem Pixel, die Teil eines Ganzen sind (z. B. eine Form), alle denselben eindeutigen Identifikationswert aufweisen. In diesem Fall ist der Wert eine Ganzzahl.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Ausgangsanschlüsse

</td>
<td style="border: 0;" valign="top">

### Parameter

</td>
</tr>
</table>

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>ID</b> *Graustufen* PRIMÄR | Die Eingabe-ID-Zuordnung, aus der eine Maske extrahiert werden soll. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Graustufen* | Die Binärmaske, die aus der Eingabe-ID-Map extrahiert wurde. |

## Parameter

|  |  |
| --- | --- |
| <b>Auswahlmodus</b> *Integer* | Die Methode zum Auswählen der Pixelwerte in der ID-Map, die in der Maske weiß sein sollen:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Solo:</b> Wählen Sie einen einzelnen Pixelwert aus</li> <li data-preserve-html="true"><b>Bereich:</b> Wählen Sie einen Bereich von Pixelwerten aus.</li> </ul> |
| <b>ID Integer</b> *Integer* *Verfügbar, wenn &#39;Auswahlmodus&#39; auf &#39;Solo&#39; festgelegt ist* | Der Pixelwert in der ID-Map, der in der Ausgabemaske weiß sein sollte. |
| <b>ID-Bereich</b> *Integer2* *Verfügbar, wenn &#39;Auswahlmodus&#39; auf &#39;Bereich&#39; festgelegt ist* | Der Bereich der Pixelwerte in der ID-Map, von Anfang bis Ende, der in der Ausgabemaske weiß sein sollte. |

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Zu maskierende ![ID: Beispiel 2](../../../../../../assets/id_to_mask_example_2.gif "ID zum Maskieren: Beispiel 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

Zu maskierende ![ID: Beispiel 3](../../../../../../assets/id_to_mask_example_3.png "ID zum Maskieren: Beispiel 3"){zoomable="yes"}

</td>
</tr>
</table>

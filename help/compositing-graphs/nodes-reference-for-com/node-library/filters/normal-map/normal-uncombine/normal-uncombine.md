---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal nicht kombinieren, um kombinierte Normalzuordnungsdaten in einzelne X-, Y- und Z-Komponenten aufzuteilen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normales Aufheben der Kombination
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Normales Aufheben der Kombination

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Normales Symbol zum Aufheben der Zusammenführung](../../../../../../assets/NormalUncombine.png "Normales Symbol zum Aufheben der Zusammenführung"){width="200px"}

<b>In:</b> Filters > Normal map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Entfernt die Oberflächendetails, die durch eine Height-Map beschrieben werden, aus einer Normalmap.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normale Kombination</b> <i>Farbe</i> PRIMÄR | Die normale Karte, aus der Details entfernt werden sollen. |
| <b>Height</b> <i>Graustufen</i> | Die Height-Map, die die Oberflächendetails darstellt, die aus der kombinierten Normalmap entfernt werden sollen. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Nicht kombinierte Normalwerte</b> <i>Farbe</i> | Die Normalmap, in der die Oberflächendetails, die durch die Eingabe-Height-Map beschrieben wurden, entfernt wurden. |
| <b>Empfohlene Intensität</b> <i>Gleitend</i> | Eine Schätzung der Intensität, die auf einen [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)-Knoten festgelegt werden sollte, der mit der Eingangs-Height-Map verbunden ist, um der Intensität der Eingangs-Normal-Map zu entsprechen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normales Format</b> *Integer* | Das Format der Eingabe-Normalmap. Kehrt den grünen Kanal effektiv um.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Die Y-Achse zeigt nach oben</li> <li data-preserve-html="true"><b>OpenGL:</b> Die Y-Achse zeigt nach unten</li> </ul> |

## Beispiele

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 2](../../../../../../assets/normal_uncombine_example_4.png "Normale Entkombination: Beispiel 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 4](../../../../../../assets/normal_uncombine_example_6.png "Normale Entkombination: Beispiel 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 6](../../../../../../assets/normal_uncombine_example_5.png "Normale Entkombination: Beispiel 6"){zoomable="yes"}

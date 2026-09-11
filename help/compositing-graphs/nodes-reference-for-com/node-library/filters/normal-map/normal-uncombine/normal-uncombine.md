---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Normal nicht kombinieren, um kombinierte Normalen-Map-Daten in einzelne X-, Y- und Z-Komponenten aufzuteilen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normales Aufheben der Kombination
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Normales Aufheben der Kombination

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Normales Symbol zum Aufheben der Zusammenführung](normal-uncombine.resources/NormalUncombine.png "Normales Symbol zum Aufheben der Zusammenführung"){width="200px"}

<b>In:</b> Filters > Normalen-Map

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Entfernt von einem Normalen-Map die Oberflächendetails, die von einem Höhen-Map beschrieben werden.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Normale Kombination</b> <i>Farbe</i> PRIMÄR | Die Normalen-Map, von der die Details entfernt werden sollen. |
| <b>Height</b> <i>Graustufen</i> | Die Höhen-Map, die die Oberflächendetails darstellt, die von der kombinierten Normalen-Map entfernt werden sollen. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Nicht kombinierte Normalwerte</b> <i>Farbe</i> | Die Normalen-Map, auf der die von der Eingabe-Höhen-Map beschriebenen Oberflächendetails entfernt wurden. |
| <b>Empfohlene Intensität</b> <i>Fließkommazahl</i> | Eine Schätzung der Intensität, die auf einen [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)-Knoten festgelegt werden sollte, der mit der Eingangs-Höhen-Map verbunden ist, um die Intensität der Eingangs-Normalen-Map anzupassen. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Normales Format</b> *Ganzzahl* | Das Format der Normalen-Map. Kehrt den grünen Kanal effektiv um.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Die Y-Achse zeigt nach oben</li> <li data-preserve-html="true"><b>OpenGL:</b> Die Y-Achse zeigt nach unten</li> </ul> |

## Beispiele

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 2](normal-uncombine.resources/normal_uncombine_example_4.png "Normale Entkombination: Beispiel 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 4](normal-uncombine.resources/normal_uncombine_example_6.png "Normale Entkombination: Beispiel 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

![Normale Entkombination: Beispiel 6](normal-uncombine.resources/normal_uncombine_example_5.png "Normale Entkombination: Beispiel 6"){zoomable="yes"}

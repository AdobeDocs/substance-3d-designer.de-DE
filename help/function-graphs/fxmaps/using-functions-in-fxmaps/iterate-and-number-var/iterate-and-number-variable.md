---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: Erfahren Sie, wie Sie in FXMaps Iterate- und Nummernvariablen verwenden, um Schleifenmuster und prozedurale Varianten zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variable "Iterate" und "Number"
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Variable &quot;Iterate&quot; und &quot;$number&quot;

![](../../../../assets/iterate-1.jpg)

Der Knoten &quot;Iterieren&quot; rendert die Knoten, die mit der rechten Ausgabe verbunden sind, so lange, wie der Wert &quot;Iterationen&quot; dies vorgibt.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1 Wiederholung: das Gaußsche Muster wird einmal gerendert |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10 Wiederholungen: Das Gaußsche Muster wird 10-mal am selben Ort gerendert. |

Bei Verwendung eines Iterate-Knotens können Sie die Variable $number verwenden, um den aktuellen Iterationswert abzurufen. $number ist ein Gleitkommawert und beginnt bei 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Diese Funktion, die im Parameter &quot;Musterversatz&quot; festgelegt ist, wird 10 Mal ausgeführt, eine für jedes Muster.

Das erste Muster hat einen $number-Wert gleich 0 und wird dann an der (0, 0)-Koordinate gerendert. Das zweite Muster hat einen $number-Wert gleich 1 und wird dann an der (0.1, 0)-Koordinate (1 x 0.1 = 0.1) usw. für die nächsten Muster gerendert.

Beispiel herunterladen: [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)

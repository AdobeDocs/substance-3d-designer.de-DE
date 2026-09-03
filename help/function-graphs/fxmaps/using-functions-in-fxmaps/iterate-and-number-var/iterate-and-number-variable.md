---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Iterieren und `$number`-Variable

![](iterate-and-number-variable.resources/iterate-and-number-variable-01.jpg)

Der Knoten &quot;Iterieren&quot; rendert die Knoten, die mit der rechten Ausgabe verbunden sind, so lange, wie dies durch den Wert &quot;Iterationen&quot; angegeben wird.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-02.png"/></div> | 1 Wiederholung: das Gaußsche Muster wird einmal gerendert |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-03.png"/></div> | 10 Iterationen: Das Gaußsche Muster wird 10-mal am selben Ort gerendert. |

Wenn Sie einen Iterate-Knoten verwenden, können Sie die Variable &quot;`$number`&quot; verwenden, um den aktuellen Wert der Iteration abzurufen. `$number` ist ein Gleitkommawert und beginnt bei 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-04.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-05.png){width="300px"}

</td>
</tr>
</table>

Diese Funktion, die im Parameter &quot;Musterversatz&quot; festgelegt ist, wird 10 Mal ausgeführt, eine für jedes Muster.

Das erste Muster hat einen `$number`-Wert gleich 0 und wird dann an der (0, 0)-Koordinate gerendert. Das zweite Muster hat einen `$number`-Wert gleich 1 und wird dann an der (0,1, 0)-Koordinate (1 x 0,1 = 0,1) usw. für die nächsten Muster gerendert.

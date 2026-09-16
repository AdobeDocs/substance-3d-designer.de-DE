---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ""
description: Verwenden Sie den Knoten "Text", um Texturen mit anpassbaren Schriftarten und Stilen zum Erstellen textbasierter Muster zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Text
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%
---

# Text

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Atomknoten: Text](text.resources/comp_text_1.png "Elementare Knoten: Text"){width="100%"}

<b>In:</b> Atomknoten

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Der Knoten &quot;Text&quot; bietet eine Möglichkeit, vom Benutzer erstellten Text in Ihren Graf zu platzieren. Benutzer können auch Einstellungen wie Schriftart, Ausrichtung und Drehung auswählen, um die Textplatzierung anzupassen.

Der Knoten Text ist sehr leistungsstark und die einzige Möglichkeit, Text einfach zu platzieren. Die Platzierung ist oft etwas kompliziert, weil die Platzierung immer auf einer begrenzten, quadratischen Arbeitsfläche erfolgt und Schriftarten von einer systemdefinierten externen Liste gesteuert werden.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="text.resources/text-tooltip.gif" alt="Text-QuickInfo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Nur TrueType (.ttf) und bestimmte OpenType-Schriftarten werden unterstützt. Wenn Schriften in der Liste fehlen, ist dies wahrscheinlich der Grund. <b>Schriftarten können nicht als Parameter gelegt werden.</b>

Wenn ein Graf, der Text verwendet, in sbsar veröffentlicht wird, wird die Schriftart in das Paket eingebettet, genau wie bei Bitmaps und anderen Ressourcen, um sicherzustellen, dass sie auf allen Systemen und in allen Anwendungen funktioniert.



## Parameter

|  |  |
| --- | --- |
| <b>Farbmodus</b> *Boolescher Wert* | Schaltet zwischen einem Graustufen- und einem Farbausgabebild um. |
| <b>Text</b> *Zeichenfolge* | Legt die Textbeschreibung fest. |
| <b>Schrift</b> *Zeichenfolge* | Die Schriftenressource, die zum Rendern des Textes verwendet wird. |
| <b>Schriftgröße</b> *Gleitend* | Die Schriftgröße für den Text in Punkt. |
| <b>Ausrichtung</b> *Integer* | Legt die Textausrichtung als links, zentriert (Standard) oder rechts fest. |
| <b>Transformation</b> *Float4* | Die 2x2-Transformationsmatrix, die auf den gerenderten Text angewendet wird. |
| <b>Position</b> *Float2* | Die Position des Textes im Ausgabebild. |
| <b>Hintergrund</b> *Gleitend/Gleitend4* | Die Hintergrundfarbe des Ausgabebilds. |
| <b>Schriftfarbe</b> *Gleitend/Gleitend4* | Die Farbe des Textes. |

## Eingangsanschlüsse

|  |  |
| --- | --- |
| <b>Hintergrund</b> *Graustufen/Farbe* PRIMÄR | Die Hintergrundfarbe des Ausgabebilds. |


## Beispiele

*Demnächst verfügbar.*

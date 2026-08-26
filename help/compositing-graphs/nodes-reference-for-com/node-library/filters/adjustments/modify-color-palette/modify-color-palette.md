---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/modify-color-palette.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Farbpalette ändern, um Farbpaletten, die aus Texturen extrahiert wurden, anzupassen und zu transformieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Modify Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbpalette ändern
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---


# Farbpalette ändern

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Farbe quantisieren&quot;](../../../../../../assets/ModifyColorPalette.png "Symbol &quot;Farbe quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ändert die Farben in einer geordneten Palette und wendet sie mithilfe einer ID-Map auf ein Bild an.

Sie können Farben auswählen, indem Sie die Indizes in der ID-Map mit den Indizes der Farben in der Palette abgleichen.

Beispielsweise wird die #2 in der Palette auf alle Pixel in der ID-Map mit einem ID-Wert von 2 angewendet.

Dieser Knoten kann in Kombination mit den folgenden Knoten verwendet werden: [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Farbpalette erstellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Farbpalette anwenden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

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
| <b>ID</b> *Graustufen* PRIMÄR | Die Eingabe-ID-Zuordnung, die zum Auswählen von Farben verwendet wurde, um diese in der Ausgabe zu ändern und zu verteilen.   Eine ID-Map ist ein Bild, bei dem Pixel, die Teil eines Ganzen sind (z. B. eine Form), alle denselben eindeutigen Identifikationswert aufweisen. In diesem Fall ist der Wert eine Ganzzahl.   Eine ID-Zuordnung kann mithilfe eines Knotens [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) erstellt werden. |
| <b>Palette</b> *Farbe* | Eine geordnete Liste von RGB-Farben, die als Pixelzeile codiert sind. Die Palette kann maximal 256 Farben enthalten. Dies ist die Palette, die der Knoten ändert.   Paletten können mit den Knoten [Farbe quantisieren](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) oder [Farbpalette erstellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md) erzeugt werden. |

## Ausgangsanschlüsse

|  |  |
| --- | --- |
| <b>Ausgabe</b> *Farbe* | Das Ergebnis der Zuordnung der Farben in der geänderten Palette zu den Indizes der ID-Map. |
| <b>Palette</b> *Farbe* | Die aktualisierte Palette mit den angewendeten angegebenen Farbänderungen.   Die Palette kann auf ein anderes Bild mit dem Knoten [Farbpalette anwenden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) oder mit dem Knoten [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) angewendet werden. |

## Parameter

|  |  |
| --- | --- |
| <b>Farbauswahlmodus</b> *Integer* | Die Methode zur Auswahl der Zielfarbe in der Palette, die geändert werden soll:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Farbindex:</b> Der Index der Zielfarbe</li> <li data-preserve-html="true"><b>Bildbereich:</b> Die Position in der ID-Map, an der der Index gesampelt werden soll. Wenn dieser Modus ausgewählt ist, steht in der 2D-Ansicht ein Positions-Gizmo zur einfachen Auswahl zur Verfügung</li> </ul> |
| <b>Farbposition</b> *Float2* *Verfügbar, wenn &quot;Farbauswahlmodus&quot; auf &quot;Bildbereich&quot; festgelegt ist* | Die Position in der ID-Map, an der der Index gesampelt werden soll.   Verwenden Sie das Gizmo in der 2D-Ansicht, um ganz einfach eine Position im Bild auszuwählen.   Tipp: Sie können das quantisierte Bild anzeigen, aus dem die ID-Map extrahiert wird, und dann den Knoten Farbpalette ändern auswählen, um das Gizmo anzuzeigen. Dadurch wird die Auswahl einer Farbe zum Bearbeiten intuitiver. |
| <b>Farbindex</b> *Integer* *Verfügbar, wenn &quot;Farbauswahlmodus&quot; auf &quot;Farbindex&quot; festgelegt ist* | Der Index der Zielfarbe.   Die Farben in der Palette werden von links nach rechts angeordnet, und der Index der ersten Farbe ist 0. |
| <b>Farbauswahlbogen</b> *Gleitend* | Steuert, wie weit die Auswahl in die benachbarten Farben reicht.   Die Farben sind in einem *Würfel* angeordnet, wobei Breite, Height und Tiefe ein Farbverlauf sind, bei dem jede Farbkomponente von 0 auf 1 zunimmt (z. B. Rot, Grün und Blau in RGB).   Dieser Parameter legt fest, wie weit um die ausgewählte Farbe im Würfel andere Farben geändert werden können, wobei 1 die Breite des gesamten Würfels ist. |
| <b>Farbauswahlkontrast</b> *Gleitend* | Steuert den Abfallverlauf der Auswahl über benachbarte Farben.   Die Farben sind in einem *Würfel* angeordnet, wobei Breite, Height und Tiefe ein Farbverlauf sind, bei dem eine Farbkomponente von 0 auf 1 zunimmt (z. B. Rot, Grün und Blau in RGB).   Mit diesem Parameter wird die Auswahl angepasst, die über andere Farben im Würfel um die ausgewählte Farbe herum abweicht. Dabei ist 0 ein glatter Verlauf von der ausgewählten Farbe bis zum äußersten und 1 ein Cutoff von vollständig eingeschlossen bis nicht eingeschlossen. |
| <b>Entfernungsfarbraum</b> *Integer* | Die Farben sind in einem *Würfel* angeordnet, wobei Breite, Height und Tiefe ein Farbverlauf sind, bei dem eine Farbkomponente von 0 auf 1 zunimmt (z. B. Rot, Grün und Blau in RGB).   Mit diesem Parameter können Sie den Farbraum auswählen, der zum Verteilen von Farben im Würfel verwendet wird, wodurch benachbarte Farben geändert werden.   Sie können den Farbraum auswählen, der zu Ihrem Anwendungsfall passt:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab (Farbe):</b> Ein standardisierter wahrnehmbarer Farbraum, der Farben so verteilt, dass Farben, die sich &quot;ähnlich&quot; fühlen, sich tatsächlich im Würfel befinden. Dies ist für Bilder geeignet, die auf Displays visualisiert werden können.</li> <li data-preserve-html="true"><b>RGB (Daten):</b> Die Farbe ist in Rot, Grün und Blau unterteilt und direkt entlang dieser Achse verteilt, wobei die menschliche Wahrnehmung ignoriert wird. Dies eignet sich für Bilder, die Rohdaten enthalten, wie z. B. normale Karten.</li> </ul> |
| <b>Modus</b> *Integer* | Die Methode zum Ändern der Zielfarbe:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Farbe überschreiben:</b> Ersetzen der Farbe durch eine andere</li> <li data-preserve-html="true"><b>HSL:</b> passen Sie die Farbe mithilfe von Farbton-, Sättigungs- und Helligkeitskorrekturversätzen an</li> </ul> |
| <b>Deckkraft</b> *Gleitend* | Steuert die Interpolation zwischen der ursprünglichen und der geänderten Farbe. Dabei bedeutet &quot;1&quot;, dass die geänderte Farbe die ursprüngliche Farbe vollständig ersetzt. |
| <b>Farbe überschreiben</b> *Float3* *Verfügbar, wenn &quot;Modus&quot; auf &quot;Farbe überschreiben&quot; festgelegt ist* | Legt die Farbe fest, die die ursprüngliche Farbe ersetzen soll. |
| <b>HSL</b> *Float3* *Verfügbar, wenn &quot;Modus&quot; auf &quot;HSL&quot; festgelegt ist* | Steuert die Versätze für Farbton, Sättigung und Helligkeit, die auf die ursprüngliche Farbe angewendet werden. |

## Beispiele

![Farbpalette ändern: Beispiel 1](../../../../../../assets/modify_color_palette_example_1.png "Farbpalette ändern: Beispiel 1"){zoomable="yes"}

![Farbpalette ändern: Beispiel 2](../../../../../../assets/modify_color_palette_example_3.png "Farbpalette ändern: Beispiel 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_before.jpg" alt="modify_color_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_after.jpg" alt="modify_color_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

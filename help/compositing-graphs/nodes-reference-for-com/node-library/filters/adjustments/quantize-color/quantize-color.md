---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-color.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Farbe quantisieren", um die Anzahl der Farbstufen für stilisierte Posterisierungseffekte zu reduzieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Farbe quantisieren
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---


# Farbe quantisieren

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Symbol &quot;Farbe quantisieren&quot;](quantize-color.resources/QuantizeColor.png "Symbol &quot;Farbe quantisieren&quot;"){width="200px"}

<b>In:</b> Filters > Adjustments

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Reduziert die Anzahl der Farben in einem Farbbild und reduziert dadurch Farbverläufe effektiv.

Zusätzlich zum verarbeiteten Bild extrahiert der Knoten auch Folgendes:

* Eine <b>Palette</b> der verbleibenden Farben, die zum Kolorieren anderer Bilder verwendet werden kann
* Eine <b>ID-Karte</b> der quantisierten Bereiche, die verwendet werden kann, um das verarbeitete Bild mit einer anderen Palette neu zu färben.
* Die <b>Menge</b> der verbleibenden Farben als ganzzahliger Rohwert

</td>
</tr>
</table>

Wenn der Parameter &quot;Alpha ignorieren&quot; auf &quot;Falsch&quot; gesetzt ist, wird der Alphakanal des Originalbildes verwendet, um die Bereiche des Bildes auszuwählen, aus denen die Farben für den Quantisierungsprozess extrahiert werden sollen, während Farben in transparenten Bereichen ignoriert werden.

Auf diese Weise können Sie die extrahierten Farben effizient steuern.

Dieser Knoten kann in Kombination mit den folgenden Knoten verwendet werden: [Farbpalette erstellen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Farbpalette anwenden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Eingabe</b> <i>Farbe</i> PRIMÄR | Das Farbbild, das quantisiert werden soll. |

<a name="outputs"></a>

## Ausgaben

|  |  |
|:---|:---|
| <b>Ausgabe</b> <i>Farbe</i> | Das quantisierte Farbbild. |
| <b>ID</b> <i>Graustufen</i> | Eine Karte, in der jeder quantisierten Farbe eine eindeutige Ganzzahlkennung zugewiesen ist.   Diese können verwendet werden für:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Extrahieren einer Maske </b> aus einigen quantisierten Bereichen mit der [ID zu Maske &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/id-to-mask/id-to-mask.md)-Knoten</li> <li data-preserve-html="true"><b>Das quantisierte Bild mit den Knoten [Farbpalette anwenden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) oder [Farbpalette ändern](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md) neu einfärben</b></li> </ul> |
| <b>Palette</b> <i>Farbe</i> | Die aus dem Bild extrahierte Palette, die die verbleibenden Farben nach der Quantisierung enthält.   Das Bild ist eine sortierte Liste von RGB-Farben, die als Pixelzeile codiert sind, und darf maximal 256 Farben enthalten.   Die Palette kann mit dem Knoten [Farbpalette anzeigen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) angezeigt werden. |
| <b>Farbmenge der Palette</b> <i>Integer</i> | Die Menge der in der Palette gespeicherten Farben. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Max. Farbmenge</b> *Integer* | Die maximale Farbmenge, die im quantisierten Bild verwendet werden soll.   Dieser Wert ist der gleiche, der in der Palette verwendet wird, die aus dem Bild extrahiert wurde.   &quot;Maximum&quot; bedeutet, dass dieser Betrag aufgrund der verwendeten Quantisierungstechnik nicht erreicht werden darf. Überprüfen Sie die Ausgabe &quot;Farbmenge der Palette&quot; auf die tatsächliche Menge der extrahierten Farben. |
| <b>Konturglättung</b> *Gleitend* | Steuert den Radius eines Glättungseffekts, der auf das Eingabebild angewendet wird und verwendet wird, um das quantisierte Bild in einheitlichere Formen zu vereinfachen.   Hinweis: Diese Glättung erfordert intensive Berechnungen, wodurch sich die Rechenzeit des Knotens merklich erhöht. |
| <b>Dithering</b> *Gleitend* | Wendet ein Dithering-Muster an, um die Verläufe und Farbübergänge im Originalbild nachzubilden, wobei jedoch nur die nach der Quantisierung verbleibenden Farben verwendet werden.   Stellen Sie sicher, dass Sie den Wert &quot;Konturglättung&quot; von 0 verwenden, um den erwarteten Dithering-Effekt zu erzielen. |
| <b>Dithering-Muster</b> *Integer* | Das Dithering-Muster, mit dem die Verläufe und Farbübergänge im Originalbild neu erstellt werden:<ul data-preserve-html="true"> <li data-preserve-html="true">Rauschfilter Blau</li> <li data-preserve-html="true">Bayer</li> </ul> |
| <b>Alpha ignorieren</b> *Boolescher Wert* | Standardmäßig wird der Alphakanal des Originalbildes verwendet, um die Bildbereiche auszuwählen, aus denen die Farben für den Quantisierungsprozess extrahiert werden sollen, während Farben in transparenten Bereichen ignoriert werden. Auf diese Weise können Sie die extrahierten Farben effizient steuern.   Sie können die Farben in den sichtbaren Teilen des Bildes nur für den Quantisierungsprozess verwenden.   Mit diesem Schalter können Sie diese Maskierung deaktivieren und das *full*-Bild unabhängig von der Transparenz verwenden. |
| <b>Entfernungsfarbraum</b> *Integer* | Die Farben sind in einem *Würfel* angeordnet, wobei Breite, Height und Tiefe ein Farbverlauf sind, bei dem jede Farbkomponente von 0 auf 1 zunimmt (z. B. Rot, Grün und Blau in RGB).   Der Quantisierungsprozess umfasst das Auswählen der *definierenden Farben* in einem Bild, das Auffinden der Farben, die diesen Farben am nächsten im Würfel liegen, und das Ersetzen dieser Farben durch diese definierende Farbe.   Mit diesem Parameter können Sie den Farbraum auswählen, der zum Verteilen von Farben im Würfel verwendet wird. Dadurch wird das Ergebnis der Quantisierung geändert, indem die Kriterien zum Erkennen einer definierenden Farbe und zum Neuanordnen benachbarter Farben geändert werden.   Sie können den Farbraum auswählen, der zu Ihrem Anwendungsfall passt:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Labor (Color):</b> Ein standardisierter wahrnehmbarer Farbraum, der Farben so verteilt, dass Farben, die sich &quot;ähnlich&quot; fühlen, sich tatsächlich im Würfel befinden. Dies eignet sich für Bilder, die auf Displays visualisiert werden können</li> <li data-preserve-html="true"><b>RGB (Daten):</b> Die Farbe wird in Rot, Grün und Blau unterteilt und direkt entlang dieser Achse verteilt, wobei die menschliche Wahrnehmung ignoriert wird. Dies eignet sich für Bilder, die Rohdaten enthalten, wie z. B. normale Karten</li> </ul> |
| <b>ID-Sortiermodus</b> *Integer* | Die Farben sind in einem *Würfel* angeordnet, wobei Breite, Height und Tiefe ein Farbverlauf sind, bei dem jede Farbkomponente von 0 auf 1 zunimmt (z. B. Rot, Grün und Blau in RGB).   Mit diesem Parameter wird die Methode ausgewählt, mit der die Liste der Farben in der extrahierten Palette sortiert wird, sowie die Indizes in den Bereichen der extrahierten ID-Map:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Z-Kurve:</b> Farben werden mithilfe einer Z-Kurve, von weiß bis schwarz, nach Farben sortiert, die im Farbwürfel als Nächstes gefunden werden.</li> <li data-preserve-html="true"><b>Farbton:</b> Farben werden nach dem nächsten Farbton sortiert</li> <li data-preserve-html="true"><b>Repräsentativität:</b> Farben werden von den meisten bis zu den am wenigsten verwendeten Farben im quantisierten Bild sortiert.</li> </ul> |
| <b>Downscale-Filter</b> *Integer* | Bei der Farbquantisierung wird ein Histogramm eines Bildes mit reduzierter Größe (d.h. verkleinert) berechnet, um die Farben nach ihrer Bedeutung zu sortieren. Dieser Parameter steuert die Methode zum Filtern des herunterskalierten Bildes vor der Berechnung seines Histogramms:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilinear:</b> wendet bilineare Filterungen auf das Bild an, was zu einem Histogramm mit interpolierten Farben führt, die möglicherweise nicht Teil des Originalbildes sind, wodurch einige der Originalfarben verwässert werden. Dies ist bei Bildern mit vielen Farben hilfreich.</li> <li data-preserve-html="true"><b>Nächster:</b> nimmt die Farbe des nächstgelegenen Pixels ohne Filterung auf, was zu einem Histogramm führt, in dem ausschließlich Farben aus dem Originalbild verwendet werden. Dies ist für Bilder mit wenigen Farben geeignet.</li> </ul> |

## Beispiele

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_6_before.jpg" alt="quantize_color_example_6_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_6_after.jpg" alt="quantize_color_example_6_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_2_before.jpg" alt="quantize_color_example_2_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_2_after.jpg" alt="quantize_color_example_2_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_3_before.jpg" alt="quantize_color_example_3_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_3_after.jpg" alt="quantize_color_example_3_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_4_before.jpg" alt="quantize_color_example_4_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_4_after.jpg" alt="quantize_color_example_4_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_5_before.jpg" alt="quantize_color_example_5_before">
      <br><i>Vorher</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_5_after.jpg" alt="quantize_color_example_5_after">
      <br><i>Nach</i>
    </td>
  </tr>
</table>

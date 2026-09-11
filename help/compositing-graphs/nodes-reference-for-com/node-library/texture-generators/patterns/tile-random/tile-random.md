---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Kachelzufall", um zufällige Kachelmuster mit prozeduralen Variationen für organische Texturen zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Kachelzufall
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# Kachelzufall

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random.png){width="128px"}

<b>In:</b> Generatoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

&quot;Kachelzufall&quot; erzeugt ein prozedurales Kachelmuster, das etwas mehr Chaos in den Kachelformen aufweist als sein Gegenstück, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Dies geschieht durch zufälliges Aufteilen bestimmter Kacheln in kleinere Kacheln. Wir empfehlen Ihnen, sich zunächst mit dem Tile Generator vertraut zu machen, bevor Sie sich mit Tile Random befassen, da viele Konzepte ähnlich sind.

Anstelle von [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) wird &quot;Zufällig&quot; verwendet, wenn das Ziel ein älteres, weniger strukturiertes Muster ist. Es hat jedoch seine Einschränkungen. Daher sollten Sie [Sampler &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) für andere erweiterte Anforderungen anordnen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Mustereingabe</b> <i>Graustufeneingabe (Farbeingabe)</i> | Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist. |
| <b>Hintergrundeingabe</b> <i>Graustufeneingabe (Farbeingabe)</i> |  |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>X Betrag</b> <i>1 - 64</i> | Anzahl der X-Wiederholungen des Musters. |
| <b>Y Betrag</b> <i>1 - 64</i> | Anzahl der Y-Wiederholungen des Musters. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Squash und dehn mit nicht quadratischen Verhältnissen. |
| <b>Muster</b> |  |
| <b>Muster</b> <i>Mustereingabe, Quadrat, Datenträger, Paraboloid, Gaußscher Text, Dorn, Pyramide, Ziegel, Abstufung, Wellen, Halbglocke, Rändelglocke, Mondsichel, Kapsel, Kegel</i> | Wählt die zu verwendende Musterform aus. |
| <b>Filterungen zur Bildeingabe (Engine > v4)</b> <i>Bilinear + Mipmaps, Bilinear, Nächste</i> |  |
| <b>Musterspezifisch</b> <i>0.0 - 1.0</i> | Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab. |
| <b>Musterspezifische Zufälligkeit</b> <i>0.0 - 1.0</i> | Der Randomisierungseffekt hängt vom ausgewählten Muster ab. |
| <b>Drehung</b> <i>0, 90, 180, 270, zufällig horizontal, zufällig vertikal</i> | Stellt die Drehung in 90-Grad-Schritten mit optionaler Randomisierung ein. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Fügt eine zufällige freie Drehung hinzu. |
| <b>Symmetrie zufällig</b> <i>0.0 - 1.0</i> | Spiegelt zufällig bestimmte Muster durch die ausgewählte Symmetrie Zufallsmodus. Je höher dieser Wert, desto mehr Muster werden gespiegelt. |
| <b>Zufallsmodus der Symmetrie</b> <i>Horizontal + Vertikal, Horizontal, Vertikal</i> | Bestimmt das Spiegelungsverhalten, wenn die zufällige Symmetrie größer als 0 ist. |
| <b>Aufspaltung</b> |  |
| <b>Modus</b> <i>keine, automatisch, automatisch horizontal, automatisch vertikal, zufällig h+v</i> | Legt die Regel für das Teilen von Kacheln fest. |
| <b>Schwellenwert</b> <i>0.0 - 1.0</i> | Größenschwellenwert für das Teilen einer Kachel. |
| <b>Multiplikator</b> <i>0 - 10</i> | Multiplikator wird aufgeteilt. Je höher dieser Wert, desto mehr Teilungen. |
| <b>Größe</b> |  |
| <b>Zufälliges X</b> <i>0.0 - 1.0</i> | Zufallsgenerator für ungleichmäßige Skalierung über X-Achse. |
| <b>Zufall Y</b> <i>0.0 - 1.0</i> | Zufallsgenerator für ungleichmäßige Skalierung über die Y-Achse. |
| <b>Interstice</b> |  |
| <b>Modus</b> <i>Relativ zum kleinsten Ziegel, Relativ zum größten Ziegel</i> | Legt fest, auf welchen Ziegel die Zwischenablage bei der Textgröße sich bezieht. |
| <b>Betrag</b> <i>0.0 - 1.0</i> | Legt die Größe des Abstands zwischen Ziegeln fest. |
| <b>Form</b> |  |
| <b>Skalierung</b> <i>0.0 - 1.0</i> | Skaliert jede Kachel global. |
| <b>Zufällige Skalierung</b> <i>0.0 - 1.0</i> | Zufällige Skalierung pro Kachel. |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Globale Drehung für jede Kachel. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Dreht sich willkürlich pro Kachel. |
| <b>Drehungseinschränkung</b> <i>False/True</i> | Schränkt die Skalierung ein, sodass sich gedrehte Kacheln nie überlappen. |
| <b>Position</b> |  |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt oder Kamera bewegt die Kacheln global, verschiebt sich nur über X-Achse |
| <b>Offset zufällig</b> <i>0.0 - 1.0</i> | Randomisiert Versatz pro Kachel, nur Folien über X-Achse |
| <b>Zufällig</b> <i>0.0 - 1.0</i> | Randomisiert die Position, die Kacheln bewegen sich auf der X- und Y-Achse. |
| <b>Random Constraints</b> <i>False/True</i> | Schränkt die Skalierung ein, sodass sich die Kacheln berühren, sich aber nicht überlappen. Reduziert den Effekt &quot;Zufällige Position&quot; erheblich. |
| <b>Farbe</b> |  |
| <b>Farbe</b> <i>(Graustufenwert) / (Farbwert)</i> | Legt die Volltonfarbe für alle Kacheln fest. |
| <b>Farbzufall</b> <i>0.0 - 1.0</i> | Randomisiert die Farbe pro Kachel. |
| <b>Farbparametrisierung</b> <i>keine, Bereich, Größe x, Größe y</i> | Macht Farbvariationen von einer dieser Einstellungen abhängig. |
| <b>Intensität der Farbparametrisierung</b> <i>0.0 - 1.0</i> | Multiplikator für den obigen Effekt &quot;Parametrisierung&quot;. |
| <b>Effekt &quot;Farbparametrisierung&quot; (nur für Farbe)</b> <i>RGB+Alpha, nur RGB, nur Alpha</i> | Bestimmt den Effekt der reinen Farbparametrisierung. |
| <b>Hintergrundfarbe</b> <i>(Graustufenwert) / (Farbwert)</i> | Legt eine einfarbige Hintergrundfarbe fest. |
| <b>Füllmethode</b> <i>Hinzufügen/Sub, Max./Hinzufügen/Sub, Alpha-Überblendung (Farbe)</i> | Legt den Mischmodus für Kacheln auf dem Hintergrund fest. |
| <b>Maske</b> |  |
| <b>Zufällig</b> <i>0.0 - 1.0</i> | Zufällig beginnt Kacheln maskieren. Je höher der Wert, desto mehr Kacheln verschwinden. |
| <b>Umkehren</b> <i>False/True</i> | Kehrt das Maskenergebnis um. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-1.png" />
        </td>
    </tr>
</table>

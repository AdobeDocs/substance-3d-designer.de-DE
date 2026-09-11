---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Verwenden Sie den Sampler-Kachelknoten zum Aufnehmen und Anordnen von Kacheln aus Eingabetexturen, um Kachelmuster in Substance 3D Designer zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sampler anordnen
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# Sampler anordnen

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-sampler.resources/tile-sampler.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Tile Sampler ist der ultimative Kachelmuster-Erzeugungsknoten. Es handelt sich um eine weiterentwickelte, komplexere Version von [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Ab 2017 2.1 sind die Unterschiede zwischen Tile Sampler und [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) viel geringer. Die Hauptunterschiede bestehen nun nur noch in den sieben verschiedenen Kartensteckplätzen, die für Skalierung, Position, Drehung, Größe, Farbe und Maskierung zur Verfügung stehen. Ihr Effekt kann separat eingemischt werden.

Kachel-Sampler ist hilfreich beim Erstellen künstlicher prozeduraler Muster, mit zusätzlicher Kontrolle über bestimmte Parameter, die von externen Eingabemaps gesteuert werden.

Vergewissern Sie sich, dass Sie mit [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) vertraut sind, bevor Sie mit Tile Sampler fortfahren. In den meisten Fällen reichen [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) aus und Sie benötigen nicht die zusätzliche Komplexität von Tile Sampler.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Mustereingabe 1-6</b> <i>Graustufen-Eingabe/Farbeingabe</i> | Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; festgelegt ist.<br><br>Die Menge der verfügbaren Eingaben wird durch den Parameter <b>Mustereingabenummer</b> bestimmt. |
| <b>Zuordnungseingabe skalieren</b> <i>Graustufen-Eingabe</i> | Graustufen-Map, um die Kachelskalierung zu steuern. |
| <b>Versatz-Zuordnungseingabe</b> <i>Graustufen-Eingabe</i> | Graustufen-Map zum Steuern des Kachel-Versatzes. |
| <b>Rotation Map-Eingabe</b> <i>Graustufen-Eingabe</i> | Graustufen-Map, um die Drehung der Kacheln zu steuern. |
| <b>Vektorzuordnungseingabe</b> <i>Farbeingabe</i> | Farbvektorkarte zur ungleichmäßigen Skalierung. |
| <b>Farbzuordnungseingabe</b> <i>Graustufen-Eingabe/Farbeingabe</i> | Karte, um die Farbtönung pro Kachel zu steuern. |
| <b>Maskenzuordnungseingabe</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Ausblenden bestimmter Kacheln. |
| <b>Musterverteilungszuordnungseingabe</b> <i>Graustufen-Eingabe</i> | Maskenschlitz, der zum Steuern mehrerer benutzerdefinierter Mustereingaben verwendet wird. |
| <b>Hintergrundeingabe</b> <i>Graustufen-Eingabe/Farbeingabe</i> | Optionales Hintergrundbild. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>X Betrag</b> <i>0 - 64</i> | Anzahl der X-Wiederholungen des Musters. |
| <b>Y Betrag</b> <i>0 - 64</i> | Anzahl der Y-Wiederholungen des Musters. |
| <b>Quadratische Ausbreitung</b> <i>False/True</i> | Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen. |
| <b>Muster</b> |  |
| <b>Muster</b> <i>Mustereingabe, Quadrat, Datenträger, Paraboloid, Gaußsch, Dorn, Pyramide, Ziegel, Abstufung, Wellen, Halbglocke, Rändelglocke, Mondsichel, Kapsel, Kegel</i> | Wählt die zu verwendende Musterform aus. |
| <b>Mustereingabenummer</b> <i>1 - 6</i> | Anzahl benutzerdefinierter Muster, aus denen zufällig ausgewählt werden soll. |
| <b>Mustereingabeverteilung</b> <i>Zufällig, Musternummer, Verteilungszuordnung</i> | Legt fest, wie mehrere Mustereingänge ausgewählt werden. &quot;Zufällig&quot; bedeutet, dass ein zufälliger Wert ausgewählt wird. &quot;Musternummer&quot; bedeutet, dass er nur in eine Schleifensequenz eingefügt wird. Die Verteilungszuordnung verwendet eine Graustufenzuordnungseingabe, um die Platzierung zu steuern. |
| <b>Mustereingabe-Filterungen (Engine > v4)</b> <i>Bilinear + Mipmaps, Bilinear, Nächste</i> |  |
| <b>Musterspezifisch</b> <i>0.0 - 1.0</i> | Hier können Sie die Form des ausgewählten Musters ändern. Der Effekt hängt vom ausgewählten Muster ab. |
| <b>Musterspezifische Zufälligkeit</b> <i>0.0 - 1.0</i> | Der Randomisierungseffekt hängt vom ausgewählten Muster ab. |
| <b>Drehung</b> <i>0, 90, 180, 270</i> | Schrittweise Drehung (90 Grad). |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Zufällige freie Drehung pro Kachel. |
| <b>Symmetrie zufällig</b> <i>0.0 - 1.0</i> | Legt die Anzahl der Kacheln fest, die gemäß dem Verhalten unten zufällig gespiegelt/gespiegelt werden sollen. |
| <b>Zufallsmodus der Symmetrie</b> <i>Horizontal + Vertikal, Horizontal, Vertikal</i> | Bestimmt das Verhalten der Symmetrie-Spiegelung. |
| <b>Größe</b> |  |
| <b>Größenmodus</b> <i>Normal, Verhältnis beibehalten, Absolut, Pixel</i> | Legt das allgemeine Verhalten der Mustergröße fest.Mit <br><br>Normal können Sie die Größe der Musterelemente definieren. Er wird durch den X- und Y-Wert beeinflusst.<br><br>Mit &quot;Verhältnis beibehalten&quot; können Sie eine Größe festlegen, die von der Größe X und Y beeinflusst wird. Das Verhältnis X und Y zwischen den beiden bleibt jedoch erhalten.<br><br>Mit &quot;Absolut&quot; können Sie eine absolute Größe festlegen, die nicht durch den X- und Y-Wert beeinflusst wird.Mit <br><br>Pixel können Sie eine absolute Größe in Pixeln festlegen, die von der X- und Y-Größe nicht beeinflusst wird. Eine Änderung der Auflösung wirkt sich auf die Größe der Elemente aus. |
| <b>Größe (Absolut/Pixel)</b> <i>0.0 - 1.0</i> | Ändert ungleichmäßige Proportionen für Kacheln. Das genaue Verhalten hängt vom Größenmodus ab. |
| <b>Größe zufällig</b> <i>0.0 - 1.0</i> | Randomisiert die Proportionen pro Kachel. |
| <b>Skalierung</b> <i>0.0 - 10.0</i> | Legt die globale Kachelskala fest. |
| <b>Zufällige Skalierung</b> <i>0.0 - 1.0</i> | Zufällige Skalierung pro Kachel |
| <b>Zuordnungsmultiplikator skalieren</b> <i>0.0 - 1.0</i> | Überblendungen im Effekt der Skalierungszuordnung. |
| <b>Vektorzuordnungsvervielfacher skalieren</b> <i>0.0 - 1.0</i> | Überblendungen der Wirkung der Skalierungsvektorkarte, um eine ungleichmäßige Skalierung zu steuern. |
| <b>Effekt &quot;Skalierungsparameter&quot;</b> <i>X und Y, X, Y</i> | Legt fest, auf welche Achsen die Skalierungsparameter sich auswirken. Kann verwendet werden, um zu erreichen, dass die Skalierungszuordnung nur das X oder Y von Elementen beeinflusst. |
| <b>Position</b> |  |
| <b>Position zufällig</b> <i>0.0 - 10.0</i> | Randomisiert die Kachelposition auf beiden Achsen. |
| <b>Offset</b> <i>0.0 - 1.0</i> | Verschiebt die Kacheln je nach Versatztyp. |
| <b>Offset-Typ</b> <i>horizontaler Quincux, vertikaler Quincux, horizontaler globaler Wert, vertikaler globaler Wert</i> | Ändert die Richtung, in die der Offset angewendet wird. |
| <b>Globaler Offset</b> <i>0.0 - 1.0</i> | Globaler Offset aller Kacheln auf X- oder Y-Achse. |
| <b>Versatz-Zuordnungsintensität</b> <i>0.0 - 1.0</i> | Überblendungen in der Stärke der Versatz-Map im Offset. |
| <b>Versatz-Winkel</b> <i>0.0 - 1.0</i> | Legt den Winkel fest, in dem verschoben werden soll. |
| <b>Vektordarstellung-Versatz</b> <i>0.0 - 1.0</i> | Verwendet die Vektorzuordnung, um Versatz und Winkel zu steuern. |
| <b>Drehung</b> |  |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Dreht alle Kacheln global. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Dreht sich willkürlich pro Kachel. |
| <b>Rotation Map-Multiplikator</b> <i>0.0 - 1.0</i> | Überblendungen der Auswirkungen des Rotation Map auf die Drehung pro Kachel. |
| <b>Vektorzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Verwendet die Vektorzuordnung zum Drehen pro Kachel. |
| <b>Farbe</b> |  |
| <b>Schwellenwert für Maskenzuordnung</b> <i>0.0 - 1.0</i> | Schwellenwert für Maskenzuordnung, wenn mit dem Ausblenden von Kacheln begonnen wird. |
| <b>Umkehren der Maskenzuordnung</b> <i>False/True</i> | Kehrt den Effekt &quot;Maskenzuordnung&quot; um. |
| <b>Maskenzuordnungs-Sampling-Technik</b> <i>Mustermitte, Musterbegrenzungsrahmen (langsamer)</i> | Legt fest, ob das Ausblenden durch einen einzelnen Punkt oder einen Begrenzungsrahmen bestimmt werden soll. Vermeidet unregelmäßige Pixel, die seltsame Effekte verursachen. |
| <b>Zufällige Maske</b> <i>0.0 - 1.0</i> | Die zufällige Maskierung funktioniert parallel zur Maskenzuordnung. |
| <b>Maske umkehren</b> <i>False/True</i> | Kehrt die zufällige Maskierung um. |
| <b>Füllmethode</b> <i>Hinzufügen/Sub, Max. (Kachel Sampler)/Hinzufügen/Sub, Alpha-Überblendung (Kachel Sampler Color)</i> | Überblendung für Kacheln auf dem Hintergrund und untereinander. |
| <b>Farbe</b> <i>(Graustufenwert) / (Farbwert)</i> | Farbfläche der Kacheln. |
| <b>Farbe/Luminanz zufällig</b> <i>0.0 - 1.0</i> | Randomisierung der Farbe pro Kachel. |
| <b>Farbparametrisierungsmodus</b> <i>Farbeingabe, Skalierung, Zeilenindex, Zeilenindex, Musterindex (Kachel-Sampler) / Farbzuordnung, Skalierung, Zeilenindex, Musterindex, Mustermittenposition, Mustermittenposition (RG) Kugelgröße (B) (Kachel-Sampler-Farbe)</i> | Legt fest, wie genau die Farbrandomisierung parametriert wird. |
| <b>Farbparametrisierungsvervielfacher</b> <i>0.0 - 1.0</i> | Überblendungen im oben genannten Effekt &quot;Parametrisierung&quot;. |
| <b>Effekt &quot;Farbparametrisierung&quot; (nur Farbe)</b> <i>RGB+Alpha, nur RGB, nur Alpha</i> | Legt fest, wie sich die Parametrisierung auf die Farbe auswirkt. |
| <b>Globale Deckkraft (nur Graustufen)</b> <i>0.0 - 1.0</i> | Legt die globale Kacheldeckkraft fest. |
| <b>Hintergrundfarbe</b> <i>(Graustufenwert) / (Farbwert)</i> | Legt eine einfarbige Hintergrundfarbe fest. |
| <b>Renderreihenfolge umkehren</b> <i>False/True</i> | Kehrt die Renderreihenfolge um und wechselt von hinten nach vorne. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-sampler.resources/tilesampler-ex2.png" /><br><i>Beispiel zeigt, wie Parameter von Eingabe-Map gesteuert werden (Musterverteilung, Skalierung, Drehung).</i>
        </td>
    </tr>
</table>

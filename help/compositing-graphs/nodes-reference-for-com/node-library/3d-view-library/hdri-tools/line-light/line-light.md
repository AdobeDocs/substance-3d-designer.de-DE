---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Linienlicht , um lineare Lichtquellen in HDRI-Umgebungen für die Simulation von Fluoreszenz- und Streifenlicht zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Linienbeleuchtung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# Linienbeleuchtung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](line-light.resources/panorama-line-light.png){width="200px"}

<b>In:</b> 3D-Ansicht > HDRI-Werkzeugs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Erzeugt eine sphärisch projizierte Linienform basierend auf den Koordinaten zweier Punkte im Raum. Im Vergleich zu [Formenlicht](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) verfügt es über mehr Optionen zum Ausrichten von Formen und zum Anwenden wiederholter Muster auf die Lichtform.

Die Positionierungsmodi für diesen Knoten sind etwas komplexer als andere HDRI-Lichtknoten. Es wird empfohlen, verschiedene Größenmodi auszuprobieren, um herauszufinden, welcher für Ihr Szenario funktioniert.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrundbildeingabe</b> <i>Farbeingabe</i> | Optionaler Hintergrund, auf dem das erzeugte Licht komponiert werden soll. |
| <b>Shape-Image-Eingabe</b> <i>Farbeingabe</i> | Optionales Bild für die Zuordnung zum Linienlicht. Wird nur verwendet, wenn der Formfarbmodus auf &quot;Bildeingabe&quot; eingestellt ist. |
| <b>Musterbildeingabe</b> <i>Graustufen-Eingabe</i> | Benutzerdefiniertes Musterbild, das verwendet wird, wenn der Parameter &quot;Muster&quot; auf &quot;Bildeingabe&quot; eingestellt ist. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Positionsmodus</b> <i>Boden/Decke, Abstand zum Ursprung, Weltpositionen</i> | Sie können aus drei verschiedenen Platzierungsmodi auswählen. Boden/Decke und Abstand zum Ursprung unterstützen die Manipulation in der 2D-Ansicht, Weltpositionen können nur über Eigenschaften verändert werden, aber es wird eine genauere Platzierung unterstützt. |
| <b>Boden-Raster anzeigen</b> <i>False/True</i> | Helfer-Funktion, um das Zeichnen eines Debug-Boden-Rasters zu ermöglichen. Hilft bei der Schätzung der Position von Linien im Raum. |
| <b>Positionskoordinaten</b> |  |
| <b>Vektor nach oben</b> <i>Z nach oben, J nach oben</i> | Nur mit dem Modus &quot;Weltposition&quot; bestimmen Sie die Ausrichtung des Koordinatensystems. |
| <b>Punkt 1 UV-Position</b> | Nur mit Boden / Decke und Abstand zum Ursprung. Legt die erste Punktposition im UV-Raum fest. |
| <b>Point 2 UV-Position</b> | Nur mit Boden / Decke und Abstand zum Ursprung. Legt die zweite Punktposition im UV-Raum fest. |
| <b>Weltrangliste für Punkt 1</b> <i>-2.0 - 2.0</i> | Nur im Modus &quot;Weltpositionen&quot;. Legt den ersten Punkt im Welt-Raum fest. Keine 2D-Ansicht-Interaktion unterstützt. |
| <b>Weltrangliste für Punkt 2</b> <i>-2.0 - 2.0</i> | Nur im Modus &quot;Weltpositionen&quot;. Legt den zweiten Punkt im Welt-Raum fest. Keine 2D-Ansicht-Interaktion unterstützt. |
| <b>Absolutes Height der Zeile</b> <i>0.0 - 1.0</i> | Nur mit Boden / Deckenpositionsmodus, setzt absolutes Height von der Decke. Verwenden Sie Boden-Raster anzeigen , um die Position besser zu schätzen. |
| <b>Abstand zum Ursprung</b> <i>0.0 - 1.0</i> | Nur mit Abstand zum Ursprung-Positionsmodus. Legt für beide Punkte den Abstand vom Mittelpunkt des Panoramas fest. |
| <b>Formfarbmodus</b> <i>RGB, Temperatur (Kelvin), Bildeingabe</i> | Wählen Sie die Methode aus, die zum Festlegen der Formfarbe verwendet werden soll. Image Input ermöglicht die Verwendung des zweiten Eingangssteckplatzes. |
| <b>Farbe</b> <i>(Farbwert)</i> | Nur bei RGB als Formfarbmodus. Wählt Farbe für die Form. |
| <b>Temperatur</b> <i>800.0 - 20000.0</i> | Nur, wenn der Formfarbmodus auf &quot;Temperatur&quot; eingestellt ist. Legt den Kelvin-Wert für die Formfarbe fest. |
| <b>Modus für die UV des Formenbilds</b> <i>Gedehnt, nur Mitte Gedehnt, Wiederholen + Abstand</i> | Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legt fest, wie das Bild auf die Linienform angewendet wird, und bestimmt das Verhalten der UV-Wiederholung. |
| <b>Abstand für die Wiederholung des Formenbilds</b> <i>0.0 - 1.0</i> | Nur bei &quot;Formfarbmodus&quot; auf &quot;Bildeingabe&quot; und &quot;UV-Modus&quot; auf &quot;Wiederholen + Abstand&quot; eingestellt. Legt den Abstand fest, der zwischen den Bildern auf einer Linie liegt. |
| <b>Shape Image Gamma</b> <i>sRGB, linear</i> | Nur bei aktiviertem Formfarbmodus &quot;Bildeingabe&quot;. Legen Sie fest, wie die Formbildeingabe interpretiert wird. |
| <b>Belichtung (EV)</b> <i>0.0 - 10.0</i> | Belichtungswert für generierte Form festlegen, optimal abgestimmt auf den Belichtungswert des Hintergrundbilds. |
| <b>Zeilendrehung</b> <i>0.0 - 1.0</i> | Dreht die Linie entlang der Achse ihrer Länge. Die Linie wird beim Drehen als flache Karte behandelt. |
| <b>Line-Thickness</b> <i>0.0 - 1.0</i> | Legt die Thickness der Zeilenkarte fest. |
| <b>Muster</b> <i>Quadrat glätten, Quadrat scharf, Kegel, Halbkugel, Bildeingabe</i> | Wählen Sie die zu verwendende Musterform aus. |
| <b>Pattern-Härte</b> <i>0.0 - 1.0</i> | Härte/Kontrast des Musters einstellen. |
| <b>Pattern-UV-Modus</b> <i>Gedehnt, nur Mitte Gedehnt, Wiederholen + Abstand</i> | Legen Sie fest, wie eine sekundäre Mustermaske verwendet wird, die über dem Formenbild angewendet wird. |
| <b>Abstand zur Musterwiederholung</b> <i>0.0 - 1.0</i> | Nur, wenn der UV-Mustermodus auf &quot;Wiederholen + Abstand&quot; eingestellt ist. Festlegen des Abstands zwischen wiederholten Mustern. |
| <b>Boden-Clipping aktivieren</b> <i>False/True</i> | Aktiviere das Beschneiden von Linien. Der Effekt ist bei Verwendung des Platzierungsmodus &quot;Boden/Decke&quot; nicht sichtbar. |
| <b>Boden-Height</b> <i>-2.0 - 0.0</i> | Legt das relative Height der für die Beschneidung verwendeten Vordergrundebene fest. Wirkt sich auf das gezeichnete Bodenraster aus. |
| <b>Hintergrundeingabe aktivieren</b> <i>False/True</i> | Schaltet die Verwendung des optionalen Hintergrundbilds um. Kompositionen generierten Licht auf dem Hintergrund. |
| <b>Hintergrundfarbe</b> <i>(Farbwert)</i> | Wenn die Option &quot;Hintergrundeingabe&quot; nicht verwendet wird, legen Sie hier einen Wert für einen einfarbigen Hintergrund fest. |
| <b>Hintergrund-Gamma</b> <i>sRGB, linear</i> | Wenn die Hintergrundeingabe verwendet wird, legen Sie fest, wie die Hintergrundeingabe interpretiert werden soll. |

## Beispiele

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="line-light.resources/line-light-ex.gif" />
        </td>
    </tr>
</table>

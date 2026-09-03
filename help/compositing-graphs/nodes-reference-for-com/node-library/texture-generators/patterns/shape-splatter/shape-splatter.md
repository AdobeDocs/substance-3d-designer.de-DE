---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Verwenden Sie den Knotenpunkt "Form-Spritzer", um Formen in Streuungen über Texturen hinweg anzuordnen, um prozedurale Muster und Details zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Formaufteilung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# Formaufteilung

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter-01.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Ein sehr komplexer Knoten, der für die Verwendung mit den zugehörigen Knoten [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) und [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md) entwickelt wurde. Wird verwendet, um Formen ähnlich wie [Sampler anordnen](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) oder [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) zu spritzen, jedoch mit einem dynamischen, nicht-destruktiven Prozess, der die Kontrolle über jeden Schritt über ein mehrstufiges System ermöglicht, das dem [Flood Fill ähnelt.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Während der Flood Fill eine Basiseingabekarte aus einer externen Quelle verwendet, generiert Shape Splatter die Zuordnung und die darauf folgenden Daten in einem einzigen Schritt als eine Art erweiterte Version von [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Der Hauptzweck besteht darin, die Platzierung von Formen auf und gesteuert durch eine Height-Map zu ermöglichen und dann verschiedene Maps aus den Splatter-Daten zu generieren. Zum Beispiel das Platzieren von Felsen, Zweigen und Blättern auf einer Landschaft, orientiert und angetrieben von verschiedenen Karten. Verschiedene Maps können dann für Height, Normal, Grundfarbe, Raueit und jeden anderen Kanal verwendet werden, während alle immer noch auf den gleichen gemeinsamen Splatter-Daten basieren.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Hintergrund-Height</b> <i>Graustufen-Eingabe</i> | Hintergrund-Height zum Platzieren von Kacheln auf verschiedenen Effekten und zum Steuern. |
| <b>Muster 1-8</b> <i>Graustufen-Eingabe</i> | Optionales Muster |
| <b>Musterverteilung</b> <i>Graustufen-Eingabe</i> | Graustufen-Map zu |
| <b>Formskalierung</b> <i>Graustufen-Eingabe</i> | Graustufen-Map, um die Kachelskalierung zu steuern. |
| <b>Formdrehung</b> <i>Graustufen-Eingabe</i> | Graustufen-Map, um die Drehung der Kacheln zu steuern. |
| <b>Height-Offset</b> <i>Graustufen-Eingabe</i> | Graustufen-Map zur Verwendung als Offset für Kachel-Height. |
| <b>Height-Skalierung</b> <i>Graustufen-Eingabe</i> | Graustufen-Map zur Verwendung als Offset für Kachel-Height. |
| <b>Zufällige Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |
| <b>Vektorzuordnung</b> <i>Farbeingabe</i> | Farbvektorkarte zur Steuerung der Kachelpositionierung und -drehung. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>X Betrag</b> <i>1 - 64</i> | Anzahl der X Wiederholungen des Musters. |
| <b>Y Betrag</b> <i>1 - 64</i> | Anzahl der Y-Wiederholungen des Musters. |
| <b>Muster</b> |  |
| <b>Mustereingabenummer</b> <i>1 - 8</i> | Legen Sie die Anzahl der zu verwendenden Muster fest. Entsperrt neue Steckplätze für Mustereingabe. |
| <b>Musterverteilungsmodus</b> <i>Zufällig, Musterindex, Zeilenindex, Spaltenindex</i> | Legen Sie fest, wie das zu verwendende Muster bestimmt wird. Zufällig oder nach Muster, Zeile oder Spalte. |
| <b>Zuordnungsmultiplikator für Musterverteilung</b> <i>0.0 - 1.0</i> | Legen Sie den Einfluss der optionalen Verteilungskarte für die Platzierung von Mustern fest. |
| <b>Musterrotation</b> <i>0, 90, 180, 270</i> | Vorgabe festlegen, Drehung der Muster um 90 Grad. |
| <b>Musterrotation zufällig</b> <i>0.0 - 1.0</i> | Legen Sie die Stärke der zufälligen 90-Grad-Schrittdrehung für Muster fest. |
| <b>Größe</b> |  |
| <b>Skalierung</b> <i>0.0 - 5.0</i> | Legen Sie die einheitliche Skalierung für jede Kachel fest. |
| <b>Zufällige Skalierung</b> <i>0.0 - 1.0</i> | Einheitliche Skalierung für jede Kachel zufällig anpassen. |
| <b>Keine Überlappung skalieren</b> <i>0.0 - 1.0</i> | Gleichmäßiges Skalieren des Zufalls, jedoch nur nach unten, um überlappende Kacheln zu vermeiden. Sollte nicht in Verbindung mit den beiden vorherigen Parametern verwendet werden. |
| <b>Zuordnungsmultiplikator skalieren</b> <i>0.0 - 1.0</i> | Legen Sie den Einfluss der Skalierungskarte fest. |
| <b>Größe</b> <i>0.0 - 1.0</i> | Ermöglicht eine ungleichmäßige Skalierung von Kacheln. |
| <b>Größenverhältnis von Bg-Steigung</b> <i>0.0 - 1.0</i> | Verwendet die Steigung der Hintergrundzuordnung (berechnet als Normal), um Kacheln nicht gleichmäßig zu skalieren. Simuliert Verformungen der Perspektive. |
| <b>Größe nach X/Y-Mengenverhältnis</b> <i>0.0 - 1.0</i> | Ungleichmäßige Skalierung zum Ausgleich eines unterschiedlichen Verhältnisses in X- und Y-Beträgen. |
| <b>Position</b> |  |
| <b>Position zufällig</b> <i>0.0 - 2.0</i> | Position mit zufälligem Versatz für jede Kachel |
| <b>Zufallsverteilung</b> <i>Gaußsch, einheitlich</i> | Legt die Berechnung fest, die für den vorherigen Parameter verwendet werden soll. Macht keinen großen Unterschied, auffälliger mit hohen Zahlen. Gaußsche Proportionen neigen dazu, eine gleichmäßigere Verteilung zu geben. |
| <b>Vektorzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Einfluss des Vektor-Eingabe-Map auf Offsets. |
| <b>Horizontaler Versatz</b> <i>-2.0 - 2.0</i> | Globaler horizontaler Versatz. |
| <b>Vertikaler Versatz</b> <i>-2.0 - 2.0</i> | Globaler vertikaler Versatz. |
| <b>Out-of-Bounds-Option</b> <i>Form skalieren, Position beschränken</i> | Aktion, die ausgeführt wird, wenn eine Kachel außerhalb des gültigen Bereichs angezeigt wird. |
| <b>Drehung</b> |  |
| <b>Drehung</b> <i>0.0 - 1.0</i> | Dreht alle Kacheln global. |
| <b>Drehung zufällig</b> <i>0.0 - 1.0</i> | Dreht sich willkürlich pro Kachel. |
| <b>Drehung aus Bg-Steigung</b> <i>0.0 - 1.0</i> | Verwendet die Steigung der Hintergrundzuordnung (berechnet als &quot;Normal&quot;), um Kacheln zu drehen. Kann verwendet werden, um Formen auf Steigungen nach oben oder unten zeigen zu lassen. |
| <b>Rotation Map-Multiplikator</b> <i>0.0 - 1.0</i> | Überblendungen der Auswirkungen des Rotation Map auf die Drehung pro Kachel. |
| <b>Vektorzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Überblendungen der Auswirkungen des Rotation Map auf die Drehung pro Kachel. |
| <b>Height</b> |  |
| <b>Automatische Anpassung der Skalierung des Heights</b> <i>False/True</i> | Passt das Height automatisch in Relation zum Hintergrund an, anstatt einen absoluten Bereich zu definieren. Ermöglicht weniger oder mehr Kontrolle. |
| <b>Height-Offset</b> <i>-1.0 - 1.0</i> | Modifizierer zum gleichmäßigen Verschieben/Versetzen aller Kacheln durch den Bereich des Heights. |
| <b>Height-Offset zufällig</b> <i>0.0 - 1.0</i> | Ändert den Height-Offset auf Kachelbasis nach dem Zufallsprinzip. |
| <b>Height-Versatzzuordnungs-Multiplikator</b> <i>0.0 - 1.0</i> | Modifizierer zum Festlegen des Einflusses der Offset-Map. |
| <b>Height-Skalierung</b> <i>0.0 - 1.0</i> | Modifizierer zum gleichmäßigen Skalieren/Erweitern aller Kacheln über den Bereich des Heights. Im Gegensatz zum Offset werden dabei Werte wie der Kontrast weiter auseinander getrieben. |
| <b>Zufällige Skalierung des Heights</b> <i>0.0 - 1.0</i> | Ändert die Height-Skalierung nach dem Zufallsprinzip pro Kachel. |
| <b>Height-Skalierungszuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Modifizierer zum Festlegen des Einflusses der Skalierungszuordnung. |
| <b>Mit Hintergrund konform</b> <i>0.0 - 1.0</i> | Wirkt sich auf die Überblendung von Kacheln mit dem Hintergrund aus. Keine konformen Mittel Höhenkarten bleiben starr, konforme Mittel folgen der Hintergrundform. Gut für Blätter oder Stöcke zum Beispiel. |
| <b>Glätten des konformen Hintergrunds</b> <i>0.0 - 2.0</i> | Glättungswert für vorherigen Effekt, um falsche oder extreme Variationen zu vermeiden. |
| <b>Neigung von Bg-Steigung</b> <i>0.0 - 1.0</i> | Anpassen/Steigung des Heights der Kachel, gesteuert durch die Steigung des Hintergrunds (berechnete Normalwerte). |
| <b>Smoothness der Hintergrund-Steigung</b> <i>0.0 - 2.0</i> | Glättungswert für vorherigen Effekt, um falsche oder extreme Variationen zu vermeiden. |
| <b>Schwarze Pixel ausschneiden</b> <i>False/True</i> | Mit dieser Option ignorieren Sie schwarze (0) Pixel aus Kachelgrundformen. |
| <b>Reduzierte Musterbasis</b> <i>False/True</i> | Passt das Kachelmischverhalten mit dem Hintergrund an: -Kacheln schneiden sich entweder mit dem Hintergrund (False) oder überschreiben den Hintergrund, wenn sie niedriger sind. |
| <b>Maskieren</b> |  |
| <b>Zufällige Maske</b> <i>0.0 - 1.0</i> | Blendet Kacheln zufällig aus. Je höher dieser Wert ist, desto mehr Kacheln werden ausgeblendet. |
| <b>Zufällige Maskenzuordnungsvervielfacher</b> <i>0.0 - 1.0</i> | Schwellenwert für Maskenzuordnung, wenn mit dem Ausblenden von Kacheln begonnen werden soll. |
| <b>Maske aus Bg-Steigung</b> <i>-1.0 - 1.0</i> | Verwendet die Steigung der Hintergrundzuordnung (berechnet als Normal), um Kacheln auszublenden. |

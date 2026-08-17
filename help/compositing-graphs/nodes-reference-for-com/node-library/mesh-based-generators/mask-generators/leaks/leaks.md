---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Lecks", um Leckmuster auf der Grundlage von Gittergeometrie zu generieren, um Wasserflecken und Flüssigkeitseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lecks
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# Lecks

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## Lecks

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Dieser Knoten stellt undichte Streifen von Dirt und Schmutz dar, die von scharfen Kanten stammen. Da Streifen mit gebackener Position erzeugt werden, laufen sie immer nach unten.

Stellen Sie sicher, dass Sie die Variationsmaske ändern: Da es die Platzierung von Streifen vorantreibt, kann es einen viel größeren Einfluss haben als bei anderen Maskengeneratoren.

## Parameter

### Eingaben

* **Position**: *Graustufen-Eingabe*\
  Gebackener Lageplan, verwendet für Streakanweisungen. Erforderlich!
* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für die Platzierung von Streifen. Erforderlich!
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung. Empfohlen, aber Sie können stattdessen flaches Weiß verwenden.
* **Normaler Weltraum**: *Farbeingabe*\
  Baked World Space Normalmap, verwendet für Streak-Richtung. Erforderlich!
* **Variationsmaske**: *Graustufen-Eingabe*\
  Optionale Variationsmaske, aktivieren Sie diese Option, indem Sie die Überschreibung auf &quot;True&quot; setzen.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Gesamtwert des Ergebnisses. Blendet den Effekt schrittweise ein und beeinflusst auch die Länge. Sollte ziemlich hoch eingestellt werden, um lange Tropfen zu erhalten.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Variation**: *0.0 - 1.0* Legt den Umfang der groß angelegten Variation fest, die zum Maskieren der Streifen verwendet wird. Wenn Sie diesen Wert auf 0 setzen, werden vollständig gleichmäßige Streifen erzeugt, also vermeiden Sie dies.
* **Länge**: *0.0 - 8.0* Länge der Streifen-Tropfen. Wenn dieser Wert in kleinem Maßstab zu hoch eingestellt wird, führt dies zu einer sichtbaren Schrittweite. Experimentiere auch mit dem Level.
* **Occlude**: *X, Y, Z, None* Legt fest, welche Richtung der AO beeinflussen soll.
* **Variationsmaske überschreiben**: *Falsch/Wahr* Aktiviert das Überschreiben der Variationsmaske mit einem benutzerdefinierten Eingabebereich. Die Verwendung von Masken mit geringerer Dichte kann interessant sein und ist eine gute Möglichkeit, die Tropfenbildung zu steuern.

## Beispielbilder

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>

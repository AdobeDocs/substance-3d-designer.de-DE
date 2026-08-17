---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Lederbekleidung", um auf der Grundlage von Gitterkrümmung und Kontaktpunkten Verschleißmasken auf Lederoberflächen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lederbekleidung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Lederbekleidung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## Lederbekleidung

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske repräsentiert den Verschleiß mit einem Ledermuster, mit mehr Verschleiß an Kanten basierend auf der Krümmung. Die Funktionalität ähnelt der von [Fiber Glass Edge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) und weist meist dieselben Parameter auf.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für die Kantenplatzierung. Erforderlich!
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map hat bestimmte Bereiche verdeckt. Empfohlen, aber nicht erforderlich.
* **Schmutz-Eingabe**: *Graustufen-Eingabe*\
  Optionaler Schmutz-Map-Eingangssteckplatz, der über den Parameter &quot;Benutzerdefinierten Schmutz verwenden&quot; umgeschaltet werden kann.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Verschleißstufe**: *0.0 - 1.0* Legt den globalen Verschleißgrad fest und zeigt ihn allmählich an.
* **Kontrast tragen**: *0.0 - 1.0* Legt den Kontrast des Effekts fest.
* **Schmutz-Betrag**: *0.0 - 1.0* Legt die Menge an Schmutz (Standardledermuster) fest, die zwischen den Kanten überblendet werden soll.
* **Maskieren der Umgebungsgeräusche**: *0.0 - 1.0* Legt fest, inwieweit der AO die Verschleißeffekte maskiert.
* **Krümmungsgewicht**: *0.0 - 1.0* Legt fest, inwieweit die Kanten der Krümmung das Endergebnis beeinflussen. Selbst wenn der Wert auf 0 gesetzt ist, benötigen Sie immer noch eine Krümmungskarte.
* **Benutzerdefinierten Schmutz verwenden**: *Falsch/Wahr* Aktiviert das Überschreiben des integrierten Standardledermusters. Verwenden Sie stattdessen einen benutzerdefinierten Eingabefach.

## Beispielbilder

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Verwenden Sie den Dirt-Knoten, um Dirt-Akkumulationsmasken basierend auf Gitterkrümmung, -position und -Verdeckung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Verschmutzung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# Verschmutzung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## Verschmutzung

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt Dirt in verdeckten und abgesenkten Kanten und Ecken dar, die auf dem gebackenen AO und der Krümmung basieren.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung. Erforderlich!
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung. Erforderlich!
* **Schmutz-Eingang**: *Graustufen-Eingabe*\
  Benutzerdefinierte Schmutz-Map-Eingabe, optional, aktiviert durch Parameter.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Normaler Weltraum**: *Farbeingabe*\
  Nur für Triplanar verwendet.
* **Position**: *Farbeingabe*\
  Nur für Triplanar verwendet.

### Parameter

* **Dirt-Ebene**: *0.0 - 1.0* Hauptsteuerung für die Menge des Dirts.
* **Kontrast des Dirts**: *0.0 - 1.0* Steuert den Hauptkontrast für den Dirt in der Maske.
* **Schmutz-Betrag**: *0.0 - 1.0* Legt fest, wie grunzig der Dirt ist. Setzen Sie den Wert auf 0, um einen einwandfreien Dirt zu erzielen.
* **Kantenmaskierung**: *0.0 - 1.0* Menge des Dirts, der von erhöhten Kanten entfernt werden soll (auf der Grundlage der Krümmungszuordnung).
* **Benutzerdefinierten Schmutz verwenden**: *Falsch/Wahr* Aktiviert die Verwendung der benutzerdefinierten Schmutz-Zuordnungseingabe anstelle des integrierten Schmutz.
* **Schmutz-Skalierung**: *1 - 16* Legt die Kachelungsskala der Schmutz-Details fest.
* **Triplanar verwenden**: *Falsch/Wahr* Verwenden Sie [Triplanare Projektion](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) für die Schmutz-Zuordnung, entfernt Nähte.
* **Triplanarer Mischkontrast**: *0.001 - 1.0* Legt den Kontrast der triplanaren Projektion fest.

## Beispielbilder

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Lackabnutzung", um Lackabnutzungsmasken basierend auf der Gittergeometrie zu generieren, um realistische Lackabtrageeffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lackverschleiß
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# Lackverschleiß

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## Lackverschleiß

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske repräsentiert das Abtragen von Farbe an den Rändern.

## Parameter

### Eingaben

* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Variationsmaske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt den gesamten Farbabrieb fest, der allmählich sichtbar wird.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Verdeckung**: *0.0 - 1.0* Legt fest, wie stark der gebackene AO den Verschleiß in dunkleren Bereichen verhindert.
* **Radius**: *0.0 - 2.0* Legt fest, wie weit sich der Chipping-Effekt von konvexen Kanten ausbreitet.
* **Variation**: *0.0 - 1.0* Legen Sie die Stärke der Variation (Schmutz) fest, die in den Effekt übergeht.
* **Variationsmaske überschreiben**: *Falsch/Wahr* Aktiviert den Eingabesteckplatz für die benutzerdefinierte Variation (Schmutz).

## Beispielbilder

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>

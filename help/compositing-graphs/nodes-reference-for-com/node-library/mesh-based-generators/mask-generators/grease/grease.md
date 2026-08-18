---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Fett", um Fettansammlungsmasken basierend auf der Gittergeometrie und den Kontaktflächen zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fett
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# Fett

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## Fett

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske ist speziell für Schriftarten und andere spezifische Bereiche vorgesehen. Generiert eine Hautfettmaske für Bereiche mit geringer Thickness.

## Parameter

### Eingaben

* **Thickness**: *Graustufen-Eingabe*\
  Thickness-Map, auf der der gesamte Effekt basiert. Erforderlich!
* **Rauschen**: *Graustufen-Eingabe*\
  Optionale Rauschkarte zum Überschreiben von Fett-Schmutz mit.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Gesamtmenge des Effekts fest, der angezeigt werden soll.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Schwellenwert für Thickness**: *0.0 - 1.0* Legt eine minimale Thickness fest, bei der der Effekt angezeigt werden soll. ebenso wichtig wie die Stufe; Passe dies an deine Thickness an.
* **Rauschen überschreiben**: *Falsch/Wahr* Einstellung zum Überschreiben der internen Schmierfett-Schmutz-Zuordnung mit benutzerdefiniertem Eingabesteckplatz.

## Beispielbilder

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>

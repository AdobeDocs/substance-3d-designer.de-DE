---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Dripping Rost", um Rost-Tropfmuster basierend auf der Gittergeometrie und der Schwerkraftrichtung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tropfender Rost
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# Tropfender Rost

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## Tropfender Rost

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt Rost-Flocken und Flecken dar, wobei die Lecks nach unten verlaufen.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Eine fertig gestellte oder generierte Karte, die Ihnen bei der Platzierung des Rosts hilft.
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Eine fertig gestellte oder generierte Karte, die Ihnen bei der Platzierung des Rosts hilft.
* **Position**: *Graustufen-Eingabe*\
  Gebackene oder generierte Karte für Tropfrichtungen.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Rost-Verteilung**: *0.0 - 1.0* Hauptsteuerung für die Menge des Rosts.
* **Kontrast des Rosts**: *0.0 - 1.0* Legt den Kontrastumfang in generierten Rost-Flecken fest (wirkt sich nicht auf Tropfen aus).
* **Smoothness wird verteilt**: *0.0 - 1.0* Stärke des Weichzeichnungs-/Verschmierungseffekts, der auf die Rost-Flecken angewendet werden soll.
* **Drips-Intensität**: *0.0 - 1.0* Legt die Stärke und die Länge der Tropfen von Flecken fest.
* **Drips-Smoothness**: *0.0 - 1.0* Menge an Unschärfe und Glättung, die auf Tropfen angewendet werden soll.
* **Anzahl der Drips-Samples**: *0 - 32* Legt die Qualitätsstufe (Schritte) für den Tropfeneffekt fest. Hat einen leichten Einfluss auf die Geschwindigkeit.

## Beispielbilder

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>

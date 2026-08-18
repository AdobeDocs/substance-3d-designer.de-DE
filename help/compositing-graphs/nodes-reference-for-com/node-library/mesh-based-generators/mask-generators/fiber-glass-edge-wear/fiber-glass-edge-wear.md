---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Edge Wear "Glasfaserknoten", um Verschleißmasken auf Glasfaserkanten basierend auf der Gitterkrümmung zu generieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glasfaser-Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Glasfaser-Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## Glasfaser-Edge Wear

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Stellt eine Maske dar, die speziell für einen Fiberglas-Verschleiß bestimmt ist, der möglicherweise für Tuch verwendet werden könnte. Durch die sehr geflieste, sich wiederholende Art der Fasern kann die Triplanar-Vermischung optional aktiviert werden.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für die Kantenhervorhebung. Erforderlich!
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map zum Maskieren von verdeckten Bereichen. Nicht erforderlich, aber definitiv empfehlenswert.
* **Schmutz-Eingabe**: *Graustufen-Eingabe*\
  Optionaler benutzerdefinierter Steckplatz zum Überschreiben des Fasermusters.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Normaler Weltraum**: *Farbeingabe*\
  Nur für Triplanar verwendet.
* **Position**: *Farbeingabe*\
  Nur für Triplanar verwendet.

### Parameter

* **Verschleißstufe**: *0.0 - 1.0* Wie bei einem [Histogrammscan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) wird der Verschleiß nach und nach aufgedeckt.
* **Kontrast tragen**: *0.0 - 1.0* Legt den Gesamteffektkontrast fest.
* **Kanten-Smoothness**: *0.0 - 16.0* Legt Anschnitt/Weichzeichnung von hervorgehobenen Kanten fest.
* **Schmutz-Betrag**: *0.0 - 1.0* Legt fest, wie viel des Fasereffekts zwischen den Kanten überblendet werden soll. Mit dem Wear Level kannst du das zusammen optimieren, um maximale Kontrolle zu erhalten.
* **Maskieren der Umgebungsgeräusche**: *0.0 - 1.0* Legt den Einfluss fest, den AO auf das Ausblenden des Effekts hat.
* **Krümmungsgewicht**: *0.0 - 1.0* Legt den Umfang des Einflusses fest, den konvexe Kanten aus der Krümmung haben.
* **Benutzerdefinierten Schmutz verwenden**: *Falsch/Wahr*&#x200B;Überschreibt integrierte Fasern mit benutzerdefinierter Karte.
* **Triplanar verwenden**: *Falsch/Wahr* Ermöglicht es [Triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md), Nähte auszublenden.
* **Triplanarer Mischkontrast**: *0.0 - 1.0* Steuert den Kontrast des Triplanar-Effekts.

## Beispielbilder

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Brick Generator", um prozedurale Brick-Muster mit anpassbaren Größen-, Offset- und Mörteleigenschaften zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ziegel-Generator
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Ziegel-Generator

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## Ziegel-Generator

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Erweiterter Brick-Pattern-Generator. Verfügt über viele Optionen zum spezifischen Generieren von künstlich geschaffenen Backsteinmustern.

Weitere Optionen finden Sie unter [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

## Parameter

* **Steine**: *1 - 64* Legt die Anzahl der Steine in X- und Y-Achsen fest.
* **Abschrägung**: *0.0 - 1.0*&#x200B;Ändert das Abschrägungsprofil für die Ziegel, ermöglicht es, in zwei Richtungen zu wechseln, und setzt Abrissprofil und Eckenrundung ein.
* **Verhältnis beibehalten**: *Falsch/Wahr* Das Profil &quot;Abgeflachte Kante&quot; wird an die Größe des Steins gebunden oder nicht.
* **Lücke**: *0.0 - 1.0* Zwischen den Steinen verbleibende Lücke. Beachten Sie, dass durch die abgeflachte Kante auch eine Lücke entsteht. Wenn Sie also die abgeflachte Kante einstellen, müssen Sie diesen Parameter korrigieren.
* **Mittlere Größe**: *0.0 - 1.0* Offset für Brickmuster, ändert die Größe aller anderen Spalten oder Zeilen.
* **Height**: *-1.0 - 1.0*&#x200B;Ändert Height-Profile. Ermöglicht die Einführung von Luminanzvariationen und allen Arten der Randomisierung.
* **Steigung**: *-1.0 - 1.0* Führt eine Steigung pro Stein ein, als ob bestimmte Steine schräg liegen.
* **Offset**: *0.0 - 1.0*\
  Verschiebt die Steine auf Zeilenbasis und wirkt sich auf den Abstand pro Zeile aus.
* **Quadratische Ausbreitung**: *False/True*\
  Ermöglicht die Kompensation von Quetsch und Dehnung bei nicht quadratischen Verhältnissen.

## Beispielbilder

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>

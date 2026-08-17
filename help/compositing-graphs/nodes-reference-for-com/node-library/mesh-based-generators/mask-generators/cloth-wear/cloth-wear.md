---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Stoffverschleiß", um auf der Grundlage von Gitterkrümmung und Kontaktflächen Verschleißmasken auf Stoffoberflächen zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tuchbekleidung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Tuchbekleidung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## Tuchbekleidung

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Die Maske stellt die gerahmten Kanten von Stoffmaterialien dar. Es verwendet eine Stoffdetail-Höhenkarte, die den größten Teil des Aussehens bestimmt; ohne entsprechende Karte sieht der Effekt sehr einfach aus.

## Parameter

### Eingaben

* **Height der Kleidung**: *Graustufen-Eingabe*\
  Height nur für das Stoffmuster. Dies ist nicht das Height Ihres (gebackenen) Objekts, sondern ein gekacheltes Detailmuster.
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.
* **Krümmung**: *Graustufen-Eingabe*\
  Gebackene/erzeugte Krümmung, um erhöhte Kanten zu bestimmen.

### Parameter

* **Anzahl der harten Kanten**: *0.0 - 1.0*
* **Weiche Kante tragen**: *0.0 - 5.0* Bestimmt, wie weichgezeichnet/weich die abgenutzten Kanten sind.

## Beispielbilder

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>

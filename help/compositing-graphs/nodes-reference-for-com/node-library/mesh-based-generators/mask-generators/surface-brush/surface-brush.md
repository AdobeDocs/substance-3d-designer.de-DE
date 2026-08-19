---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Oberflächenpinsel", um Masken basierend auf der Oberflächenausrichtung zu generieren, um gerichtete Verwitterungs- und Abnutzungseffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oberflächenpinsel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Oberflächenpinsel

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## Oberflächenpinsel

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Diese Maske stellt einen interessanten Effekt des Metallpinselns auf eine Objektoberfläche dar, verdeckt von Objektgeometrie und AO.

## Parameter

### Eingaben

* **Normaler Weltraum**: *Farbeingabe*
* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Position**: *Graustufen-Eingabe*
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die globale Effektstufe fest, die allmählich sichtbar wird.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Scratches Länge**: *0.0 - 8.0* Legt die Länge von Kratzern fest. Kleinere Werte sind mehr wie Punkte, höhere Werte sind lange Streifen.
* **Achse verschließen**: *X, Y, Z, keine* Achse des Objekts, das Kratzer erhalten soll. Ändert nicht die Richtung der Kratzer.
* **Achsenintensität verdecken**: *0.0 - 1.0* Stärke des Effekts &quot;Verdeckung der Achse&quot;.
* **Verdeckung**: *0.0 - 1.0* Stärke des AO bei verdeckenden Kratzern.
* **Scharfzeichnungsintensität**: *0.0 - 1.0* Legen Sie den Grad der Nachschärfung fest, der auf die Kratzer angewendet werden soll.

## Beispielbilder

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>

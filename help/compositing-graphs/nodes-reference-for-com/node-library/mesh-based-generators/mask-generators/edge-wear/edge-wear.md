---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Edge Wear , um Verschleißmasken an Netzkanten zu generieren, um realistische Kantenschäden und Wettereffekte zu erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**In:** *Mesh-basierte Generatoren**/Masken-Generatoren*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Generiert eine Schwarzweißmaske auf der Grundlage von durch Baking erzeugte Map und Benutzereinstellungen. Ähnlich wie [Smart Masks](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Dieser Knoten stellt den Verschleiß von Objektkanten dar. Es verfügt über einige Parameter, ist aber nicht am einfachsten zu verwenden: Wir empfehlen Ihnen, herumzuspielen und ein Gefühl für die Dinge zu bekommen. Der Knoten ist recht leistungsstark, obwohl keine benutzerdefinierte Überschreibungsmaske ausgeführt werden kann.

## Parameter

### Eingaben

* **Krümmung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung
* **Maske (optional)**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Ebene**: *0.0 - 1.0*\
  Legt die Gesamtverteilung des Effekts fest.
* **Kontrast**: *0.0 - 1.0*\
  Passt den Kontrast des Ergebnisses an.
* **Schwellenwert**: *0.0 - 1.0*&#x200B;Ähnlich wie &quot;Level&quot; legt die Gesamtverteilung des Effekts fest.
* **Kantenbreite**: *0.0 - 1.0* Legt die Fülle des Markierungseffekts fest. Reduzieren, um sie sparsamer zu machen.
* **Störung**: *0.0 - 1.0*\
  Legt die Stärke des Rauschens fest, das zum Aufbrechen der Smoothness hinzugefügt werden soll.

## Beispielbilder

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>

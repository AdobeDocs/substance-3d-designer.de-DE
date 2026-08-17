---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Leder-Verwitterung", um Ledermaterialien auf der Grundlage einer Gitterkrümmung Verschleißmuster und Alterungseffekte hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lederwetter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Lederwetter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## Lederwetter

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Vollmaterial-Effekt, der auf mehreren Kanälen gleichzeitig funktioniert. Es fügt einen zufälligen Lederverschleißeffekt hinzu, mit Kontrolle für Alter und Schmutzigkeit. Es ähnelt [Fabric Weathering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), wurde aber speziell auf Leder abgestimmt.\
Dieser Effekt funktioniert nicht sehr gut, es sei denn, Sie haben die richtigen gebackenen AO und World Space Normalmaps angeschlossen, da es diese benötigt, um alles adäquat zu berechnen und zu generieren.

Vergewissern Sie sich, dass Sie die [Link Creation Modes](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) vollständig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

## Parameter

### Eingaben

* **Ambient-Verdeckung**: *Graustufen-Eingabe*\
  Durch Baking erzeugte Map für interne Effekte und Maskierung.
* **Normaler Weltraum**: *Farbeingabe*
* **Maske** : *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Erweitert**
  * **Normales Format**: *DirectX, OpenGL*\
    Wechselt zwischen verschiedenen Normalmap-Formaten (invertiert den grünen Kanal).
  * **Maske**: *False/True*\
    Schaltet die Verwendung der Maskenkarte ein oder aus.
* **Effekt**
  * **Dust**: *0.0 - 1.0*&#x200B;Überblendungen mit einer dunkleren Dust, basierend auf den Bereichen, die in der Normalmap des Weltraums nach oben zeigen.
  * **Schmutzigkeit**: *0.0 - 1.0*&#x200B;Überblendungen in einem globalen Dirt-/Verwischungseffekt, der hauptsächlich auf verdeckten (dunklen) Bereichen in der AO basiert.
  * **Kanten, die** tragen: *0.0 - 1.0* Fügt Kantenschärfe/-intensivierung hinzu, basierend auf &quot;Material Normal&quot;.
  * **Verwendet**: *0.0 - 1.0* Vermischt sich in einem globalen, abgenutzten Lederlook.
  * **Alter**: *0.0 - 1.0* Verblendungen in einem abgenutzten Lederlook in Falten basierend auf AO. Die Platzierung wird stark von Age Treshold beeinflusst.
  * **Altersgrenze**: *0.0 - 1.0* Legt den Aussehen-Schwellenwert für den Effekt &quot;Alter&quot; fest.
  * **Skalierung der Risse**: *1.0 - 16.0* Legt die Tiefe des abgenutzten Leders von Used and Age fest.
  * **Risse-Verkrümmungsintensität**: *0.0 - 1.0* Legt die Intensität des abgenutzten Leders von Used and Age fest.
  * **Scratches mit scharfen Kanten skalieren**: *1.0 - 32.0*
  * **Intensität der Verkrümmung der scharfen Kanten der Scratches**: *0.0 - 1.0*
  * **Lederentsättigung verwendet**: *0.0 - 1.0* Legt die Sättigung des verschlissenen Lederlooks von &quot;Age&quot; und &quot;Used&quot;-Effekten fest.
  * **Verwendete Lederhelligkeit**: *0.0 - 1.0* Legt die Helligkeit des abgenutzten Lederlooks aus den Effekten &quot;Alter&quot; und &quot;Verwendet&quot; fest.
* **Überblenden**
  * **Diffuse Intensität**: *0.0 - 1.0*\
    Mischungsstärke des Diffusors.
  * **Grundfarbintensität**: *0.0 - 1.0*\
    Mischungsstärke der Grundfarbe.
  * **Normalintensität**: *0.0 - 1.0*\
    Die Füllkraft von &quot;Normal&quot;.
  * **Specular-Intensität**: *0.0 - 1.0*\
    Die Stärke des Speculars.
  * **Glanzintensität**: *0.0 - 1.0*\
    Die Stärke des Glanzes beim Mischen.
  * **Intensität der Raueit**: *0.0 - 1.0*\
    Die Stärke der Raueit.
  * **Umgebungsintensität der Verdeckung**: *0.0 - 1.0*\
    Mischfestigkeit der Ambient-Verdeckung.
  * **Height-Intensität**: *0.0 - 1.0*\
    Die Stärke des Heights beim Mischen.

## Beispielbilder

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>

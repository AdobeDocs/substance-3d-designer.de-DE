---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Weiche Struktur", um Verschleiß- und Alterungseffekte auf Basis von Gittergeometrie und Krümmung zu Gewebematerialien hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gewebeverwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# Gewebeverwitterung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## Gewebeverwitterung

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Vollmaterial-Effekt, der auf mehreren Kanälen gleichzeitig funktioniert. Es fügt einen zufälligen Stoff-Verschleißeffekt hinzu, mit Kontrolle für Alter und Schmutzigkeit.\
Dieser Effekt funktioniert nicht sehr gut, es sei denn, Sie haben die richtigen gebackenen AO und World Space Normalmaps angeschlossen, da es diese benötigt, um alles adäquat zu berechnen und zu erzeugen.

Vergewissern Sie sich, dass Sie die [Link Creation Modes](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) vollständig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

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
  * **Verwendet**: *0.0 - 1.0*&#x200B;Überblendungen in sehr dunklem, akkumuliertem Dirt in Falten, basierend auf AO. Maximal- und Minimalwerte sind in der Regel sehr extrem, verwenden Sie diese mit Vorsicht.
  * **Alter**: *0.0 - 1.0*&#x200B;Überblendungen über ein globales Kachelverschleißmuster. Die Einstellung &quot;Schwellenwert&quot; unten steuert den AO-Einfluss. Maximal- und Minimalwerte sind in der Regel sehr extrem.
  * **Altersgrenze**: *0.0 - 1.0* Legt den Umfang fest, in dem der AO den Age-Parameter beeinflusst.
  * **Alter steigt**: *0.0 - 1.0* Steuert das Mischen von subtilen zusätzlichen Falten im Effekt &quot;Alter&quot;.
  * **Scratches mit scharfen Kanten skalieren**: *1.0 - 32.0* Legt die Skalierung kleiner Kratzer fest, die hauptsächlich den Effekt &quot;Verwendet und alt&quot; wegkratzen.
  * **Intensität der Verkrümmung der scharfen Kanten der Scratches**: *0.0 - 1.0* Legt die Intensität der Verformung für die oben genannten kleinen Kratzer fest.
  * **Alte Fabric-Entsättigung**: *0.0 - 1.0* Steuert die Entsättigung des Effekts Alter.
  * **Alte Fabric-Helligkeit**: *0.0 - 1.0* Steuert die Helligkeit des Effekts Alter. *Dies ist ein sehr wichtiger Parameter, der geändert werden muss, um das gewünschte Aussehen zu erhalten. Die Ergebnisse können jedoch extrem sein: mit subtilen Änderungen verwenden.*
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

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>

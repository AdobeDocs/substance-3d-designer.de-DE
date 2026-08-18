---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Moosverwitterung", um Materialien Mooswachstumsmuster basierend auf der Gitterkrümmung und -position hinzuzufügen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Moosverwitterung
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# Moosverwitterung

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## Moosverwitterung

**In:** *Mesh-basierte Generatoren**/Wetter*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist ein Vollmaterial-Effekt, der auf mehreren Kanälen gleichzeitig funktioniert. Es erzeugt einen überwucherten Mooseffekt mit einer einzigen Steuerung für die Propagierung.

Dieser Effekt eignet sich am besten für eine fertig gestellte Weltraum-Positions-Map und eine zusätzliche Höhenmap. Dies ist zwar keine exakte Anforderung, verleiht dem Effekt aber eine glaubwürdigere Platzierung.

Vergewissern Sie sich, dass Sie die [Verknüpfungserstellungsmodi](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) richtig verstehen, wenn Sie mit vollständigen Materialien arbeiten.

## Parameter

### Eingaben

* **Position**: *Farbeingabe*\
  Weltall-Position gebacken.
* **Height** : *Graustufen-Eingabe*\
  Zusätzliche Höhenzuordnungs-Eingabe.
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
  * **Moosweitergabe**: *0.0 - 1.0* Legt die Ausbreitung des Mooses fest. Wächst in Stufen von leichter Bedeckung bis zu schwerem, dickem, dunklem Moos.
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

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>

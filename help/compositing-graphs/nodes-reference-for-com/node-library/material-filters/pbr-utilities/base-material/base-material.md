---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Basismaterial", um Materialeigenschaften für die Neuerstellung physikalisch basierter Basismaterialien zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Basismaterial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# Basismaterial

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## Basismaterial

**In:** *Materialfilter/PBR-Dienstprogramme*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Der schnellste und einfachste Weg zum Erstellen eines Mehrkanalmaterials in [Adobe Substance 3D Designer](https://www.adobe.com/de/products/substance3d-designer.html). Dieser Knoten gibt ein gebündeltes vollständiges Material zurück, das auf einfachen Farbeinstellungen und -werten basiert. Diese kann dann als Platzhalter verwendet werden oder um sie zu einem komplexen Material zu verfeinern.

Der Knoten ist sehr nützlich, wenn Sie vollständige Requisiten texturieren und mehrere Materialien mischen möchten. Sie können sogar jedes einzelne Material von diesem Knoten aus beginnen, ohne jemals eine komplexe Materialbasis zu benötigen.

## Parameter

### Eingaben

* Optionale Eingänge für jeden Kanal, der mit den Schaltern in &quot;Benutzerdefinierte Eingänge&quot; umgeschaltet werden kann.

### Parameter

* **PBR-Workflow**: *Metall - Raueit, Specular - Glanzgrad* Legt das verwendete PBR-Modell fest.
* **Materialvorgabe**: *Benutzerdefiniert, Dielektrisch, Gold, Silber, Aluminium, Eisen, Kupfer, Titan, Nickel, Kobalt, Platin* Kurze Abkürzung zum Erstellen bestimmter Metalle. Deaktiviert irrelevante Optionen.
* **Grundfarbe**: *(Farbwert)*Volltonfarbe, die für die Grundfarbe verwendet wird.
* **Metallisch**: *(Graustufenwert)*Für &quot;Metallisch&quot; verwendeter Wert.
* **Diffuse Farbe**: *(Farbwert)*Für &quot;Diffus&quot; verwendete Volltonfarbe.
* **Specular**: *(Farbwert)*Für Specular verwendete Volltonfarbe.
* **Specular-Vorgaben**: *Kunststoff, Holz, Stein, Ziegel, Sand, Beton, Gewebe, gerostetes Metall, Wasser, Eis, Glas* Optionale Schnellvorgaben zur Einstellung der PBR-korrekten Specular-Werte.
* **Specular-Bereich**: *0.0 - 1.0* Passt den Specular-Bereich an.
* **Raueit - Glossarität**
  * **Rohheitswert**: *(Graustufenwert)*Legen Sie den globalen Basisrauheitswert fest, wenn Kanal aktiv ist.
  * **Glossarwert**: *(Graustufenwert)*Volltonfarbe wird für Glossiness verwendet, wenn Kanal aktiv ist.
  * **Schmutz-Betrag**: *0.0 - 1.0* Umfang, in dem die optionale Schmutz-Map-Eingabe in Glanz oder Raueit überblendet wird.
  * **Schmutz-Kachelung**: *1 - 16* Umfang, in dem die optionale Schmutz-Karte durch Kacheln gekennzeichnet wird.
  * **Benutzerdefinierte Schmutz-Eingabe**: *Falsch/Wahr* Aktiviert oder deaktiviert die optionale benutzerdefinierte Schmutz-Zuordnung .
* **Normal**
  * **Normal von Height-Intensität**: *0.0 - 16.0* Konvertiert optional die benutzerdefinierte Höhenkarte in normal und gibt diese als materielle Normalmap zurück.
* **Height**
  * **Height-Position**: *0.0 - 1.0* Fester Wert wird für die Height-Ausgabe verwendet.
  * **Height-Bereich**: *0.0 - 1.0* Legt den Einfluss der benutzerdefinierten Höhenzuordnung fest, sofern aktiviert.
* **Benutzerdefinierte Zuordnungen**
  * Schaltet alle benutzerdefinierten Maps ein bzw. aus, wobei diese anstelle der festen Werte zurückgegeben werden.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Basismaterial", um Basismaterial-Eigenschaften für das Erstellen physikalisch basierter Material von Grund auf neu zu erstellen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Basismaterial
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# Basismaterial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/pbr-base-material.png){width="128px"}

<b>In:</b> Materialfiltern > PBR-Dienstprogramme

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Der schnellste und einfachste Weg zum Erstellen eines Mehrkanal-Materials in [Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html). Dieser Knoten gibt ein gebündeltes vollständiges Material zurück, das auf einfachen Farbflächeneinstellungen und -werten basiert. Diese kann dann als Platzhalter verwendet oder in ein komplexes Material eingearbeitet werden.

Dieser Knoten ist sehr nützlich, wenn Sie vollständige Requisiten texturieren und mehrere Materialien mischen möchten. Sie können sogar jedes einzelne Material von diesem Node aus starten, ohne jemals eine komplexe Material-Basis zu benötigen.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
|  | Optionale Eingänge für jeden Kanal, der mit den Schaltern in &quot;Benutzerdefinierte Eingänge&quot; umgeschaltet werden kann. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>PBR-Workflow</b> <i>Metall - Rauheit, Specular - Glanz</i> | Legt das verwendete PBR-Modell fest. |
| <b>Materialvorgabe</b> <i>Benutzerdefiniert, Dielektrisch, Gold, Silber, Aluminium, Eisen, Kupfer, Titan, Nickel, Kobalt, Platin</i> | Schneller Tastaturbefehl zur Herstellung bestimmter Metalle. Deaktiviert irrelevante Optionen. |
| <b>Grundfarbe</b> <i>(Farbwert)</i> | Für die Grundfarbe verwendete Volltonfarbe. |
| <b>Metallisch</b> <i>(Graustufenwert)</i> | Solider Wert für Metallic. |
| <b>Diffuse </b> <i>(Farbwert)</i> | Volltonfarbe für Diffuse. |
| <b>Specular</b> <i>(Farbwert)</i> | Für Specular verwendete Volltonfarbe. |
| <b>Specular-Vorgaben</b> <i>Kunststoff, Holz, Stein, Ziegel, Sand, Beton, Gewebe, rostetes Metall, Wasser, Eis, Glas</i> | Optionale Schnellvorgaben zum Festlegen von PBR-korrekten Specular-Werten. |
| <b>Specular-Bereich</b> <i>0.0 - 1.0</i> | Passt den Specular-Bereich an. |
| <b>Rauheit - Glanz</b> |  |
| <b>Wert der Rauheit</b> <i>(Graustufenwert)</i> | Legen Sie den globalen Basiswert der Rauheit fest, wenn der Kanal aktiv ist. |
| <b>Wert des Glanzes</b> <i>(Graustufenwert)</i> | Volltonfarbe für Glanz, wenn Kanal aktiviert ist. |
| <b>Schmutz-Betrag</b> <i>0.0 - 1.0</i> | Inwieweit der optionale Schmutz-Map-Eingang in Glanz oder Rauheit eingeblendet wird. |
| <b>Schmutz-Kachelung</b> <i>1 - 16</i> | Umfang der Kachelung der optionalen Schmutz-Karte durch. |
| <b>Benutzerdefinierte Schmutz-Eingabe</b> <i>False/True</i> | Aktiviert oder deaktiviert die optionale benutzerdefinierte Schmutz-Zuordnung . |
| <b>Normal</b> |  |
| <b>Normal von Height-Intensität</b> <i>0.0 - 16.0</i> | Konvertiert optional die benutzerdefinierte Höhenkarte in Normal und gibt diese als Material-Normalmap zurück. |
| <b>Height</b> |  |
| <b>Height-Position</b> <i>0.0 - 1.0</i> | Durchgezogener Wert für Height-Ausgabe. |
| <b>Height-Bereich</b> <i>0.0 - 1.0</i> | Legt den Einfluss der benutzerdefinierten Höhenkarte fest, sofern aktiviert. |
| <b>Benutzerdefinierte Zuordnungen</b> | Schaltet alle benutzerdefinierten Maps ein bzw. aus, wobei diese anstelle der festen Werte zurückgegeben werden. |

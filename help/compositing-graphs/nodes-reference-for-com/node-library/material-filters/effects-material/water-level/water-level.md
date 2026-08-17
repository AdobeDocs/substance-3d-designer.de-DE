---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Wasserstand", um Materialien auf der Grundlage des Heights für den Wasserstand zu mischen und realistische Wassereffekte zu erzielen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Wasserstand
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Wasserstand

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## Wasserstand

**In:** *Materialfilter/Effekte*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

All-in-One-Effekt, der einen Wasserpegel zu einem vollen Materialeinsatz hinzufügt. Das Eingabematerial muss über eine gute, hochwertige Höhenkarte verfügen, damit der Effekt funktioniert. Das Ergebnis ist PBR-korrekt.

## Parameter

### Eingaben

* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte.

### Parameter

* **Kanäle**\
  Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Wasserstand**: *0.0 - 1.0* Hauptsteuerung zum Anheben oder Absenken des Wasserspiegels.
* **Wasserdunkel**: *0.0 - 1.0* Legt allgemeine &quot;Transparenz&quot; des Wassers fest.
* **Kantennässe**: *0.0 - 1.0* Bestimmt, wie viel von einem feuchten Aussehen die Wasserränder haben sollen.
* **Kantenfeuchtigkeitsentfernung**: *0.0 - 1.0* Legt fest, wie weit die feuchten Kanten reichen.
* **Tiefen-Weichzeichnungsbetrag**: *0.0 - 1.0* Legt die Stärke der Weichzeichnung basierend auf der Tiefe unter Wasser fest. Ändert den Weichzeichnungsradius.
* **Tiefe-Weichzeichnungsdeckkraft**: *0.0 - 1.0* Bestimmt, wie viel Tiefe-Weichzeichnung eingeblendet wird. Diese Einstellung kann verwendet werden, um die Wirkung der Weichzeichnung zu verringern.
* **Schlammfarbe**: *(Farbwert)*Legt die Farbe des Schlammeffekts fest.
* **Schlamm-Tiefe**: *0.0 - 1.0* Legt die Tiefe fest, mit der Schlamm im Verhältnis zum Wasserstand auftritt.
* **Schlammdeckkraft**: *0.0 - 1.0* Legt die globale Deckkraft des Schlammeffekts fest.
* **Frost**: *0.0 - 1.0* Legt die Stärke des Frostes fest. Beginnt, von den Außenkanten aus sichtbar zu werden, und bewegt sich nach innen.
* **Frostintensität**: *0.0 - 1.0* Legt die Intensität des Frostes fest und steuert die &quot;Deckkraft&quot; des Effekts.
* **Frost-Risse**: *0.0 - 1.0* Legt die Anzahl der Risse in den Überblendungen von gefrorenem zu flüssigem Material fest.
* **Frost-Normalformat**: *DirectX/OpenGL* Schaltet den grünen Kanal des Frost-Normalmap-Effekts um.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

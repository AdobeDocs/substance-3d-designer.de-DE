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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Wasserstand

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>In:</b> Materialfilter > Effekte

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

All-in-One-Effekt, der einen Wasserpegel zu einem vollen Materialeinsatz hinzufügt. Das Eingabematerial muss über eine gute, hochwertige Höhenkarte verfügen, damit der Effekt funktioniert. Das Ergebnis ist PBR-korrekt.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Wasserstand</b> <i>0.0 - 1.0</i> | Hauptsteuerung zur Erhöhung oder Senkung des Wasserspiegels. |
| <b>Wasserdunkel</b> <i>0.0 - 1.0</i> | Legt allgemeine &quot;Transparenz&quot; des Wassers fest. |
| <b>Kantennässe</b> <i>0.0 - 1.0</i> | Bestimmt, wie viel Feuchtigkeit die Kanten des Wassers aufweisen sollen. |
| <b>Kantenfeuchtigkeitsentfernung</b> <i>0.0 - 1.0</i> | Legt fest, wie weit die nassen Kanten reichen. |
| <b>Tiefen-Weichzeichnungsbetrag</b> <i>0.0 - 1.0</i> | Legt den Weichzeichnungsgrad basierend auf der Tiefe unter Wasser fest. Ändert den Weichzeichnungsradius. |
| <b>Tiefe-Weichzeichnungsdeckkraft</b> <i>0.0 - 1.0</i> | Bestimmt, wie viel Tiefe der Weichzeichner einblendet, um die Wirkung des Weichzeichners zu verringern. |
| <b>Schlammfarbe</b> <i>(Farbwert)</i> | Legt die Farbe des Schlammeffekts fest. |
| <b>Schlamm-Tiefe</b> <i>0.0 - 1.0</i> | Legt die Tiefe fest, mit der Schlamm im Verhältnis zum Wasserstand auftritt. |
| <b>Schlammdeckkraft</b> <i>0.0 - 1.0</i> | Legt die globale Deckkraft des Schlammeffekts fest. |
| <b>Frost</b> <i>0.0 - 1.0</i> | Legt die Stärke des Frostes fest. Beginnt, von den Außenkanten aus sichtbar zu werden, und bewegt sich nach innen. |
| <b>Frostintensität</b> <i>0.0 - 1.0</i> | Legt die Intensität des Frostes fest und steuert die &quot;Deckkraft&quot; des Effekts. |
| <b>Frost-Risse</b> <i>0.0 - 1.0</i> | Legt die Anzahl der Risse in den Übergängen von &quot;Gefriert&quot; zu &quot;Flüssigkeiten&quot; fest. |
| <b>Frost-Normalformat</b> <i>DirectX/OpenGL</i> | Schaltet den Frost-Normalmap-Effekt auf den grünen Kanal um. |

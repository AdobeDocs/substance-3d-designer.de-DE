---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Bitmap zu Materiallicht", um Bitmapbilder schnell in Materialien mit optimierter Beleuchtung für schnelle Workflows zu konvertieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap in Materiallicht
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# Bitmap in Materiallicht

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bitmap-to-material-light.resources/b2m-light.png)

<b>In:</b> Materialfilter > 1-Click

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten konvertiert eine einzelne Diffuse/Grundfarbe-Eingabe in ein vollständiges Material. Als einfache, &quot;leichte&quot; Version von [Allegorithmic&#39;s vollwertigem Bitmap2Material, die separat erworben werden kann](https://www.allegorithmic.com/products/bitmap2material), gibt sie Ihnen einen kleinen Vorgeschmack auf die Vollversion. In einfacheren Fällen kann sie gut funktionieren.

Obwohl nicht garantiert, dass perfekte, PBR-korrekte Materialien entstehen, ist es eine gute und schnelle Möglichkeit, loszulegen, wenn Sie nur ein einzelnes Bild haben und ein vollständiges Material wünschen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schaltet die Materialkanäle in dieser Gruppe ein und aus, z. B. bei Verwendung von Specular-/Glanzkarten anstelle von Metallisch/Raueit. |
| <b>Global</b> |  |
| <b>Tiefen-Saldo</b> <i>-1.0 - 1.0</i> | Legt eine Vorspannung/Verschiebung für die Höhenkarte fest. |
| <b>Diffus</b> |  |
| <b>Scharfzeichnen</b> <i>0.0 - 1.0</i> | Fügt dem diffusen Ergebnis die Schärfe hinzu. |
| <b>Farbton</b> <i>0.0 - 1.0</i> | Tint diffundieren mit einer vom Benutzer ausgewählten Farbtonverschiebung. |
| <b>Sättigung</b> <i>0.0 - 1.0</i> | Ändert die Sättigung der Diffuse. |
| <b>Helligkeit</b> <i>0.0 - 1.0</i> | Passt die Helligkeit der Diffuse an. |
| <b>Kontrast</b> <i>-1.0 - 1.0</i> | Passt den Kontrast des Ergebnisses an. |
| <b>Relief</b> | Die Gruppe &quot;Relief&quot; steuert sowohl die Ausgabe als auch die Ausgabe als Height. |
| <b>Normales Ausgabeformat</b> <i>DirectX, OpenGL</i> | Wechselt zwischen normalen Formaten (wird grün gespiegelt). |
| <b>Generiertes Relief umkehren</b> <i>False/True</i> | Kehrt die Interpretation des Heights um. |
| <b>Normale Stärke</b> <i>0.0 - 20.0</i> | Legt die Stärke der generierten Normalmap fest. |
| <b>Relief-Equalizer</b> <i>0.0 - 1.0</i> | Legt Konvertierungssalden für verschiedene Detailskalen fest. |
| <b>Pinch-Intensität</b> <i>0.0 - 1.0</i> | Schärft normale Übergänge. Fügt vor dem Konvertieren in das normale Format einen Scharfzeichnungsfilter hinzu, um die Kanten deutlicher herauszuarbeiten. |
| <b>Normaler Scharfzeichner</b> <i>0.0 - 1.0</i> | Schärft Normalmap nach der Konvertierung, bringt die Details heraus. |
| <b>Normales Weichzeichnen</b> <i>0.0 - 1.0</i> | Reduziert die Normalmap nach der Konvertierung und blendet Details aus. |
| <b>Specular</b> |  |
| <b>Einfluss der Specular-Diffuse</b> <i>0.0 - 1.0</i> | Legt den Einfluss von Diffuse auf den Specular fest. Wirkt sich auch auf die Ausgabe von Glanz und Rauheit aus. |
| <b>Sättigung des Speculars</b> <i>0.0 - 1.0</i> | Ändert die Sättigung für den Specular. |
| <b>Specular Sharpen</b> <i>0.0 - 1.0</i> | Schärft die Specular-Ausgabe. |
| <b>Specular level in </b> <i>0.0 - 1.0</i> | Legt die Eingangspegel für die Interpretation des Specular fest. |
| <b>Specular level versendet</b> <i>0.0 - 1.0</i> | Ändert die Ausgangspegel des Speculars. |
| <b>Metallic Specular-Einfluss</b> <i>0.0 - 1.0</i> | Bestimmt den Einfluss des optionalen Metallic Eingangs auf die Specular-Map. |
| <b>Glanz</b> |  |
| <b>Glanz-Stufen in </b> <i>0.0 - 1.0</i> | Legt die Eingangspegel für die Interpretation des Glanzes fest. |
| <b>Glanz-Levels ausgehend</b> <i>0.0 - 1.0</i> | Ändert die Glanz-Ausgangspegel. |
| <b>Metallic Glanz </b> <i>0.0 - 1.0</i> | Bestimmt den Einfluss der optionalen Metallic Eingabe auf die Glanz-Map. |
| <b>Rauheit</b> |  |
| <b>Rauheiten in </b> <i>0.0 - 1.0</i> | Legt die Eingangspegel für die Interpretation der Rauheit fest. |
| <b>Rauheit wird ausgeglichen</b> <i>0.0 - 1.0</i> | Ändert die Ausgabepegel der Rauheit. |
| <b>Einfluss auf die Metallische Rauheit</b> <i>0.0 - 1.0</i> | Bestimmt den Einfluss der optionalen Metallic Eingabe auf die Glanz-Map. |
| <b>Ambient occlusion</b> |  |
| <b>Ambient occlusion in Diffuse</b> <i>0.0 - 1.0</i> | Überblendungen in generiertem AO in der Diffuse. |
| <b>Ambient occlusion Spread</b> <i>0.0 - 1.0</i> | Legt fest, wie weit generiertes AO sich ausbreitet. |
| <b>Ambient occlusion Lichtdistanz</b> <i>0.0 - 1.0</i> | Legt die AO-Interpretation der &quot;Tiefe&quot; fest. Hat weniger Einfluss, wenn es eine große Verteilung gibt. |
| <b>Ambient occlusion Lichtwinkel</b> <i>0.0 - 1.0</i> | Legt den Geworfen Winkel für die gefälschte Beleuchtung fest. Kann verwendet werden, um jede Richtung AO zu kompensieren, die sich bereits im Diffuse befindet, wenn sie auf einen entgegengesetzten Winkel eingestellt ist. |
| <b>Ambient occlusion-Stufen</b> <i>0.0 - 1.0</i> | Ändert AO-Ausgangspegel. |

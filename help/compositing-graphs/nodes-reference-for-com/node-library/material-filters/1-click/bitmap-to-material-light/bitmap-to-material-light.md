---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Bitmap in Materiallicht

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## Bitmap in Materiallicht

**In:** *Materialfilter/1-Klick*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten konvertiert eine einzelne Diffuse/Grundfarbe-Eingabe in ein vollständiges Material. Als einfache, &quot;leichte&quot; Version von [Allegorithmic&#39;s vollwertigem Bitmap2Material, die separat erworben werden kann](https://www.allegorithmic.com/products/bitmap2material), gibt sie Ihnen einen kleinen Vorgeschmack auf die Vollversion. In einfacheren Fällen kann sie gut funktionieren.

Obwohl nicht garantiert, dass perfekte, PBR-korrekte Materialien entstehen, ist es eine gute und schnelle Möglichkeit, loszulegen, wenn Sie nur ein einzelnes Bild haben und ein vollständiges Material wünschen.

## Parameter

* **Kanäle**
  * Schaltet die Materialkanäle in dieser Gruppe ein und aus, z. B. bei Verwendung von Specular-/Glanzkarten anstelle von Metallisch/Raueit.
* **Global**
  * **Tiefen-Saldo**: *-1.0 - 1.0* Legt eine Vorspannung/Verschiebung für die Höhenkarte fest.
* **Diffus**
  * **Scharfzeichnen**: *0.0 - 1.0* Fügt dem diffusen Ergebnis eine Scharfzeichnung hinzu.
  * **Farbton**: *0.0 - 1.0* Farbtöne diffundieren mit einer vom Benutzer ausgewählten Farbtonverschiebung.
  * **Sättigung**: *0.0 - 1.0*&#x200B;Ändert die Sättigung des Diffuse-Ergebnisses.
  * **Helligkeit**: *0.0 - 1.0* Passt die Helligkeit des diffusen Ergebnisses an.
  * **Kontrast**: *-1.0 - 1.0*\
    Passt den Kontrast des Ergebnisses an.
* **Relief**\
  Die Gruppe &quot;Relief&quot; steuert sowohl die Ausgabe als auch die Ausgabe als Height.
  * **Normales Ausgabeformat**: *DirectX, OpenGL* Wechselt zwischen Normalformaten (spiegelt grün).
  * **Generiertes Relief umkehren**: *Falsch/Wahr* Kehrt die Interpretation des Heights um.
  * **Normalstärke**: *0.0 - 20.0* Legt die Stärke der generierten Normalmap fest.
  * **Relief-Equalizer**: *0.0 - 1.0* Legt Konvertierungssalden für verschiedene Detailskalen fest.
  * **Pinch-Intensität**: *0.0 - 1.0* Schärft normale Übergänge. Fügt vor dem Konvertieren in das normale Format einen Scharfzeichnungsfilter hinzu, um die Kanten deutlicher herauszuarbeiten.
  * **Normaler Scharfzeichner**: *0.0 - 1.0* Schärft die Normalmap nach der Konvertierung und bringt die Details zum Vorschein.
  * **Normale Weiche**: *0.0 - 1.0* Die Normalmap wird nach der Konvertierung weichgezeichnet. Details werden ausgeblendet.
* **Specular**
  * **Diffuser Einfluss auf den Specular**: *0.0 - 1.0* Legt den Einfluss von Diffuse auf den Specular fest. Wirkt sich auch auf die Ausgaben für &quot;Glossiness&quot; und &quot;Raueit&quot; aus.
  * **Sättigung des Speculars**: *0.0 - 1.0*&#x200B;Ändert die Sättigung für die Specular-Ausgabe.
  * **Specular Sharpen**: *0.0 - 1.0* Schärft die Specular-Ausgabe.
  * **Specular level in**: *0.0 - 1.0* Legt die Eingangspegel für die Specular-Interpretation fest.
  * **Specular level aus**: *0.0 - 1.0*&#x200B;Ändert die Ausgangspegel des Speculars.
  * **Metallischer Specular-Einfluss**: *0.0 - 1.0* Bestimmt den Einfluss des optionalen Metallic-Eingangs auf die Specular-Map.
* **Glossarität**
  * **Glossarstufen in**: *0.0 - 1.0* Legt die Eingangspegel für die Glossiness-Interpretation fest.
  * **Glossarstufen ausgehend**: *0.0 - 1.0*&#x200B;Ändert die Glossiness-Ausgabeebenen.
  * **Metallischer Glanzeinfluss**: *0.0 - 1.0* Bestimmt den Einfluss des optionalen metallischen Eingangs auf die Glossiness-Map.
* **Raueit**
  * **Raueitsstufen in**: *0.0 - 1.0* Legt die Eingangspegel für die Rauigkeitsinterpretation fest.
  * **Raueit wird ausgeglichen**: *0.0 - 1.0*&#x200B;Ändert die Raueit-Ausgabeebenen.
  * **Einfluss der metallischen Raueit**: *0.0 - 1.0* Bestimmt den Einfluss des optionalen metallischen Eingangs auf die Glossiness-Map.
* **Umgebungs-Verdeckung**
  * **Verdeckung in Diffuse**: *0.0 - 1.0*&#x200B;Überblendungen in generiertem AO in Diffuse-Ausgabe.
  * **Verteilung der umgebenden Verdeckung**: *0.0 - 1.0* Legt fest, wie weit die generierten AO-Spreads reichen.
  * **Umgebungslichtabstand der Verdeckung**: *0.0 - 1.0* Legt eine O-Interpretation für &quot;Tiefe&quot; fest. Hat weniger Einfluss, wenn es eine große Verteilung gibt.
  * **Umgebungslichtwinkel der Verdeckung**: *0.0 - 1.0* Legt den gefälschten AO-Abspielwinkel der Beleuchtung fest. Kann verwendet werden, um jede Richtung AO zu kompensieren, die sich bereits im Diffuse befindet, wenn sie auf einen entgegengesetzten Winkel eingestellt ist.
  * **Umgebungs-Verdeckungen**: *0.0 - 1.0*&#x200B;Ändert AO-Ausgabepegel.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

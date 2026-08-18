---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Form-Spritzer in Maske", um Spritzmuster in Masken umzuwandeln, die Material vermischen und Effekte erzeugen.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Formaufteilung für Maske
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Formaufteilung für Maske

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## Formaufteilung für Maske

**In:** *Texturgeneratoren**/Muster*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Konvertiert [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)-Daten in eine Schwarzweiß-Maske basierend auf Muster-ID. Ermöglicht es Ihnen beispielsweise, eine Maske nur für einen bestimmten Mustertyp zu erstellen. Enthält zusätzliche Optionen zum Auswählen eines Bereichs von Muster-IDs und zum zufälligen Ausblenden einiger Formen.

## Parameter

### Parameter

* **Muster-ID-Startbereich**: *1 - 8* Legen Sie die erste Muster-ID im Bereich fest, die ausgewählt werden soll.
* **Pattern-ID-Endbereich**: *1 - 8* Legen Sie die letzte Muster-ID im Bereich fest, die ausgewählt werden soll.
* **Zufallsmaske**: *0.0 - 1.0* Legen Sie die Proportion von Mustern fest, die zufällig maskiert werden sollen.
* **Ausgabe**: *Binärmaske, Ganzzahlmaske, Graustufenwerte* Bestimmt den Typ der Ausgabewerte. Binärmaske gibt nur Schwarzweiß, 0-oder-1-Werte zurück. Ganzzahlige Maske kodiert höhere Werte bis zu 8 für jedes Muster im HDR-Format. Die Graustufenwerte verteilen den Bereich proportional zwischen 0 und 1.

</td>
</tr>
</table>

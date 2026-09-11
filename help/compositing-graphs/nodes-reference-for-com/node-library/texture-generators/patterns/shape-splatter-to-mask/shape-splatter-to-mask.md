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
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# Formaufteilung für Maske

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter-to-mask.resources/shape-splatter-to-mask.png){width="128px"}

<b>In:</b> Texturgeneratoren > Muster

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Konvertiert [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)-Daten in eine Schwarzweiß-Maske basierend auf Muster-ID. Ermöglicht es Ihnen beispielsweise, eine Maske nur für einen bestimmten Mustertyp zu erstellen. Enthält zusätzliche Optionen zum Auswählen eines Bereichs von Muster-IDs und zum zufälligen Ausblenden einiger Formen.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Muster-ID-Startbereich</b> <i>1 - 8</i> | Legen Sie die erste Muster-ID im Bereich fest, die ausgewählt werden soll. |
| <b>Pattern-ID-Endbereich</b> <i>1 - 8</i> | Letzte Muster-ID im Bereich festlegen. |
| <b>Zufallsmaske</b> <i>0.0 - 1.0</i> | Legen Sie die Proportion der Muster fest, die nach dem Zufallsprinzip maskiert werden sollen. |
| <b>Ausgabe</b> <i>Binärmaske, Ganzzahl-Maske, Graustufenwerte</i> | Bestimmen Sie den Typ der Ausgabewerte. Binärmaske gibt nur Schwarzweiß, 0-oder-1-Werte zurück. Ganzzahlige Maske kodiert höhere Werte bis zu 8 für jedes Muster im HDR-Format. Die Graustufenwerte verteilen den Bereich proportional zwischen 0 und 1. |

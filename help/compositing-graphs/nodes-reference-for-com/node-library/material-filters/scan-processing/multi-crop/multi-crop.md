---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multi Crop", um mehrere Texturkanäle gleichzeitig zuzuschneiden und so gescannte Materialien effizient zu verarbeiten.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mehrfachzuschnitt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Mehrfachzuschnitt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## Mehrfachzuschnitt (Graustufen)

**In:** *Materialfilter/Scanverarbeitung*

**Fortgeschrittene**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multikanal-Version von &quot;Zuschneiden&quot;. Es schneidet einen Bereich aus einem Bild aus und ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel nach Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel nach Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie im ursprünglichen [Zuschneiden](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).

## Parameter

### Parameter

* **Eingabeanzahl**: *1 - 8* Legt die Anzahl der parallel zu verarbeitenden Eingaben fest.
* **Eingabegröße**: *0 - 8192* Auflösung und Proportionen der Eingabebilder. Sehr wichtig für nicht quadratische Bilder.
* **Hintergrund**: *(Farbwert) / (Graustufenwert)*Einheitlicher Hintergrundwert für Bereiche, die nicht von der Freistellung abgedeckt werden.
* **Transformieren**: *(Transformationsmatrix)*\
  Dreht und skaliert das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Offset**: *0.0 - 1.0*\
  Verschiebt oder verschiebt das Ergebnis. Das Ergebnis kann durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Ist normal (nur für Farbversion)**: *Falsch/Wahr* Ob die Eingabe als Normalmap behandelt werden soll oder nicht.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Materialtransformation", um Transformationen auf Materialausgaben anzuwenden, einschließlich Drehung, Skalierung und Versatz.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialtransformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Materialtransformation

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## Materialtransformation

**In:** *Materialfilter/Transformationen*

**Einfach**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Bei &quot;Materialtransformation&quot; handelt es sich einfach um die &quot;Multi-Channel&quot;-Materialversion von [dem atomaren 2D-Transformationsknoten](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Es transformiert alle Kanäle eines Eingabematerials gleichzeitig mit derselben Schnittstelle wie &quot;2D transformieren&quot;.

Achten Sie nur darauf, die Kanäle richtig einzurichten! Standardmäßig sind &quot;Metallisch/Raueit&quot; und &quot;Specular/Glanz&quot; aktiviert, was zu Verwirrung führen kann.

## Parameter

* **Transformation**: *(Transformationsmatrix)*\
  Dreht und skaliert das Ergebnis. Das Verschieben/Schwenken erfolgt über den Parameter &quot;Versatz&quot;
* **Offset**: *-0.5 - 0.5*\
  Verschiebt oder verschiebt das Ergebnis. Wenn die Transformationssteuerung vorhanden ist, kann das Ergebnis durch direkte Interaktion mit der Arbeitsfläche geändert werden.
* **Normales Format**\
  Wählen Sie zwischen DirectX- und OpenGL-Formaten (Grün umkehren).
* **Kanäle**\
  Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>

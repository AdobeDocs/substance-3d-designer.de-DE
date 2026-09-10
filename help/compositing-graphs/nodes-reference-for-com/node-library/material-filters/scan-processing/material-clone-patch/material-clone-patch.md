---
helpx_url: "https://helpx.adobe.com/de/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Material Klon Patch-Knoten, um Bereiche der Textur zu klonen und auszubessern, um Artefakte in gescannten Materialien zu reparieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Klon Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# Material Klon Patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/clone-patch-material.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multi-Channel-Vollversion des Materials [Klon-Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Es führt einen Klon-Patch auf allen Kanälen eines Materials durch. [Weitere Informationen finden Sie in der Originalversion!](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Das ist sehr nützlich, wenn Sie ein Detail aus allen Kanälen eines Materials entfernen möchten. Gibt Debugbilder für mehrere Kanäle aus, um zu sehen, wie der Smart-Patch-Bereich genau aussieht.

</td>
</tr>
</table>

<a name="inputs"></a>

## Eingaben

|  |  |
|:---|:---|
| <b>Maske</b> <i>Graustufen-Eingabe</i> | Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar. |

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Kanäle</b> | Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden. |
| <b>Form</b> <i>Quadrat, Datenträger</i> | Legt die Stempelform fest. Wird nur als Basis verwendet. |
| <b>Edge</b> |  |
| <b>Schwellenwert (für mehrere Kanäle)</b> <i>0.0 - 1.0</i> | Legt fest, wie weit der angeglichene Bereich reichen soll. Dieser Effekt wächst stufenweise entlang der Formen im Zielbereich, sodass er bei einheitlichen Hintergründen sehr wenig Wirkung hat. Achten Sie darauf, dies zu sehr zwischen den Kanälen zu ändern, da dies zu visuellen Diskrepanzen führen könnte! |
| <b>Weichzeichnen</b> <i>0.0 - 2.0</i> | Weichzeichnet die Kanten des Stempelbereichs, falls ein weicherer Übergang erforderlich ist. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Rundet die Kanten der Stempelform ab, sodass die Umrisse glatter werden. |
| <b>Auflösung des Rasters</b> <i>1 - 11</i> | Legt die Qualitätsauflösung der Füllmethode fest. Je höher der Wert, desto präziser kann die Füllmethode sein. |
| <b>Transformationen</b> |  |
| <b>Quellmatrix</b> <i>(Transformationsmatrix)</i> | Transformieren die Quelle bei (Skalierung und Drehung). Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. |
| <b>Quellversatz</b> <i>-0.5 - 0.5</i> | Kamera bewegt den Quellspeicherort bei. Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. *Dieser Parameter ist wahrscheinlich der Hauptparameter, den Sie ändern möchten!* |
| <b>Zielmatrix</b> <i>(Transformationsmatrix)</i> | Transformieren den Zielspeicherort (Skalierung und Drehung) bei. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen. |
| <b>Zielversatz</b> <i>-0.5 - 0.5</i> | Kamera bewegt den Zielspeicherort bei. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen. |

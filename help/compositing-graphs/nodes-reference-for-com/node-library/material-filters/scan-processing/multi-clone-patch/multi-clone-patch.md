---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten "Multi Clone Patch", um mehrere Texturkanäle zu klonen und auszubessern und so gescannte Materialartefakte zu reparieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch für mehrere Klone
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# Patch für mehrere Klone

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/multi-clone-patch-01.png){width="128px"}

![](multi-clone-patch.resources/multi-clone-patch-02.png){width="128px"}

<b>In:</b> Materialfilter > Scanverarbeitung

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Beschreibung

Dieser Knoten ist die Multieingabeversion von [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Es verbindet bis zu acht Eingänge miteinander und führt für alle die exakt gleiche Kopierpatchoperation durch. Es ist hauptsächlich für die Verwendung mit Mehrfachwinkelfotos vorgesehen, die dann mit [Mehrfachwinkel zu Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) oder [Mehrfachwinkel zu Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) kombiniert werden.

>[!NOTE]
>
> Weitere Informationen finden Sie unter [Klonpatch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Weitere Informationen finden Sie unter [Materialklonpatch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) für die Materialversion.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parameter

|  |  |
|:---|:---|
| <b>Eingabeanzahl</b> <i>1 - 8</i> | Legt die Anzahl der Eingaben fest, die den gleichen Patch-Vorgang erhalten. |
| <b>Ist normal (nur für Farbe)</b> <i>False/True</i> | Legt fest, ob die Eingabe eine Normalmap ist und ob die Füllmethode als solche behandelt werden soll. |
| <b>Form</b> <i>Quadrat, Datenträger</i> | Legt die Stempelform fest. Wird nur als Basis verwendet. |
| <b>Edge</b> |  |
| <b>Schwellenwert</b> <i>0.0 - 1.0</i> | Legt fest, wie weit der angeglichene Bereich reichen soll. Dieser wächst schrittweise entlang der Formen im Zielbereich. Es hat sehr wenig Wirkung mit einheitlichen Hintergründen. |
| <b>Weichzeichnen</b> <i>0.0 - 2.0</i> | Weichzeichnet die Kanten des Stempelbereichs, falls ein weicherer Übergang erforderlich ist. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Rundet die Kanten der Stempelform ab, sodass die Umrisse glatter werden. |
| <b>Auflösung des Rasters</b> <i>1 - 11</i> | Legt die Qualitätsauflösung der Füllmethode fest. Je höher der Wert, desto präziser kann die Füllmethode sein. |
| <b>Transformationen</b> |  |
| <b>Quellmatrix</b> <i>(Transformationsmatrix)</i> | Transformieren die Quelle bei (Skalierung und Drehung). Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. |
| <b>Quellversatz</b> <i>-0.5 - 0.5</i> | Kamera bewegt den Quellspeicherort bei. Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. *Dieser Parameter ist wahrscheinlich der Hauptparameter, den Sie ändern möchten!* |
| <b>Zielmatrix</b> <i>(Transformationsmatrix)</i> | Transformieren den Zielspeicherort (Skalierung und Drehung) bei. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen. |
| <b>Zielversatz</b> <i>-0.5 - 0.5</i> | Kamera bewegt den Zielspeicherort bei. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen. |

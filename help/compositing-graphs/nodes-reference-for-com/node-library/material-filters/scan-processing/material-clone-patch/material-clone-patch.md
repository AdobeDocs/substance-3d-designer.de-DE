---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Verwenden Sie den Knoten Material Clone Patch, um Texturbereiche zu klonen und auszubessern, um Artefakte in gescannten Materialien zu reparieren.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materialklonpflaster
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# Materialklonpflaster

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## Materialklonpflaster

**In:** *Materialfilter/Scanverarbeitung*

**Komplex**

</td>
<td style="border: 0;" valign="top">

## Beschreibung

Dies ist die Multi-Channel-Vollversion von [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Es führt einen Klon-Patch auf allen Kanälen eines Materials durch. [Weitere Informationen finden Sie in der Originalversion!](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Das ist sehr nützlich, wenn du ein Detail aus allen Kanälen eines Materials entfernen möchtest. Gibt Debugbilder für mehrere Kanäle aus, um zu sehen, wie der Smart-Patch-Bereich genau aussieht.

## Parameter

### Eingaben

* **Maske**: *Graustufen-Eingabe*\
  Maskenschlitz zum Maskieren der Knoteneffekte. Mit dem Parameter &quot;Maske&quot; umschaltbar.

### Parameter

* **Kanäle**
  * Schalten Sie die Materialkanäle in dieser Gruppe ein und aus, z. B. wenn Sie Specular-/Glanzkarten anstelle von &quot;Metallisch/Raueit&quot; verwenden.
* **Form**: *Quadrat, Datenträger* Legt die Stempelform fest. Wird nur als Basis verwendet.
* **Edge**
  * **Schwellenwert (für mehrere Kanäle)**: *0.0 - 1.0* Legt fest, wie weit der angeglichene Bereich reichen soll. Dieser wächst stufenweise, entlang der Formen im Zielbereich, hat also bei einheitlichen Hintergründen sehr wenig Effekt*.*Achten Sie darauf, dies zu stark zwischen den Kanälen zu ändern, da es zu visuellen Abweichungen führen könnte!
  * **Weichzeichnen**: *0.0 - 2.0* Weichzeichnet die Kanten des Stempelbereichs, falls ein weicherer Übergang erforderlich ist.
  * **Smoothness**: *0.0 - 2.0* Rundet die Kanten der Stempelform ab und sorgt so für glattere Konturen.
  * **Rasterauflösung**: *1 - 11* Legt die Qualitätsauflösung der Füllmethode fest. Je höher der Wert, desto präziser kann die Füllmethode sein.
* **Transformationen**
  * **Quellmatrix**: *(Transformationsmatrix)*Transformiert die Quelle (Skalierung und Drehung). Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden.
  * **Quellversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Quellspeicherort. Kann nicht auf der Arbeitsfläche durchgeführt werden. Nur diese Parameter können geändert werden. *Dieser Parameter ist wahrscheinlich der Hauptparameter, den Sie ändern möchten!*
  * **Zielmatrix**: *(Transformationsmatrix)*Transformiert die Zielposition (Skalierung und Drehung). Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.
  * **Zielversatz**: *-0.5 - 0.5*&#x200B;Übersetzt den Zielspeicherort. Kann auch durch Gizmo auf der Arbeitsfläche erfolgen.

## Beispielbilder

|  |
| --- |
| Es sind keine Bilder an diese Seite angehängt. |

</td>
</tr>
</table>
